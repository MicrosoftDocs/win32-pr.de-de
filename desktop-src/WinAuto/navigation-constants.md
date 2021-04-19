---
title: Navigations Konstanten (Oleacc. h)
description: In diesem Thema werden die Konstanten Werte beschrieben, die in Oleacc. h definiert sind, die die räumliche Richtung (oben, unten, Links und rechts) oder die logische (erste untergeordnete, letzte, nächste und vorherige) Richtung angeben, die beobachtet wird, wenn Clients IAccessible accNavigate verwenden, um von einem Benutzeroberflächen Element zu einem anderen innerhalb desselben Containers zu navigieren.
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de5f4eaa3fc7fb24583e49bdd14acb9633b2bd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352960"
---
# <a name="navigation-constants"></a><span data-ttu-id="402f1-103">Navigations Konstanten</span><span class="sxs-lookup"><span data-stu-id="402f1-103">Navigation Constants</span></span>

<span data-ttu-id="402f1-104">In diesem Thema werden die Konstanten Werte beschrieben, die in Oleacc. h definiert sind, die die *räumliche* Richtung (oben, unten, Links und rechts) oder die *logische* (erste untergeordnete, letzte, nächste und vorherige) Richtung angeben, die beobachtet wird, wenn Clients [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) verwenden, um innerhalb desselben Containers von einem Benutzeroberflächen Element zu einem anderen zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="402f1-104">This topic describes the constant values, defined in oleacc.h, that indicate the *spatial* (up, down, left, and right) or *logical* (first child, last, next, and previous) direction observed when clients use [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to navigate from one user interface element to another within the same container.</span></span> <span data-ttu-id="402f1-105">Weitere Informationen finden Sie unter [Objekt Navigations Eigenschaften und-Methoden](object-navigation-properties-and-methods.md).</span><span class="sxs-lookup"><span data-stu-id="402f1-105">For more information, see [Object Navigation Properties and Methods](object-navigation-properties-and-methods.md).</span></span>

<span data-ttu-id="402f1-106">Die Microsoft Active Accessibility-Navigations Konstanten lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="402f1-106">The Microsoft Active Accessibility navigation constants are as follows:</span></span>



| <span data-ttu-id="402f1-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="402f1-107">Constant</span></span>                                                                                                                                                                  | <span data-ttu-id="402f1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="402f1-108">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <span data-ttu-id="402f1-109"><dt>**navDir \_ nach unten**</dt></span><span class="sxs-lookup"><span data-stu-id="402f1-109"><dt>**NAVDIR\_DOWN**</dt></span></span> </dl>                   | <span data-ttu-id="402f1-110">Navigieren Sie zu dem neben geordneten Objekt, das sich unterhalb des Start Objekts befindet.</span><span class="sxs-lookup"><span data-stu-id="402f1-110">Navigate to the sibling object that is located below the starting object.</span></span><br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <span data-ttu-id="402f1-111"><dt>**navDir, \_ FirstChild**</dt></span><span class="sxs-lookup"><span data-stu-id="402f1-111"><dt>**NAVDIR\_FIRSTCHILD**</dt></span></span> </dl> | <span data-ttu-id="402f1-112">Navigieren Sie zum ersten untergeordneten Element dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="402f1-112">Navigate to the first child of this object.</span></span> <span data-ttu-id="402f1-113">Wenn dieses Flag verwendet wird, muss der **LVAL** -Member des *varstart* -Parameters "childID Self" lauten \_ .</span><span class="sxs-lookup"><span data-stu-id="402f1-113">When this flag is used, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <span data-ttu-id="402f1-114"><dt>**navDir \_ LastChild**</dt></span><span class="sxs-lookup"><span data-stu-id="402f1-114"><dt>**NAVDIR\_LASTCHILD**</dt></span></span> </dl>    | <span data-ttu-id="402f1-115">Navigieren Sie zum letzten untergeordneten Element dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="402f1-115">Navigate to the last child of this object.</span></span> <span data-ttu-id="402f1-116">Wenn Sie dieses Flag verwenden, muss das **LVAL** -Element des *varstart* -Parameters "childID Self" lauten \_ .</span><span class="sxs-lookup"><span data-stu-id="402f1-116">When using this flag, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <span data-ttu-id="402f1-117"><dt>**navDir \_ Links**</dt></span><span class="sxs-lookup"><span data-stu-id="402f1-117"><dt>**NAVDIR\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="402f1-118">Navigieren Sie zu dem neben geordneten Objekt, das sich auf der linken Seite des Start Objekts befindet.</span><span class="sxs-lookup"><span data-stu-id="402f1-118">Navigate to the sibling object located to the left of the starting object.</span></span><br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <span data-ttu-id="402f1-119"><dt>**nächste navDir \_**</dt></span><span class="sxs-lookup"><span data-stu-id="402f1-119"><dt>**NAVDIR\_NEXT**</dt></span></span> </dl>                   | <span data-ttu-id="402f1-120">Navigieren Sie zum nächsten logischen Objekt. im Allgemeinen ist es ein gleich geordnetes Element des Start Objekts.</span><span class="sxs-lookup"><span data-stu-id="402f1-120">Navigate to the next logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <span data-ttu-id="402f1-121"><dt>**früher navDir \_**</dt></span><span class="sxs-lookup"><span data-stu-id="402f1-121"><dt>**NAVDIR\_PREVIOUS**</dt></span></span> </dl>       | <span data-ttu-id="402f1-122">Navigieren Sie zum vorherigen logischen Objekt. im Allgemeinen ist es ein gleich geordnetes Element des Start Objekts.</span><span class="sxs-lookup"><span data-stu-id="402f1-122">Navigate to the previous logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <span data-ttu-id="402f1-123"><dt>**navDir \_ right**</dt></span><span class="sxs-lookup"><span data-stu-id="402f1-123"><dt>**NAVDIR\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="402f1-124">Navigieren Sie zu dem neben geordneten Objekt, das sich auf der rechten Seite des Start Objekts befindet.</span><span class="sxs-lookup"><span data-stu-id="402f1-124">Navigate to the sibling object that is located to the right of the starting object.</span></span><br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <span data-ttu-id="402f1-125"><dt>**navDir nach \_ oben**</dt></span><span class="sxs-lookup"><span data-stu-id="402f1-125"><dt>**NAVDIR\_UP**</dt></span></span> </dl>                         | <span data-ttu-id="402f1-126">Navigieren Sie zu dem neben geordneten Objekt, das sich oberhalb des Anfangs Objekts befindet.</span><span class="sxs-lookup"><span data-stu-id="402f1-126">Navigate to the sibling object that is located above the starting object.</span></span><br/>                                                                  |



## <a name="requirements"></a><span data-ttu-id="402f1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="402f1-127">Requirements</span></span>



| <span data-ttu-id="402f1-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="402f1-128">Requirement</span></span> | <span data-ttu-id="402f1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="402f1-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="402f1-130">Header</span><span class="sxs-lookup"><span data-stu-id="402f1-130">Header</span></span><br/> | <dl> <span data-ttu-id="402f1-131"><dt>Oleacc. h</dt></span><span class="sxs-lookup"><span data-stu-id="402f1-131"><dt>Oleacc.h</dt></span></span> </dl> |



 

 





