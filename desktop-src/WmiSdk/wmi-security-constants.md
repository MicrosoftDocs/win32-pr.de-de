---
description: WMI prüft die Zugriffsrechte für Anwendungen und Skripts.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: WMI-Sicherheits Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218165"
---
# <a name="wmi-security-constants"></a><span data-ttu-id="2998f-103">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="2998f-103">WMI Security Constants</span></span>

<span data-ttu-id="2998f-104">WMI prüft die Zugriffsrechte für Anwendungen und Skripts für Objekte wie WMI-Namespaces, Drucker, Dienste, DCOM-Anwendungen, Dateien, Freigaben und andere Sicherungs fähige Objekte.</span><span class="sxs-lookup"><span data-stu-id="2998f-104">WMI checks access rights for applications and scripts for objects such as WMI namespaces, printer, services, DCOM applications, files, shares, and other securable objects.</span></span> <span data-ttu-id="2998f-105">Der Zugriff auf diese Sicherungs fähigen Objekte wird durch Zugriffs Steuerungs Einträge (Access Control Entries, ACE) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="2998f-105">Access to theses securable objects is controlled by access control entries (ACE).</span></span> <span data-ttu-id="2998f-106">Jeder ACE enthält Listen, die festlegen, auf welche Gruppen oder Benutzer zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2998f-106">Each ACE contains lists that designate which groups or users have access.</span></span> <span data-ttu-id="2998f-107">Weitere Informationen zu Sicherheits-und Zugriffs Steuerungs Listen (ACLs, DACLs oder SACLs) finden Sie unter [Access Control Listen (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [Sicherheits Deskriptoren](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="2998f-107">For more information about security and access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

<span data-ttu-id="2998f-108">Viele Anbieter Methoden in WMI, die Sicherungs fähige Objekte betreffen, erfordern, dass der Administrator bestimmte Berechtigungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2998f-108">Many provider methods in WMI that affect securable objects require the administrator to enable certain privileges.</span></span> <span data-ttu-id="2998f-109">Welche Version der Berechtigung Sie verwenden, hängt von der Programmiersprache ab, wie in [**Berechtigungs Konstanten**](privilege-constants.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2998f-109">Which version of the privilege you use depends on the programming language, as shown in [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="2998f-110">Die Sicherheits Konstanten werden in den folgenden Themen definiert:</span><span class="sxs-lookup"><span data-stu-id="2998f-110">The security constants are defined in the following topics:</span></span>

-   [<span data-ttu-id="2998f-111">**Ereignis Sicherheits Konstanten**</span><span class="sxs-lookup"><span data-stu-id="2998f-111">**Event Security Constants**</span></span>](event-security-constants.md)
-   [<span data-ttu-id="2998f-112">**Datei-und Verzeichniszugriffs Rechte-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="2998f-112">**File and Directory Access Rights Constants**</span></span>](file-and-directory-access-rights-constants.md)
-   [<span data-ttu-id="2998f-113">**Namespace-Zugriffsrechte Konstanten**</span><span class="sxs-lookup"><span data-stu-id="2998f-113">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
-   [<span data-ttu-id="2998f-114">**Namespace-ACE-Flag-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="2998f-114">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
-   [<span data-ttu-id="2998f-115">**Namespace-ACE-Typkonstanten**</span><span class="sxs-lookup"><span data-stu-id="2998f-115">**Namespace ACE Type Constants**</span></span>](namespace-ace-type-constants.md)
-   [<span data-ttu-id="2998f-116">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="2998f-116">**Privilege Constants**</span></span>](privilege-constants.md)

 

 
