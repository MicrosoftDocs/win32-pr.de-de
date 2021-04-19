---
description: Microsoft Digest führt eine anfängliche Authentifizierung aus, wenn der Server die erste Anforderungs Antwort von einem Client empfängt.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Microsoft Digest Authentication (Microsoft Digest-Authentifizierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362390"
---
# <a name="microsoft-digest-authentication"></a><span data-ttu-id="440a7-103">Microsoft Digest Authentication (Microsoft Digest-Authentifizierung)</span><span class="sxs-lookup"><span data-stu-id="440a7-103">Microsoft Digest Authentication</span></span>

<span data-ttu-id="440a7-104">Microsoft Digest führt eine anfängliche Authentifizierung aus, wenn der Server die erste Anforderungs Antwort von einem Client empfängt.</span><span class="sxs-lookup"><span data-stu-id="440a7-104">Microsoft Digest performs an initial authentication when the server receives the first challenge response from a client.</span></span> <span data-ttu-id="440a7-105">Der Server überprüft, ob der Client nicht authentifiziert wurde, und führt dann die anfängliche Authentifizierung durchzugreifen auf die Dienste eines Domänen Controllers durch.</span><span class="sxs-lookup"><span data-stu-id="440a7-105">The server verifies that the client has not been authenticated and then performs the initial authentication by accessing the services of a domain controller.</span></span> <span data-ttu-id="440a7-106">Eine ausführliche Beschreibung dieses Verfahrens finden [Sie unter erste Authentifizierung mit Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="440a7-106">For a detailed description of this procedure, see [Initial Authentication Using Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span></span>

<span data-ttu-id="440a7-107">Wenn die anfängliche Authentifizierung erfolgreich ist, erhält der Server einen Digest- [*Sitzungsschlüssel*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="440a7-107">When the initial authentication is successful the server receives a Digest [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="440a7-108">Der Server speichert diesen Schlüssel zwischen und verwendet ihn, um nachfolgende Anforderungen für Ressourcen vom Client zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="440a7-108">The server caches this key and uses it to authenticate subsequent requests for resources from the client.</span></span> <span data-ttu-id="440a7-109">Diese Authentifizierung ist lokal, d. h., Sie erfordert keinen Zugriff auf einen Domänen Controller.</span><span class="sxs-lookup"><span data-stu-id="440a7-109">This authentication is local, that is, it does not require access to a domain controller.</span></span> <span data-ttu-id="440a7-110">Eine ausführliche Beschreibung dieser Vorgehensweise finden [Sie unter Authentifizieren von nachfolgenden Anforderungen mit Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="440a7-110">For a detailed description of this procedure see [Authenticating Subsequent Requests Using Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span></span>

<span data-ttu-id="440a7-111">Wenn Sie http verwenden, wird keine Verbindung zwischen Client und Server hergestellt.</span><span class="sxs-lookup"><span data-stu-id="440a7-111">When using HTTP, there is no connection maintained between client and server.</span></span> <span data-ttu-id="440a7-112">Um den Domänen Controller-Datenverkehr zu reduzieren und die Leistung zu verbessern, werden von Microsoft Digest Informationen zwischengespeichert</span><span class="sxs-lookup"><span data-stu-id="440a7-112">To reduce domain controller traffic and improve performance, Microsoft Digest caches information received after successful authentication.</span></span> <span data-ttu-id="440a7-113">Weitere Informationen zu diesem Prozess finden Sie unter [beibehalten des Sicherheits Kontexts zwischen Verbindungen](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="440a7-113">For information about this process, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span>

 

 
