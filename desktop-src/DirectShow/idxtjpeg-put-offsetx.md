---
description: Die Put \_ OffsetX-Methode gibt den horizontalen Offset des Ursprungs zum Löschen an.
ms.assetid: 7bc721fd-7e72-49d4-90ae-a193df46326c
title: Idxtjpeg::p ut_OffsetX-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 70bb908be3f2e2173ebae12f45e24600b38a0441
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361280"
---
# <a name="idxtjpegput_offsetx-method"></a><span data-ttu-id="8634d-103">Idxtjpeg::p UT \_ OffsetX-Methode</span><span class="sxs-lookup"><span data-stu-id="8634d-103">IDxtJpeg::put\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="8634d-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="8634d-104">\[Deprecated.</span></span> <span data-ttu-id="8634d-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="8634d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8634d-106">Die- `put_OffsetX` Methode gibt den horizontalen Offset des Ursprungs für das Löschen an.</span><span class="sxs-lookup"><span data-stu-id="8634d-106">The `put_OffsetX` method specifies the horizontal offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8634d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8634d-107">Syntax</span></span>


```C++
HRESULT put_OffsetX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="8634d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8634d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8634d-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8634d-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8634d-110">Der horizontale Offset des Ursprungs der Löschung in Pixel.</span><span class="sxs-lookup"><span data-stu-id="8634d-110">The horizontal offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="8634d-111">Der Mittelpunkt der Löschung wird um diesen Betrag versetzt.</span><span class="sxs-lookup"><span data-stu-id="8634d-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8634d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8634d-112">Return value</span></span>

<span data-ttu-id="8634d-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8634d-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8634d-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8634d-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8634d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8634d-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8634d-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="8634d-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8634d-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="8634d-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8634d-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8634d-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8634d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8634d-119">Requirements</span></span>



| <span data-ttu-id="8634d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8634d-120">Requirement</span></span> | <span data-ttu-id="8634d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8634d-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8634d-122">Header</span><span class="sxs-lookup"><span data-stu-id="8634d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8634d-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="8634d-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8634d-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8634d-124">Library</span></span><br/> | <dl> <span data-ttu-id="8634d-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="8634d-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8634d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8634d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8634d-127">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8634d-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




