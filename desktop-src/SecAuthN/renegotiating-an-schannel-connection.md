---
description: Zum Ändern der Attribute einer Verbindung, z. b. der Verschlüsselungs Sammlung oder der Client Authentifizierung, können Sie eine &0034, eine \# Wiederholung&\# 0034 oder eine erneute Aushandlung der Verbindung anfordern.
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: Neuverhandlung einer Kanalverbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fbcd25dad39ab7f35e77277eee9275004cd8a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367917"
---
# <a name="renegotiating-an-schannel-connection"></a>Neuverhandlung einer Kanalverbindung

Wenn Sie die Attribute einer Verbindung ändern möchten, z. b. die Verschlüsselungs Sammlung oder die Client Authentifizierung, können Sie eine Wiederholung oder eine erneute Aushandlung der Verbindung anfordern.

Wenn die zu ändernde Attribute über Anmelde Informationen gesteuert werden, müssen Sie vor der erneuten Aushandlung der Verbindung neue Anmelde Informationen abrufen. Weitere Informationen finden Sie unter Abrufen von [SChannel-Anmelde](obtaining-schannel-credentials.md)Informationen.

Um eine Wiederholung von einer Client Anwendung anzufordern, müssen Sie die Funktion [**InitializeSecurityContext (SChannel)**](./initializesecuritycontext--schannel.md) aufzurufen. Server Anwendungen nennen die Funktion " [**akzeptsecuritycontext" (SChannel)**](acceptsecuritycontext--schannel.md) . Legen Sie die Parameter wie folgt fest:

-   Geben Sie den vorhandenen [*Sicherheitskontext*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) im Parameter " *phcontext* " an.
-   (Nur Clients) Geben Sie den gleichen Servernamen (im *psztargetname* -Parameter) an, wie beim Einrichten des Kontexts angegeben.
-   Geben Sie ggf. neue Anmelde Informationen mithilfe des Parameters *phcredential* an.
-   Wenn Sie Kontext Attribute ändern möchten, die nicht mit den Anmelde Informationen verknüpft sind, geben Sie diese Attribute mithilfe des *fContextReq* -Parameters an.

Nachdem Sie die entsprechende Funktion aufgerufen haben, sollte Ihre Anwendung die Ergebnisse an den Client senden und die Verarbeitung eingehender Nachrichten mit der Funktion [**DecryptMessage (SChannel)**](decryptmessage--schannel.md) fortsetzen.

Die Funktion [**DecryptMessage (SChannel)**](decryptmessage--schannel.md) gibt Sekunde zurück \_ , die ich erneut \_ aushandeln, wenn SChannel für die Fortsetzung ihrer Anwendung bereit ist. Wenn Sie die Sekunde nach der erneuten Aushandlung von \_ \_ Rückgabecode erhalten, muss Ihre Anwendung " [**Accept-SecurityContext (SChannel)**](acceptsecuritycontext--schannel.md) (Server)" oder " [**InitializeSecurityContext (SChannel)**](./initializesecuritycontext--schannel.md) (Clients)" abrufen und die Inhalte der von "DecryptMessage" zurückgegebenen SECBUFFER_EXTRA in der SECBUFFER_TOKEN übergeben. Nachdem dieser Rückruf einen Wert zurückgegeben hat, fahren Sie so fort, als ob Ihre Anwendung eine neue Verbindung erstellt hat.

 

 
