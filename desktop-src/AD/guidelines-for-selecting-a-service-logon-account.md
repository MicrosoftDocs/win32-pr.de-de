---
title: Richtlinien für das Auswählen eines Dienst Anmelde Kontos
description: Ein Win32-basierter Dienst kann im Sicherheitskontext eines lokalen Benutzerkontos, eines Domänen Benutzerkontos oder des Kontos "LocalSystem" ausgeführt werden.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Richtlinien für das Auswählen eines Dienst Anmelde Konto-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bb8f5b4fe6a57863c09c9563454fc3ec09e75c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036358"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a><span data-ttu-id="44a84-104">Richtlinien für das Auswählen eines Dienst Anmelde Kontos</span><span class="sxs-lookup"><span data-stu-id="44a84-104">Guidelines for Selecting a Service Logon Account</span></span>

<span data-ttu-id="44a84-105">Ein Win32-basierter Dienst kann im Sicherheitskontext eines lokalen Benutzerkontos, eines Domänen Benutzerkontos oder des Kontos "LocalSystem" ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="44a84-105">A Win32-based service can run in the security context of a local user account, a domain user account, or the LocalSystem account.</span></span> <span data-ttu-id="44a84-106">Um zu entscheiden, welches Konto verwendet werden soll, sollte ein Administrator den Dienst mit dem minimalen Satz an Berechtigungen installieren, der zum Durchführen der Dienst Vorgänge erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="44a84-106">To decide which account to use, an administrator should install the service with the minimum set of permissions required to perform the service operations.</span></span> <span data-ttu-id="44a84-107">In einem typischen, Verzeichnis aktivierten Dienst bedeutet dies, dass das Dienst Installationsprogramm ein Domänen Benutzerkonto für den Dienst erstellen und diesem Konto die für den Dienst zur Laufzeit erforderlichen Zugriffsrechte und Berechtigungen erteilen soll.</span><span class="sxs-lookup"><span data-stu-id="44a84-107">In a typical directory-enabled service, this means the service installer should create a domain user account for the service and grant that account the specific access rights and privileges required by the service at run time.</span></span> <span data-ttu-id="44a84-108">Ein Dienst sollte nur unter dem Konto "LocalSystem" ausgeführt werden, wenn der Dienst Administratorrechte erfordert oder als Teil des Betriebssystems auf dem lokalen Computer fungieren muss.</span><span class="sxs-lookup"><span data-stu-id="44a84-108">A service should only run under the LocalSystem account if the service requires administrative privileges or must act as part of the operating system on the local computer.</span></span>

<span data-ttu-id="44a84-109">Beachten Sie, dass der Dienst Installer standardmäßig den Dienst so einrichten muss, dass er unter einem Domänen Benutzerkonto ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44a84-109">Be aware that the service installer should, by default, set up the service to run under a domain user account.</span></span> <span data-ttu-id="44a84-110">Um den Dienst unter dem Konto "LocalSystem" auszuführen, sollte das Dienst Installationsprogramm den Administrator über die entsprechende Berechtigung Abfragen.</span><span class="sxs-lookup"><span data-stu-id="44a84-110">To run the service under the LocalSystem account, the service installer should query the administrator for permission to do so.</span></span>

<span data-ttu-id="44a84-111">Weitere Informationen zu Beschreibungen, Vorteilen und Nachteilen der einzelnen Kontotypen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="44a84-111">For more information about descriptions, advantages, and disadvantages of each account type, see:</span></span>

-   <span data-ttu-id="44a84-112">[Lokale Benutzerkonten](local-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="44a84-112">[Local User Accounts](local-user-accounts.md).</span></span>
-   <span data-ttu-id="44a84-113">[Domänen Benutzerkonten](domain-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="44a84-113">[Domain User Accounts](domain-user-accounts.md).</span></span>
-   <span data-ttu-id="44a84-114">[Das LocalSystem-Konto](the-localsystem-account.md).</span><span class="sxs-lookup"><span data-stu-id="44a84-114">[The LocalSystem Account](the-localsystem-account.md).</span></span>

 

 




