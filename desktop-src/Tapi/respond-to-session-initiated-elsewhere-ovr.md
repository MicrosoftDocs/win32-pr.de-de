---
description: Wenn eine neue Kommunikationssitzung eintrifft, erhalten TAPI-Anwendungen, die ein Interesse an der Adresse und dem Medientyp registriert haben, eine Ereignisbenachrichtigung.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Reagieren auf an anderer Stelle initiierte Sitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74554b48919f7532561bfdf0bab7a163a58fbeb3734dc15e4a8d7e0869dad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072850"
---
# <a name="respond-to-session-initiated-elsewhere"></a>Reagieren auf an anderer Stelle initiierte Sitzungen

Wenn eine neue Kommunikationssitzung eintrifft, erhalten TAPI-Anwendungen, die ein Interesse an der Adresse und dem Medientyp registriert haben, eine [Ereignisbenachrichtigung.](event-notification.md) [](address-ovr.md) [](media-type-ovr.md) Nur einer Anwendung werden Besitzrechte [für](privilege-ovr.md) die Sitzung angeboten. Diese Anwendung kann die Sitzung nicht ablehnen.

Der anfängliche Aufrufstatus einer eingehenden Sitzung wird angeboten. Während sich der Aufruf im Angebotszustand befindet, kann eine Anwendung Informationen wie den Bearermodus und den Aufrufgrund abrufen, wenn die Dienstanbieter diese Informationen angegeben haben und verfügbar sind. Einige Aufrufinformationen sind möglicherweise nicht sofort verfügbar, z. B. die Aufrufer-ID.

Es gibt sechs grundlegende Antworten auf eine angebotene [Sitzung:](answer-ovr.md) [Antwort,](accept-ovr.md)Annehmen, [Übergabe,](handoffs-ovr.md) [Ablegen,](drop-ovr.md)Weiterleiten [und](forward-ovr.md) [Umleiten](redirect-ovr.md)von . Je nach Dienstanbieter ist der vollständige Satz dieser Vorgänge möglicherweise nicht verfügbar.

 

 



