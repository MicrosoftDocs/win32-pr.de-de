---
description: Ruft den Globally Unique Identifier (GUID) der Erkennung ab.
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: 'Iinkanalysiserkenzer:: GetGuid-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetGuid
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9a027a405829e6d1237a8ec90dd59fcc8905006d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862711"
---
# <a name="iinkanalysisrecognizergetguid-method"></a><span data-ttu-id="4cf1b-103">Iinkanalysiserkenzer:: GetGuid-Methode</span><span class="sxs-lookup"><span data-stu-id="4cf1b-103">IInkAnalysisRecognizer::GetGuid method</span></span>

<span data-ttu-id="4cf1b-104">Ruft den Globally Unique Identifier (GUID) der Erkennung ab.</span><span class="sxs-lookup"><span data-stu-id="4cf1b-104">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf1b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cf1b-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="4cf1b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cf1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf1b-107">*pId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4cf1b-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cf1b-108">Die GUID, die diese [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4cf1b-108">The GUID that identifies this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cf1b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cf1b-109">Return value</span></span>

<span data-ttu-id="4cf1b-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4cf1b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cf1b-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cf1b-111">Requirements</span></span>



| <span data-ttu-id="4cf1b-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cf1b-112">Requirement</span></span> | <span data-ttu-id="4cf1b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4cf1b-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf1b-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4cf1b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf1b-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cf1b-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4cf1b-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4cf1b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf1b-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4cf1b-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4cf1b-118">Header</span><span class="sxs-lookup"><span data-stu-id="4cf1b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cf1b-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4cf1b-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4cf1b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4cf1b-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cf1b-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cf1b-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4cf1b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cf1b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf1b-123">**Iinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="4cf1b-123">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="4cf1b-124">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="4cf1b-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




