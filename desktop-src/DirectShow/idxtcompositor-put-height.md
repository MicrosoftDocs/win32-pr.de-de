---
description: Die Put \_ Height-Methode gibt die Höhe des Ziel Rechtecks an.
ms.assetid: 032b5468-bce8-4492-abbe-e442131ebe3a
title: Idxtcompositor::p ut_Height-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_Height
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 883a3261b6322a69e0e1612b724a9f570953dc97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364968"
---
# <a name="idxtcompositorput_height-method"></a><span data-ttu-id="91e70-103">Idxtcompositor::p UT \_ Height-Methode</span><span class="sxs-lookup"><span data-stu-id="91e70-103">IDxtCompositor::put\_Height method</span></span>

> [!Note]  
> <span data-ttu-id="91e70-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="91e70-104">\[Deprecated.</span></span> <span data-ttu-id="91e70-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="91e70-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="91e70-106">Die- `put_Height` Methode gibt die Höhe des Ziel Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="91e70-106">The `put_Height` method specifies the height of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="91e70-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="91e70-107">Syntax</span></span>


```C++
HRESULT put_Height(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="91e70-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="91e70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91e70-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91e70-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91e70-110">Die Höhe des Ziel Rechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="91e70-110">The height of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91e70-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91e70-111">Return value</span></span>

<span data-ttu-id="91e70-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="91e70-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="91e70-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="91e70-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="91e70-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91e70-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="91e70-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="91e70-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="91e70-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="91e70-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="91e70-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="91e70-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91e70-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91e70-118">Requirements</span></span>



| <span data-ttu-id="91e70-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91e70-119">Requirement</span></span> | <span data-ttu-id="91e70-120">Wert</span><span class="sxs-lookup"><span data-stu-id="91e70-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91e70-121">Header</span><span class="sxs-lookup"><span data-stu-id="91e70-121">Header</span></span><br/>  | <dl> <span data-ttu-id="91e70-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="91e70-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="91e70-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91e70-123">Library</span></span><br/> | <dl> <span data-ttu-id="91e70-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="91e70-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91e70-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91e70-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91e70-126">**Idxtcompositor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91e70-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




