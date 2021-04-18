---
description: Die Put \_ KeyType-Methode gibt den Schlüsseltyp an.
ms.assetid: 4a6201e6-1939-4da6-8c9f-1c34b9713ecb
title: Idxtkey::p ut_KeyType-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e5e501c1f678adb857e39d579fbd958127652a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372331"
---
# <a name="idxtkeyput_keytype-method"></a><span data-ttu-id="b8f24-103">Idxtkey::p UT- \_ KeyType-Methode</span><span class="sxs-lookup"><span data-stu-id="b8f24-103">IDxtKey::put\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="b8f24-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b8f24-104">\[Deprecated.</span></span> <span data-ttu-id="b8f24-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b8f24-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b8f24-106">Die- `put_KeyType` Methode gibt den Typ des Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="b8f24-106">The `put_KeyType` method specifies the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f24-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8f24-107">Syntax</span></span>


```C++
HRESULT put_KeyType(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="b8f24-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8f24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f24-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8f24-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8f24-110">Gibt den Schlüsseltyp an.</span><span class="sxs-lookup"><span data-stu-id="b8f24-110">Specifies the key type.</span></span> <span data-ttu-id="b8f24-111">Dieser Parameter muss einen der folgenden Enumerationswerte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b8f24-111">This parameter must be one of the following enumeration values.</span></span>



| <span data-ttu-id="b8f24-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b8f24-112">Value</span></span>             | <span data-ttu-id="b8f24-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8f24-113">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b8f24-114">dxtkey \_ RGB</span><span class="sxs-lookup"><span data-stu-id="b8f24-114">DXTKEY\_RGB</span></span>       | <span data-ttu-id="b8f24-115">Chroma-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b8f24-115">Chroma key.</span></span> <span data-ttu-id="b8f24-116">(Schlüssel für RGB-Wert.)</span><span class="sxs-lookup"><span data-stu-id="b8f24-116">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="b8f24-117">dxtkey \_ nicht rot</span><span class="sxs-lookup"><span data-stu-id="b8f24-117">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="b8f24-118">Nicht-rote Taste.</span><span class="sxs-lookup"><span data-stu-id="b8f24-118">Nonred key.</span></span> <span data-ttu-id="b8f24-119">(Macht blaue und grüne Bereiche transparent.)</span><span class="sxs-lookup"><span data-stu-id="b8f24-119">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="b8f24-120">dxtkey- \_ Leuchtkraft</span><span class="sxs-lookup"><span data-stu-id="b8f24-120">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="b8f24-121">Der Schlüssel für die Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="b8f24-121">Luminance key.</span></span>                                        |
| <span data-ttu-id="b8f24-122">dxtkey \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="b8f24-122">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="b8f24-123">Schlüssel nach Alpha Wert.</span><span class="sxs-lookup"><span data-stu-id="b8f24-123">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="b8f24-124">dxtkey- \_ Farbton</span><span class="sxs-lookup"><span data-stu-id="b8f24-124">DXTKEY\_HUE</span></span>       | <span data-ttu-id="b8f24-125">Schlüssel nach Farbton.</span><span class="sxs-lookup"><span data-stu-id="b8f24-125">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f24-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8f24-126">Return value</span></span>

<span data-ttu-id="b8f24-127">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b8f24-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b8f24-128">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b8f24-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f24-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8f24-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8f24-130">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b8f24-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b8f24-131">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b8f24-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b8f24-132">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8f24-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8f24-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8f24-133">Requirements</span></span>



| <span data-ttu-id="b8f24-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8f24-134">Requirement</span></span> | <span data-ttu-id="b8f24-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b8f24-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f24-136">Header</span><span class="sxs-lookup"><span data-stu-id="b8f24-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b8f24-137"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b8f24-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b8f24-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8f24-138">Library</span></span><br/> | <dl> <span data-ttu-id="b8f24-139"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b8f24-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8f24-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8f24-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f24-141">**Idxtkey-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b8f24-141">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




