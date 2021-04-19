---
description: Die get \_ offsty-Methode ruft den vertikalen Offset des Ursprungs der Löschung ab.
ms.assetid: 0d8b8df2-b916-4143-b1f1-7912ef3fa025
title: 'Idxtjpeg:: get_OffsetY-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76c0d60ac5150fcec1bde63ccb4e03d820c38ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369640"
---
# <a name="idxtjpegget_offsety-method"></a><span data-ttu-id="0ef76-103">Idxtjpeg:: get \_ offsty-Methode</span><span class="sxs-lookup"><span data-stu-id="0ef76-103">IDxtJpeg::get\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="0ef76-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="0ef76-104">\[Deprecated.</span></span> <span data-ttu-id="0ef76-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="0ef76-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0ef76-106">Die- `get_OffsetY` Methode ruft den vertikalen Offset des Ursprungs der Löschung ab.</span><span class="sxs-lookup"><span data-stu-id="0ef76-106">The `get_OffsetY` method retrieves the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef76-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ef76-107">Syntax</span></span>


```C++
HRESULT get_OffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0ef76-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ef76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef76-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0ef76-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef76-110">Empfängt den vertikalen Offset des Ursprungs der Löschung in Pixel.</span><span class="sxs-lookup"><span data-stu-id="0ef76-110">Receives the vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="0ef76-111">Der Mittelpunkt der Löschung wird um diesen Betrag versetzt.</span><span class="sxs-lookup"><span data-stu-id="0ef76-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef76-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ef76-112">Return value</span></span>

<span data-ttu-id="0ef76-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0ef76-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0ef76-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0ef76-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef76-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ef76-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0ef76-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="0ef76-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0ef76-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="0ef76-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0ef76-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0ef76-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0ef76-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ef76-119">Requirements</span></span>



| <span data-ttu-id="0ef76-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ef76-120">Requirement</span></span> | <span data-ttu-id="0ef76-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0ef76-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef76-122">Header</span><span class="sxs-lookup"><span data-stu-id="0ef76-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0ef76-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0ef76-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0ef76-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ef76-124">Library</span></span><br/> | <dl> <span data-ttu-id="0ef76-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="0ef76-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef76-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ef76-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef76-127">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0ef76-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




