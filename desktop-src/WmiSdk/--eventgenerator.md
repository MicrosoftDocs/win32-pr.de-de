---
description: Fungiert als übergeordnete Klasse für Klassen, die die Generierung von Ereignissen steuern, z. b. Timer-Ereignisse.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: __EventGenerator-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b40524405c3b284e7ec61414e36448cb37afeab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218657"
---
# <a name="__eventgenerator-class"></a><span data-ttu-id="cd77a-103">\_\_Eventgenerator-Klasse</span><span class="sxs-lookup"><span data-stu-id="cd77a-103">\_\_EventGenerator class</span></span>

<span data-ttu-id="cd77a-104">Die **\_ \_ eventgenerator** -System Klasse ist eine abstrakte Basisklasse, die als übergeordnete Klasse für Klassen fungiert, die die Generierung von Ereignissen steuern, z. b. [Timer-Ereignisse](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="cd77a-104">The **\_\_EventGenerator** system class is an abstract base class that serves as a parent class for classes that control the generation of events, such as [timer events](receiving-a-timed-or-repeating-event.md).</span></span>

<span data-ttu-id="cd77a-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="cd77a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cd77a-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cd77a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd77a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd77a-107">Syntax</span></span>

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a><span data-ttu-id="cd77a-108">Member</span><span class="sxs-lookup"><span data-stu-id="cd77a-108">Members</span></span>

<span data-ttu-id="cd77a-109">Die **\_ \_ eventgenerator** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="cd77a-109">The **\_\_EventGenerator** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd77a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd77a-110">Remarks</span></span>

<span data-ttu-id="cd77a-111">Die **\_ \_ eventgenerator** -Klasse wird von " [**\_ \_ indicationrelated**](--indicationrelated.md)" abgeleitet, die keine Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="cd77a-111">The **\_\_EventGenerator** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd77a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd77a-112">Requirements</span></span>



| <span data-ttu-id="cd77a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd77a-113">Requirement</span></span> | <span data-ttu-id="cd77a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cd77a-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="cd77a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd77a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cd77a-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd77a-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="cd77a-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd77a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cd77a-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd77a-118">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="cd77a-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd77a-119">Namespace</span></span><br/>                | <span data-ttu-id="cd77a-120">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="cd77a-120">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="cd77a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd77a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd77a-122">**\_\_Indicationrelated**</span><span class="sxs-lookup"><span data-stu-id="cd77a-122">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="cd77a-123">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="cd77a-123">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

