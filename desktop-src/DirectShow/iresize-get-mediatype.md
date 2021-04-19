---
description: Die "get \_ MediaType"-Methode gibt den aktuellen Ausgabe Medientyp des resizerfilterfilters zurück.
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: 'Iresize:: get_MediaType-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b03bad7f8686fd580f7dd5fc347c347ade1c1c97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370317"
---
# <a name="iresizeget_mediatype-method"></a><span data-ttu-id="9080e-103">Iresize:: get \_ mediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="9080e-103">IResize::get\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="9080e-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9080e-104">\[Deprecated.</span></span> <span data-ttu-id="9080e-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="9080e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9080e-106">Die `get_MediaType` -Methode gibt den aktuellen Ausgabe Medientyp des resizerfilterfilters zurück.</span><span class="sxs-lookup"><span data-stu-id="9080e-106">The `get_MediaType` method returns the resizer filter's current output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9080e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9080e-107">Syntax</span></span>


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="9080e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9080e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9080e-109">*PMT* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9080e-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9080e-110">Zeiger auf eine vom Aufrufer zugeordnete Objekt- [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9080e-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span> <span data-ttu-id="9080e-111">Die-Methode füllt diese-Struktur mit dem Medientyp.</span><span class="sxs-lookup"><span data-stu-id="9080e-111">The method fills this structure with the media type.</span></span> <span data-ttu-id="9080e-112">Der Aufrufer muss ggf. den Format Block freigeben.</span><span class="sxs-lookup"><span data-stu-id="9080e-112">The caller must release the format block, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9080e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9080e-113">Return value</span></span>

<span data-ttu-id="9080e-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9080e-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9080e-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9080e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9080e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9080e-116">Remarks</span></span>

<span data-ttu-id="9080e-117">Wenn der Ausgabe Medientyp nicht festgelegt wurde, wird ein Standard Medientyp zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9080e-117">If the output media type has not been set, return a default media type.</span></span> <span data-ttu-id="9080e-118">Der Filter muss seinen Ausgabe Medientyp aktualisieren, wenn die Methoden **Put \_ mediaType** oder **Put \_ size** aufgerufen werden. der von zurückgegebene Medientyp `get_MediaType` muss diese Änderungen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="9080e-118">The filter must update its output media type when the **put\_MediaType** or **put\_Size** methods are called; the media type returned by `get_MediaType` must reflect these changes.</span></span>

> [!Note]  
> <span data-ttu-id="9080e-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9080e-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9080e-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="9080e-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9080e-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9080e-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9080e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9080e-122">Requirements</span></span>



| <span data-ttu-id="9080e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9080e-123">Requirement</span></span> | <span data-ttu-id="9080e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9080e-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9080e-125">Version</span><span class="sxs-lookup"><span data-stu-id="9080e-125">Version</span></span><br/> | <span data-ttu-id="9080e-126">DirectX 9,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9080e-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="9080e-127">Header</span><span class="sxs-lookup"><span data-stu-id="9080e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9080e-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9080e-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9080e-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9080e-129">Library</span></span><br/> | <dl> <span data-ttu-id="9080e-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="9080e-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9080e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9080e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9080e-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="9080e-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="9080e-133">**Iresize-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9080e-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




