---
description: Gibt den Wert an, den eine Eigenschaft zu einem bestimmten Zeitpunkt annimmt.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: DEXTER_PARAM Struktur ("qedit. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371594"
---
# <a name="dexter_param-structure"></a><span data-ttu-id="3d4e6-103">Dexter- \_ param-Struktur</span><span class="sxs-lookup"><span data-stu-id="3d4e6-103">DEXTER\_PARAM structure</span></span>

> [!Note]  
> <span data-ttu-id="3d4e6-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3d4e6-104">\[Deprecated.</span></span> <span data-ttu-id="3d4e6-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="3d4e6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3d4e6-106">Gibt den Wert an, den eine Eigenschaft zu einem bestimmten Zeitpunkt annimmt.</span><span class="sxs-lookup"><span data-stu-id="3d4e6-106">Specifies the value that a property assumes at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d4e6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d4e6-107">Syntax</span></span>


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a><span data-ttu-id="3d4e6-108">Member</span><span class="sxs-lookup"><span data-stu-id="3d4e6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3d4e6-109">**Name**</span><span class="sxs-lookup"><span data-stu-id="3d4e6-109">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="3d4e6-110">Der Name der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3d4e6-110">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="3d4e6-111">**dispID**</span><span class="sxs-lookup"><span data-stu-id="3d4e6-111">**dispID**</span></span>
</dt> <dd>

<span data-ttu-id="3d4e6-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="3d4e6-112">Reserved.</span></span> <span data-ttu-id="3d4e6-113">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="3d4e6-113">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3d4e6-114">**nwerte**</span><span class="sxs-lookup"><span data-stu-id="3d4e6-114">**nValues**</span></span>
</dt> <dd>

<span data-ttu-id="3d4e6-115">Anzahl der Werte, die von der-Eigenschaft angenommen werden.</span><span class="sxs-lookup"><span data-stu-id="3d4e6-115">Number of values that the property assumes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d4e6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d4e6-116">Remarks</span></span>

<span data-ttu-id="3d4e6-117">Das-Objekt muss die **IDispatch** -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3d4e6-117">The object must support the **IDispatch** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d4e6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d4e6-118">Requirements</span></span>



| <span data-ttu-id="3d4e6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d4e6-119">Requirement</span></span> | <span data-ttu-id="3d4e6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3d4e6-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d4e6-121">Header</span><span class="sxs-lookup"><span data-stu-id="3d4e6-121">Header</span></span><br/> | <dl> <span data-ttu-id="3d4e6-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3d4e6-122"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d4e6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d4e6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4e6-124">**Ipropertysetter**</span><span class="sxs-lookup"><span data-stu-id="3d4e6-124">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="3d4e6-125">**Wert von Dexter \_**</span><span class="sxs-lookup"><span data-stu-id="3d4e6-125">**DEXTER\_VALUE**</span></span>](dexter-value.md)
</dt> </dl>

 

 




