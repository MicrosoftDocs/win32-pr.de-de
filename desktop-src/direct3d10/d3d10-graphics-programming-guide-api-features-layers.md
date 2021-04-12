---
description: API-Ebenen (Direct3D 10)
ms.assetid: 19c81383-6ac7-49ea-98a3-bf761a32ab40
title: API-Ebenen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4427083bdcaf389c4b01b590a1bc3fef7eb878b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392994"
---
# <a name="api-layers-direct3d-10"></a>API-Ebenen (Direct3D 10)

Die Direct3D 10-Laufzeit wird mit Ebenen erstellt, beginnend mit den grundlegenden Funktionen im Kern und der Erstellung Optionaler und Entwickler-Assist-Funktionen in äußeren Schichten.

## <a name="core-layer"></a>Kern Ebene

Standardmäßig ist die Kern Ebene vorhanden. Bereitstellung einer sehr dünnen Zuordnung zwischen der API und dem Gerätetreiber, wodurch der Aufwand für hochfrequenzaufrufe minimiert wird. Da die Kern Ebene für die Leistung wichtig ist, wird nur eine kritische Validierung durchführt.

Die übrigen Ebenen sind optional. Als allgemeine Regel fügen Ebenen Funktionen hinzu, ändern jedoch das vorhandene Verhalten nicht. Beispielsweise haben die Kernfunktionen die gleichen Rückgabewerte, die unabhängig von der instanziierten debugschicht sind, obwohl eine zusätzliche Debugausgabe bereitgestellt werden kann, wenn die debugschicht instanziiert wird.

Erstellen Sie Ebenen, wenn ein Gerät durch Aufrufen von [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) erstellt wird, und stellen Sie mindestens ein [**d3d10 \_ Flag zum Erstellen des \_ Geräts \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) bereit.

## <a name="debug-layer"></a>Ebene Debuggen

Die Debug-Ebene bietet umfassende zusätzliche Parameter-und Konsistenz Validierung (z. b. das Überprüfen der shaderverknüpfung und Ressourcen Bindung, das Überprüfen der Parameter Konsistenz und das Melden von Fehlerbeschreibungen). Die von der debugschicht generierte Ausgabe besteht aus einer Warteschlange von Zeichen folgen, auf die über die [**ID3D10InfoQueue-Schnittstelle**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) zugegriffen werden kann (siehe [Anpassen der Debugausgabe mit ID3D10InfoQueue (Direct3D 10)](d3d10-graphics-programming-guide-api-features-layers-info-queue.md)). Fehler, die von der Kern Ebene generiert werden, werden durch Warnungen der debugschicht hervorgehoben.

Um ein Gerät zu erstellen, das die debugschicht unterstützt, müssen Sie das DirectX SDK (zum Abrufen D3D10SDKLayers.DLL) installieren und dann \_ das \_ Flag d3d10 Create Device \_ Debug beim Aufrufen von [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)angeben. Natürlich wird das Ausführen einer Anwendung mit der debugschicht wesentlich langsamer. Um Debugmeldungen für d3dx10-APIs zu aktivieren/deaktivieren, wenden Sie [**D3DX10DebugMute**](d3dx10debugmute.md)an.

Wenn die debugschicht Speicher Verluste auflistet, gibt Sie eine Liste von Objekt Schnittstellen Zeigern zusammen mit ihren anzeigen Amen aus. Der standardmäßige Anzeige Name ist " &lt; unbenannt &gt; ". Sie können den anzeigen Amen mithilfe der [**ID3D10DeviceChild:: setprivatedata**](/windows/desktop/api/D3D10/nf-d3d10-id3d10devicechild-setprivatedata) -Methode und der **wkpdid \_ D3DDebugObjectName** GUID in D3Dcommon. h festlegen. Verwenden Sie z. b. den folgenden Code, um ptexture mit dem Namen des sdgers mytexture.jpg zu benennen:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



In der Regel sollten Sie diese Aufrufe aus der Produktionsversion kompilieren.

## <a name="switch-to-reference-layer"></a>Wechsel-zu-Verweis-Ebene

Diese Ebene ermöglicht es einer Anwendung, zwischen einem Hardware Gerät (HAL) und einem Referenz-oder Software Gerät (Ref) zu wechseln. Um ein Gerät zu wechseln, müssen Sie zunächst ein Gerät erstellen, das die Wechsel-zu-Verweis-Schicht unterstützt (siehe [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) und dann [**ID3D10SwitchToRef:: setuseref**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10switchtoref-setuseref)aufrufen.

Alle Gerätezustände, Ressourcen und Objekte werden über diesen Geräte Übergang verwaltet. Es ist jedoch manchmal nicht möglich, Ressourcen Daten genau abzugleichen. Dies liegt daran, dass einige Informationen für ein Hardware Gerät verfügbar sind, das für ein Referenzgerät nicht verfügbar ist.

Praktisch alle Echtzeitanwendungen verwenden die HAL-Implementierung der Pipeline. Wenn die Pipeline von einem Hardware Gerät zu einem Referenzgerät gewechselt wird, werden Renderingvorgänge sowohl in der Hardware als auch in der Software gleichzeitig durchgeführt. Beim Rendern des Software Geräts müssen Ressourcen in den Systemspeicher heruntergeladen werden. Dies erfordert möglicherweise, dass andere im Systemspeicher zwischengespeicherte Ressourcen entfernt werden, um Platz zu schaffen.

> [!Note]  
> Diese Funktion für die Switch-zu-Verweis-Ebene wird nur in Direct3D 10 und Direct3D 10,1 unterstützt und wird in Direct3D 11 und höheren Versionen nicht mehr unterstützt.

 

## <a name="thread-safe-layer"></a>Thread-Safe Ebene

Diese Ebene ist so konzipiert, dass Multithreadanwendungen von mehreren Threads aus auf das Gerät zugreifen können.

Eine Direct3D 10-Anwendung kann eine Geräte Synchronisierung mithilfe von Gerätefunktionen steuern. Dies ermöglicht es einer Anwendung, kritische Abschnitte zu aktivieren bzw. zu deaktivieren (Vorübergehendes Aktivieren/Deaktivieren des Multithreading Schutzes) und eine kritische Abschnitts Sperre über mehrere Direct3D 10 API-Einstiegspunkte zu nehmen bzw. freizugeben. Die Thread sichere Ebene ist standardmäßig aktiviert. Bei Anwendungen mit nur einem Thread hat die Thread sichere Schicht keine Auswirkung auf die Leistung.



|                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> Im Gegensatz zu Direct3D 9 ist die Direct3D 10-API standardmäßig vollständig Thread sicher.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Features (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




