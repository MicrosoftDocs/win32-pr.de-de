---
description: Anwendungen können Hardware Abfragen, um die unterstützten Direct3D-Gerätetypen zu erkennen. Dieser Abschnitt enthält Informationen zu den Hauptaufgaben beim Auflisten von Anzeige Adaptern und Auswählen von Direct3D-Geräten.
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: Auswählen eines Geräts (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdfa1faf38007f00959ac7263b4538954044688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522763"
---
# <a name="selecting-a-device-direct3d-9"></a>Auswählen eines Geräts (Direct3D 9)

Anwendungen können Hardware Abfragen, um die unterstützten Direct3D-Gerätetypen zu erkennen. Dieser Abschnitt enthält Informationen zu den Hauptaufgaben beim Auflisten von Anzeige Adaptern und Auswählen von Direct3D-Geräten.

Eine Anwendung muss eine Reihe von Aufgaben ausführen, um ein entsprechendes Direct3D-Gerät auszuwählen. Beachten Sie, dass die folgenden Schritte für eine Vollbildanwendung vorgesehen sind und in den meisten Fällen eine Anwendung die meisten dieser Schritte überspringen kann.

1.  Zuerst muss die Anwendung die Anzeige Adapter im System auflisten. Bei einem Adapter handelt es sich um eine physische Hardware. Beachten Sie, dass die Grafikkarte möglicherweise mehr als einen Adapter enthält. Dies ist der Fall mit einer zweiköpfigen Anzeige. Anwendungen, die nicht die Unterstützung für mehrere Monitore betreffen, können diesen Schritt ignorieren und übergeben D3DADAPTER \_ standardmäßig an die [**IDirect3D9:: enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) -Methode in Schritt 2.
2.  Für jeden Adapter listet die Anwendung die unterstützten Anzeigemodi durch Aufrufen von [**IDirect3D9:: enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)auf.
3.  Bei Bedarf überprüft die Anwendung die Hardwarebeschleunigung in jedem enumerationsanzeigemodus durch Aufrufen von [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), wie im folgenden Codebeispiel gezeigt. Beachten Sie, dass dies nur eine der möglichen Verwendungsmöglichkeiten für **IDirect3D9:: checkdebug Type** ist. Weitere Informationen finden Sie [unter Bestimmen des Hardware Supports (Direct3D 9)](determining-hardware-support.md).
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

    

4.  Die Anwendung überprüft die gewünschte Funktionsebene für das Gerät auf diesem Adapter durch Aufrufen der [**IDirect3D9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) -Methode. Die Funktion, die von dieser Methode zurückgegeben wird, ist garantiert für ein Gerät über alle Anzeigemodi hinweg konstant und wird von [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)überprüft.
5.  Geräte können immer auf Oberflächen des Formats eines aufgelisteten Anzeigemodus Renderingmodus Renderingmodus, der vom Gerät unterstützt wird. Wenn die Anwendung auf eine Oberfläche eines anderen Formats renderert werden muss, kann Sie [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)aufgerufen werden. Wenn das Gerät in das Format rendern kann, ist sichergestellt, dass alle von [**IDirect3D9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) zurückgegebenen Funktionen anwendbar sind.
6.  Schließlich kann die Anwendung ermitteln, ob multisamplinggrad-Techniken, z. b. Vollbild-Antialiasing, mit der [**IDirect3D9:: checkdevicemultisampletype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) -Methode für ein Renderformat unterstützt werden.

Nachdem Sie die obigen Schritte ausgeführt haben, sollte die Anwendung über eine Liste der Anzeigemodi verfügen, in der Sie ausgeführt werden kann. Der letzte Schritt besteht darin, zu überprüfen, ob ausreichend Speicherplatz für das Gerät verfügbar ist, um die erforderliche Anzahl von Puffern und Antialiasing zu unterstützen. Dieser Test ist erforderlich, da der Arbeitsspeicher Verbrauch für die Kombination aus Modus und Multisampling ohne Überprüfung nicht vorhergesagt werden kann. Außerdem verfügen einige Anzeige Adapter Architekturen möglicherweise nicht über eine konstante Menge an Speicherplatz, auf den Gerät zugegriffen werden kann. Dies bedeutet, dass eine Anwendung in der Lage sein sollte, out-of-Video-Memory-Fehler zu melden, wenn Sie in den Vollbildmodus wechseln. In der Regel sollte eine Anwendung den Vollbildmodus aus der Liste der Modi entfernen, die Sie für einen Benutzer anbietet, oder es sollte versucht werden, weniger Arbeitsspeicher zu belegen, indem die Anzahl der Back Puffer reduziert wird oder eine weniger komplexe multisamplinggrad-Methode verwendet wird.

Eine Anwendungs Anwendung führt einen ähnlichen Satz von Aufgaben aus.

1.  Er bestimmt das Desktop Rechteck, das durch den Client Bereich des Fensters abgedeckt wird.
2.  Es listet Adapter auf und sucht den Adapter, dessen Monitor den Client Bereich abdeckt. Wenn der Client Bereich im Besitz mehrerer Adapter ist, kann die Anwendung jeden Adapter unabhängig voneinander steuern oder einen einzelnen Adapter übertragen und Direct3D Pixel von einem Gerät zu einem anderen in der Präsentation übertragen. Die Anwendung kann auch zwei vorangehende Schritte ignorieren und den D3DADAPTER- \_ Standard Adapter verwenden. Beachten Sie, dass dies zu einem langsameren Vorgang führen kann, wenn das Fenster auf einem sekundären Monitor platziert wird.
3.  Die Anwendung muss [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) aufgerufen werden, um zu bestimmen, ob das Gerät das Rendering zu einem Hintergrund Puffer des angegebenen Formats im Desktop Modus unterstützen kann. [**IDirect3D9:: getadapterdisplaymode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) kann zum Bestimmen des Desktop Anzeige Formats verwendet werden, wie im folgenden Codebeispiel gezeigt.
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

 

 
