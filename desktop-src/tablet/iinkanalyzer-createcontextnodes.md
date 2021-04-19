---
description: Erstellt ein icontextnodes-Objekt.
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'Iinkanalyzer:: kreatecontextnodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07bdfc9a32fd4aec8e716cdd3c788c211c1adaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359852"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a><span data-ttu-id="a53ae-103">Iinkanalyzer:: anatecontextnodes-Methode</span><span class="sxs-lookup"><span data-stu-id="a53ae-103">IInkAnalyzer::CreateContextNodes method</span></span>

<span data-ttu-id="a53ae-104">Erstellt ein [**icontextnodes**](icontextnodes.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a53ae-104">Creates an [**IContextNodes**](icontextnodes.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a53ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a53ae-105">Syntax</span></span>


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="a53ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a53ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a53ae-107">*ppcontextnodes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a53ae-107">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a53ae-108">Ein Zeiger auf das [**icontextnodes**](icontextnodes.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a53ae-108">A pointer to the [**IContextNodes**](icontextnodes.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a53ae-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a53ae-109">Return value</span></span>

<span data-ttu-id="a53ae-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a53ae-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a53ae-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a53ae-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a53ae-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnodes* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="a53ae-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodes* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a53ae-113">Verwenden Sie diese Methode, um eine leere [**icontextnodes**](icontextnodes.md) -Auflistung zu erstellen, die mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a53ae-113">Use this method to create an empty [**IContextNodes**](icontextnodes.md) collection that is associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="a53ae-114">Die neue **icontextnodes** -Auflistung ist nicht Teil der Kontext Struktur des **iinkanalyzer** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a53ae-114">The new **IContextNodes** collection is not part of the **IInkAnalyzer** object's context tree.</span></span>

## <a name="requirements"></a><span data-ttu-id="a53ae-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a53ae-115">Requirements</span></span>



| <span data-ttu-id="a53ae-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a53ae-116">Requirement</span></span> | <span data-ttu-id="a53ae-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a53ae-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a53ae-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a53ae-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a53ae-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a53ae-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a53ae-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a53ae-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a53ae-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a53ae-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a53ae-122">Header</span><span class="sxs-lookup"><span data-stu-id="a53ae-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a53ae-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a53ae-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a53ae-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a53ae-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a53ae-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a53ae-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a53ae-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a53ae-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53ae-127">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="a53ae-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a53ae-128">**Icontextnodes**</span><span class="sxs-lookup"><span data-stu-id="a53ae-128">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="a53ae-129">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="a53ae-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

