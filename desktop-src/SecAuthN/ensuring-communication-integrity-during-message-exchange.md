---
description: Nachdem ein Sicherheitskontext eingerichtet wurde, kann die Anwendung die Nachrichten Unterstützungsfunktionen verwenden, um Manipulations geschützte Nachrichten zu übertragen.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Sicherstellen der Kommunikations Integrität während des Nachrichten Austauschs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70545abf11a933cd3bb6d0c32f3312637fcccbe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128805"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a><span data-ttu-id="25624-103">Sicherstellen der Kommunikations Integrität während des Nachrichten Austauschs</span><span class="sxs-lookup"><span data-stu-id="25624-103">Ensuring Communication Integrity During Message Exchange</span></span>

<span data-ttu-id="25624-104">Nachdem ein [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) eingerichtet wurde, kann die Anwendung die [Nachrichten Unterstützungs](authentication-functions.md) Funktionen verwenden, um Manipulations geschützte Nachrichten zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="25624-104">After a [*security context*](/windows/desktop/SecGloss/s-gly) is established, the application can use the [message support](authentication-functions.md) functions to transmit tamper-resistant messages.</span></span>

<span data-ttu-id="25624-105">Der Client oder Server übergibt den Sicherheitskontext und eine Meldung an die [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) -Funktion, um eine sichere Signatur zu generieren, die verhindert, dass die Nachricht während der Übertragung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="25624-105">The client or server passes the security context and a message to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a secure signature that prevents the message from being modified while in transit.</span></span> <span data-ttu-id="25624-106">Der Empfänger der Nachricht Ruft die [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="25624-106">The receiver of the message calls the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function.</span></span> <span data-ttu-id="25624-107">**VerifySignature** verwendet die Informationen in der Signatur, um sicherzustellen, dass die empfangene Nachricht während der Übertragung nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="25624-107">**VerifySignature** uses the information in the signature to verify that the message received was not modified during transmission.</span></span> <span data-ttu-id="25624-108">Der Client und der Server können verschlüsselte Nachrichten auch mit [**verschlüsselungsmessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) und [**DecryptMessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)austauschen.</span><span class="sxs-lookup"><span data-stu-id="25624-108">The client and server can also exchange encrypted messages using [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span>

<span data-ttu-id="25624-109">Der Server in einer authentifizierten Verbindung kann auch Verbindungen mit anderen Remote Computern im Namen des Clients nach [**dem Aufruf von**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext)"Identitätsnachweis Nachweis" herstellen.</span><span class="sxs-lookup"><span data-stu-id="25624-109">The server in an authenticated connection can also make connections with other remote computers in the name of the client after calling [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).</span></span>

 

 
