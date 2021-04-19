---
description: Die Put \_ borderweichheit-Methode gibt die Breite des unscharf-Bereichs um die Ränder des Abbild Musters an.
ms.assetid: 9fdbda7f-c89b-4ed8-8035-054bc28f3231
title: Idxtjpeg::p ut_BorderSoftness-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c72f59798ca84d01be79110cd4792da0a77f408
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373961"
---
# <a name="idxtjpegput_bordersoftness-method"></a><span data-ttu-id="f9b91-103">Idxtjpeg::p UT \_ borderweichheit-Methode</span><span class="sxs-lookup"><span data-stu-id="f9b91-103">IDxtJpeg::put\_BorderSoftness method</span></span>

> [!Note]  
> <span data-ttu-id="f9b91-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f9b91-104">\[Deprecated.</span></span> <span data-ttu-id="f9b91-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f9b91-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f9b91-106">Die- `put_BorderSoftness` Methode gibt die Breite des unscharf-Bereichs um die Ränder des-Abbild Musters an.</span><span class="sxs-lookup"><span data-stu-id="f9b91-106">The `put_BorderSoftness` method specifies the width of the blurry region around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b91-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9b91-107">Syntax</span></span>


```C++
HRESULT put_BorderSoftness(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="f9b91-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9b91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9b91-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9b91-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b91-110">Die Breite des unscharf-Bereichs in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f9b91-110">The width of the blurry region, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9b91-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9b91-111">Return value</span></span>

<span data-ttu-id="f9b91-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f9b91-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f9b91-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f9b91-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9b91-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9b91-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f9b91-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f9b91-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f9b91-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="f9b91-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f9b91-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9b91-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f9b91-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9b91-118">Requirements</span></span>



| <span data-ttu-id="f9b91-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9b91-119">Requirement</span></span> | <span data-ttu-id="f9b91-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f9b91-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b91-121">Header</span><span class="sxs-lookup"><span data-stu-id="f9b91-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f9b91-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f9b91-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f9b91-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9b91-123">Library</span></span><br/> | <dl> <span data-ttu-id="f9b91-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="f9b91-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9b91-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9b91-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b91-126">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f9b91-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




