---
description: Die get \_ ScaleX-Methode ruft den Betrag ab, um den das Löschen horizontal gestreckt wird.
ms.assetid: 74c3f60b-68d9-4a8e-a6e5-767ce281a9fb
title: 'Idxtjpeg:: get_ScaleX-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0532e3c068c0ea9641d1fffbcc3d1327290bae02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357681"
---
# <a name="idxtjpegget_scalex-method"></a><span data-ttu-id="56c91-103">Idxtjpeg:: get \_ ScaleX-Methode</span><span class="sxs-lookup"><span data-stu-id="56c91-103">IDxtJpeg::get\_ScaleX method</span></span>

> [!Note]  
> <span data-ttu-id="56c91-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="56c91-104">\[Deprecated.</span></span> <span data-ttu-id="56c91-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="56c91-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="56c91-106">Die- `get_ScaleX` Methode ruft den Betrag ab, um den das Löschen horizontal gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="56c91-106">The `get_ScaleX` method retrieves the amount by which the wipe is stretched horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c91-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56c91-107">Syntax</span></span>


```C++
HRESULT get_ScaleX(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="56c91-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="56c91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56c91-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="56c91-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="56c91-110">Empfängt den Betrag, um den das Löschen horizontal gestreckt wird, als Prozentsatz der ursprünglichen Definition für das Löschen.</span><span class="sxs-lookup"><span data-stu-id="56c91-110">Receives the amount by which the wipe is stretched horizontally, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="56c91-111">Der Wert 1,0 bedeutet beispielsweise keine Streckung, und 2,0 bedeutet, dass 200% gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="56c91-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56c91-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56c91-112">Return value</span></span>

<span data-ttu-id="56c91-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="56c91-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56c91-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="56c91-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="56c91-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56c91-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="56c91-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="56c91-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="56c91-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="56c91-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="56c91-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="56c91-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56c91-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56c91-119">Requirements</span></span>



| <span data-ttu-id="56c91-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56c91-120">Requirement</span></span> | <span data-ttu-id="56c91-121">Wert</span><span class="sxs-lookup"><span data-stu-id="56c91-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56c91-122">Header</span><span class="sxs-lookup"><span data-stu-id="56c91-122">Header</span></span><br/>  | <dl> <span data-ttu-id="56c91-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="56c91-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="56c91-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56c91-124">Library</span></span><br/> | <dl> <span data-ttu-id="56c91-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="56c91-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56c91-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56c91-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c91-127">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="56c91-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




