---
title: Was sind die grundlegenden Aktionen der Steuerungspunkt-API?
description: Alle Steuerungspunkte führen die folgenden Aufgaben aus.
ms.assetid: f681468f-90ab-4533-8ee7-6e4f93e08cf2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a102c389a41b32fd7a79bf749ce38f1267912c3993e2461adac9b6730ea92325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513640"
---
# <a name="what-are-the-basic-actions-of-the-control-point-api"></a>Was sind die grundlegenden Aktionen der Steuerungspunkt-API?

Alle Kontrollpunkte führen die folgenden Aufgaben aus:

-   Suchen Sie verfügbare UPnP-basierte Geräte im Netzwerk.
-   Bestimmen Sie, welches dieser Geräte von Interesse ist.
-   Geben Sie Steuerungsanforderungen an die für Sie interessanten Geräte aus, und empfangen Sie von den Geräten generierte Ereignisse.

Eine Anwendung muss zunächst verfügbare UPnP-basierte Geräte im Netzwerk suchen, indem sie eine Suche durchführen. Da die von der UPnP-Architektur definierten Suchkriterien recht weit gefasst sind, findet die Anwendung möglicherweise mehr Geräte als erforderlich. Daher muss die Anwendung die Merkmale der gefundenen Geräte untersuchen, um zu bestimmen, welche geräte den Suchkriterien am besten entsprechen. Die Anwendung kann dann Steuerungsanforderungen an diese Geräte senden.

In den folgenden Abschnitten wird beschrieben, wie diese Vorgänge mithilfe der Steuerungspunkt-API mit UPnP-Technologie durchgeführt werden:

-   [Suchen von Geräten](finding-devices.md)
-   [Beschreiben von Geräten](describing-devices.md)
-   [Steuern von Geräten](controlling-devices.md)

Eine ausführliche Dokumentation zu den einzelnen Schnittstellen in der Control Point-API finden Sie in der [Referenz zur Control Point-API.](control-point-api-with-upnp-technology-reference.md)

 

 




