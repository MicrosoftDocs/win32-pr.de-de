---
description: Ruft die Bezeichner für die Gebiets Schemas ab, die von diesem iinkanalysiserkenzer unterstützt werden.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: 'Iinkanalysiserkenzer:: GetLanguages-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862708"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a><span data-ttu-id="b9927-103">Iinkanalysiserkenzer:: GetLanguages-Methode</span><span class="sxs-lookup"><span data-stu-id="b9927-103">IInkAnalysisRecognizer::GetLanguages method</span></span>

<span data-ttu-id="b9927-104">Ruft die Bezeichner für die Gebiets Schemas ab, die von diesem [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b9927-104">Retrieves the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9927-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9927-105">Syntax</span></span>


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a><span data-ttu-id="b9927-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9927-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9927-107">*pullanguagescount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b9927-107">*pulLanguagesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9927-108">Die Anzahl der Bezeichner in *ppullanguages*.</span><span class="sxs-lookup"><span data-stu-id="b9927-108">The number of identifiers in *ppulLanguages*.</span></span>

</dd> <dt>

<span data-ttu-id="b9927-109">*ppullanguages* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9927-109">*ppulLanguages* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9927-110">Ein Zeiger auf die Bezeichner für die Gebiets Schemas, die von diesem [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b9927-110">A pointer to the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9927-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9927-111">Return value</span></span>

<span data-ttu-id="b9927-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b9927-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b9927-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9927-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b9927-114">Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppullanguages* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="b9927-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppulLanguages* when you no longer need the information.</span></span>

 

<span data-ttu-id="b9927-115">Diese Methode gibt ein leeres Array für Objekt-und Gesten Erkennungs Tools zurück.</span><span class="sxs-lookup"><span data-stu-id="b9927-115">This method returns an empty array for object and gesture recognizers.</span></span>

<span data-ttu-id="b9927-116">Weitere Informationen zu sprach Bezeichnern finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="b9927-116">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9927-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9927-117">Requirements</span></span>



| <span data-ttu-id="b9927-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9927-118">Requirement</span></span> | <span data-ttu-id="b9927-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b9927-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9927-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9927-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b9927-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9927-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b9927-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9927-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b9927-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b9927-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b9927-124">Header</span><span class="sxs-lookup"><span data-stu-id="b9927-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9927-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b9927-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b9927-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b9927-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9927-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9927-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b9927-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9927-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9927-129">**Iinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="b9927-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="b9927-130">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="b9927-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

