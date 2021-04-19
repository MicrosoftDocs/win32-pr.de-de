---
description: Die get \_ size-Methode gibt die aktuelle Ausgabegröße und den Stretch-Modus zurück.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'Iresize:: get_Size-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b9fe4971fd9ede0f695fe06a4102da8243e7c720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372717"
---
# <a name="iresizeget_size-method"></a><span data-ttu-id="ff6c5-103">Iresize:: get \_ size-Methode</span><span class="sxs-lookup"><span data-stu-id="ff6c5-103">IResize::get\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="ff6c5-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-104">\[Deprecated.</span></span> <span data-ttu-id="ff6c5-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ff6c5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ff6c5-106">Die- `get_Size` Methode gibt die aktuelle Ausgabegröße und den Stretch-Modus zurück.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-106">The `get_Size` method returns the current output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff6c5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff6c5-107">Syntax</span></span>


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
);
```



## <a name="parameters"></a><span data-ttu-id="ff6c5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff6c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff6c5-109">*piheight* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ff6c5-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff6c5-110">Empfängt die Höhe des Videos in Pixel.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ff6c5-111">*piwidth* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ff6c5-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff6c5-112">Empfängt die Video Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-112">Receives the video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ff6c5-113">*PFLAG* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ff6c5-113">*pFlag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff6c5-114">Empfängt ein Flag, das den streckungs Modus angibt.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-114">Receives a flag specifying the stretch mode.</span></span> <span data-ttu-id="ff6c5-115">Informationen zu möglichen Werten finden Sie unter [**Größenänderung für Flags**](resize-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="ff6c5-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff6c5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff6c5-116">Return value</span></span>

<span data-ttu-id="ff6c5-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff6c5-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff6c5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff6c5-119">Remarks</span></span>

<span data-ttu-id="ff6c5-120">Wenn der Ausgabetyp nicht festgelegt wurde, sollte der Filter Standardwerte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-120">If the output type has not been set, the filter should return default values.</span></span> <span data-ttu-id="ff6c5-121">Diese Werte können zur Entwurfszeit willkürlich ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-121">These values can be arbitrarily chosen at design time.</span></span>

> [!Note]  
> <span data-ttu-id="ff6c5-122">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ff6c5-123">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ff6c5-124">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ff6c5-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ff6c5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff6c5-125">Requirements</span></span>



| <span data-ttu-id="ff6c5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff6c5-126">Requirement</span></span> | <span data-ttu-id="ff6c5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ff6c5-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff6c5-128">Version</span><span class="sxs-lookup"><span data-stu-id="ff6c5-128">Version</span></span><br/> | <span data-ttu-id="ff6c5-129">DirectX 9,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ff6c5-129">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="ff6c5-130">Header</span><span class="sxs-lookup"><span data-stu-id="ff6c5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ff6c5-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ff6c5-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ff6c5-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff6c5-132">Library</span></span><br/> | <dl> <span data-ttu-id="ff6c5-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="ff6c5-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff6c5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff6c5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff6c5-135">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="ff6c5-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="ff6c5-136">**Iresize-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ff6c5-136">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




