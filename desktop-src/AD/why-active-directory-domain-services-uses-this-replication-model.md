---
title: Warum Active Directory Domain Services dieses Replikations Modell verwendet
description: In diesem Thema werden die Gründe für das frei Form System erläutert, das von Active Directory Domain Services für ein Replikations Modell verwendet wird.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Replikations Modell Active Directory, Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855372"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a>Warum Active Directory Domain Services dieses Replikations Modell verwendet

In diesem Thema werden die Gründe für das frei Form System erläutert, das von Active Directory Domain Services für ein Replikations Modell verwendet wird.

Active Directory Domain Services sind aus folgenden Gründen ein frei Form System:

-   Kunden benötigen eine hochgradig verteilte Lösung, bei der Teile des Verzeichnisses auf Ihre Netzwerke verteilt und lokal verwaltet werden können.
-   Große Kunden wachsen häufig auf Millionen von Objekten, Hunderte oder Tausende von Replikaten oder beides.
-   Viele Kunden Netzwerke bieten nur zeitweilig eine Verbindung zu einigen Standorten. Beispielsweise werden remoteöl-drillingplattformen und-Systeme auf dem Meeres System ausgeliefert, damit das System teilweise verbundene oder getrennte Vorgänge tolerieren muss.

Es gibt keine Möglichkeit, eine umfassende Kenntnis des aktuellen oder zukünftigen Zustands eines verteilten Systems zu gewährleisten, weil Informationen zu Zustandsänderungen weitergegeben werden müssen und die Weitergabe Zeit in Anspruch nimmt.

Eng gekoppelte Systeme behandeln die Unsicherheit, indem Sie versuchen, Sie auszuschließen. Dies erfolgt durch Einschränkungen bei Updates, die erfordern, dass alle Knoten oder die Mehrzahl der Knoten verfügbar sind, bevor Updates durchgeführt werden können, indem verteilte Sperr Schemas verwendet werden oder ein Single-Mastering für kritische Ressourcen verwendet wird. Dadurch werden alle Knoten auf eine gute Verbindung beschränkt oder eine Kombination dieser Techniken. Je stärker die Computer Knoten in einem verteilten System gekoppelt sind, desto niedriger ist die Skalierungs Grenze.

Frei Formsysteme behandeln die Unsicherheit, indem Sie Sie tolerieren. Mit einem frei Form System können die Knoten unterschiedliche Ansichten des gesamten Systemstatus aufweisen und Algorithmen zum Auflösen von Konflikten bereitstellen.

Eng gekoppelte Lösungen wurden aufgrund der Anforderungen an die lokale Verwaltung, den getrennten Betrieb und die Skalierbarkeit einer sehr großen Anzahl von Knoten als ungeeignet für Active Directory Domain Services zurückgewiesen. Das lose gekoppelte Modell, das von der multimasterlose Datenkonsistenz mit Konvergenz gewählt wurde, erfüllt alle Anforderungen.

 

 




