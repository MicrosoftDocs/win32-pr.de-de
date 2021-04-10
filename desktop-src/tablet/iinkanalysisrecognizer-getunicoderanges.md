---
description: Ruft ein Array von Zeichen Bereichen ab, die die unterstützten Unicode-Zeichen Bereiche darstellen.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'Iinkanalysiserkenzer:: GetUnicodeRanges-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862707"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a><span data-ttu-id="06613-103">Iinkanalysiserkenzer:: GetUnicodeRanges-Methode</span><span class="sxs-lookup"><span data-stu-id="06613-103">IInkAnalysisRecognizer::GetUnicodeRanges method</span></span>

<span data-ttu-id="06613-104">Ruft ein Array von Zeichen Bereichen ab, die die unterstützten Unicode-Zeichen Bereiche darstellen.</span><span class="sxs-lookup"><span data-stu-id="06613-104">Retrieves an array of character ranges representing the supported Unicode character ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="06613-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06613-105">Syntax</span></span>


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a><span data-ttu-id="06613-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06613-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06613-107">*pulnummeriofranges* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="06613-107">*pulNumberOfRanges* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="06613-108">Die Anzahl der Zeichen Bereiche, auf die von *ppullowunicode* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="06613-108">The number of character ranges pointed to by *ppulLowUnicode*.</span></span>

</dd> <dt>

<span data-ttu-id="06613-109">*ppullowunicode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="06613-109">*ppulLowUnicode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06613-110">Ein Zeiger auf ein Array von Zeichen Bereichen, die die unterstützten Unicode-Zeichen Bereiche darstellen.</span><span class="sxs-lookup"><span data-stu-id="06613-110">Pointer to an array of character ranges representing the supported Unicode character ranges.</span></span>

</dd> <dt>

<span data-ttu-id="06613-111">*ppusunicoderangelength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="06613-111">*ppusUnicodeRangeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06613-112">Ein Zeiger auf ein Array von-Werten, das die Länge der einzelnen Array Punkte von *ppullowunicode* angibt.</span><span class="sxs-lookup"><span data-stu-id="06613-112">Pointer to an array of values indicating the length of each array point to by *ppulLowUnicode*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06613-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06613-113">Return value</span></span>

<span data-ttu-id="06613-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="06613-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06613-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06613-115">Requirements</span></span>



| <span data-ttu-id="06613-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06613-116">Requirement</span></span> | <span data-ttu-id="06613-117">Wert</span><span class="sxs-lookup"><span data-stu-id="06613-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06613-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06613-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06613-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06613-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="06613-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06613-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06613-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="06613-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="06613-122">Header</span><span class="sxs-lookup"><span data-stu-id="06613-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="06613-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="06613-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="06613-124">DLL</span><span class="sxs-lookup"><span data-stu-id="06613-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06613-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06613-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="06613-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06613-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06613-127">**Iinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="06613-127">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




