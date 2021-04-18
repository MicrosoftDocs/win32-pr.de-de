---
description: Die Put \_ mediaType-Methode legt den Ausgabe Medientyp für den Filter zum Ändern der Größe fest.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: Iresize::p ut_MediaType-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364921"
---
# <a name="iresizeput_mediatype-method"></a><span data-ttu-id="cb0db-103">Iresize::p UT \_ mediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="cb0db-103">IResize::put\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="cb0db-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cb0db-104">\[Deprecated.</span></span> <span data-ttu-id="cb0db-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cb0db-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cb0db-106">Die- `put_MediaType` Methode legt den Ausgabe Medientyp für den Filter zum Ändern der Größe fest.</span><span class="sxs-lookup"><span data-stu-id="cb0db-106">The `put_MediaType` method sets the output media type on the resizer filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb0db-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb0db-107">Syntax</span></span>


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="cb0db-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb0db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb0db-109">*PMT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb0db-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb0db-110">Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="cb0db-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb0db-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb0db-111">Return value</span></span>

<span data-ttu-id="cb0db-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="cb0db-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cb0db-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cb0db-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb0db-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb0db-114">Remarks</span></span>

<span data-ttu-id="cb0db-115">Des ruft diese Methode auf, bevor eine Verbindung mit der Ausgabe-PIN des Filters hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cb0db-115">DES calls this method before it connects the filter's output pin.</span></span> <span data-ttu-id="cb0db-116">Verwenden Sie den Medientyp als Medientyp der Ausgabepin.</span><span class="sxs-lookup"><span data-stu-id="cb0db-116">Use the media type as the output pin's media type.</span></span> <span data-ttu-id="cb0db-117">Geben Sie diesen Medientyp in der [**ctransformfilter:: getmediatype**](ctransformfilter-getmediatype.md) -Methode zurück, und überprüfen Sie diesen Typ in der [**ctransformfilter:: checktransform**](ctransformfilter-checktransform.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cb0db-117">Return this media type in the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method, and check agsint this type in the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span> <span data-ttu-id="cb0db-118">Des ruft diese Methode niemals auf, nachdem die Ausgabe-PIN verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="cb0db-118">DES never calls this method after the output pin is connected.</span></span>

<span data-ttu-id="cb0db-119">Derzeit legt des den Ausgabe Medientyp auf ein unkomprimiertes RGB-Format mit einem **videoinfoheader** -Format Block (Formattyp ist gleich Format \_ videoinfo) fest.</span><span class="sxs-lookup"><span data-stu-id="cb0db-119">Currently, DES always sets the output media type to an uncompressed RGB format with a **VIDEOINFOHEADER** format block (format type equals FORMAT\_VideoInfo).</span></span> <span data-ttu-id="cb0db-120">Der Untertyp ist möglicherweise mediasubtype \_ ARGB32, womit 32-Bit-RGB mit einem Alphakanal angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb0db-120">The subtype might be MEDIASUBTYPE\_ARGB32, which indicates 32-bit RGB with an alpha channel.</span></span>

> [!Note]  
> <span data-ttu-id="cb0db-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cb0db-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cb0db-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="cb0db-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cb0db-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb0db-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb0db-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb0db-124">Requirements</span></span>



| <span data-ttu-id="cb0db-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb0db-125">Requirement</span></span> | <span data-ttu-id="cb0db-126">Wert</span><span class="sxs-lookup"><span data-stu-id="cb0db-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb0db-127">Version</span><span class="sxs-lookup"><span data-stu-id="cb0db-127">Version</span></span><br/> | <span data-ttu-id="cb0db-128">DirectX 9,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="cb0db-128">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="cb0db-129">Header</span><span class="sxs-lookup"><span data-stu-id="cb0db-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cb0db-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cb0db-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cb0db-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cb0db-131">Library</span></span><br/> | <dl> <span data-ttu-id="cb0db-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="cb0db-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb0db-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb0db-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb0db-134">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="cb0db-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="cb0db-135">**Iresize-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cb0db-135">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




