---
description: Ruft den Herstellernamen des iinkanalysiserkenzer-Elements ab.
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: 'Iinkanalysiserkenzer:: getvendor-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetVendor
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a48bec62ed4a6a9d94d54ea3a1ba4a53eddd4b7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129473"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a><span data-ttu-id="8e4a9-103">Iinkanalysiserkenzer:: getvendor-Methode</span><span class="sxs-lookup"><span data-stu-id="8e4a9-103">IInkAnalysisRecognizer::GetVendor method</span></span>

<span data-ttu-id="8e4a9-104">Ruft den Herstellernamen des [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)-Elements ab.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-104">Retrieves the vendor name of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e4a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e4a9-105">Syntax</span></span>


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a><span data-ttu-id="8e4a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e4a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e4a9-107">*pbstrinvendor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8e4a9-107">*pbstrVendor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e4a9-108">Der Name des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-108">The name of the vendor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e4a9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e4a9-109">Return value</span></span>

<span data-ttu-id="8e4a9-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8e4a9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8e4a9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e4a9-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8e4a9-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**sysfrestring**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) für \* *pbstrinvendor* , wenn Sie die Zeichenfolge nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrVendor* when you no longer need to use the string.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8e4a9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e4a9-113">Requirements</span></span>



| <span data-ttu-id="8e4a9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e4a9-114">Requirement</span></span> | <span data-ttu-id="8e4a9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8e4a9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e4a9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e4a9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8e4a9-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e4a9-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8e4a9-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e4a9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8e4a9-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8e4a9-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8e4a9-120">Header</span><span class="sxs-lookup"><span data-stu-id="8e4a9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e4a9-121"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8e4a9-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8e4a9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8e4a9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e4a9-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e4a9-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8e4a9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e4a9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e4a9-125">**Iinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8e4a9-126">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="8e4a9-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

