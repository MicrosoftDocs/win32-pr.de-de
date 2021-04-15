---
title: Size-Typfunktion (D2d1helper. h)
description: Erstellt eine Größen Struktur, die die Breite und Höhe unter Verwendung des angegebenen Datentyps speichert.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Size-Typfunktion Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476257"
---
# <a name="sizetype-function"></a><span data-ttu-id="0aca2-104">Size- <Type> Funktion</span><span class="sxs-lookup"><span data-stu-id="0aca2-104">Size<Type> Function</span></span>

<span data-ttu-id="0aca2-105">Erstellt eine Größen Struktur, die die Breite und Höhe unter Verwendung des angegebenen Datentyps speichert.</span><span class="sxs-lookup"><span data-stu-id="0aca2-105">Creates a size structure that stores its width and height using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a><span data-ttu-id="0aca2-106">Vorlagenparameter</span><span class="sxs-lookup"><span data-stu-id="0aca2-106">Template Parameters</span></span>



| <span data-ttu-id="0aca2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0aca2-107">Parameter</span></span> | <span data-ttu-id="0aca2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aca2-108">Description</span></span>                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aca2-109">type</span><span class="sxs-lookup"><span data-stu-id="0aca2-109">Type</span></span>      | <span data-ttu-id="0aca2-110">Der Datentyp, der zum Speichern der Breite und Höhe der Größe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0aca2-110">The data type used to store the width and height of the size.</span></span> <span data-ttu-id="0aca2-111">Mögliche Werte sind float und UInt32.</span><span class="sxs-lookup"><span data-stu-id="0aca2-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="0aca2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0aca2-112">Parameters</span></span>



| <span data-ttu-id="0aca2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0aca2-113">Parameter</span></span> | <span data-ttu-id="0aca2-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aca2-114">Description</span></span>        |
|-----------|--------------------|
| <span data-ttu-id="0aca2-115">width</span><span class="sxs-lookup"><span data-stu-id="0aca2-115">width</span></span>     | <span data-ttu-id="0aca2-116">Die Breite der Größe.</span><span class="sxs-lookup"><span data-stu-id="0aca2-116">The size's width.</span></span>  |
| <span data-ttu-id="0aca2-117">height</span><span class="sxs-lookup"><span data-stu-id="0aca2-117">height</span></span>    | <span data-ttu-id="0aca2-118">Die Höhe der Größe.</span><span class="sxs-lookup"><span data-stu-id="0aca2-118">The size's height.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="0aca2-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0aca2-119">Return Value</span></span>

<span data-ttu-id="0aca2-120">Eine Größe, die die angegebene Breite und Höhe enthält.</span><span class="sxs-lookup"><span data-stu-id="0aca2-120">A size that contains the specified width and height.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aca2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0aca2-121">Requirements</span></span>



| <span data-ttu-id="0aca2-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0aca2-122">Requirement</span></span> | <span data-ttu-id="0aca2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0aca2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aca2-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0aca2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0aca2-125">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0aca2-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="0aca2-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0aca2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0aca2-127">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0aca2-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="0aca2-128">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="0aca2-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="0aca2-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="0aca2-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="0aca2-130">Header</span><span class="sxs-lookup"><span data-stu-id="0aca2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aca2-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aca2-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="0aca2-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0aca2-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="0aca2-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0aca2-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="0aca2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0aca2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aca2-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aca2-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





