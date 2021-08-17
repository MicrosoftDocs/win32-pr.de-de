---
title: Softwareebenen
description: Die Direct3D 11-Runtime wird mit Ebenen erstellt, beginnend mit der grundlegenden Funktionalität im Kern und dem Erstellen optionaler und Entwicklerunterstützungsfunktionen in äußeren Ebenen. In diesem Abschnitt werden die Funktionen der einzelnen Ebenen beschrieben.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59d0405d53526b8fb0b93e52fd1a53b5c17839f6c58df919bac335b21ad2477
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124361"
---
# <a name="software-layers"></a>Softwareebenen

Die Direct3D 11-Runtime wird mit Ebenen erstellt, beginnend mit der grundlegenden Funktionalität im Kern und dem Erstellen optionaler und Entwicklerunterstützungsfunktionen in äußeren Ebenen. In diesem Abschnitt werden die Funktionen der einzelnen Ebenen beschrieben.

Im Allgemeinen fügen Ebenen Funktionen hinzu, ändern jedoch das vorhandene Verhalten nicht. Kernfunktionen verfügen beispielsweise unabhängig von der instanziierten Debugebene über die gleichen Rückgabewerte, obwohl eine zusätzliche Debugausgabe bereitgestellt werden kann, wenn die Debugebene instanziiert wird.

Um Ebenen zu erstellen, wenn ein Gerät erstellt wird, rufen [**Sie D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) auf, und stellen Sie mindestens einen [**D3D11 \_ CREATE DEVICE \_ \_ FLAG-Wert**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) bereit.

Direct3D 11 bietet die folgenden Laufzeitebenen:

-   [Kernebene](#core-layer)
-   [Debugebene](#debug-layer)
-   [Zugehörige Themen](#related-topics)

## <a name="core-layer"></a>Kernebene

Die Kernebene ist standardmäßig vorhanden. bereitstellung einer sehr schlanken Zuordnung zwischen der API und dem Gerätetreiber, wodurch der Mehraufwand für Aufrufe mit hoher Häufigkeit minimiert wird. Da die Kernebene für die Leistung von entscheidender Bedeutung ist, führt sie nur eine kritische Überprüfung durch. Die übrigen Ebenen sind optional.

## <a name="debug-layer"></a>Debugebene

Die Debugebene bietet eine umfassende zusätzliche Parameter- und Konsistenzüberprüfung (z. B. Überprüfen der Shaderbindung und Ressourcenbindung, Überprüfen der Parameterkonsistenz und Melden von Fehlerbeschreibungen).

Um ein Gerät zu erstellen, das die Debugebene unterstützt, müssen Sie das DirectX SDK installieren (um D3D11SDKLayers.dll zu erhalten) und dann das **D3D11 \_ CREATE \_ DEVICE \_ DEBUG-Flag** angeben, wenn Sie die [**D3D11CreateDevice-Funktion**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder die [**D3D11CreateDeviceAndSwapChain-Funktion**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) aufrufen. Wenn Sie Ihre Anwendung mit aktivierter Debugebene ausführen, ist die Anwendung erheblich langsamer. Verwenden Sie jedoch die Debugebene, um sicherzustellen, dass Ihre Anwendung vor dem Versand von Fehlern und Warnungen bereinigt wird. Weitere Informationen finden Sie unter [Verwenden der Debugebene zum Debuggen von Apps.](using-the-debug-layer-to-test-apps.md)


> [!Note]  
> Installieren Sie für Windows 7 mit Plattformupdate für Windows 7 (KB2670838) oder Windows 8.x zum Erstellen eines Geräts, das die Debugebene unterstützt, das Windows Software Development Kit (SDK) für Windows 8.x, um D3D11 \_1SDKLayers.dll zu erhalten.


> [!Note]  
> Um Windows 10 ein Gerät zu erstellen, das die Debugebene unterstützt, aktivieren Sie das optionale Feature "Grafiktools". Wechseln Sie zum bereich Einstellungen unter System, Apps & Features, Optionale Features verwalten, Feature hinzufügen, und suchen Sie dann nach "Grafiktools".


> [!Note]  
> Informationen zum Remotedebuggen von DirectX-Apps finden Sie unter [Remotedebuggen von DirectX-Apps.](/windows/desktop/direct3dtools/debugging-directx-apps-remotely)

 

Alternativ können Sie das Debugflag mithilfe der [DirectX-Systemsteuerung](/previous-versions//bb219725(v=vs.85)) aktivieren/deaktivieren, die im DirectX SDK enthalten sind.

Wenn die Debugebene Speicherverluste auflistet, gibt sie eine Liste von Objektschnittstellenzeigern zusammen mit ihren Anzeigenamen aus. Der Standardmäßige Anzeigename ist &lt; "unbenannt". &gt; Sie können den Anzeigenamen mithilfe der [**ID3D11DeviceChild::SetPrivateData-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) und der **GUID WKPDID \_ D3DDebugObjectName** in D3Dcommon.h festlegen. Verwenden Sie beispielsweise den folgenden Code, um pTexture mit dem SDKLayer-Namen mytexture.jpg zu benennen:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



In der Regel sollten Sie diese Aufrufe aus Ihrer Produktionsversion kompilieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 