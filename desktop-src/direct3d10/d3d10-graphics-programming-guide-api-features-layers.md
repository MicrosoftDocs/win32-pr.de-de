---
description: API-Ebenen (Direct3D 10)
ms.assetid: 19c81383-6ac7-49ea-98a3-bf761a32ab40
title: API-Ebenen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd452032eda61c49edbf007b5ebaf0314f9054fe0b016cf07e3f4473ae3abee6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119990"
---
# <a name="api-layers-direct3d-10"></a>API-Ebenen (Direct3D 10)

Die Direct3D 10-Runtime wird mit Ebenen erstellt, beginnend mit der grundlegenden Funktionalität im Kern und dem Erstellen optionaler und Entwicklerunterstützungsfunktionen in äußeren Ebenen.

## <a name="core-layer"></a>Kernebene

Die Kernebene ist standardmäßig vorhanden. bereitstellung einer sehr schlanken Zuordnung zwischen der API und dem Gerätetreiber, wodurch der Mehraufwand für Aufrufe mit hoher Häufigkeit minimiert wird. Da die Kernebene für die Leistung von entscheidender Bedeutung ist, führt sie nur eine kritische Überprüfung durch.

Die übrigen Ebenen sind optional. Im Allgemeinen fügen Ebenen Funktionen hinzu, ändern jedoch das vorhandene Verhalten nicht. Kernfunktionen verfügen beispielsweise unabhängig von der instanziierten Debugebene über die gleichen Rückgabewerte, obwohl eine zusätzliche Debugausgabe bereitgestellt werden kann, wenn die Debugebene instanziiert wird.

Erstellen Sie Ebenen, wenn ein Gerät erstellt wird, indem [**Sie D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) aufrufen und mindestens einen [**D3D10 \_ CREATE DEVICE \_ \_ FLAG-Wert**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) bereitstellen.

## <a name="debug-layer"></a>Debugebene

Die Debugebene bietet eine umfassende zusätzliche Parameter- und Konsistenzüberprüfung (z. B. Überprüfen der Shaderbindung und Ressourcenbindung, Überprüfen der Parameterkonsistenz und Melden von Fehlerbeschreibungen). Die von der Debugebene generierte Ausgabe besteht aus einer Warteschlange von Zeichenfolgen, auf die über die [**ID3D10InfoQueue-Schnittstelle**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) zugegriffen werden kann (siehe Anpassen der [Debugausgabe mit ID3D10InfoQueue (Direct3D 10)](d3d10-graphics-programming-guide-api-features-layers-info-queue.md)). Von der Kernebene generierte Fehler werden mit Warnungen der Debugschicht hervorgehoben.

Um ein Gerät zu erstellen, das die Debugebene unterstützt, müssen Sie das DirectX SDK installieren (um D3D10SDKLayers.DLL zu erhalten) und dann das D3D10 \_ CREATE \_ DEVICE \_ DEBUG-Flag angeben, wenn [**Sie D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)aufrufen. Natürlich ist das Ausführen einer Anwendung mit der Debugebene erheblich langsamer. Um Debugmeldungen für D3DX10-APIs zu aktivieren/zu deaktivieren, rufen Sie [**D3DX10DebugMute auf.**](d3dx10debugmute.md)

Wenn die Debugebene Speicherverluste auflistet, gibt sie eine Liste von Objektschnittstellenzeigern zusammen mit ihren Anzeigenamen aus. Der Standardmäßige Anzeigename ist &lt; "unbenannt". &gt; Sie können den Anzeigenamen mithilfe der [**ID3D10DeviceChild::SetPrivateData-Methode**](/windows/desktop/api/D3D10/nf-d3d10-id3d10devicechild-setprivatedata) und der **GUID WKPDID \_ D3DDebugObjectName** in D3Dcommon.h festlegen. Verwenden Sie beispielsweise den folgenden Code, um pTexture mit dem SDKLayer-Namen mytexture.jpg zu benennen:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



In der Regel sollten Sie diese Aufrufe aus Ihrer Produktionsversion kompilieren.

## <a name="switch-to-reference-layer"></a>Wechseln zur Referenzebene

Diese Ebene ermöglicht es einer Anwendung, zwischen einem Hardwaregerät (HARDWARE Device, HALOGEN) und einem Referenz- oder Softwaregerät (REF) zu übergehen. Um ein Gerät zu wechseln, müssen Sie zunächst ein Gerät erstellen, das die Switch-to-Reference-Ebene unterstützt (siehe [**D3D10CreateDevice),**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)und dann [**ID3D10SwitchToRef::SetUseRef**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10switchtoref-setuseref)aufrufen.

Alle Gerätezustände, Ressourcen und Objekte werden durch diesen Geräteübergang verwaltet. Es ist jedoch manchmal nicht möglich, Ressourcendaten genau abzugleichen. Dies liegt daran, dass einige Informationen für ein Hardwaregerät verfügbar sind, das für ein Referenzgerät nicht verfügbar ist.

Praktisch alle Echtzeitanwendungen verwenden die MSI-Implementierung der Pipeline. Wenn die Pipeline von einem Hardwaregerät auf ein Referenzgerät umgestellt wird, werden Renderingvorgänge sowohl in Hardware als auch in Software gleichzeitig ausgeführt. Während das Softwaregerät gerendert wird, müssen Ressourcen in den Systemspeicher heruntergeladen werden. Dies erfordert möglicherweise, dass andere im Systemspeicher zwischengespeicherte Ressourcen entfernt werden, um Platz zu schaffen.

> [!Note]  
> Dieses Feature zur Verweisebene wird nur in Direct3D 10 und Direct3D 10.1 und in Direct3D 11 und höher nicht mehr unterstützt.

 

## <a name="thread-safe-layer"></a>Thread-Safe Ebene

Diese Ebene ist so konzipiert, dass Multithreadanwendungen von mehreren Threads aus auf das Gerät zugreifen können.

Eine Direct3D 10-Anwendung kann eine Gerätesynchronisierung mithilfe von Gerätefunktionen steuern. Dadurch kann eine Anwendung kritische Abschnitte aktivieren/deaktivieren (multithreading-Schutz vorübergehend aktivieren/deaktivieren) und eine Kritische-Abschnitt-Sperre für mehrere Direct3D 10-API-Einstiegspunkte verwenden/freigeben. Die threadsichere Ebene ist standardmäßig aktiviert. Bei Singlethreadanwendungen hat die threadsichere Ebene keine Auswirkungen auf die Leistung.




Unterschiede zwischen Direct3D 9 und Direct3D 10:

- Im Gegensatz zu Direct3D 9 ist die Direct3D 10-API standardmäßig vollständig threadsicher.



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Features (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




