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
# <a name="bits-upload-protocol"></a><span data-ttu-id="c95a3-103">Bits-Upload-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c95a3-103">BITS Upload Protocol</span></span>

<span data-ttu-id="c95a3-104">In diesem Abschnitt wird das Netzwerkprotokoll für die Auftrags Typen "Bits Upload" und "Upload-Reply" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c95a3-104">This section describes the network protocol for BITS upload and upload-reply job types.</span></span> <span data-ttu-id="c95a3-105">Das Bits-uploadprotokoll wird über HTTP 1,1 geschichtet und verwendet viele der vorhandenen HTTP-Header und definiert neue Header.</span><span class="sxs-lookup"><span data-stu-id="c95a3-105">The BITS upload protocol is layered on top of HTTP 1.1 and uses many of the existing HTTP headers and defines new headers.</span></span> <span data-ttu-id="c95a3-106">Das Bits-uploadprotokoll unterstützt eine einzelne Uploaddatei pro Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c95a3-106">The BITS upload protocol supports a single upload file per session.</span></span>

<span data-ttu-id="c95a3-107">Bits verwendet Pakete, um Client Anforderungen und Server Antworten zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c95a3-107">BITS uses packets to describe client requests and server responses.</span></span> <span data-ttu-id="c95a3-108">Der Bits-Packet-Type-Header gibt den Typ des zu sendenden Pakets an.</span><span class="sxs-lookup"><span data-stu-id="c95a3-108">The BITS-Packet-Type header specifies the type of packet being sent.</span></span> <span data-ttu-id="c95a3-109">Jedes Paket enthält bestimmte Header.</span><span class="sxs-lookup"><span data-stu-id="c95a3-109">Each packet contains specific headers.</span></span> <span data-ttu-id="c95a3-110">Bits verwendet das Bits \_ Post-Verb, um Bits-Uploadpakete zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c95a3-110">BITS uses the BITS\_POST verb to identify BITS upload packets.</span></span> <span data-ttu-id="c95a3-111">Antwort Pakete verwenden immer den ACK-Pakettyp, der für Bestätigungen steht.</span><span class="sxs-lookup"><span data-stu-id="c95a3-111">Response packets always use the Ack packet type which stands for acknowledge.</span></span> <span data-ttu-id="c95a3-112">Das ACK-Paket wird im Kontext der vorherigen Anforderung gesendet. Es darf nur eine ausstehende Anforderung gleichzeitig vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c95a3-112">The Ack packet is sent in the context of the previous request; there can be only one outstanding request at one time.</span></span>

<span data-ttu-id="c95a3-113">Für Upload-Antwort-Aufträge verwendet Bits dieses Protokoll, um die Datei hochzuladen, verwendet jedoch dieses Protokoll nicht, um die Antwort an den Client zu senden.</span><span class="sxs-lookup"><span data-stu-id="c95a3-113">For upload-reply jobs, BITS uses this protocol to upload the file but does not use this protocol to send the reply to the client.</span></span> <span data-ttu-id="c95a3-114">Stattdessen sendet der BITS-Server den Speicherort der Antwortdatei an den Client, und der Client erstellt einen Bits-Download Auftrag zum Herunterladen der Antwortdatei.</span><span class="sxs-lookup"><span data-stu-id="c95a3-114">Instead, the BITS server sends the location of the reply file to the client and the client creates a BITS download job to download the reply file.</span></span>

<span data-ttu-id="c95a3-115">Verwenden Sie das uploadprotokoll, um den Bits-Client oder die Server Software durch ihre eigene Implementierung zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c95a3-115">Use the upload protocol to replace the BITS client or server software with your own implementation.</span></span> <span data-ttu-id="c95a3-116">Eine Liste der vom BITS-Client gesendeten Anforderungs Pakete finden Sie unter [Bits-Anforderungs Pakete](bits-request-packets.md).</span><span class="sxs-lookup"><span data-stu-id="c95a3-116">For a list of request packets sent by the BITS client, see [BITS Request Packets](bits-request-packets.md).</span></span> <span data-ttu-id="c95a3-117">Eine Liste der vom BITS-Server gesendeten Antwort Pakete finden Sie unter [Bits-Antwort Pakete](bits-response-packets.md).</span><span class="sxs-lookup"><span data-stu-id="c95a3-117">For a list of response packets sent by the BITS server, see [BITS Response Packets](bits-response-packets.md).</span></span>

<span data-ttu-id="c95a3-118">Der Client bestimmt, wie er auf Fehler oder unerwartete Pakete vom BITS-Server reagiert.</span><span class="sxs-lookup"><span data-stu-id="c95a3-118">The client determines how it responds to errors or unexpected packets from the BITS server.</span></span> <span data-ttu-id="c95a3-119">Wenn der Server ein Paket empfängt, das er nicht erwartet, sollte der Server ein ACK-Paket mit dem Rückgabecode 400 (ungültige Anforderung) senden.</span><span class="sxs-lookup"><span data-stu-id="c95a3-119">If the server receives a packet that it does not expect, the server should send an Ack packet with a 400 (Bad Request) return code.</span></span>

 

 




