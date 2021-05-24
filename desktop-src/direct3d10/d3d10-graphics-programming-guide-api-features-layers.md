---
description: API-Ebenen (Direct3D 10)
ms.assetid: 19c81383-6ac7-49ea-98a3-bf761a32ab40
title: API-Ebenen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b07b33dfd8280af13ea3df74e5e6d0fd040bb2c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335414"
---
# <a name="api-layers-direct3d-10"></a>API-Ebenen (Direct3D 10)

Die Direct3D 10-Runtime wird mit Ebenen erstellt, beginnend mit der grundlegenden Funktionalität im Kern und dem Erstellen optionaler und entwicklerassistenter Funktionen in äußeren Ebenen.

## <a name="core-layer"></a>Kernebene

Die Kernebene ist standardmäßig vorhanden. Stellt eine sehr schlanke Zuordnung zwischen der API und dem Gerätetreiber bereit, wodurch der Mehraufwand für hochfrequente Aufrufe minimiert wird. Da die Kernebene für die Leistung unerlässlich ist, führt sie nur eine kritische Überprüfung durch.

Die verbleibenden Ebenen sind optional. In der Regel fügen Ebenen Funktionen hinzu, ändern jedoch nicht das vorhandene Verhalten. Kernfunktionen verfügen beispielsweise unabhängig von der instanziierten Debugebene über dieselben Rückgabewerte, obwohl zusätzliche Debugausgabe bereitgestellt werden kann, wenn die Debugebene instanziiert wird.

Erstellen Sie Ebenen, wenn ein Gerät erstellt wird, indem [**Sie D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) aufrufen und mindestens einen [**D3D10 \_ CREATE DEVICE \_ \_ FLAG-Wert**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) liefern.

## <a name="debug-layer"></a>Debugebene

Die Debugebene bietet umfangreiche zusätzliche Parameter- und Konsistenzüberprüfungen (z. B. Überprüfen der Shaderverknüpfung und Ressourcenbindung, Überprüfen der Parameterkonsistenz und Melden von Fehlerbeschreibungen). Die von der Debugebene generierte Ausgabe besteht aus einer Warteschlange von Zeichenfolgen, auf die über die [**ID3D10InfoQueue-Schnittstelle**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) zugegriffen werden kann (siehe Anpassen der Debugausgabe mit [ID3D10InfoQueue (Direct3D 10)](d3d10-graphics-programming-guide-api-features-layers-info-queue.md)). Fehler, die von der Kernebene generiert werden, werden von der Debugebene mit Warnungen hervorgehoben.

Um ein Gerät zu erstellen, das die Debugebene unterstützt, müssen Sie das DirectX SDK installieren (um D3D10SDKLayers.DLL zu erhalten), und dann das D3D10 CREATE DEVICE DEBUG-Flag angeben, wenn \_ \_ Sie \_ [**D3D10CreateDevice aufrufen.**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) Natürlich wird die Ausführung einer Anwendung mit der Debugebene erheblich langsamer sein. Rufen Sie zum Aktivieren/Deaktivieren von Debugmeldungen für D3DX10-APIs [**D3DX10DebugMute auf.**](d3dx10debugmute.md)

Wenn die Debugebene Speicherverluste auflistet, gibt sie eine Liste von Objektschnittstellenzeigern zusammen mit ihren Anzeigenamen aus. Der Standardmäßige Anzeigename ist &lt; "unbenannt". &gt; Sie können den Anzeigenamen mithilfe der [**ID3D10DeviceChild::SetPrivateData-Methode**](/windows/desktop/api/D3D10/nf-d3d10-id3d10devicechild-setprivatedata) und der **GUID WKPDID \_ D3DDebugObjectName** in D3Dcommon.h festlegen. Verwenden Sie beispielsweise den folgenden Code, um pTexture mit dem SDKLayer-Namen mytexture.jpg zu benennen:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



In der Regel sollten Sie diese Aufrufe aus Ihrer Produktionsversion kompilieren.

## <a name="switch-to-reference-layer"></a>Wechseln zur Referenzebene

Diese Ebene ermöglicht einer Anwendung den Übergang zwischen einem Hardwaregerät (HARDWARE Device, HALOGEN) und einem Referenz- oder Softwaregerät (Ref). Um ein Gerät zu wechseln, müssen Sie zunächst ein Gerät erstellen, das die Switch-to-Reference-Ebene unterstützt (siehe [**D3D10CreateDevice),**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)und dann [**ID3D10SwitchToRef::SetUseRef**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10switchtoref-setuseref)aufrufen.

Alle Gerätezustände, Ressourcen und Objekte werden durch diesen Geräteübergang verwaltet. Es ist jedoch manchmal nicht möglich, Ressourcendaten genau abzugleichen. Dies liegt daran, dass einige Informationen für ein Hardwaregerät verfügbar sind, das für ein Referenzgerät nicht verfügbar ist.

Praktisch alle Echtzeitanwendungen verwenden die MSI-Implementierung der Pipeline. Wenn die Pipeline von einem Hardwaregerät auf ein Referenzgerät umgestellt wird, werden Renderingvorgänge sowohl in Hardware als auch in Software gleichzeitig ausgeführt. Wenn das Softwaregerät gerendert wird, müssen Ressourcen in den Systemspeicher heruntergeladen werden. Dies erfordert möglicherweise, dass andere im Systemspeicher zwischengespeicherte Ressourcen entfernt werden, um Platz zu schaffen.

> [!Note]  
> Dieses Feature zur Verweisebene wird nur in Direct3D 10 und Direct3D 10.1 und in Direct3D 11 und höher nicht mehr unterstützt.

 

## <a name="thread-safe-layer"></a>Thread-Safe Ebene

Diese Ebene ist so konzipiert, dass Multithreadanwendungen von mehreren Threads aus auf das Gerät zugreifen können.

Eine Direct3D 10-Anwendung kann eine Gerätesynchronisierung mithilfe von Gerätefunktionen steuern. Auf diese Weise kann eine Anwendung kritische Abschnitte aktivieren/deaktivieren (vorübergehend multithreading-Schutz aktivieren/deaktivieren) und eine kritische Abschnittssperre über mehrere Direct3D 10-API-Einstiegspunkte verwenden/deaktivieren. Die threadsichere Ebene ist standardmäßig aktiviert. Bei Singlethreadanwendungen hat die threadsichere Ebene keine Auswirkungen auf die Leistung.




Unterschiede zwischen Direct3D 9 und Direct3D 10:

- Im Gegensatz zu Direct3D 9 ist die Direct3D 10-API standardmäßig vollständig threadsicher.



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Features (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




