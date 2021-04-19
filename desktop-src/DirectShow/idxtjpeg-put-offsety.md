---
description: Die Put \_ Offset-Methode gibt den vertikalen Offset des Ursprungs zum Löschen an.
ms.assetid: 1dfd18cf-06ae-46eb-80d7-078efc243bb1
title: Idxtjpeg::p ut_OffsetY-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f68a18d01acf519032bce31c28515bc7ac81c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361665"
---
# <a name="idxtjpegput_offsety-method"></a><span data-ttu-id="feb6a-103">Idxtjpeg::p UT- \_ offserty-Methode</span><span class="sxs-lookup"><span data-stu-id="feb6a-103">IDxtJpeg::put\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="feb6a-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="feb6a-104">\[Deprecated.</span></span> <span data-ttu-id="feb6a-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="feb6a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="feb6a-106">Die- `put_OffsetY` Methode gibt den vertikalen Offset des Ursprungs für das Löschen an.</span><span class="sxs-lookup"><span data-stu-id="feb6a-106">The `put_OffsetY` method specifies the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb6a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="feb6a-107">Syntax</span></span>


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="feb6a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="feb6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feb6a-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="feb6a-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feb6a-110">Der vertikale Offset des Ursprungs der Löschung in Pixel.</span><span class="sxs-lookup"><span data-stu-id="feb6a-110">The vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="feb6a-111">Der Mittelpunkt der Löschung wird um diesen Betrag versetzt.</span><span class="sxs-lookup"><span data-stu-id="feb6a-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feb6a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="feb6a-112">Return value</span></span>

<span data-ttu-id="feb6a-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="feb6a-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="feb6a-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="feb6a-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="feb6a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="feb6a-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="feb6a-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="feb6a-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="feb6a-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="feb6a-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="feb6a-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="feb6a-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="feb6a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="feb6a-119">Requirements</span></span>



| <span data-ttu-id="feb6a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="feb6a-120">Requirement</span></span> | <span data-ttu-id="feb6a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="feb6a-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="feb6a-122">Header</span><span class="sxs-lookup"><span data-stu-id="feb6a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="feb6a-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="feb6a-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="feb6a-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="feb6a-124">Library</span></span><br/> | <dl> <span data-ttu-id="feb6a-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="feb6a-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feb6a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="feb6a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb6a-127">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="feb6a-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




