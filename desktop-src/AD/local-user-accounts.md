---
title: Verwenden eines lokalen Benutzerkontos als Dienst Anmelde Konto
description: Ein lokales Benutzerkonto (Namensformat \ 0034;. \\ Benutzername \ 0034;) ist nur in der SAM-Datenbank des Host Computers vorhanden. in Active Directory Domain Services ist kein Benutzerobjekt vorhanden.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84da502e99d2e5cd74e98e9f792e06f74f4852e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100594"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a><span data-ttu-id="74590-103">Verwenden eines lokalen Benutzerkontos als Dienst Anmelde Konto</span><span class="sxs-lookup"><span data-stu-id="74590-103">Using a Local User Account as a Service Logon Account</span></span>

<span data-ttu-id="74590-104">Ein lokales Benutzerkonto (Namensformat: "). \\ Der *Benutzername*") ist nur in der SAM-Datenbank des Host Computers vorhanden. in Active Directory Domain Services ist kein Benutzerobjekt vorhanden.</span><span class="sxs-lookup"><span data-stu-id="74590-104">A local user account (name format: ".\\*UserName*") exists only in the SAM database of the host computer; it does not have a user object in Active Directory Domain Services.</span></span> <span data-ttu-id="74590-105">Dies bedeutet, dass ein lokales Konto nicht von der Domäne authentifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="74590-105">This means that a local account cannot be authenticated by the domain.</span></span> <span data-ttu-id="74590-106">Folglich hat ein Dienst, der im Sicherheitskontext eines lokalen Benutzerkontos ausgeführt wird, keinen Zugriff auf Netzwerkressourcen (mit Ausnahme eines anonymen Benutzers) und kann keine gegenseitige Kerberos-Authentifizierung unterstützen, bei der der Dienst von seinen Clients authentifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="74590-106">Consequently, a service that runs in the security context of a local user account does not have access to network resources (except as an anonymous user), and it cannot support Kerberos mutual authentication in which the service is authenticated by its clients.</span></span> <span data-ttu-id="74590-107">Aus diesen Gründen eignen sich lokale Benutzerkonten normalerweise nicht für verzeichnisfähige Dienste.</span><span class="sxs-lookup"><span data-stu-id="74590-107">For these reasons, local user accounts are typically inappropriate for directory-enabled services.</span></span> <span data-ttu-id="74590-108">Auf der Plus Seite können Fehler im Dienst das System nicht beschädigen.</span><span class="sxs-lookup"><span data-stu-id="74590-108">On the plus side, bugs in the service cannot damage the system.</span></span> <span data-ttu-id="74590-109">Wenn Ihr Dienst unter diesen Beschränkungen ausgeführt werden kann, sollte dies der Fall sein.</span><span class="sxs-lookup"><span data-stu-id="74590-109">If your service can run under those limitations, it should.</span></span>

 

 




