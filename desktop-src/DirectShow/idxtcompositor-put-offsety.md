---
description: Die Put \_ offsty-Methode gibt den vertikalen Offset des Ziel Rechtecks an.
ms.assetid: 68f2774d-9f26-4829-835d-b338c39f1c99
title: Idxtcompositor::p ut_OffsetY-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a20c3812a1fb9756f01ae3a7eb684a6cf6ba0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357949"
---
# <a name="idxtcompositorput_offsety-method"></a><span data-ttu-id="78f30-103">Idxtcompositor::p UT \_ offserty-Methode</span><span class="sxs-lookup"><span data-stu-id="78f30-103">IDxtCompositor::put\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="78f30-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="78f30-104">\[Deprecated.</span></span> <span data-ttu-id="78f30-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="78f30-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="78f30-106">Die- `put_OffsetY` Methode gibt den vertikalen Offset des Ziel Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="78f30-106">The `put_OffsetY` method specifies the vertical offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="78f30-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78f30-107">Syntax</span></span>


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="78f30-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78f30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78f30-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78f30-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78f30-110">Der vertikale Offset des Ziel Rechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="78f30-110">The vertical offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78f30-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78f30-111">Return value</span></span>

<span data-ttu-id="78f30-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="78f30-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78f30-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78f30-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="78f30-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78f30-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="78f30-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="78f30-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="78f30-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="78f30-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="78f30-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="78f30-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="78f30-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78f30-118">Requirements</span></span>



| <span data-ttu-id="78f30-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78f30-119">Requirement</span></span> | <span data-ttu-id="78f30-120">Wert</span><span class="sxs-lookup"><span data-stu-id="78f30-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78f30-121">Header</span><span class="sxs-lookup"><span data-stu-id="78f30-121">Header</span></span><br/>  | <dl> <span data-ttu-id="78f30-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="78f30-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="78f30-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78f30-123">Library</span></span><br/> | <dl> <span data-ttu-id="78f30-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="78f30-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78f30-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78f30-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78f30-126">**Idxtcompositor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="78f30-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




