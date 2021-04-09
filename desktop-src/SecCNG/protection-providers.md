---
description: Ab Windows 8 hat Microsoft damit begonnen, die Anbieter zu verteilen, mit denen Sie verschlüsselte Geheimnisse und Nachrichten auf allen Computern sicher freigeben können.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Schutz Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959434"
---
# <a name="protection-providers"></a><span data-ttu-id="56b6b-103">Schutz Anbieter</span><span class="sxs-lookup"><span data-stu-id="56b6b-103">Protection Providers</span></span>

<span data-ttu-id="56b6b-104">Ab Windows 8 hat Microsoft damit begonnen, die Anbieter zu verteilen, mit denen Sie verschlüsselte Geheimnisse und Nachrichten auf allen Computern sicher freigeben können.</span><span class="sxs-lookup"><span data-stu-id="56b6b-104">Beginning with Windows 8, Microsoft began distributing the providers that enable you to securely share encrypted secrets and messages across computers.</span></span> <span data-ttu-id="56b6b-105">Zurzeit sind zwei Schlüsselschutz Anbieter vorhanden.</span><span class="sxs-lookup"><span data-stu-id="56b6b-105">There are currently two key protection providers.</span></span> <span data-ttu-id="56b6b-106">Mit dem Microsoft-Schlüsselschutz Anbieter können Sie Inhalte für eine Gruppe in einer Active Directory-Gesamtstruktur schützen.</span><span class="sxs-lookup"><span data-stu-id="56b6b-106">The Microsoft Key Protection provider allows you to protect content to a group in an Active Directory forest.</span></span> <span data-ttu-id="56b6b-107">Mit dem Microsoft-Client Schlüsselschutz-Anbieter können Sie Inhalte für eine Reihe von webanmelde Informationen schützen.</span><span class="sxs-lookup"><span data-stu-id="56b6b-107">The Microsoft Client Key Protection provider allows you to protect content to a set of web credentials.</span></span>

<span data-ttu-id="56b6b-108">Die richtige zu verwendende Schutzvorrichtung wird automatisch für Sie ausgewählt, wenn die [**ncryptkreateschutzdescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) -Funktion die als Eingabe bereitgestellte Schutz Beschreibungszeichenfolge analysiert.</span><span class="sxs-lookup"><span data-stu-id="56b6b-108">The correct protector to use is automatically chosen for you when the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function parses the protection descriptor rule string your provide as input.</span></span> <span data-ttu-id="56b6b-109">Der Microsoft-Schlüsselschutz Anbieter wird für Regel Zeichenfolgen ausgewählt, die mit sid, SDDL und local beginnen.</span><span class="sxs-lookup"><span data-stu-id="56b6b-109">The Microsoft Key Protection provider is chosen for rule strings that begin with SID, SDDL, and LOCAL.</span></span> <span data-ttu-id="56b6b-110">Der Microsoft-Client Schlüsselschutz-Anbieter analysiert Regel Zeichenfolgen, die mit webanmelde Informationen beginnen.</span><span class="sxs-lookup"><span data-stu-id="56b6b-110">The Microsoft Client Key Protection provider parses rule strings that begin with WEBCREDENTIALS.</span></span> <span data-ttu-id="56b6b-111">Weitere Informationen zu Regel Zeichenfolgen finden Sie unter [Schutz Deskriptoren](protection-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="56b6b-111">For more information about rule strings, see [Protection Descriptors](protection-descriptors.md).</span></span>

> [!Note]  
> <span data-ttu-id="56b6b-112">Benutzerdefinierte Anbieter sind zurzeit nicht zulässig. [CNG-DPAPI](cng-dpapi.md)</span><span class="sxs-lookup"><span data-stu-id="56b6b-112">Custom providers are not currently allowed.[CNG DPAPI](cng-dpapi.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="56b6b-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56b6b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56b6b-114">CNG-DPAPI</span><span class="sxs-lookup"><span data-stu-id="56b6b-114">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="56b6b-115">**Ncryptkreateschutzdescriptor**</span><span class="sxs-lookup"><span data-stu-id="56b6b-115">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[<span data-ttu-id="56b6b-116">Schutz Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="56b6b-116">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> </dl>

 

 



