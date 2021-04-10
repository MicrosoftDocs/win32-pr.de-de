---
description: Ruft das icontextnode-Objekt ab, das die Quelle für diesen icontextlink ist.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'Icontextlink:: getsourcenode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eddab21740bf30c67e247cec89723bc47cd9dca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214672"
---
# <a name="icontextlinkgetsourcenode-method"></a><span data-ttu-id="aa625-103">Icontextlink:: getsourcenode-Methode</span><span class="sxs-lookup"><span data-stu-id="aa625-103">IContextLink::GetSourceNode method</span></span>

<span data-ttu-id="aa625-104">Ruft das [**icontextnode**](icontextnode.md) -Objekt ab, das die Quelle für diesen [**icontextlink**](icontextlink.md)ist.</span><span class="sxs-lookup"><span data-stu-id="aa625-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa625-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa625-105">Syntax</span></span>


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="aa625-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa625-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa625-107">*ppsrccontextnodeid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="aa625-107">*ppSrcContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa625-108">Ein Zeiger auf das [**icontextnode**](icontextnode.md) -Objekt, das die Quelle für diesen [**icontextlink**](icontextlink.md)ist.</span><span class="sxs-lookup"><span data-stu-id="aa625-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa625-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa625-109">Return value</span></span>

<span data-ttu-id="aa625-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="aa625-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aa625-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa625-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="aa625-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppsrccontextnodeid* , wenn Sie den Quellknoten nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="aa625-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSrcContextNodeId* when you no longer need to use the source node.</span></span>

 

<span data-ttu-id="aa625-113">Wenn das [**icontextlink**](icontextlink.md) -Objekt zwischen einem Knoten mit Schreibvorgang und einem Knoten mit Zeichnung verknüpft ist, ist der Quellknoten in der Regel der Knoten, der die Zeichnung enthält.</span><span class="sxs-lookup"><span data-stu-id="aa625-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the source node is generally the node that contains drawing.</span></span>

<span data-ttu-id="aa625-114">Wenn das [**icontextlink**](icontextlink.md) -Objekt den Linktyp engeschlossen aufweist (siehe [**icontextlink:: getcontextlinkdirection**](icontextlink-getcontextlinkdirection.md)), ist der Quellknoten der Knoten, der den Zielknoten einschließt.</span><span class="sxs-lookup"><span data-stu-id="aa625-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the source node is the node that encloses the destination node.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa625-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa625-115">Requirements</span></span>



| <span data-ttu-id="aa625-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa625-116">Requirement</span></span> | <span data-ttu-id="aa625-117">Wert</span><span class="sxs-lookup"><span data-stu-id="aa625-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa625-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa625-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aa625-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa625-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aa625-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa625-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aa625-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aa625-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="aa625-122">Header</span><span class="sxs-lookup"><span data-stu-id="aa625-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa625-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="aa625-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="aa625-124">DLL</span><span class="sxs-lookup"><span data-stu-id="aa625-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa625-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa625-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="aa625-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa625-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa625-127">**Icontextlink**</span><span class="sxs-lookup"><span data-stu-id="aa625-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="aa625-128">**Icontextlink:: getdestinationnode**</span><span class="sxs-lookup"><span data-stu-id="aa625-128">**IContextLink::GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)
</dt> <dt>

[<span data-ttu-id="aa625-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="aa625-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="aa625-130">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="aa625-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

