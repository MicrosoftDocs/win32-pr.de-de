---
title: Gründe für die Verwendung dieses Replikationsmodells durch Active Directory Domain Services
description: In diesem Thema werden die Gründe für das Freiformsystem erläutert, das von Active Directory Domain Services für ein Replikationsmodell verwendet wird.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Replikationsmodell Active Directory , Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79c137fadf768c97b6d8be962b22c74b45e30bc41c7dfb7e9ea67e1f145cd92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181991"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a>Gründe für die Verwendung dieses Replikationsmodells durch Active Directory Domain Services

In diesem Thema werden die Gründe für das Freiformsystem erläutert, das von Active Directory Domain Services für ein Replikationsmodell verwendet wird.

Active Directory Domain Services sind aus folgenden Gründen ein Freiformsystem:

-   Kunden benötigen eine hochgradig verteilte Lösung, in der Teile des Verzeichnisses auf ihre Netzwerke verteilt und lokal verwaltet werden können.
-   Große Kunden wachsen häufig auf Millionen von Objekten, Hunderte oder Tausende von Replikaten oder beides an.
-   Viele Kundennetzwerke bieten nur zeitweilige Verbindungen mit einigen Standorten. Beispielsweise sind Remote-Öl-Drillplattformen und -versande auf See, sodass das System gegenüber teilweise verbundenen oder getrennten Vorgängen tolerant sein muss.

Es gibt keine Möglichkeit, eine vollständige Kenntnis des aktuellen oder zukünftigen Zustands eines verteilten Systems zu gewährleisten, da das Wissen über Zustandsänderungen weitergegeben werden muss und die Weitergabe eine Zeit in Anspruch nimmt, während der weitere Zustandsänderungen auftreten können.

Eng gekoppelte Systeme bewältigen die Unsicherheit, indem sie versuchen, sie zu beseitigen. Dies erfolgt durch Einschränkungen für Updates, die erfordern, dass alle Knoten oder ein Großteil der Knoten verfügbar sein müssen, bevor Updates ausgeführt werden können, verteilte Sperrschemas oder Singlemastering für kritische Ressourcen, das Einschränken aller Knoten für eine gute Verbindung oder eine Kombination dieser Techniken. Je enger die Computingknoten in einem verteilten System gekoppelt sind, desto niedriger ist der Skalierungsgrenzwert.

Freiformsysteme behandeln Unsicherheit, indem sie sie tolerieren. Ein Freiformsystem ermöglicht es den Knoten, unterschiedliche Ansichten des Gesamtsystemzustands zu erhalten, und stellt Algorithmen zum Lösen von Konflikten bereit.

Eng gekoppelte Lösungen wurden aufgrund der Anforderungen an die lokale Verwaltung, den getrennten Betrieb und die Skalierbarkeit für eine sehr große Anzahl von Knoten als ungeeignet für Active Directory Domain Services abgelehnt. Das ausgewählte lose gekoppelte Modell, die lose Multimasterkonsistenz mit Konvergenz, erfüllt alle Anforderungen.

 

 




