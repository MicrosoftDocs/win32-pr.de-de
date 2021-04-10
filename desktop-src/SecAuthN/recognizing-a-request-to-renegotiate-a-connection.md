---
description: Die Funktion DecryptMessage (allgemein) fängt Anforderungen für die Aushandlung aus dem Absender der Nachricht ab. Sie benachrichtigt Ihre Anwendung, indem Sie die Nachrichten Daten entschlüsselt und den Wert von Sekunde zurückgibt, der erneut \_ \_ ausgehandelt wird.
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: Erkennen einer Anforderung zum Aushandeln einer Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ae8083c59485b8b7c917fe03893fa363f5a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042222"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a><span data-ttu-id="815c0-104">Erkennen einer Anforderung zum Aushandeln einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="815c0-104">Recognizing a Request to Renegotiate a Connection</span></span>

<span data-ttu-id="815c0-105">Die Funktion [**DecryptMessage (allgemein)**](decryptmessage--general.md) fängt Anforderungen für die Aushandlung aus dem Absender der Nachricht ab.</span><span class="sxs-lookup"><span data-stu-id="815c0-105">The [**DecryptMessage (General)**](decryptmessage--general.md) function traps requests for renegotiation coming from the message sender.</span></span> <span data-ttu-id="815c0-106">Sie benachrichtigt Ihre Anwendung, indem Sie die Nachrichten Daten entschlüsselt und den Wert von Sekunde zurückgibt, der erneut \_ \_ ausgehandelt wird.</span><span class="sxs-lookup"><span data-stu-id="815c0-106">It notifies your application by decrypting the message data and returning the SEC\_I\_RENEGOTIATE value.</span></span>

<span data-ttu-id="815c0-107">Diese Anforderungen müssen von Ihrer Anwendung verarbeitet werden, indem Sie " [**Accept-SecurityContext (allgemein)**](acceptsecuritycontext--general.md) (Server)" oder " [**InitializeSecurityContext (allgemein)**](initializesecuritycontext--general.md) (Clients)" aufrufen und den Inhalt der von "DecryptMessage" in der SECBUFFER_TOKEN zurückgegebenen SECBUFFER_EXTRA übergeben.</span><span class="sxs-lookup"><span data-stu-id="815c0-107">Your application must handle such requests by calling [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (servers) or [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) (clients) and passing the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="815c0-108">Nachdem dieser anfängliche-Befehl einen Wert zurückgegeben hat, fahren Sie so fort, als ob die Anwendung eine neue Verbindung erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="815c0-108">After this initial call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 



