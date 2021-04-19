---
description: Beim Erstellen eines Security Support Provider SSP-Sicherheitspakets sollten Sie dem in die Domäne eingebundener Client nicht gestatten, sich mit einem zwei teiligen Dienstanbieter Namen (Service Provider Name, SPN) in der folgenden Form bei einem Domänen Controller zu authentifizieren.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Verwenden von dreiteiligen Prinzipal Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346924"
---
# <a name="using-three-part-principal-names"></a><span data-ttu-id="5424b-103">Verwenden von dreiteiligen Prinzipal Namen</span><span class="sxs-lookup"><span data-stu-id="5424b-103">Using Three Part Principal Names</span></span>

<span data-ttu-id="5424b-104">Beim Erstellen eines Security Support Provider SSP-Sicherheitspakets sollten Sie dem in die Domäne eingebundener Client nicht gestatten, sich mit einem zwei teiligen Dienstanbieter Namen (Service Provider Name, SPN) in der folgenden Form bei einem Domänen Controller zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="5424b-104">When creating a security support provider (SSP) security package, you should not allow the domain joined client to authenticate to a domain controller by using a two part service provider name (SPN) of the following form.</span></span>

-   <span data-ttu-id="5424b-105"><*Protokoll* >/< *Hostname*></span><span class="sxs-lookup"><span data-stu-id="5424b-105"><*protocol*>/<*host name*></span></span>

<span data-ttu-id="5424b-106">Ein Client sollte sich stets authentifizieren, indem er die Domäne angibt.</span><span class="sxs-lookup"><span data-stu-id="5424b-106">A client should always authenticate by specifying the domain.</span></span>

-   <span data-ttu-id="5424b-107"><*Protokoll* >/< *Hostname* >/< *Domänen Name*></span><span class="sxs-lookup"><span data-stu-id="5424b-107"><*protocol*>/<*host name*>/<*domain name*></span></span>

<span data-ttu-id="5424b-108">Ein in eine Domäne eingebundener Client, der sich mit einem zwei teiligen SPN anmeldet, kann möglicherweise die Identität des Domänen Controllers annehmen.</span><span class="sxs-lookup"><span data-stu-id="5424b-108">A domain joined client that logs on with a two part SPN may be able to impersonate the domain controller.</span></span> <span data-ttu-id="5424b-109">Wenn Sie zwei teilige SPNs zulassen, sollten Sie einen Protokolleintrag erstellen, der genügend Informationen enthält, um dem Administrator die Identifizierung des Aufrufers zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5424b-109">If you allow two part SPNs, you should create a log entry that contains enough information to enable the administrator to identify the caller.</span></span>

 

 



