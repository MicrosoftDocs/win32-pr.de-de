---
description: Ruft die Funktionen des Erkennungs Moduls ab.
ms.assetid: 9014bd9b-54fb-4735-9eb8-56a6188a5fc0
title: 'Iinkanalysiserkenzer:: getfunktionalitäten-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetCapabilities
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07b66ffbed6f3e57edb8a6bfad36959fabbc047c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129477"
---
# <a name="iinkanalysisrecognizergetcapabilities-method"></a><span data-ttu-id="0490c-103">Iinkanalysiserkenzer:: getfunktionalitäten-Methode</span><span class="sxs-lookup"><span data-stu-id="0490c-103">IInkAnalysisRecognizer::GetCapabilities method</span></span>

<span data-ttu-id="0490c-104">Ruft die Funktionen des Erkennungs Moduls ab.</span><span class="sxs-lookup"><span data-stu-id="0490c-104">Retrieves the capabilities of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0490c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0490c-105">Syntax</span></span>


```C++
HRESULT GetCapabilities(
  [out] InkAnalysisRecognizerCapabilities *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="0490c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0490c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0490c-107">*pfunktionen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0490c-107">*pCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0490c-108">Eine bitweise Kombination von [**Erkennungsfunktionen**](recognizercapabilities.md) -Werten.</span><span class="sxs-lookup"><span data-stu-id="0490c-108">A bitwise combination of [**RecognizerCapabilities**](recognizercapabilities.md) values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0490c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0490c-109">Return value</span></span>

<span data-ttu-id="0490c-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0490c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0490c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0490c-111">Remarks</span></span>

<span data-ttu-id="0490c-112">Dieser Wert ist für jede [ **iinkanalysiserkenzer** konstant.](iinkanalysisrecognizer.md)</span><span class="sxs-lookup"><span data-stu-id="0490c-112">This value is constant for each [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="0490c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0490c-113">Requirements</span></span>



| <span data-ttu-id="0490c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0490c-114">Requirement</span></span> | <span data-ttu-id="0490c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0490c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0490c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0490c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0490c-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0490c-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0490c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0490c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0490c-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0490c-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0490c-120">Header</span><span class="sxs-lookup"><span data-stu-id="0490c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0490c-121"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0490c-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0490c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0490c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0490c-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0490c-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0490c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0490c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0490c-125">**Iinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="0490c-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="0490c-126">**Erkennungsfunktionen**</span><span class="sxs-lookup"><span data-stu-id="0490c-126">**RecognizerCapabilities**</span></span>](recognizercapabilities.md)
</dt> <dt>

[<span data-ttu-id="0490c-127">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="0490c-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




