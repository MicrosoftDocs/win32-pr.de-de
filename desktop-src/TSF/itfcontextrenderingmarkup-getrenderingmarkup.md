---
title: ITF contextrenderingmarkup GetRenderingMarkup-Methode
description: Die ITF contextrenderingmarkup GetRenderingMarkup-Methode ruft einen Enumerator der rendermarkups für den angegebenen Bereich ab.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- GetRenderingMarkup-Methode-Text Dienst-Framework
- GetRenderingMarkup Method Text Services Framework, ITF contextrenderingmarkup-Schnittstelle
- ITF contextrenderingmarkup Interface Text Services Framework, GetRenderingMarkup-Methode
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728553"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a><span data-ttu-id="accdf-106">ITF contextrenderingmarkup:: GetRenderingMarkup-Methode</span><span class="sxs-lookup"><span data-stu-id="accdf-106">ITfContextRenderingMarkup::GetRenderingMarkup method</span></span>

<span data-ttu-id="accdf-107">Die **ITF contextrenderingmarkup:: GetRenderingMarkup** -Methode ruft einen Enumerator der rendermarkups für den angegebenen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="accdf-107">The **ITfContextRenderingMarkup::GetRenderingMarkup** method retrieves an enumerator of the rendering markups for the given range.</span></span>

## <a name="syntax"></a><span data-ttu-id="accdf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="accdf-108">Syntax</span></span>


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="accdf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="accdf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="accdf-110">*EC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="accdf-110">*ec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accdf-111">\[in \] einem schreibgeschützten Bearbeitungs Cookie, um auf den Kontext zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="accdf-111">\[in\] A read only edit cookie to access the context.</span></span>

</dd> <dt>

<span data-ttu-id="accdf-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="accdf-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accdf-113">\[in\]</span><span class="sxs-lookup"><span data-stu-id="accdf-113">\[in\]</span></span>



| <span data-ttu-id="accdf-114">Wert</span><span class="sxs-lookup"><span data-stu-id="accdf-114">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="accdf-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="accdf-115">Meaning</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <span data-ttu-id="accdf-116"><dt>**TF \_ GRM \_ include- \_ Eigenschaft**</dt></span><span class="sxs-lookup"><span data-stu-id="accdf-116"><dt>**TF\_GRM\_INCLUDE\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="accdf-117">Wenn dieses Bit 1 ist, enthält der Enumerator die GUID- \_ Eigenschaft des prop- \_ Attributs.</span><span class="sxs-lookup"><span data-stu-id="accdf-117">If this bit is 1, the enumerator will include the GUID\_PROP\_ATTRIBUTE property.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="accdf-118">*prangecover* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="accdf-118">*pRangeCover* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accdf-119">\[in \] einem Zeiger auf eine [itfrange](/windows/desktop/api/Msctf/nn-msctf-itfrange) -Schnittstelle des Bereichs zum Aufzählen der rendermarkups.</span><span class="sxs-lookup"><span data-stu-id="accdf-119">\[in\] A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface of the range to enumerate the rendering markups.</span></span>

</dd> <dt>

<span data-ttu-id="accdf-120">*ppum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="accdf-120">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="accdf-121">\[\]ein Zeiger zum Abrufen des [ienumtfrenderingmarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) -Schnittstellen Zeigers.</span><span class="sxs-lookup"><span data-stu-id="accdf-121">\[out\] A pointer to retrieve [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="accdf-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="accdf-122">Return value</span></span>

<span data-ttu-id="accdf-123">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="accdf-123">This method can return one of these values.</span></span>



| <span data-ttu-id="accdf-124">Wert</span><span class="sxs-lookup"><span data-stu-id="accdf-124">Value</span></span>                                                                                | <span data-ttu-id="accdf-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="accdf-125">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="accdf-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="accdf-126"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="accdf-127">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="accdf-127">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="accdf-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="accdf-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="accdf-129">Diese Methode befindet sich derzeit nicht in den öffentlichen Header Dateien.</span><span class="sxs-lookup"><span data-stu-id="accdf-129">This method is not currently in the public header files.</span></span> <span data-ttu-id="accdf-130">Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.</span><span class="sxs-lookup"><span data-stu-id="accdf-130">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

