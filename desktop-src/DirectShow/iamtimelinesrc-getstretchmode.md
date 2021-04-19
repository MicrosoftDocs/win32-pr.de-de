---
description: Die getstretchmode-Methode ruft den streckungs Modus ab. Der streckungs Modus bestimmt, wie eine Videoquelle gerendert wird, wenn deren Größe nicht den Ausgabe Dimensionen entspricht.
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: 'Iamtimelinesrc:: getstretchmode-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f10552ac67c50e8656f303fd524bdad2cd07823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367807"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a><span data-ttu-id="169af-104">Iamtimelinesrc:: getstretchmode-Methode</span><span class="sxs-lookup"><span data-stu-id="169af-104">IAMTimelineSrc::GetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="169af-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="169af-105">\[Deprecated.</span></span> <span data-ttu-id="169af-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="169af-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="169af-107">Die- `GetStretchMode` Methode ruft den streckungs Modus ab.</span><span class="sxs-lookup"><span data-stu-id="169af-107">The `GetStretchMode` method retrieves the stretch mode.</span></span> <span data-ttu-id="169af-108">Der streckungs Modus bestimmt, wie eine Videoquelle gerendert wird, wenn deren Größe nicht den Ausgabe Dimensionen entspricht.</span><span class="sxs-lookup"><span data-stu-id="169af-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="169af-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="169af-109">Syntax</span></span>


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="169af-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="169af-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="169af-111">*pnstretchmode*</span><span class="sxs-lookup"><span data-stu-id="169af-111">*pnStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="169af-112">Empfängt ein Flag, das den aktuellen streckungs Modus angibt.</span><span class="sxs-lookup"><span data-stu-id="169af-112">Receives a flag indicating the current stretch mode.</span></span> <span data-ttu-id="169af-113">Eine Liste möglicher Werte finden Sie unter [**Resize Flags**](resize-flags.md).</span><span class="sxs-lookup"><span data-stu-id="169af-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="169af-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="169af-114">Return value</span></span>

<span data-ttu-id="169af-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="169af-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="169af-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="169af-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="169af-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="169af-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="169af-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="169af-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="169af-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="169af-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="169af-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="169af-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="169af-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="169af-121">Requirements</span></span>



| <span data-ttu-id="169af-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="169af-122">Requirement</span></span> | <span data-ttu-id="169af-123">Wert</span><span class="sxs-lookup"><span data-stu-id="169af-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="169af-124">Header</span><span class="sxs-lookup"><span data-stu-id="169af-124">Header</span></span><br/>  | <dl> <span data-ttu-id="169af-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="169af-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="169af-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="169af-126">Library</span></span><br/> | <dl> <span data-ttu-id="169af-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="169af-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="169af-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="169af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="169af-129">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="169af-129">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="169af-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="169af-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




