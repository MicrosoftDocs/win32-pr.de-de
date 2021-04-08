---
description: Der dynamische Qualifizierer gibt eine Klasse an, deren Instanzen dynamisch erstellt werden. Der Wert dieses Qualifizierers muss auf "true" festgelegt werden.
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: Dynamischer Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864023"
---
# <a name="dynamic-qualifier"></a><span data-ttu-id="9de2d-104">Dynamischer Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="9de2d-104">Dynamic Qualifier</span></span>

<span data-ttu-id="9de2d-105">Der **dynamische** Qualifizierer gibt eine Klasse an, deren Instanzen dynamisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9de2d-105">The **Dynamic** qualifier indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="9de2d-106">Der Wert dieses Qualifizierers muss auf " **true**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9de2d-106">The value of this qualifier must be set to **TRUE**.</span></span>

<span data-ttu-id="9de2d-107">Der **dynamische** Qualifizierer muss für alle Klassen angegeben werden, die Daten enthalten und für die Instanzen dynamisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9de2d-107">The **Dynamic** qualifier must be specified on all classes that contain data and for which instances are created dynamically.</span></span> <span data-ttu-id="9de2d-108">Der [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) wird normalerweise auch angegeben, um den für die Bereitstellung der Daten verantwortlichen Anbieter zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9de2d-108">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is typically also specified to identify the provider responsible for supplying the data.</span></span>

<span data-ttu-id="9de2d-109">Klassen, die nur Methoden enthalten, die implementieren müssen, erfordern nicht den **dynamischen** Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="9de2d-109">Classes that contain only methods that need implementation do not require the **Dynamic** qualifier.</span></span> <span data-ttu-id="9de2d-110">Nur der [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) ist erforderlich, um den Namen des Anbieters anzugeben, um die Implementierung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9de2d-110">Only the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is required to specify the name of the provider to supply the implementation.</span></span>

<span data-ttu-id="9de2d-111">Alle Klassen, die von einer dynamischen Klasse abgeleitet werden, müssen dynamisch sein.</span><span class="sxs-lookup"><span data-stu-id="9de2d-111">All classes derived from a dynamic class must be dynamic.</span></span> <span data-ttu-id="9de2d-112">Eine statische Klasse kann nicht von einer dynamischen Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="9de2d-112">You cannot derive a static class from a dynamic class.</span></span>

<span data-ttu-id="9de2d-113">Wenn **Dynamic** für eine Eigenschaft einer Instanz angegeben ist, muss auch der **propertycontext** -Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9de2d-113">When **Dynamic** is specified on a property of an instance, the **PropertyContext** qualifier must also be specified.</span></span>

## <a name="requirements"></a><span data-ttu-id="9de2d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9de2d-114">Requirements</span></span>



| <span data-ttu-id="9de2d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9de2d-115">Requirement</span></span> | <span data-ttu-id="9de2d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9de2d-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9de2d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9de2d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9de2d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9de2d-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9de2d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9de2d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9de2d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9de2d-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9de2d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9de2d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de2d-122">**WMI-Standard Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="9de2d-122">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="9de2d-123">WMI Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="9de2d-123">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="9de2d-124">Fügen eines Qualifizierers</span><span class="sxs-lookup"><span data-stu-id="9de2d-124">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




