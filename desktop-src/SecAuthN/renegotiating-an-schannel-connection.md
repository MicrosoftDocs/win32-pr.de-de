---
description: Um die Attribute einer Verbindung zu ändern, z. B. die Verschlüsselungssammlung oder die Clientauthentifizierung, können Sie eine &\# 0034;redo&0034 oder eine Neuverhandlung der \# Verbindung anfordern.
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: Neuverhandlung einer Kanalverbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b904400f5a440046214c39ea736c296685e0e56859f43b3a458f621d2a07d273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919399"
---
# <a name="renegotiating-an-schannel-connection"></a>Neuverhandlung einer Kanalverbindung

Um die Attribute einer Verbindung zu ändern, z. B. die Verschlüsselungssammlung oder die Clientauthentifizierung, können Sie eine "Erneute" oder Neuverhandlung der Verbindung anfordern.

Wenn die Attribute, die Sie ändern möchten, durch Anmeldeinformationen gesteuert werden, müssen Sie neue Anmeldeinformationen abrufen, bevor Sie die Verbindung neu aushandeln. Weitere Informationen finden Sie unter [Abrufen von Schannel-Anmeldeinformationen.](obtaining-schannel-credentials.md)

Rufen Sie die [**InitializeSecurityContext-Funktion (Schannel)**](./initializesecuritycontext--schannel.md) auf, um eine Wiederholen-Funktion von einer Clientanwendung an fordern. Serveranwendungen rufen die [**Funktion AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) auf. Legen Sie die Parameter wie folgt fest:

-   Geben Sie den vorhandenen [*Sicherheitskontext*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) im *phContext-Parameter* an.
-   (nur Clients) Geben Sie den gleichen Servernamen (im *Parameter pszTargetName)* an, den Sie beim Einrichten des Kontexts angegeben haben.
-   Geben Sie neue Anmeldeinformationen an, indem Sie *ggf. den Parameter phCredential* verwenden.
-   Wenn Sie Kontextattribute ändern möchten, die nicht mit den Anmeldeinformationen in Zusammenhang stehen, geben Sie diese Attribute mit dem *fContextReq-Parameter* an.

Nach dem Aufruf der entsprechenden Funktion sollte Ihre Anwendung die Ergebnisse an den Client senden und die Verarbeitung eingehender Nachrichten mithilfe der [**Funktion DecryptMessage (Schannel)**](decryptmessage--schannel.md) fortsetzen.

Die [**Funktion DecryptMessage (Schannel)**](decryptmessage--schannel.md) gibt SEC \_ I RENEGOTIATE zurück, wenn Schannel bereit ist, ihre \_ Anwendung fortzufahren. Wenn Sie den SEC I RENEGOTIATE-Rückgabecode erhalten, muss Ihre Anwendung \_ \_ [**AcceptSecurityContext (Schannel) (Server)**](acceptsecuritycontext--schannel.md) oder [**InitializeSecurityContext (Schannel) (Clients)**](./initializesecuritycontext--schannel.md) aufrufen und den Inhalt von SECBUFFER_EXTRA übergeben, der von DecryptMessage im SECBUFFER_TOKEN zurückgegeben wird. Nachdem dieser Aufruf einen Wert zurückgegeben hat, fahren Sie so fort, als ob Ihre Anwendung eine neue Verbindung erstellt hat.

 

 
