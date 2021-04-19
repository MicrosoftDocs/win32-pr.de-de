---
description: Stellt eine Beziehung zwischen zwei icontextnode-Objekten dar.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Icontextlink-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357353"
---
# <a name="icontextlink-interface"></a><span data-ttu-id="304e8-103">Icontextlink-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="304e8-103">IContextLink interface</span></span>

<span data-ttu-id="304e8-104">Stellt eine Beziehung zwischen zwei [**icontextnode**](icontextnode.md) -Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="304e8-104">Represents a relationship between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="304e8-105">Member</span><span class="sxs-lookup"><span data-stu-id="304e8-105">Members</span></span>

<span data-ttu-id="304e8-106">Die **icontextlink** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="304e8-106">The **IContextLink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="304e8-107">**Icontextlink** enthält auch die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="304e8-107">**IContextLink** also has these types of members:</span></span>

-   [<span data-ttu-id="304e8-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="304e8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="304e8-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="304e8-109">Methods</span></span>

<span data-ttu-id="304e8-110">Die **icontextlink** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="304e8-110">The **IContextLink** interface has these methods.</span></span>



| <span data-ttu-id="304e8-111">Methode</span><span class="sxs-lookup"><span data-stu-id="304e8-111">Method</span></span>                                                                  | <span data-ttu-id="304e8-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="304e8-112">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="304e8-113">**Getcontextlinkdirection**</span><span class="sxs-lookup"><span data-stu-id="304e8-113">**GetContextLinkDirection**</span></span>](icontextlink-getcontextlinkdirection.md) | <span data-ttu-id="304e8-114">Ruft den Beziehungstyp ab, den dieser **icontextlink** darstellt.</span><span class="sxs-lookup"><span data-stu-id="304e8-114">Retrieves the type of relationship this **IContextLink** represents.</span></span><br/>                                         |
| [<span data-ttu-id="304e8-115">**Getdestinationnode**</span><span class="sxs-lookup"><span data-stu-id="304e8-115">**GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)           | <span data-ttu-id="304e8-116">Ruft das [**icontextnode**](icontextnode.md) -Objekt ab, das das Ziel für diesen **icontextlink** ist.</span><span class="sxs-lookup"><span data-stu-id="304e8-116">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this **IContextLink**.</span></span><br/> |
| [<span data-ttu-id="304e8-117">**Getsourcenode**</span><span class="sxs-lookup"><span data-stu-id="304e8-117">**GetSourceNode**</span></span>](icontextlink-getsourcenode.md)                     | <span data-ttu-id="304e8-118">Ruft das [**icontextnode**](icontextnode.md) -Objekt ab, das die Quelle für diesen **icontextlink** ist.</span><span class="sxs-lookup"><span data-stu-id="304e8-118">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this **IContextLink**.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="304e8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="304e8-119">Remarks</span></span>

<span data-ttu-id="304e8-120">Im folgenden finden Sie ein Beispiel für eine Beziehung, die durch ein **icontextlink** -Objekt dargestellt wird:</span><span class="sxs-lookup"><span data-stu-id="304e8-120">The following is an example of a relationship represented by an **IContextLink** object:</span></span>

-   <span data-ttu-id="304e8-121">Wenn ein AnalysisHint-Knoten in der Handschrift Analyse verwendet wird, erstellt der Ink-Analyse Vorgang ein **icontextlink** -Objekt vom Typ AnalysisHint zwischen dem Knoten des Analyse Hinweises und dem Knoten, der das Schreiben innerhalb des Bereichs des Hinweises enthält.</span><span class="sxs-lookup"><span data-stu-id="304e8-121">When an AnalysisHint node is used in ink analysis, the ink analysis operation creates an **IContextLink** object of type AnalysisHint between the analysis hint node and the node that contains writing within the area of the hint.</span></span> <span data-ttu-id="304e8-122">Der Quellknoten ist der Analyse Hinweis Knoten, und der Zielknoten ist der Knoten, der Schreibvorgänge enthält.</span><span class="sxs-lookup"><span data-stu-id="304e8-122">The source node is the analysis hint node and the destination node is the node that contains writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="304e8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="304e8-123">Requirements</span></span>



| <span data-ttu-id="304e8-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="304e8-124">Requirement</span></span> | <span data-ttu-id="304e8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="304e8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304e8-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="304e8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="304e8-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="304e8-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="304e8-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="304e8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="304e8-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="304e8-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="304e8-130">Header</span><span class="sxs-lookup"><span data-stu-id="304e8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="304e8-131"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="304e8-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="304e8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="304e8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="304e8-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="304e8-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="304e8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="304e8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="304e8-135">**Icontextnode:: getcontextlinks**</span><span class="sxs-lookup"><span data-stu-id="304e8-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="304e8-136">**Icontextlinks**</span><span class="sxs-lookup"><span data-stu-id="304e8-136">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="304e8-137">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="304e8-137">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="304e8-138">Kontext Knoten Typen</span><span class="sxs-lookup"><span data-stu-id="304e8-138">Context Node Types</span></span>](context-node-types.md)
</dt> </dl>

 

