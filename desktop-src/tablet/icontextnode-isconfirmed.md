---
description: Ruft einen Wert ab, der angibt, ob der an diese Methode weiter gegebene ConfirmationType für diesen icontextnode festgelegt wurde.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'Icontextnode:: isconfirmed-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 300e0126b4a1ff55d372ff31deebde0eab686645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526519"
---
# <a name="icontextnodeisconfirmed-method"></a><span data-ttu-id="901c0-103">Icontextnode:: isconfirmed-Methode</span><span class="sxs-lookup"><span data-stu-id="901c0-103">IContextNode::IsConfirmed method</span></span>

<span data-ttu-id="901c0-104">Ruft einen Wert ab, der angibt, ob der an diese Methode weiter gegebene ConfirmationType für diesen icontextnode festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="901c0-104">Retrieves a value that indicates whether the ConfirmationType passed in to this method has been set on this IContextNode.</span></span>

## <a name="syntax"></a><span data-ttu-id="901c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="901c0-105">Syntax</span></span>


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a><span data-ttu-id="901c0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="901c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="901c0-107">*confirmedtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="901c0-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="901c0-108">Der zu testende bestätentyp.</span><span class="sxs-lookup"><span data-stu-id="901c0-108">The confirmation type being tested for.</span></span>

</dd> <dt>

<span data-ttu-id="901c0-109">*pftypebestätigt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="901c0-109">*pfTypeConfirmed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="901c0-110">**Variant \_ TRUE** , wenn der in confirmedtype weiter gegebene Typ für dieses [**icontextnode**](icontextnode.md) -Objekt festgelegt wurde. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="901c0-110">**VARIANT\_TRUE** if the type passed in confirmedType has been set on this [**IContextNode**](icontextnode.md) object; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="901c0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="901c0-111">Return value</span></span>

<span data-ttu-id="901c0-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="901c0-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="901c0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="901c0-113">Remarks</span></span>

<span data-ttu-id="901c0-114">Dieser Wert wird durch die [**icontextnode:: Confirm**](icontextnode-confirm.md) -Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="901c0-114">This value is set by the [**IContextNode::Confirm**](icontextnode-confirm.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="901c0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="901c0-115">Requirements</span></span>



| <span data-ttu-id="901c0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="901c0-116">Requirement</span></span> | <span data-ttu-id="901c0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="901c0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="901c0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="901c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="901c0-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="901c0-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="901c0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="901c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="901c0-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="901c0-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="901c0-122">Header</span><span class="sxs-lookup"><span data-stu-id="901c0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="901c0-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="901c0-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="901c0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="901c0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="901c0-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="901c0-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="901c0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="901c0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="901c0-127">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="901c0-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="901c0-128">**Icontextnode:: Confirm**</span><span class="sxs-lookup"><span data-stu-id="901c0-128">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="901c0-129">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="901c0-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




