---
description: Ruft das icontextnode-Objekt ab, das das Ziel für diesen icontextlink ist.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'Icontextlink:: getdestinationnode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343728"
---
# <a name="icontextlinkgetdestinationnode-method"></a><span data-ttu-id="be2e8-103">Icontextlink:: getdestinationnode-Methode</span><span class="sxs-lookup"><span data-stu-id="be2e8-103">IContextLink::GetDestinationNode method</span></span>

<span data-ttu-id="be2e8-104">Ruft das [**icontextnode**](icontextnode.md) -Objekt ab, das das Ziel für diesen [**icontextlink**](icontextlink.md)ist.</span><span class="sxs-lookup"><span data-stu-id="be2e8-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="be2e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be2e8-105">Syntax</span></span>


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="be2e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be2e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be2e8-107">*ppdstcontextnodeid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="be2e8-107">*ppDstContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be2e8-108">Ein Zeiger auf das [**icontextnode**](icontextnode.md) -Objekt, das das Ziel für diesen [**icontextlink**](icontextlink.md)ist.</span><span class="sxs-lookup"><span data-stu-id="be2e8-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be2e8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be2e8-109">Return value</span></span>

<span data-ttu-id="be2e8-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="be2e8-110">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be2e8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be2e8-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="be2e8-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppdstcontextnodeid* , wenn Sie den Zielknoten nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="be2e8-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppDstContextNodeId* when you no longer need to use the destination node.</span></span>

 

<span data-ttu-id="be2e8-113">Wenn das [**icontextlink**](icontextlink.md) -Objekt zwischen einem Knoten mit Schreibvorgang und einem Knoten mit Zeichnung verknüpft ist, ist der Zielknoten in der Regel der Knoten, der Schreibvorgänge enthält.</span><span class="sxs-lookup"><span data-stu-id="be2e8-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the destination node is generally the node that contains writing.</span></span>

<span data-ttu-id="be2e8-114">Wenn das [**icontextlink**](icontextlink.md) -Objekt den Linktyp engeschlossen aufweist (siehe [**icontextlink:: getcontextlinkdirection**](icontextlink-getcontextlinkdirection.md)), ist der Zielknoten das [**icontextnode**](icontextnode.md) -Objekt, das eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="be2e8-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the destination node is the [**IContextNode**](icontextnode.md) object that is enclosed.</span></span>

## <a name="requirements"></a><span data-ttu-id="be2e8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be2e8-115">Requirements</span></span>



| <span data-ttu-id="be2e8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be2e8-116">Requirement</span></span> | <span data-ttu-id="be2e8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="be2e8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be2e8-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be2e8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="be2e8-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be2e8-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be2e8-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be2e8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="be2e8-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="be2e8-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="be2e8-122">Header</span><span class="sxs-lookup"><span data-stu-id="be2e8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="be2e8-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="be2e8-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="be2e8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="be2e8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be2e8-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be2e8-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="be2e8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be2e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be2e8-127">**Icontextlink**</span><span class="sxs-lookup"><span data-stu-id="be2e8-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="be2e8-128">**Icontextlink:: getsourcenode**</span><span class="sxs-lookup"><span data-stu-id="be2e8-128">**IContextLink::GetSourceNode**</span></span>](icontextlink-getsourcenode.md)
</dt> <dt>

[<span data-ttu-id="be2e8-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="be2e8-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="be2e8-130">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="be2e8-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

