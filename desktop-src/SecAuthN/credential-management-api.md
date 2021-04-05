---
description: Credential Management-API
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: Credential Management-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cae5054d0a32f42616f2845dcf18ab71ad0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757290"
---
# <a name="credential-management-api"></a><span data-ttu-id="9866c-103">Credential Management-API</span><span class="sxs-lookup"><span data-stu-id="9866c-103">Credential Management API</span></span>

<span data-ttu-id="9866c-104">Die Funktionen zur Verwaltung von Anmelde Informationen bilden die Funktionen, die von einem Anmelde Informationen-Manager implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9866c-104">The credential management functions constitute the set of functions that a credential manager must implement.</span></span> <span data-ttu-id="9866c-105">Diese lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9866c-105">These are:</span></span>

-   <span data-ttu-id="9866c-106">[**Nplogonnotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), eine Ereignishandlerfunktion, die von der MPR aufgerufen wird, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="9866c-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), an event-handler function that the MPR calls when a user logs on.</span></span>
-   <span data-ttu-id="9866c-107">[**Nppasswordchangenotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), eine Ereignishandlerfunktion, die von MPR aufgerufen wird, wenn ein Konto Kennwort geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9866c-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), an event-handler function the MPR calls when an account password is changed.</span></span>

<span data-ttu-id="9866c-108">Die Funktionen für die Verwaltung von Anmelde Informationen werden immer im Systemkontext ("LocalSystem") statt im Benutzer Kontext aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9866c-108">The credential management functions are always called in the system context (LocalSystem) rather than the user context.</span></span>

<span data-ttu-id="9866c-109">Weitere Informationen zum Erstellen und Registrieren einer Anwendung für die Anmelde Informationsverwaltung finden Sie unter [Implementieren einer](implementing-a-credential-manager.md) Anmelde Informationsverwaltung und [Registrieren von Netzwerkanbietern und Anmelde Informations Managern](registering-network-providers-and-credential-managers.md).</span><span class="sxs-lookup"><span data-stu-id="9866c-109">For more information about how to create and register a credential manager application, see [Implementing a Credential Manager](implementing-a-credential-manager.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

 



