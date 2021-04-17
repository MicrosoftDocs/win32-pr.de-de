---
description: Ruft den erkannten Zeichen folgen Wert des ianalysisalternate-Objekts ab.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'Ianalysisalternate:: GetRecognizedString-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5489773b29ade35d4b7297065c1104bfecefa117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526570"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a><span data-ttu-id="00d79-103">Ianalysisalternate:: GetRecognizedString-Methode</span><span class="sxs-lookup"><span data-stu-id="00d79-103">IAnalysisAlternate::GetRecognizedString method</span></span>

<span data-ttu-id="00d79-104">Ruft den erkannten Zeichen folgen Wert des [**ianalysisalternate**](ianalysisalternate.md) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="00d79-104">Gets the recognized string value of the [**IAnalysisAlternate**](ianalysisalternate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00d79-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="00d79-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00d79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d79-107">*pbstrauerkenzedstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="00d79-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00d79-108">Ein Zeiger auf den **BSTR** -Wert, der auf den erkannten Zeichen folgen Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="00d79-108">A pointer to the **BSTR** that is set to the recognized string value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00d79-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00d79-109">Return value</span></span>

<span data-ttu-id="00d79-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="00d79-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00d79-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00d79-111">Requirements</span></span>



| <span data-ttu-id="00d79-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00d79-112">Requirement</span></span> | <span data-ttu-id="00d79-113">Wert</span><span class="sxs-lookup"><span data-stu-id="00d79-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d79-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00d79-114">Minimum supported client</span></span><br/> | <span data-ttu-id="00d79-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00d79-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="00d79-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00d79-116">Minimum supported server</span></span><br/> | <span data-ttu-id="00d79-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="00d79-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="00d79-118">Header</span><span class="sxs-lookup"><span data-stu-id="00d79-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d79-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="00d79-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="00d79-120">DLL</span><span class="sxs-lookup"><span data-stu-id="00d79-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00d79-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00d79-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="00d79-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00d79-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d79-123">**Ianalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="00d79-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="00d79-124">**Iinkanalyzer:: GetRecognizedString-Methode**</span><span class="sxs-lookup"><span data-stu-id="00d79-124">**IInkAnalyzer::GetRecognizedString Method**</span></span>](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




