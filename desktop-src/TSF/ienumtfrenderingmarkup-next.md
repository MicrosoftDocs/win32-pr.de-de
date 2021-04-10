---
title: Ienumtfrenderingmarkup Next-Methode
description: Die ienumtfrenderingmarkup Next-Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Next-Methode Text Services-Framework
- Next Method Text Services Framework, ienumtfrenderingmarkup-Schnittstelle
- Ienumtfrenderingmarkup Interface Text Services-Framework, Next-Methode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039239"
---
# <a name="ienumtfrenderingmarkupnext-method"></a><span data-ttu-id="c0759-106">Ienumtfrenderingmarkup:: Next-Methode</span><span class="sxs-lookup"><span data-stu-id="c0759-106">IEnumTfRenderingMarkup::Next method</span></span>

<span data-ttu-id="c0759-107">Die **ienumtfrenderingmarkup:: Next** -Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.</span><span class="sxs-lookup"><span data-stu-id="c0759-107">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0759-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0759-108">Syntax</span></span>


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="c0759-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0759-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0759-110">*ulcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c0759-110">*ulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0759-111">\[Out \] gibt die Anzahl der abzurufenden Elemente an.</span><span class="sxs-lookup"><span data-stu-id="c0759-111">\[out\] Specifies the number of elements to obtain.</span></span>

</dd> <dt>

<span data-ttu-id="c0759-112">*ppelement* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c0759-112">*ppElement* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0759-113">\[Out- \] Zeiger auf ein Array von [tf \_ renderingmarkup](/windows/desktop/TSF/tf-renderingmarkup) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="c0759-113">\[out\] Pointer to an array of [TF\_RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) structures.</span></span> <span data-ttu-id="c0759-114">Dieses Array muss mindestens eine *ulcount* -Elementgröße aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c0759-114">This array must be at least *ulCount* elements in size.</span></span>

</dd> <dt>

<span data-ttu-id="c0759-115">*pcfetch* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c0759-115">*pcFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0759-116">\[Out- \] Zeiger auf einen Ulong-Wert, der die Anzahl der tatsächlich erhaltenen Elemente empfängt.</span><span class="sxs-lookup"><span data-stu-id="c0759-116">\[out\] Pointer to a ULONG value that receives the number of elements actually obtained.</span></span> <span data-ttu-id="c0759-117">Dieser Wert kann kleiner als die Anzahl der angeforderten Elemente sein.</span><span class="sxs-lookup"><span data-stu-id="c0759-117">This value can be less than the number of items requested.</span></span> <span data-ttu-id="c0759-118">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="c0759-118">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0759-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0759-119">Return value</span></span>

<span data-ttu-id="c0759-120">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c0759-120">This method can return one of these values.</span></span>



| <span data-ttu-id="c0759-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c0759-121">Value</span></span>                                                                                        | <span data-ttu-id="c0759-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0759-122">Description</span></span>                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0759-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c0759-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c0759-124">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c0759-124">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="c0759-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c0759-125"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="c0759-126">Die Methode hat das Ende der Enumeration erreicht, bevor die angegebene Anzahl von Elementen abgerufen werden konnte.</span><span class="sxs-lookup"><span data-stu-id="c0759-126">The method reached the end of the enumeration before the specified number of elements could be obtained.</span></span><br/> |
| <dl> <span data-ttu-id="c0759-127"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c0759-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c0759-128">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c0759-128">One or more parameters are invalid.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="c0759-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0759-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c0759-130">Diese Methode befindet sich derzeit nicht in den öffentlichen Header Dateien.</span><span class="sxs-lookup"><span data-stu-id="c0759-130">This method is not currently in the public header files.</span></span> <span data-ttu-id="c0759-131">Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.</span><span class="sxs-lookup"><span data-stu-id="c0759-131">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

