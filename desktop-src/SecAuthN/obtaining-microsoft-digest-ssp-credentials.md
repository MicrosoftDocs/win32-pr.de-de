---
description: Benutzer Anmelde Informationen sind für Microsoft Digest erforderlich. sowohl der Client als auch der Server müssen gültige Anmelde Informationen aufweisen, bevor Sie einen Sicherheitskontext für den Nachrichtenaustausch einrichten können. Anmelde Informationen werden verwendet, um Anmelde Informationen abzurufen und zu präsentieren.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Abrufen von Microsoft Digest SSP-Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484710"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a><span data-ttu-id="4353b-104">Abrufen von Microsoft Digest SSP-Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="4353b-104">Obtaining Microsoft Digest SSP Credentials</span></span>

<span data-ttu-id="4353b-105">Benutzer [*Anmelde*](../secgloss/c-gly.md) Informationen sind für Microsoft Digest erforderlich. sowohl der Client als auch der Server müssen gültige Anmelde Informationen aufweisen, bevor Sie einen [*Sicherheitskontext*](../secgloss/s-gly.md) für den Nachrichtenaustausch einrichten können.</span><span class="sxs-lookup"><span data-stu-id="4353b-105">User [*credentials*](../secgloss/c-gly.md) are required by Microsoft Digest; both client and server must present valid credentials before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="4353b-106">Anmelde Informationen werden verwendet, um Anmelde Informationen abzurufen und zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="4353b-106">Credentials handles are used to obtain and present credentials.</span></span>

<span data-ttu-id="4353b-107">Da das Anmelde Informationen-Handle zum Speichern von Konfigurationsinformationen verwendet wird, kann das gleiche Handle nicht sowohl für Client seitige als auch für serverseitige Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4353b-107">Because the credential handle is used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="4353b-108">Dies bedeutet, dass Anwendungen, die sowohl Client-als auch Serververbindungen unterstützen, mindestens zwei Handles für die Anmelde Informationen erhalten müssen.</span><span class="sxs-lookup"><span data-stu-id="4353b-108">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="4353b-109">Um ein Handle für die für Microsoft Digest erforderlichen Anmelde Informationen abzurufen, müssen Sie die [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4353b-109">To get a handle to the credentials required by Microsoft Digest, call the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span>

<span data-ttu-id="4353b-110">Die folgenden C-sprach Beispiele veranschaulichen das Abrufen von Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="4353b-110">The following C language examples demonstrate obtaining credentials.</span></span>

-   [<span data-ttu-id="4353b-111">Abrufen der standardmäßigen Hashwert</span><span class="sxs-lookup"><span data-stu-id="4353b-111">Obtaining Default Digest Credentials</span></span>](obtaining-default-digest-credentials.md)
-   [<span data-ttu-id="4353b-112">Abrufen alternativer Digest-Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="4353b-112">Obtaining Alternate Digest Credentials</span></span>](obtaining-alternate-digest-credentials.md)

 

 
