---
description: Ruft die global eindeutigen Bezeichner (GUIDs) für die Eigenschaften ab, die von diesem iinkanalysiserkenzer für Analyseergebnisse generiert werden können.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'Iinkanalysiserkenzer:: GetSupportedProperties-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5507e135241285b8f316d3ff3c2a4ef4d904296f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958972"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a><span data-ttu-id="b61f4-103">Iinkanalysiserkenzer:: GetSupportedProperties-Methode</span><span class="sxs-lookup"><span data-stu-id="b61f4-103">IInkAnalysisRecognizer::GetSupportedProperties method</span></span>

<span data-ttu-id="b61f4-104">Ruft die global eindeutigen Bezeichner (GUIDs) für die Eigenschaften ab, die von diesem [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) für Analyseergebnisse generiert werden können.</span><span class="sxs-lookup"><span data-stu-id="b61f4-104">Retrieves the globally unique identifiers (GUIDs) for the properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

## <a name="syntax"></a><span data-ttu-id="b61f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b61f4-105">Syntax</span></span>


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="b61f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b61f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b61f4-107">*pulpropertiescount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b61f4-107">*pulPropertiesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b61f4-108">Die Anzahl der GUIDs in *ppproperties*.</span><span class="sxs-lookup"><span data-stu-id="b61f4-108">The number of GUIDs in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="b61f4-109">*ppproperties* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b61f4-109">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b61f4-110">Ein Zeiger auf die GUIDs von Eigenschaften, die von diesem [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) für Analyseergebnisse generiert werden können.</span><span class="sxs-lookup"><span data-stu-id="b61f4-110">A pointer to the GUIDs of properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b61f4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b61f4-111">Return value</span></span>

<span data-ttu-id="b61f4-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b61f4-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b61f4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b61f4-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b61f4-114">Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppproperties* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="b61f4-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppProperties* when you no longer need the information.</span></span>

 

<span data-ttu-id="b61f4-115">Eine Erkennung kann Zeilenmetriken, Zeilennummern, Vertrauens Ebenen usw. unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b61f4-115">A recognizer can support line metrics, line numbers, confidence levels, and so on.</span></span> <span data-ttu-id="b61f4-116">Eine umfassende Liste der Eigenschaften, die von einer Erkennung unterstützt werden können, finden Sie unter [erkentionproperty-Konstanten](recognitionproperty-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b61f4-116">For a complete list of the properties that a recognizer can support, see [RecognitionProperty Constants](recognitionproperty-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b61f4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b61f4-117">Requirements</span></span>



| <span data-ttu-id="b61f4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b61f4-118">Requirement</span></span> | <span data-ttu-id="b61f4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b61f4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b61f4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b61f4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b61f4-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b61f4-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b61f4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b61f4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b61f4-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b61f4-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b61f4-124">Header</span><span class="sxs-lookup"><span data-stu-id="b61f4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b61f4-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b61f4-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b61f4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b61f4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b61f4-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b61f4-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b61f4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b61f4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b61f4-129">**Iinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="b61f4-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="b61f4-130">Erkentionproperty-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b61f4-130">RecognitionProperty Constants</span></span>](recognitionproperty-constants.md)
</dt> <dt>

[<span data-ttu-id="b61f4-131">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="b61f4-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

