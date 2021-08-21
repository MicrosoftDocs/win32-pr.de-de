---
title: Implementieren eines gehosteten Geräts
description: Der Gerätehost mit UPnP-Technologie implementiert die Ermittlung, Beschreibung, Steuerung und Ereignisermittlung der UPnP-Kernprotokolle.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fd12788c40d21dc84e896f1aba83085b440b86fbb54b68b4fbcfddbbe910c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008050"
---
# <a name="implementing-a-hosted-device"></a>Implementieren eines gehosteten Geräts

Der Gerätehost mit UPnP-Technologie implementiert die wichtigsten UPnP-Protokolle: Ermittlung, Beschreibung, Steuerung und Ereigniserkennung. Der Entwickler, der ein gehostetes Gerät implementiert, muss nur Die folgenden Angaben machen:

-   Eine Beschreibung des Geräts und seiner Dienste.
-   Eine Implementierung der Gerätefunktionalität.

Der Entwickler eines Uhrgeräts muss z. B. UPnP-basierte Geräte- und Dienstbeschreibungen dafür sowie eine Implementierung der Uhrfunktionen (z. B. Zeit behalten, Zeit festlegen und auf Abfragen für die aktuelle Zeit reagieren) bereitstellen. Der Gerätehost:

-   Kündigt das Gerät gemäß dem UPnP-Ermittlungsprotokoll an.
-   Antwortet auf Abfragen für die Beschreibung des Geräts.
-   Leitet Steuerungsanforderungen an den Teil des Gerätecodes weiter, der die Uhrfunktionen implementiert.
-   Verwaltet Ereignisabonnements für Dienste.
-   Sendet Ereignisbenachrichtigungen an Abonnenten, wenn sich der Zustand des Diensts ändert.

 

 




