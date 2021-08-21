---
description: Anwendungen können Hardware abfragen, um die unterstützten Direct3D-Gerätetypen zu erkennen. Dieser Abschnitt enthält Informationen zu den wichtigsten Aufgaben, die beim Aufzählen von Anzeigeadaptern und beim Auswählen von Direct3D-Geräten erforderlich sind.
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: Auswählen eines Geräts (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63428e15948e15790364f310d55989a9bbc7339846f7db5d301e316bee4d872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044248"
---
# <a name="selecting-a-device-direct3d-9"></a>Auswählen eines Geräts (Direct3D 9)

Anwendungen können Hardware abfragen, um die unterstützten Direct3D-Gerätetypen zu erkennen. Dieser Abschnitt enthält Informationen zu den wichtigsten Aufgaben, die beim Aufzählen von Anzeigeadaptern und beim Auswählen von Direct3D-Geräten erforderlich sind.

Eine Anwendung muss eine Reihe von Aufgaben ausführen, um ein geeignetes Direct3D-Gerät auszuwählen. Beachten Sie, dass die folgenden Schritte für eine Vollbildanwendung vorgesehen sind und dass eine Anwendung mit Fenstern in den meisten Fällen die meisten dieser Schritte überspringen kann.

1.  Zunächst muss die Anwendung die Anzeigeadapter auf dem System aufzählen. Ein Adapter ist ein physischer Hardwareteil. Beachten Sie, dass die Grafikkarte möglicherweise mehr als einen einzelnen Adapter enthält, wie dies bei einer Anzeige mit Doppelkopf der Fall ist. Anwendungen, die keine Unterstützung für mehrere Monitore haben, können diesen Schritt ignorieren und D3DADAPTER \_ DEFAULT an die [**IDirect3D9::EnumAdapterModes-Methode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) in Schritt 2 übergeben.
2.  Für jeden Adapter listet die Anwendung die unterstützten Anzeigemodi auf, indem [**sie IDirect3D9::EnumAdapterModes aufruft.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)
3.  Bei Bedarf überprüft die Anwendung durch Aufrufen von [**IDirect3D9::CheckDeviceType,**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)ob hardwarebeschleunigung in jedem aufzählten Anzeigemodus vorhanden ist, wie im folgenden Codebeispiel gezeigt. Beachten Sie, dass dies nur eine der möglichen Verwendungsmöglichkeiten für **IDirect3D9::CheckDeviceType** ist. Weitere Informationen finden Sie unter [Bestimmen der Hardwareunterstützung (Direct3D 9).](determining-hardware-support.md)
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    Params.BackBufferFormat = D3DFMT_X1R5G5B5; 

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, 
                      Device.m_DevType, 
                      Params.BackBufferFormat, Params.BackBufferFormat, 
                      FALSE))) 
        return E_FAIL;
    ```

    

4.  Die Anwendung überprüft die gewünschte Funktionalitätsebene für das Gerät auf diesem Adapter, indem sie die [**IDirect3D9::GetDeviceCaps-Methode aufruft.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) Die von dieser Methode zurückgegebene Funktion ist für ein Gerät über alle Anzeigemodi hinweg garantiert konstant, überprüft durch [**IDirect3D9::CheckDeviceType.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
5.  Geräte können immer auf Oberflächen im Format eines aufzählten Anzeigemodus gerendert werden, der vom Gerät unterstützt wird. Wenn die Anwendung auf einer Oberfläche eines anderen Formats gerendert werden muss, kann sie [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)aufrufen. Wenn das Gerät im Format gerendert werden kann, ist sichergestellt, dass alle von [**IDirect3D9::GetDeviceCaps zurückgegebenen**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) Funktionen anwendbar sind.
6.  Schließlich kann die Anwendung mithilfe der [**IDirect3D9::CheckDeviceMultiSampleType-Methode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) ermitteln, ob Multisamplingtechniken wie Antialiasing für vollständige Szenen für ein Renderformat unterstützt werden.

Nach Abschluss der vorherigen Schritte sollte die Anwendung über eine Liste der Anzeigemodi verfügen, in denen sie ausgeführt werden kann. Der letzte Schritt besteht darin, zu überprüfen, ob genügend Arbeitsspeicher verfügbar ist, auf den das Gerät zugreifen kann, um die erforderliche Anzahl von Puffern und Antialiasing aufzunehmen. Dieser Test ist erforderlich, da der Arbeitsspeicherverbrauch für die Kombination aus Modus und Multisample nicht vorhergesagt werden kann, ohne ihn zu überprüfen. Darüber hinaus verfügen einige Adapterarchitekturen für die Anzeige möglicherweise nicht über eine konstante Menge an Gerätespeicher, auf die zugegriffen werden kann. Dies bedeutet, dass eine Anwendung In-of-Video-Memory-Fehler melden kann, wenn sie in den Vollbildmodus wechselt. In der Regel sollte eine Anwendung den Vollbildmodus aus der Liste der Modi entfernen, die sie für einen Benutzer anbietet, oder sie sollte versuchen, weniger Arbeitsspeicher zu verbrauchen, indem sie die Anzahl der Hintergrundpuffer reduziert oder eine weniger komplexe Multisampling-Technik verwendet.

Eine Anwendung mit Fenstern führt einen ähnlichen Satz von Aufgaben aus.

1.  Es bestimmt das Desktoprechteck, das vom Clientbereich des Fensters abgedeckt wird.
2.  Es listet Adapter auf und sucht nach dem Adapter, dessen Monitor den Clientbereich abdeckt. Wenn sich der Clientbereich im Besitz mehrerer Adapter befindet, kann die Anwendung auswählen, dass jeder Adapter unabhängig voneinander betrieben werden soll oder ob ein einzelner Adapter mit Direct3D-Übertragungspixeln von einem Gerät auf ein anderes übertragen werden soll. Die Anwendung kann auch zwei vorherige Schritte ignorieren und den D3DADAPTER \_ DEFAULT-Adapter verwenden. Beachten Sie, dass dies zu einem langsameren Vorgang führen kann, wenn das Fenster auf einem sekundären Monitor platziert wird.
3.  Die Anwendung sollte [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) aufrufen, um zu bestimmen, ob das Gerät das Rendern in einen Hintergrundpuffer im angegebenen Format im Desktopmodus unterstützen kann. [**IDirect3D9::GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) kann verwendet werden, um das Desktopanzeigeformat zu bestimmen, wie im folgenden Codebeispiel gezeigt.
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    // Use the current display mode.
    D3DDISPLAYMODE mode;

    if(FAILED(m_pD3D->GetAdapterDisplayMode(Device.m_uAdapter , &mode)))
        return E_FAIL;

    Params.BackBufferFormat = mode.Format;

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, Device.m_DevType, 
    Params.BackBufferFormat, Params.BackBufferFormat, FALSE)))
        return E_FAIL;
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
