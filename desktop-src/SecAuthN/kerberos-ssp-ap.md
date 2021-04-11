---
description: Das Kerberos-Authentifizierungs Paket wird bei der Anmeldung bei einem Netzwerk verwendet. lokale Anmeldungen werden von MSV1 0 verarbeitet \_ .
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: Kerberos SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042383"
---
# <a name="kerberos-sspap"></a><span data-ttu-id="66b18-103">Kerberos SSP/AP</span><span class="sxs-lookup"><span data-stu-id="66b18-103">Kerberos SSP/AP</span></span>

<span data-ttu-id="66b18-104">Das [*Kerberos*](../secgloss/k-gly.md) -Authentifizierungs Paket wird bei der Anmeldung bei einem Netzwerk verwendet. lokale Anmeldungen werden von MSV1 0 verarbeitet \_ .</span><span class="sxs-lookup"><span data-stu-id="66b18-104">The [*Kerberos*](../secgloss/k-gly.md) authentication package is used when logging on to a network; local logons are handled by MSV1\_0.</span></span>

<span data-ttu-id="66b18-105">Wenn ein Benutzer sich mit einem Netzwerk Konto anmeldet, versucht Kerberos standardmäßig, eine Verbindung mit dem Kerberos- [*Schlüsselverteilungscenter*](../secgloss/k-gly.md) (KDC) auf dem Domänen Controller herzustellen und ein Ticket Erstellungs Ticket (TGT) zu erhalten, indem die vom Benutzer bereitgestellten Anmeldedaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66b18-105">When a user logs on using a network account, by default, Kerberos attempts to connect to the Kerberos [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) on the domain controller and obtain a ticket granting ticket (TGT) by using the logon data supplied by the user.</span></span>

<span data-ttu-id="66b18-106">Wenn ein Kerberos-KDC nicht verfügbar ist, verwendet Windows MSV1 \_ 0 und die Passthrough-Authentifizierung, wie unter [MSV1 \_ 0 Authentication Package](msv1-0-authentication-package.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="66b18-106">If a Kerberos KDC is not available, Windows uses MSV1\_0 and pass-through authentication as described in [MSV1\_0 Authentication Package](msv1-0-authentication-package.md).</span></span>

<span data-ttu-id="66b18-107">Das Kerberos-Authentifizierungs Paket unterstützt Version 5, Revision 6 des Kerberos-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="66b18-107">The Kerberos authentication package supports version 5, revision 6 of the Kerberos protocol.</span></span> <span data-ttu-id="66b18-108">Dieses Protokoll basiert auf Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).</span><span class="sxs-lookup"><span data-stu-id="66b18-108">This protocol is based on Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).</span></span> <span data-ttu-id="66b18-109">Weitere Informationen finden Sie auf der IETF-Website:</span><span class="sxs-lookup"><span data-stu-id="66b18-109">For more information, see the IETF website:</span></span>

[https://www.ietf.org](https://www.ietf.org/)

<span data-ttu-id="66b18-110">Weitere Informationen zu Kerberos finden Sie unter [Microsoft Kerberos](microsoft-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="66b18-110">For more information about Kerberos, see [Microsoft Kerberos](microsoft-kerberos.md).</span></span>

## <a name="kerberos-credential-formats"></a><span data-ttu-id="66b18-111">Kerberos-Anmelde Informationsformate</span><span class="sxs-lookup"><span data-stu-id="66b18-111">Kerberos Credential Formats</span></span>

<span data-ttu-id="66b18-112">Die Benutzer [*Anmelde*](../secgloss/c-gly.md) Informationen, die nach einem erfolgreichen Anmeldeversuch vom Kerberos-Authentifizierungs Paket zugewiesen werden, sind ein Ticket und ein temporärer Verschlüsselungsschlüssel, der häufig als [*Sitzungsschlüssel*](../secgloss/s-gly.md)bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="66b18-112">The user [*credentials*](../secgloss/c-gly.md) assigned by the Kerberos authentication package after a successful logon attempt are a ticket and a temporary encryption key, often called a [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="66b18-113">Das Ticket enthält sowohl eine verschlüsselte Kopie der Anmelde Informationen des Clients als auch den Sitzungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="66b18-113">The ticket contains both an encrypted copy of the client's credentials and the session key.</span></span>

 

 
