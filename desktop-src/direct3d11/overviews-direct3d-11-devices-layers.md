---
title: Software Ebenen
description: Die Direct3D 11-Laufzeit wird mit Ebenen erstellt, beginnend mit den grundlegenden Funktionen im Kern und der Erstellung Optionaler und Entwickler-Assist-Funktionen in äußeren Schichten. In diesem Abschnitt werden die Funktionen der einzelnen Ebenen beschrieben.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516805"
---
# <a name="software-layers"></a>Software Ebenen

Die Direct3D 11-Laufzeit wird mit Ebenen erstellt, beginnend mit den grundlegenden Funktionen im Kern und der Erstellung Optionaler und Entwickler-Assist-Funktionen in äußeren Schichten. In diesem Abschnitt werden die Funktionen der einzelnen Ebenen beschrieben.

Als allgemeine Regel fügen Ebenen Funktionen hinzu, ändern jedoch das vorhandene Verhalten nicht. Beispielsweise haben die Kernfunktionen die gleichen Rückgabewerte, die unabhängig von der instanziierten debugschicht sind, obwohl eine zusätzliche Debugausgabe bereitgestellt werden kann, wenn die debugschicht instanziiert wird.

Um Ebenen zu erstellen, wenn ein Gerät erstellt wird, rufen Sie [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) auf, und geben Sie mindestens ein [**D3D11 \_ Flag zum Erstellen des \_ Geräts \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) an.

Direct3D 11 stellt die folgenden Lauf Zeitebenen bereit:

-   [Kern Ebene](#core-layer)
-   [Ebene Debuggen](#debug-layer)
-   [Zugehörige Themen](#related-topics)

## <a name="core-layer"></a>Kern Ebene

Standardmäßig ist die Kern Ebene vorhanden. Bereitstellung einer sehr dünnen Zuordnung zwischen der API und dem Gerätetreiber, wodurch der Aufwand für hochfrequenzaufrufe minimiert wird. Da die Kern Ebene für die Leistung wichtig ist, wird nur eine kritische Validierung durchführt. Die übrigen Ebenen sind optional.

## <a name="debug-layer"></a>Ebene Debuggen

Die Debug-Ebene bietet umfassende zusätzliche Parameter-und Konsistenz Validierung (z. b. das Überprüfen der shaderverknüpfung und Ressourcen Bindung, das Überprüfen der Parameter Konsistenz und das Melden von Fehlerbeschreibungen).

Um ein Gerät zu erstellen, das die debugschicht unterstützt, müssen Sie das DirectX SDK (zum Abrufen D3D11SDKLayers.dll) installieren und dann das **D3D11 \_ Create \_ Device \_ Debug** -Flag angeben, wenn Sie die [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) -Funktion oder die [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) -Funktion aufrufen. Wenn Sie die Anwendung mit aktivierter debugschicht ausführen, wird die Anwendung wesentlich langsamer. Um jedoch sicherzustellen, dass Ihre Anwendung Fehler und Warnungen vor dem Versenden bereinigt, verwenden Sie die Debug-Ebene. Weitere Informationen finden Sie unter [Verwenden der Debug-Ebene zum Debuggen von apps](using-the-debug-layer-to-test-apps.md).


> [!Note]  
> Installieren Sie das Windows Software Development Kit (SDK) für Windows 7 (KB2670838) oder Windows 8. x, um ein Gerät zu erstellen, das die debugschicht unterstützt, und installieren Sie das Windows Software Development Kit (SDK) für Windows 8. x, um D3D111SDKLayers.dll zu erhalten \_ .


> [!Note]  
> Aktivieren Sie für Windows 10 das optionale Feature "Graphics Tools", um ein Gerät zu erstellen, das die debugschicht unterstützt. Wechseln Sie zum Bereich "Einstellungen" unter "System", "Apps & Features", "optionale Features verwalten", "Features hinzufügen", und suchen Sie nach "Grafik Tools".


> [!Note]  
> Informationen zum Remote Debuggen von DirectX-apps finden Sie unter [Remote Debuggen von DirectX-apps](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).

 

Alternativ können Sie das Debugflag mithilfe der [DirectX-Systemsteuerung](/previous-versions//bb219725(v=vs.85)) aktivieren bzw. deaktivieren, die als Teil des DirectX SDK enthalten ist.

Wenn die debugschicht Speicher Verluste auflistet, gibt Sie eine Liste von Objekt Schnittstellen Zeigern zusammen mit ihren anzeigen Amen aus. Der standardmäßige Anzeige Name ist " &lt; unbenannt &gt; ". Sie können den anzeigen Amen mithilfe der [**ID3D11DeviceChild:: setprivatedata**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) -Methode und der **wkpdid \_ D3DDebugObjectName** GUID in D3Dcommon. h festlegen. Verwenden Sie z. b. den folgenden Code, um ptexture mit dem Namen des sdgers mytexture.jpg zu benennen:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



In der Regel sollten Sie diese Aufrufe aus der Produktionsversion kompilieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 