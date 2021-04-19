---
title: Point2-Typfunktion (D2d1helper. h)
description: Erstellt einen Punkt, der seine Koordinaten unter Verwendung des angegebenen Datentyps speichert.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Point2-Typfunktion Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346733"
---
# <a name="point2type-function"></a><span data-ttu-id="6b33d-104">Point2- <Type> Funktion</span><span class="sxs-lookup"><span data-stu-id="6b33d-104">Point2<Type> Function</span></span>

<span data-ttu-id="6b33d-105">Erstellt einen Punkt, der seine Koordinaten unter Verwendung des angegebenen Datentyps speichert.</span><span class="sxs-lookup"><span data-stu-id="6b33d-105">Creates a point that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a><span data-ttu-id="6b33d-106">Vorlagenparameter</span><span class="sxs-lookup"><span data-stu-id="6b33d-106">Template Parameters</span></span>



| <span data-ttu-id="6b33d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b33d-107">Parameter</span></span> | <span data-ttu-id="6b33d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b33d-108">Description</span></span>                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b33d-109">type</span><span class="sxs-lookup"><span data-stu-id="6b33d-109">Type</span></span>      | <span data-ttu-id="6b33d-110">Der Datentyp, der verwendet wird, um die x-Koordinate und die y-Koordinate des Punkts zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6b33d-110">The data type used to store the x-coordinate and y-coordinate of the point.</span></span> <span data-ttu-id="6b33d-111">Mögliche Werte sind float und UInt32.</span><span class="sxs-lookup"><span data-stu-id="6b33d-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="6b33d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b33d-112">Parameters</span></span>



| <span data-ttu-id="6b33d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b33d-113">Parameter</span></span> | <span data-ttu-id="6b33d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b33d-114">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="6b33d-115">x</span><span class="sxs-lookup"><span data-stu-id="6b33d-115">x</span></span>         | <span data-ttu-id="6b33d-116">Die x-Koordinate des Punkts.</span><span class="sxs-lookup"><span data-stu-id="6b33d-116">The x-coordinate of the point.</span></span> |
| <span data-ttu-id="6b33d-117">Y</span><span class="sxs-lookup"><span data-stu-id="6b33d-117">y</span></span>         | <span data-ttu-id="6b33d-118">Die y-Koordinate des Punkts.</span><span class="sxs-lookup"><span data-stu-id="6b33d-118">The y-coordinate of the point.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="6b33d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b33d-119">Return Value</span></span>

<span data-ttu-id="6b33d-120">Ein Punkt, der die angegebene x-Koordinate und y-Koordinate enthält.</span><span class="sxs-lookup"><span data-stu-id="6b33d-120">A point that contains the specified x-coordinate and y-coordinate.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b33d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b33d-121">Requirements</span></span>



| <span data-ttu-id="6b33d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b33d-122">Requirement</span></span> | <span data-ttu-id="6b33d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6b33d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b33d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b33d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6b33d-125">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6b33d-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="6b33d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b33d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6b33d-127">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6b33d-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="6b33d-128">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="6b33d-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="6b33d-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="6b33d-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="6b33d-130">Header</span><span class="sxs-lookup"><span data-stu-id="6b33d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b33d-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b33d-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="6b33d-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b33d-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b33d-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b33d-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="6b33d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6b33d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b33d-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b33d-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





