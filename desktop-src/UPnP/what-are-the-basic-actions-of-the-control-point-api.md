---
title: Was sind die grundlegenden Aktionen der Steuerungspunkt-API?
description: Alle Kontrollpunkte führen die folgenden Aufgaben aus.
ms.assetid: f681468f-90ab-4533-8ee7-6e4f93e08cf2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252e2db09aa8283034da20dc1bd2dc877bf0e5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713529"
---
# <a name="what-are-the-basic-actions-of-the-control-point-api"></a>Was sind die grundlegenden Aktionen der Steuerungspunkt-API?

Alle Kontrollpunkte führen die folgenden Aufgaben aus:

-   Suchen Sie verfügbare UPnP-basierte Geräte im Netzwerk.
-   Bestimmen Sie, welche dieser Geräte von Interesse sind.
-   Ausstellen Sie Steuerungsanforderungen an die relevanten Geräte, und empfangen Sie von den Geräten generierte Ereignisse.

Eine Anwendung muss zuerst verfügbare UPnP-basierte Geräte im Netzwerk suchen, indem Sie eine Suche durchführen. Da die von der UPnP-Architektur definierten Suchkriterien ziemlich breit sind, kann die Anwendung mehr Geräte als benötigt finden. Daher muss die Anwendung die Merkmale der gefundenen Geräte überprüfen, um festzustellen, welche mit den Suchkriterien am ehesten übereinstimmen. Die Anwendung kann dann Steuerungsanforderungen an diese Geräte ausstellen.

In den folgenden Abschnitten wird beschrieben, wie diese Vorgänge mit der Steuerungspunkt-API mit UPnP-Technologie durchgeführt werden:

-   [Suchen nach Geräten](finding-devices.md)
-   [Beschreiben von Geräten](describing-devices.md)
-   [Steuern von Geräten](controlling-devices.md)

Eine ausführliche Dokumentation zu den einzelnen Schnittstellen in der Steuerungspunkt-API finden Sie unter [Steuerungspunkt-API-Referenz](control-point-api-with-upnp-technology-reference.md).

 

 




