---
description: Die setstretchmode-Methode legt den streckungs Modus fest. Der streckungs Modus bestimmt, wie eine Videoquelle gerendert wird, wenn deren Größe nicht den Ausgabe Dimensionen entspricht.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'Iamtimelinesrc:: setstretchmode-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2fae71362f6e09d2eae6c2cdf574a2fbda43930b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366896"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a><span data-ttu-id="fa405-104">Iamtimelinesrc:: setstretchmode-Methode</span><span class="sxs-lookup"><span data-stu-id="fa405-104">IAMTimelineSrc::SetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="fa405-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="fa405-105">\[Deprecated.</span></span> <span data-ttu-id="fa405-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="fa405-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fa405-107">Die- `SetStretchMode` Methode legt den streckungs Modus fest.</span><span class="sxs-lookup"><span data-stu-id="fa405-107">The `SetStretchMode` method sets the stretch mode.</span></span> <span data-ttu-id="fa405-108">Der streckungs Modus bestimmt, wie eine Videoquelle gerendert wird, wenn deren Größe nicht den Ausgabe Dimensionen entspricht.</span><span class="sxs-lookup"><span data-stu-id="fa405-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa405-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa405-109">Syntax</span></span>


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="fa405-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa405-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa405-111">*nstretchmode*</span><span class="sxs-lookup"><span data-stu-id="fa405-111">*nStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="fa405-112">Flag, das den aktuellen streckungs Modus angibt.</span><span class="sxs-lookup"><span data-stu-id="fa405-112">Flag indicating the current stretch mode.</span></span> <span data-ttu-id="fa405-113">Eine Liste möglicher Werte finden Sie unter [**Resize Flags**](resize-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fa405-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa405-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa405-114">Return value</span></span>

<span data-ttu-id="fa405-115">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="fa405-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa405-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa405-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fa405-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fa405-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fa405-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="fa405-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fa405-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fa405-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fa405-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa405-120">Requirements</span></span>



| <span data-ttu-id="fa405-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa405-121">Requirement</span></span> | <span data-ttu-id="fa405-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fa405-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa405-123">Header</span><span class="sxs-lookup"><span data-stu-id="fa405-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fa405-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fa405-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fa405-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa405-125">Library</span></span><br/> | <dl> <span data-ttu-id="fa405-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="fa405-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa405-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa405-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa405-128">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fa405-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="fa405-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="fa405-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




