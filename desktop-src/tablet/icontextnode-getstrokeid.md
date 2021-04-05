---
description: Ruft den Strich Bezeichner für den Strich ab, auf den durch einen Indexwert im icontextnode-Objekt verwiesen wird.
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: 'Icontextnode:: getstrokeid-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b193b3719ac6b67284e3ff8c4297455888f6c9cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751841"
---
# <a name="icontextnodegetstrokeid-method"></a><span data-ttu-id="709fe-103">Icontextnode:: getstrokeid-Methode</span><span class="sxs-lookup"><span data-stu-id="709fe-103">IContextNode::GetStrokeId method</span></span>

<span data-ttu-id="709fe-104">Ruft den Strich Bezeichner für den Strich ab, auf den durch einen Indexwert im [**icontextnode**](icontextnode.md) -Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="709fe-104">Retrieves the stroke identifier for the stroke referenced by an index value within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="709fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="709fe-105">Syntax</span></span>


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="709fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="709fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="709fe-107">*ulindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="709fe-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="709fe-108">Der Index des Strichs, der zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="709fe-108">The index of the stroke to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="709fe-109">*plstrokeid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="709fe-109">*plStrokeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="709fe-110">Der Strich Bezeichner für den Strich, auf den vom *ulindex* -Parameter innerhalb des aktuellen [**icontextnode**](icontextnode.md) -Objekts verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="709fe-110">The stroke identifier for the stroke referenced by the *ulIndex* parameter within the current [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="709fe-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="709fe-111">Return value</span></span>

<span data-ttu-id="709fe-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="709fe-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="709fe-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="709fe-113">Requirements</span></span>



| <span data-ttu-id="709fe-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="709fe-114">Requirement</span></span> | <span data-ttu-id="709fe-115">Wert</span><span class="sxs-lookup"><span data-stu-id="709fe-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="709fe-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="709fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="709fe-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="709fe-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="709fe-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="709fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="709fe-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="709fe-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="709fe-120">Header</span><span class="sxs-lookup"><span data-stu-id="709fe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="709fe-121"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="709fe-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="709fe-122">DLL</span><span class="sxs-lookup"><span data-stu-id="709fe-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="709fe-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="709fe-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="709fe-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="709fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="709fe-125">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="709fe-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="709fe-126">**Icontextnode:: GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="709fe-126">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="709fe-127">**Icontextnode:: getstrokecount**</span><span class="sxs-lookup"><span data-stu-id="709fe-127">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="709fe-128">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="709fe-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




