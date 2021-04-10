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
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a>Erkennen einer Anforderung zum Aushandeln einer Verbindung

Die Funktion [**DecryptMessage (allgemein)**](decryptmessage--general.md) fängt Anforderungen für die Aushandlung aus dem Absender der Nachricht ab. Sie benachrichtigt Ihre Anwendung, indem Sie die Nachrichten Daten entschlüsselt und den Wert von Sekunde zurückgibt, der erneut \_ \_ ausgehandelt wird.

Diese Anforderungen müssen von Ihrer Anwendung verarbeitet werden, indem Sie " [**Accept-SecurityContext (allgemein)**](acceptsecuritycontext--general.md) (Server)" oder " [**InitializeSecurityContext (allgemein)**](initializesecuritycontext--general.md) (Clients)" aufrufen und den Inhalt der von "DecryptMessage" in der SECBUFFER_TOKEN zurückgegebenen SECBUFFER_EXTRA übergeben. Nachdem dieser anfängliche-Befehl einen Wert zurückgegeben hat, fahren Sie so fort, als ob die Anwendung eine neue Verbindung erstellt hat.

 

 



