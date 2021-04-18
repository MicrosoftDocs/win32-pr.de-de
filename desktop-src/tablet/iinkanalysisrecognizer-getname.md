---
description: Ruft den Namen der Erkennung ab.
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: 'Iinkanalysiserkenzer:: GetName-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fe263878d1fd5e914cf033111997d297a20c54f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345739"
---
# <a name="iinkanalysisrecognizergetname-method"></a><span data-ttu-id="b146e-103">Iinkanalysiserkenzer:: GetName-Methode</span><span class="sxs-lookup"><span data-stu-id="b146e-103">IInkAnalysisRecognizer::GetName method</span></span>

<span data-ttu-id="b146e-104">Ruft den Namen der Erkennung ab.</span><span class="sxs-lookup"><span data-stu-id="b146e-104">Retrieves the name of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b146e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b146e-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="b146e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b146e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b146e-107">*pbstrinname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b146e-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b146e-108">Der Name der Erkennung.</span><span class="sxs-lookup"><span data-stu-id="b146e-108">The name of the recognizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b146e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b146e-109">Return value</span></span>

<span data-ttu-id="b146e-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b146e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b146e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b146e-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b146e-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**sysfrestring**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) für \* *pbstrinname* , wenn Sie die Zeichenfolge nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="b146e-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrName* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="b146e-113">Der Name wird für die Regions neutrale Sprache lokalisiert, die die Erkennung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b146e-113">The name is localized for the region-neutral language that the recognizer supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="b146e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b146e-114">Requirements</span></span>



| <span data-ttu-id="b146e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b146e-115">Requirement</span></span> | <span data-ttu-id="b146e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b146e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b146e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b146e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b146e-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b146e-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b146e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b146e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b146e-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b146e-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b146e-121">Header</span><span class="sxs-lookup"><span data-stu-id="b146e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b146e-122"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b146e-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b146e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b146e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b146e-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b146e-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b146e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b146e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b146e-126">**Iinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="b146e-126">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="b146e-127">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="b146e-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

