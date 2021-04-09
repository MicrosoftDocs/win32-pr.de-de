---
description: Ist das Windows-Modul, das die interaktive Anmeldung für eine Anmelde Sitzung ausführt. Das Winlogon-Verhalten kann durch Implementieren und Registrieren eines Anmelde Informationsanbieters angepasst werden.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon-und Anmelde Informationsanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958869"
---
# <a name="winlogon-and-credential-providers"></a><span data-ttu-id="e2386-104">Winlogon-und Anmelde Informationsanbieter</span><span class="sxs-lookup"><span data-stu-id="e2386-104">Winlogon and Credential Providers</span></span>

<span data-ttu-id="e2386-105">[*Winlogon*](../secgloss/w-gly.md) ist das Windows-Modul, das die interaktive Anmeldung für eine [*Anmelde Sitzung*](../secgloss/l-gly.md)ausführt.</span><span class="sxs-lookup"><span data-stu-id="e2386-105">[*Winlogon*](../secgloss/w-gly.md) is the Windows module that performs interactive logon for a [*logon session*](../secgloss/l-gly.md).</span></span> <span data-ttu-id="e2386-106">Das Winlogon-Verhalten kann durch Implementieren und Registrieren eines Anmelde Informationsanbieters angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="e2386-106">Winlogon behavior can be customized by implementing and registering a Credential Provider.</span></span>

<span data-ttu-id="e2386-107">Weitere Informationen zum Implementieren eines Anmelde Informationsanbieters finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="e2386-107">For information about implementing a Credential Provider, see the following topics.</span></span>



| <span data-ttu-id="e2386-108">Thema</span><span class="sxs-lookup"><span data-stu-id="e2386-108">Topic</span></span>                                                                                                           | <span data-ttu-id="e2386-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2386-109">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2386-110">Vom Anmelde Informationsanbieter gesteuerte Windows-Anmeldevorgang</span><span class="sxs-lookup"><span data-stu-id="e2386-110">Credential Provider driven Windows Logon Experience</span></span>](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | <span data-ttu-id="e2386-111">Übersicht über die Winlogon-und Anmelde Informationsanbieter-Architektur und einen Beispiel-Anmelde Informationsanbieter.</span><span class="sxs-lookup"><span data-stu-id="e2386-111">Overview of Winlogon and Credential Provider architecture and a sample Credential Provider.</span></span><br/> |
| [<span data-ttu-id="e2386-112">Shellschnittstellen</span><span class="sxs-lookup"><span data-stu-id="e2386-112">Shell Interfaces</span></span>](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | <span data-ttu-id="e2386-113">Referenz zur Anmelde Informationsanbieter-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e2386-113">Credential Provider interface reference.</span></span><br/>                                                    |
| [<span data-ttu-id="e2386-114">Anmelde Informationsanbieter in Windows 10</span><span class="sxs-lookup"><span data-stu-id="e2386-114">Credential Providers in Windows 10</span></span>](credential-providers-in-windows.md)<br/>                            | <span data-ttu-id="e2386-115">Drittanbieter-Anmelde Informationsanbieter und System Anmelde Informationsanbieter in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2386-115">Third-party credential providers and system credential providers in Windows 10.</span></span><br/>             |



 

<span data-ttu-id="e2386-116">Eine Beispiel Implementierung für den Anmelde Informationsanbieter finden Sie im Beispiel im Windows SDK-Installationsverzeichnis unter \\ Samples \\ Security \\ kredentialprovider.</span><span class="sxs-lookup"><span data-stu-id="e2386-116">For a sample Credential Provider implementation, see the sample located in the Windows SDK installation directory under \\Samples\\Security\\CredentialProvider.</span></span>

<span data-ttu-id="e2386-117">**Windows Server 2003 und Windows XP:** Anmelde Informationsanbieter werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2386-117">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span> <span data-ttu-id="e2386-118">Weitere Informationen zum Anpassen von Winlogon finden Sie unter [Winlogon und Gina](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="e2386-118">For information about customizing Winlogon, see [Winlogon and GINA](winlogon-and-gina.md).</span></span>

 

 
