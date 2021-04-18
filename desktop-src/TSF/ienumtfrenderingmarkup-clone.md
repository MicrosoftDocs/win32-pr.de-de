---
title: Ienumtfrenderingmarkup-Klon Methode
description: Die ' ienumtfrenderingmarkup '-Klon Methode erstellt eine Kopie des Enumeratorobjekts.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Klon Methode Text Services-Framework
- Klon Methode Text Dienste-Framework, ienumtfrenderingmarkup-Schnittstelle
- Ienumtfrenderingmarkup Interface Text Services-Framework, Klon Methode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340501"
---
# <a name="ienumtfrenderingmarkupclone-method"></a><span data-ttu-id="6c900-106">Ienumtfrenderingmarkup:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="6c900-106">IEnumTfRenderingMarkup::Clone method</span></span>

<span data-ttu-id="6c900-107">Die **ienumtfrenderingmarkup:: Clone** -Methode erstellt eine Kopie des Enumeratorobjekts.</span><span class="sxs-lookup"><span data-stu-id="6c900-107">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c900-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c900-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="6c900-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c900-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c900-110">*ppum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c900-110">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c900-111">\[\]ein Zeiger auf eine [ienumtfrenderingmarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6c900-111">\[out\] A pointer to a [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c900-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c900-112">Return value</span></span>

<span data-ttu-id="6c900-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6c900-113">This method can return one of these values.</span></span>



| <span data-ttu-id="6c900-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6c900-114">Value</span></span>                                                                                        | <span data-ttu-id="6c900-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c900-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="6c900-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6c900-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6c900-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6c900-117">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="6c900-118"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="6c900-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="6c900-119">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6c900-119">An unspecified error occurred.</span></span><br/>      |
| <dl> <span data-ttu-id="6c900-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="6c900-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6c900-121">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c900-121">One or more parameters are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c900-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c900-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6c900-123">Diese Methode befindet sich derzeit nicht in den öffentlichen Header Dateien.</span><span class="sxs-lookup"><span data-stu-id="6c900-123">This method is not currently in the public header files.</span></span> <span data-ttu-id="6c900-124">Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.</span><span class="sxs-lookup"><span data-stu-id="6c900-124">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

