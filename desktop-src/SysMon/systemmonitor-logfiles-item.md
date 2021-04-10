---
title: Logfiles. Item (Eigenschaft)
description: Ruft die angegebene logfileitem-Instanz aus der Auflistung ab.
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- Element Eigenschaften-sysmon
- Element Eigenschaft sysmon, Logfiles-Klasse
- Logfiles-Klasse (Sysmon), Item-Eigenschaft
topic_type:
- apiref
api_name:
- LogFiles.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85af003cd6c0291ec90d17906f249726dfd526f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040340"
---
# <a name="logfilesitem-property"></a><span data-ttu-id="8aa33-106">Logfiles. Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8aa33-106">LogFiles.Item property</span></span>

<span data-ttu-id="8aa33-107">Ruft die angegebene [**logfileitem**](logfileitem.md) -Instanz aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="8aa33-107">Retrieves the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span>

<span data-ttu-id="8aa33-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8aa33-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aa33-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8aa33-109">Syntax</span></span>


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a><span data-ttu-id="8aa33-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8aa33-110">Property value</span></span>

<span data-ttu-id="8aa33-111">[**Logfileitem**](logfileitem.md) -Instanz, die dem angegebenen Indexwert entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aa33-111">[**LogFileItem**](logfileitem.md) instance that corresponds to the specified index value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aa33-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8aa33-112">Remarks</span></span>

<span data-ttu-id="8aa33-113">Dies ist die Standard Eigenschaft des [**Logfiles**](systemmonitor-logfiles.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="8aa33-113">This is the default property of the [**LogFiles**](systemmonitor-logfiles.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa33-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8aa33-114">Requirements</span></span>



| <span data-ttu-id="8aa33-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8aa33-115">Requirement</span></span> | <span data-ttu-id="8aa33-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8aa33-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa33-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8aa33-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8aa33-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8aa33-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8aa33-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8aa33-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8aa33-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8aa33-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8aa33-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8aa33-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8aa33-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8aa33-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa33-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8aa33-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa33-124">LogFiles</span><span class="sxs-lookup"><span data-stu-id="8aa33-124">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="8aa33-125">**Logfileitem**</span><span class="sxs-lookup"><span data-stu-id="8aa33-125">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="8aa33-126">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="8aa33-126">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





