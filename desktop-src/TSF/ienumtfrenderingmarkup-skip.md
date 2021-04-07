---
title: Ienumtfrenderingmarkup Skip-Methode
description: Die ienumtfrenderingmarkup Skip-Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Skip-Methode, Text Dienste-Framework
- Skip-Methode (Text Dienste-Framework), ienumtfrenderingmarkup-Schnittstelle
- Ienumtfrenderingmarkup Interface Text Services-Framework, Skip-Methode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718173"
---
# <a name="ienumtfrenderingmarkupskip-method"></a><span data-ttu-id="205e1-106">Ienumtfrenderingmarkup:: Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="205e1-106">IEnumTfRenderingMarkup::Skip method</span></span>

<span data-ttu-id="205e1-107">Die **ienumtfrenderingmarkup:: Skip** -Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.</span><span class="sxs-lookup"><span data-stu-id="205e1-107">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="205e1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="205e1-108">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a><span data-ttu-id="205e1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="205e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="205e1-110">*ulcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="205e1-110">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205e1-111">\[in \] gibt die Anzahl der zu über springenden Elemente an.</span><span class="sxs-lookup"><span data-stu-id="205e1-111">\[in\] Specifies the number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="205e1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="205e1-112">Return value</span></span>

<span data-ttu-id="205e1-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="205e1-113">This method can return one of these values.</span></span>



| <span data-ttu-id="205e1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="205e1-114">Value</span></span>                                                                                   | <span data-ttu-id="205e1-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="205e1-115">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="205e1-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="205e1-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="205e1-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="205e1-117">The method was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="205e1-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="205e1-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="205e1-119">Die Methode hat das Ende der Enumeration erreicht, bevor die angegebene Anzahl von Elementen übersprungen werden konnte.</span><span class="sxs-lookup"><span data-stu-id="205e1-119">The method reached the end of the enumeration before the specified number of elements could be skipped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="205e1-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="205e1-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="205e1-121">Diese Methode befindet sich derzeit nicht in den öffentlichen Header Dateien.</span><span class="sxs-lookup"><span data-stu-id="205e1-121">This method is not currently in the public header files.</span></span> <span data-ttu-id="205e1-122">Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.</span><span class="sxs-lookup"><span data-stu-id="205e1-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 





