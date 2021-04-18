---
description: Die getmediatype-Methode ruft den unkomprimierten Medientyp für die Gruppe ab.
ms.assetid: 129ed688-0f03-4ccb-b65f-d61f02cb94b2
title: 'Iamtimelinegroup:: getmediatype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2122b5429ffa66d278ccfe59553ac85fb0dee562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365840"
---
# <a name="iamtimelinegroupgetmediatype-method"></a><span data-ttu-id="ccadc-103">Iamtimelinegroup:: getmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="ccadc-103">IAMTimelineGroup::GetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="ccadc-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ccadc-104">\[Deprecated.</span></span> <span data-ttu-id="ccadc-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ccadc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ccadc-106">Die- `GetMediaType` Methode ruft den unkomprimierten Medientyp für die Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ccadc-106">The `GetMediaType` method retrieves the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccadc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccadc-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="ccadc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccadc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccadc-109">*PMT* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ccadc-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccadc-110">Zeiger auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die mit dem Medientyp gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ccadc-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccadc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ccadc-111">Return value</span></span>

<span data-ttu-id="ccadc-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ccadc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ccadc-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ccadc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccadc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccadc-114">Remarks</span></span>

<span data-ttu-id="ccadc-115">Der Aufrufer muss den Format Block des zurückgegebenen Medientyps freigeben, der im **pbformat** -Member der zurückgegebenen \_ \_ Medientyp-Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ccadc-115">The caller must free the returned media type's format block, given in the **pbFormat** member of the returned AM\_MEDIA\_TYPE structure.</span></span> <span data-ttu-id="ccadc-116">Sie können die Hilfsfunktion " [**fremediatype**](freemediatype.md) " aus der Basisklassen Bibliothek verwenden.</span><span class="sxs-lookup"><span data-stu-id="ccadc-116">You can use the helper function [**FreeMediaType**](freemediatype.md) from the base class library.</span></span>

> [!Note]  
> <span data-ttu-id="ccadc-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ccadc-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ccadc-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ccadc-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ccadc-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ccadc-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ccadc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccadc-120">Requirements</span></span>



| <span data-ttu-id="ccadc-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccadc-121">Requirement</span></span> | <span data-ttu-id="ccadc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ccadc-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccadc-123">Header</span><span class="sxs-lookup"><span data-stu-id="ccadc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ccadc-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ccadc-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ccadc-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ccadc-125">Library</span></span><br/> | <dl> <span data-ttu-id="ccadc-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="ccadc-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccadc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccadc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccadc-128">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ccadc-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="ccadc-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="ccadc-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




