---
title: Rect-Typfunktion (D2d1helper. h)
description: Erstellt eine Rechteck Struktur, die seine Koordinaten unter Verwendung des angegebenen Datentyps speichert.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Rect-Typfunktion Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ed16ecd5a79c73ecb7341b9aa7f3378854dd4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338752"
---
# <a name="recttype-function"></a><span data-ttu-id="07a40-104">Rect- <Type> Funktion</span><span class="sxs-lookup"><span data-stu-id="07a40-104">Rect<Type> Function</span></span>

<span data-ttu-id="07a40-105">Erstellt eine Rechteck Struktur, die seine Koordinaten unter Verwendung des angegebenen Datentyps speichert.</span><span class="sxs-lookup"><span data-stu-id="07a40-105">Creates a rectangle structure that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a><span data-ttu-id="07a40-106">Vorlagenparameter</span><span class="sxs-lookup"><span data-stu-id="07a40-106">Template Parameters</span></span>



| <span data-ttu-id="07a40-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="07a40-107">Parameter</span></span> | <span data-ttu-id="07a40-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07a40-108">Description</span></span>                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a40-109">type</span><span class="sxs-lookup"><span data-stu-id="07a40-109">Type</span></span>      | <span data-ttu-id="07a40-110">Der Datentyp, der zum Speichern der Abmessungen des Rechtecks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07a40-110">The data type used to store the dimensions of the rectangle.</span></span> <span data-ttu-id="07a40-111">Mögliche Werte sind **float** und **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="07a40-111">Possible values are **FLOAT** and **UINT32**.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="07a40-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="07a40-112">Parameters</span></span>



| <span data-ttu-id="07a40-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="07a40-113">Parameter</span></span> | <span data-ttu-id="07a40-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07a40-114">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="07a40-115">Linker Join</span><span class="sxs-lookup"><span data-stu-id="07a40-115">left</span></span>      | <span data-ttu-id="07a40-116">Die x-Koordinate der oberen linken Ecke des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="07a40-116">The x-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="07a40-117">top</span><span class="sxs-lookup"><span data-stu-id="07a40-117">top</span></span>       | <span data-ttu-id="07a40-118">Die y-Koordinate der oberen linken Ecke des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="07a40-118">The y-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="07a40-119">Rechts</span><span class="sxs-lookup"><span data-stu-id="07a40-119">right</span></span>     | <span data-ttu-id="07a40-120">Die x-Koordinate der unteren rechten Ecke des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="07a40-120">The x-coordinate of the rectangle's lower-right corner.</span></span> |
| <span data-ttu-id="07a40-121">bottom</span><span class="sxs-lookup"><span data-stu-id="07a40-121">bottom</span></span>    | <span data-ttu-id="07a40-122">Die y-Koordinate der unteren rechten Ecke des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="07a40-122">The y-coordinate of the rectangle's lower-right corner.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="07a40-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07a40-123">Return Value</span></span>

<span data-ttu-id="07a40-124">Eine Rechteck Struktur, die die angegebenen Koordinaten enthält.</span><span class="sxs-lookup"><span data-stu-id="07a40-124">A rectangle structure that contains the specified coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="07a40-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07a40-125">Requirements</span></span>



| <span data-ttu-id="07a40-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07a40-126">Requirement</span></span> | <span data-ttu-id="07a40-127">Wert</span><span class="sxs-lookup"><span data-stu-id="07a40-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a40-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07a40-128">Minimum supported client</span></span><br/> | <span data-ttu-id="07a40-129">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="07a40-129">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="07a40-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07a40-130">Minimum supported server</span></span><br/> | <span data-ttu-id="07a40-131">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="07a40-131">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="07a40-132">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="07a40-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="07a40-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="07a40-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="07a40-134">Header</span><span class="sxs-lookup"><span data-stu-id="07a40-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="07a40-135"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="07a40-135"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="07a40-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07a40-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="07a40-137"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07a40-137"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="07a40-138">DLL</span><span class="sxs-lookup"><span data-stu-id="07a40-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07a40-139"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07a40-139"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





