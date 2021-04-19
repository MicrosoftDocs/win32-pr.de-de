---
description: Die Put \_ srcoffanty-Methode gibt den vertikalen Offset des Quell Rechtecks an.
ms.assetid: abdc520f-8de6-4a4f-aa8f-facedaa8fce1
title: Idxtcompositor::p ut_SrcOffsetY-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcOffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ad574939ce9f3d694944d39af76787dd19a22735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360348"
---
# <a name="idxtcompositorput_srcoffsety-method"></a><span data-ttu-id="78ba3-103">Idxtcompositor::p UT \_ srcoffserty-Methode</span><span class="sxs-lookup"><span data-stu-id="78ba3-103">IDxtCompositor::put\_SrcOffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="78ba3-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="78ba3-104">\[Deprecated.</span></span> <span data-ttu-id="78ba3-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="78ba3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="78ba3-106">Die- `put_SrcOffsetY` Methode gibt den vertikalen Offset des Quell Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="78ba3-106">The `put_SrcOffsetY` method specifies the vertical offset of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="78ba3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78ba3-107">Syntax</span></span>


```C++
HRESULT put_SrcOffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="78ba3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78ba3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78ba3-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78ba3-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ba3-110">Der vertikale Offset des Quell Rechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="78ba3-110">The vertical offset of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78ba3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78ba3-111">Return value</span></span>

<span data-ttu-id="78ba3-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="78ba3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78ba3-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78ba3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="78ba3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78ba3-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="78ba3-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="78ba3-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="78ba3-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="78ba3-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="78ba3-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="78ba3-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="78ba3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78ba3-118">Requirements</span></span>



| <span data-ttu-id="78ba3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78ba3-119">Requirement</span></span> | <span data-ttu-id="78ba3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="78ba3-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78ba3-121">Header</span><span class="sxs-lookup"><span data-stu-id="78ba3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="78ba3-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="78ba3-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="78ba3-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78ba3-123">Library</span></span><br/> | <dl> <span data-ttu-id="78ba3-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="78ba3-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78ba3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78ba3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78ba3-126">**Idxtcompositor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="78ba3-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




