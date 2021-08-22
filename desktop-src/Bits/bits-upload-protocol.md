---
title: BITS Hochladen Protocol
description: In diesem Abschnitt wird das Netzwerkprotokoll für bits upload- und upload-reply-Auftragstypen beschrieben.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01fea1ff4703dba9a0429c0b37e9c34ebe0d0099016af788c972dd8ee9fddef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021237"
---
# <a name="bits-upload-protocol"></a>BITS Hochladen Protocol

In diesem Abschnitt wird das Netzwerkprotokoll für bits upload- und upload-reply-Auftragstypen beschrieben. Das BITS-Uploadprotokoll basiert auf HTTP 1.1 und verwendet viele der vorhandenen HTTP-Header und definiert neue Header. Das BITS-Uploadprotokoll unterstützt eine einzelne Uploaddatei pro Sitzung.

BITS verwendet Pakete, um Clientanforderungen und Serverantworten zu beschreiben. Der BITS-Packet-Type-Header gibt den Typ des gesendeten Pakets an. Jedes Paket enthält bestimmte Header. BITS verwendet das BITS \_ POST-Verb, um BITS-Uploadpakete zu identifizieren. Antwortpakete verwenden immer den Pakettyp "Ack", der für "bestätigen" steht. Das Ack-Paket wird im Kontext der vorherigen Anforderung gesendet. Es kann nur eine ausstehende Anforderung gleichzeitig vorhanden sein.

Bei Upload-Antwort-Aufträgen verwendet BITS dieses Protokoll, um die Datei hochzuladen, aber nicht dieses Protokoll, um die Antwort an den Client zu senden. Stattdessen sendet der BITS-Server den Speicherort der Antwortdatei an den Client, und der Client erstellt einen BITS-Downloadauftrag, um die Antwortdatei herunterzuladen.

Verwenden Sie das Uploadprotokoll, um den BITS-Client oder die Serversoftware durch Ihre eigene Implementierung zu ersetzen. Eine Liste der vom BITS-Client gesendeten Anforderungspakete finden Sie unter [BITS-Anforderungspakete.](bits-request-packets.md) Eine Liste der vom BITS-Server gesendeten Antwortpakete finden Sie unter [BITS-Antwortpakete.](bits-response-packets.md)

Der Client bestimmt, wie er auf Fehler oder unerwartete Pakete vom BITS-Server reagiert. Wenn der Server ein Paket empfängt, das nicht erwartet wird, sollte der Server ein Ack-Paket mit dem Rückgabecode 400 (Ungültige Anforderung) senden.

 

 




