---
description: Gibt eine Eigenschaft an, die für einen Übergang oder einen Effekt festgelegt werden soll, zusammen mit der Anzahl der unterschiedlichen Werte, die die Eigenschaft über die Dauer des Übergangs oder Effekts annimmt.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: DEXTER_VALUE Struktur ("qedit. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371593"
---
# <a name="dexter_value-structure"></a><span data-ttu-id="21079-103">Struktur von Dexter- \_ Werten</span><span class="sxs-lookup"><span data-stu-id="21079-103">DEXTER\_VALUE structure</span></span>

> [!Note]  
> <span data-ttu-id="21079-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="21079-104">\[Deprecated.</span></span> <span data-ttu-id="21079-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="21079-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="21079-106">Gibt eine Eigenschaft an, die für einen Übergang oder einen Effekt festgelegt werden soll, zusammen mit der Anzahl der unterschiedlichen Werte, die die Eigenschaft über die Dauer des Übergangs oder Effekts annimmt.</span><span class="sxs-lookup"><span data-stu-id="21079-106">Identifies a property that is to be set on a transition or effect, along with the number of distinct values that the property assumes over the duration of the transition or effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="21079-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="21079-107">Syntax</span></span>


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a><span data-ttu-id="21079-108">Member</span><span class="sxs-lookup"><span data-stu-id="21079-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="21079-109">**Ramelow**</span><span class="sxs-lookup"><span data-stu-id="21079-109">**v**</span></span>
</dt> <dd>

<span data-ttu-id="21079-110">Der Wert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="21079-110">Value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="21079-111">**imposante**</span><span class="sxs-lookup"><span data-stu-id="21079-111">**rt**</span></span>
</dt> <dd>

<span data-ttu-id="21079-112">Der Zeitpunkt, zu dem die Eigenschaft den Wert annimmt, relativ zum Anfang des Übergangs oder Effekts.</span><span class="sxs-lookup"><span data-stu-id="21079-112">Time at which the property assumes the value, relative to the start of the transition or effect.</span></span>

</dd> <dt>

<span data-ttu-id="21079-113">**dwinterp**</span><span class="sxs-lookup"><span data-stu-id="21079-113">**dwInterp**</span></span>
</dt> <dd>

<span data-ttu-id="21079-114">Flag, das angibt, wie die-Eigenschaft vom vorherigen Wert zu diesem Wert verläuft.</span><span class="sxs-lookup"><span data-stu-id="21079-114">Flag indicating how the property progresses from the previous value to this value.</span></span> <span data-ttu-id="21079-115">Dies muss eine der folgenden Ressourcen sein:</span><span class="sxs-lookup"><span data-stu-id="21079-115">Must be one of the following:</span></span>



| <span data-ttu-id="21079-116">Wert</span><span class="sxs-lookup"><span data-stu-id="21079-116">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="21079-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="21079-117">Meaning</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <span data-ttu-id="21079-118"><dt>**dexterf \_ springen**</dt></span><span class="sxs-lookup"><span data-stu-id="21079-118"><dt>**DEXTERF\_JUMP**</dt></span></span> </dl>                      | <span data-ttu-id="21079-119">Die Eigenschaft springt zum angegebenen Zeitpunkt sofort in den neuen Wert.</span><span class="sxs-lookup"><span data-stu-id="21079-119">The property jumps instantly to the new value at the specified time.</span></span><br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <span data-ttu-id="21079-120"><dt>**dexterf- \_ Interpolate**</dt></span><span class="sxs-lookup"><span data-stu-id="21079-120"><dt>**DEXTERF\_INTERPOLATE**</dt></span></span> </dl> | <span data-ttu-id="21079-121">Die-Eigenschaft wird linear aus dem vorherigen Wert interpoliert.</span><span class="sxs-lookup"><span data-stu-id="21079-121">The property is interpolated linearly over time from the previous value.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21079-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21079-122">Requirements</span></span>



| <span data-ttu-id="21079-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21079-123">Requirement</span></span> | <span data-ttu-id="21079-124">Wert</span><span class="sxs-lookup"><span data-stu-id="21079-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21079-125">Header</span><span class="sxs-lookup"><span data-stu-id="21079-125">Header</span></span><br/> | <dl> <span data-ttu-id="21079-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="21079-126"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21079-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21079-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21079-128">**Ipropertysetter**</span><span class="sxs-lookup"><span data-stu-id="21079-128">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="21079-129">**Dexter \_ -Parameter**</span><span class="sxs-lookup"><span data-stu-id="21079-129">**DEXTER\_PARAM**</span></span>](dexter-param.md)
</dt> </dl>

 

 




