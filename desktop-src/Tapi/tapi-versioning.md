---
description: Erfahren Sie mehr über die TAPI-Versionierung. Im Laufe der Zeit können verschiedene Versionen von TAPI, Anwendungen und Dienstanbietern erstellt werden.
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: TAPI-Versionierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853cf9d5f3744e11936f121986edc4e6e027d251
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989295"
---
# <a name="tapi-versioning"></a>TAPI-Versionierung

Im Laufe der Zeit können verschiedene Versionen von TAPI, Anwendungen und Dienstanbietern erstellt werden. Diese neuen Versionen können neue Definitionen erstellen, z. B. für neue Features, neue Member in Datenstrukturen und neue Bitfelder. Versionsnummern sind daher erforderlich, um anzugeben, wie verschiedene Datenstrukturen interpretiert werden.

Um eine optimale Interoperabilität verschiedener Versionen von Anwendungen, Versionen von TAPI selbst und Versionen von Dienstanbietern verschiedener Anbieter zu ermöglichen, bietet Microsoft-Telefonie einen einfachen Mechanismus zur Versionsaushandlung für Anwendungen. Es gibt zwei verschiedene Versionen, die TAPI und der Telefoniedienstanbieter für jedes Liniengerät zustimmen müssen. Die erste Version ist die Version, die mit TAPI und dem Telefoniedienstanbieter (TSP) Basic und Supplementary Telefonie ausgehandelt wurde, die als TAPI-Schnittstellenversion bezeichnet wird. Die andere ist für anbieterspezifische Erweiterungen (sofern verfügbar) und wird als Erweiterungsversion bezeichnet. Das Format der Datenstrukturen und Datentypen, die von den grundlegenden und ergänzenden Features von TAPI verwendet werden, wird durch die TAPI-Version definiert, während die Erweiterungsversion das Format der Datenstrukturen bestimmt, die von den herstellerspezifischen Erweiterungen definiert werden.

Die [**lineNegotiateAPIVersion-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) handelt eine TAPI-Version aus, [**und lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) handelt die Version der TSP-Erweiterung aus. Ein einzelner TSP kann mehrere Versionen behandeln, und eine Anwendung muss bei Verwendung eines älteren TSP auf die Verwendung einer älteren Version "zurückfallen". In **lineNegotiateAPIVersion** wird der *dwApiVersion-Parameter* standardmäßig wie folgt auf einen Wert entsprechend der Version festgelegt.



| TAPI-Version | Standardwert |
|--------------|---------------|
| 1.3          | 0x00010003    |
| 1.4          | 0x00010004    |
| 2.0          | 0x00020000    |
| 2.1          | 0x00020001    |
| 2.2          | 0x00020002    |



 

TapI erleichtert dies jedoch deutlich, solange der TSP selbst eine neuere Version als die Anwendung verwendet. Wenn der TSP tatsächlich neuer ist, kann TAPI "down" in die Version der Anwendung übersetzen. TapI 2.0-TSPs müssen z. B. nicht speziell mit TAPI Version 1.4 zu tun haben. Wenn eine TAPI 1.4-Anwendung ausgeführt wird, konvertiert TAPI alle TAPI 2.0-Strukturen und -Nachrichten in TAPI 1.4-Entsprechungen oder so nah wie möglich. Wenn in TAPI 1.4 keine näherungsbasierten Informationen enthalten sind, gehen alle TAPI 2.0-spezifischen Informationen verloren.

Die genaue Bedeutung einer Erweiterungsversion ist anbieterspezifisch. Informationen zur Verwendung eines TSP, der Erweiterungen unterstützt, finden Sie in der Dokumentation des Anbieters.

Es gibt eine Reihe von Versionen von TAPI. Während die meisten dieser Versionen Änderungen an den TAPI- und TSPI-Dokumentationssätzen (Telefonie-Dienstanbieterschnittstelle) umfassten, gibt es weitere Auswirkungen auf jede Version, nämlich architektonische Unterschiede, Betriebssystemvariationen, verteilbare Elemente und TSP-Entwicklungsprobleme.



| TAPI-Version        | Distribution                                                   |
|---------------------|----------------------------------------------------------------|
| 1.0 – 1.2           | Betaversionen, die nicht mehr verwendet werden sollten.              |
| [1.4](tapi-1-4.md) | In Windows 95 enthalten.                                        |
| [1.5](tapi-1-5.md) | Enthalten in Windows CE 1.0.                                    |
| [2.0](tapi-2-0.md) | Enthalten in Windows NT 4.0 mit SP3.                           |
| [2.1](tapi-2-1.md) | Enthalten in Windows NT 4.0 mit SP4 und Windows 98.            |
| [2.2](tapi-2-2.md) | Enthalten in Windows Server 2003, Windows XP und Windows 2000. |



 

 

 



