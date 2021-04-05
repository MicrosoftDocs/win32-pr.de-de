---
title: Bits-Upload-Protokoll
description: In diesem Abschnitt wird das Netzwerkprotokoll für die Auftrags Typen "Bits Upload" und "Upload-Reply" beschrieben.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642426decd0bc37390fa9fdd9b1ad2be11a0aa84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708142"
---
# <a name="bits-upload-protocol"></a>Bits-Upload-Protokoll

In diesem Abschnitt wird das Netzwerkprotokoll für die Auftrags Typen "Bits Upload" und "Upload-Reply" beschrieben. Das Bits-uploadprotokoll wird über HTTP 1,1 geschichtet und verwendet viele der vorhandenen HTTP-Header und definiert neue Header. Das Bits-uploadprotokoll unterstützt eine einzelne Uploaddatei pro Sitzung.

Bits verwendet Pakete, um Client Anforderungen und Server Antworten zu beschreiben. Der Bits-Packet-Type-Header gibt den Typ des zu sendenden Pakets an. Jedes Paket enthält bestimmte Header. Bits verwendet das Bits \_ Post-Verb, um Bits-Uploadpakete zu identifizieren. Antwort Pakete verwenden immer den ACK-Pakettyp, der für Bestätigungen steht. Das ACK-Paket wird im Kontext der vorherigen Anforderung gesendet. Es darf nur eine ausstehende Anforderung gleichzeitig vorhanden sein.

Für Upload-Antwort-Aufträge verwendet Bits dieses Protokoll, um die Datei hochzuladen, verwendet jedoch dieses Protokoll nicht, um die Antwort an den Client zu senden. Stattdessen sendet der BITS-Server den Speicherort der Antwortdatei an den Client, und der Client erstellt einen Bits-Download Auftrag zum Herunterladen der Antwortdatei.

Verwenden Sie das uploadprotokoll, um den Bits-Client oder die Server Software durch ihre eigene Implementierung zu ersetzen. Eine Liste der vom BITS-Client gesendeten Anforderungs Pakete finden Sie unter [Bits-Anforderungs Pakete](bits-request-packets.md). Eine Liste der vom BITS-Server gesendeten Antwort Pakete finden Sie unter [Bits-Antwort Pakete](bits-response-packets.md).

Der Client bestimmt, wie er auf Fehler oder unerwartete Pakete vom BITS-Server reagiert. Wenn der Server ein Paket empfängt, das er nicht erwartet, sollte der Server ein ACK-Paket mit dem Rückgabecode 400 (ungültige Anforderung) senden.

 

 




