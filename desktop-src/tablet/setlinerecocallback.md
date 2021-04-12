---
description: Legt eine Rückruffunktion fest, die während der Zeilen Erkennung verwendet werden soll.
ms.assetid: 0b07ec80-328a-471b-b554-fa66f56a2871
title: Setlinerecocallback-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineRecoCallback
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: b256a38d6d6ee6ecf43994c6619c369ea6ca2212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216586"
---
# <a name="setlinerecocallback-function"></a><span data-ttu-id="62915-103">Setlinerecocallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="62915-103">SetLineRecoCallback function</span></span>

<span data-ttu-id="62915-104">Legt eine Rückruffunktion fest, die während der Zeilen Erkennung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="62915-104">Sets a callback function to be used during line recognition.</span></span>

<span data-ttu-id="62915-105">Diese Hilfsfunktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="62915-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="62915-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="62915-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineRecoCallback(
  _In_ INT_PTR        hDivider,
       GetLineRecoDef pfn
);
```



## <a name="parameters"></a><span data-ttu-id="62915-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="62915-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62915-108">*hdivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62915-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62915-109">Ein Handle für das [**InkDivider**](inkdivider-class.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="62915-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="62915-110">*PFN*</span><span class="sxs-lookup"><span data-stu-id="62915-110">*pfn*</span></span> 
</dt> <dd>

<span data-ttu-id="62915-111">Ein Zeiger auf eine Funktion, die aufgerufen wird, wenn die Erkennung für den weiter gegebenen [**InkDivider**](inkdivider-class.md) erfolgt.</span><span class="sxs-lookup"><span data-stu-id="62915-111">A pointer to a function that is called when recognition occurs on the [**InkDivider**](inkdivider-class.md) passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62915-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62915-112">Return value</span></span>

<span data-ttu-id="62915-113">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="62915-113">This function can return one of these values.</span></span>



| <span data-ttu-id="62915-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="62915-114">Return code</span></span>                                                                                  | <span data-ttu-id="62915-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62915-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="62915-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="62915-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="62915-117">Die Funktion wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62915-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="62915-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="62915-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="62915-119">Der *pdivider* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="62915-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62915-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62915-120">Remarks</span></span>

<span data-ttu-id="62915-121">Im folgenden finden Sie die Syntax für die Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="62915-121">The following is the syntax for the callback function.</span></span>

``` syntax
public delegate void GetLineRecoDef(
        int cStrokes, 
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.I4, SizeParamIndex = 0)]int [] aStrokeIds, 
        float degrees, 
        Point point, 
        [MarshalAs(UnmanagedType.BStr)] out string lineString, 
        out int cSegment, 
        out int[] strokeIdOrdered, 
        out int[] segmentStrokes,
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.BStr)] out string [] aSegmentString
    );
```

## <a name="requirements"></a><span data-ttu-id="62915-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62915-122">Requirements</span></span>



| <span data-ttu-id="62915-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62915-123">Requirement</span></span> | <span data-ttu-id="62915-124">Wert</span><span class="sxs-lookup"><span data-stu-id="62915-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62915-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62915-125">Minimum supported client</span></span><br/> | <span data-ttu-id="62915-126">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62915-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="62915-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62915-127">Minimum supported server</span></span><br/> | <span data-ttu-id="62915-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="62915-128">None supported</span></span><br/>                                                             |
| <span data-ttu-id="62915-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="62915-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="62915-130"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62915-130"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




