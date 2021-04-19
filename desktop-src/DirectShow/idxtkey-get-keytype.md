---
description: Die get \_ KeyType-Methode ruft den Schlüsseltyp ab.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'Idxtkey:: get_KeyType-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370645"
---
# <a name="idxtkeyget_keytype-method"></a><span data-ttu-id="d57a4-103">Idxtkey:: get \_ KeyType-Methode</span><span class="sxs-lookup"><span data-stu-id="d57a4-103">IDxtKey::get\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="d57a4-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d57a4-104">\[Deprecated.</span></span> <span data-ttu-id="d57a4-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d57a4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d57a4-106">Die- `get_KeyType` Methode ruft den Schlüsseltyp ab.</span><span class="sxs-lookup"><span data-stu-id="d57a4-106">The `get_KeyType` method retrieves the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57a4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d57a4-107">Syntax</span></span>


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d57a4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d57a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d57a4-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d57a4-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d57a4-110">Empfängt einen der folgenden Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="d57a4-110">Receives one of the following enumeration values.</span></span>



| <span data-ttu-id="d57a4-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d57a4-111">Value</span></span>             | <span data-ttu-id="d57a4-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d57a4-112">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="d57a4-113">dxtkey \_ RGB</span><span class="sxs-lookup"><span data-stu-id="d57a4-113">DXTKEY\_RGB</span></span>       | <span data-ttu-id="d57a4-114">Chroma-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="d57a4-114">Chroma key.</span></span> <span data-ttu-id="d57a4-115">(Schlüssel für RGB-Wert.)</span><span class="sxs-lookup"><span data-stu-id="d57a4-115">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="d57a4-116">dxtkey \_ nicht rot</span><span class="sxs-lookup"><span data-stu-id="d57a4-116">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="d57a4-117">Nicht-rote Taste.</span><span class="sxs-lookup"><span data-stu-id="d57a4-117">Nonred key.</span></span> <span data-ttu-id="d57a4-118">(Macht blaue und grüne Bereiche transparent.)</span><span class="sxs-lookup"><span data-stu-id="d57a4-118">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="d57a4-119">dxtkey- \_ Leuchtkraft</span><span class="sxs-lookup"><span data-stu-id="d57a4-119">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="d57a4-120">Der Schlüssel für die Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="d57a4-120">Luminance key.</span></span>                                        |
| <span data-ttu-id="d57a4-121">dxtkey \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="d57a4-121">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="d57a4-122">Schlüssel nach Alpha Wert.</span><span class="sxs-lookup"><span data-stu-id="d57a4-122">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="d57a4-123">dxtkey- \_ Farbton</span><span class="sxs-lookup"><span data-stu-id="d57a4-123">DXTKEY\_HUE</span></span>       | <span data-ttu-id="d57a4-124">Schlüssel nach Farbton.</span><span class="sxs-lookup"><span data-stu-id="d57a4-124">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d57a4-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d57a4-125">Return value</span></span>

<span data-ttu-id="d57a4-126">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d57a4-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d57a4-127">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d57a4-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d57a4-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d57a4-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d57a4-129">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d57a4-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d57a4-130">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="d57a4-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d57a4-131">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d57a4-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d57a4-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d57a4-132">Requirements</span></span>



| <span data-ttu-id="d57a4-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d57a4-133">Requirement</span></span> | <span data-ttu-id="d57a4-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d57a4-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d57a4-135">Header</span><span class="sxs-lookup"><span data-stu-id="d57a4-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d57a4-136"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d57a4-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d57a4-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d57a4-137">Library</span></span><br/> | <dl> <span data-ttu-id="d57a4-138"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="d57a4-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d57a4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d57a4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57a4-140">**Idxtkey-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d57a4-140">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




