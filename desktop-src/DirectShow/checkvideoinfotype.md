---
description: Die checkvideoinfotype-Funktion überprüft einen Medientyp, der eine videoinfoheader-Format Struktur enthält, für bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: Checkvideoinfotype-Funktion (checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 7c3a3c9603f974458ed3012dc651815abd432645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371624"
---
# <a name="checkvideoinfotype-function"></a><span data-ttu-id="3a80e-103">Checkvideoinfotype-Funktion</span><span class="sxs-lookup"><span data-stu-id="3a80e-103">CheckVideoInfoType function</span></span>

<span data-ttu-id="3a80e-104">Die- `CheckVideoInfoType` Funktion überprüft einen Medientyp, der eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Format Struktur für bestimmte häufige Fehler enthält, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.</span><span class="sxs-lookup"><span data-stu-id="3a80e-104">The `CheckVideoInfoType` function checks a media type that contains a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="3a80e-105">Diese Funktion garantiert nicht, dass der Medientyp gültig ist oder dass der Code, der die Struktur verwendet, sicher ist.</span><span class="sxs-lookup"><span data-stu-id="3a80e-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3a80e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a80e-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="3a80e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a80e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a80e-108">*PMT*</span><span class="sxs-lookup"><span data-stu-id="3a80e-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="3a80e-109">Zeiger auf die zu validierende [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.</span><span class="sxs-lookup"><span data-stu-id="3a80e-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a80e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a80e-110">Return value</span></span>

<span data-ttu-id="3a80e-111">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3a80e-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="3a80e-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3a80e-112">Return code</span></span>                                                                                                | <span data-ttu-id="3a80e-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a80e-113">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="3a80e-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a80e-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="3a80e-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3a80e-115">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="3a80e-116"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3a80e-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="3a80e-117">**Null** -Zeiger Wert.</span><span class="sxs-lookup"><span data-stu-id="3a80e-117">**NULL** pointer value.</span></span><br/> |
| <dl> <span data-ttu-id="3a80e-118"><dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt></span><span class="sxs-lookup"><span data-stu-id="3a80e-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="3a80e-119">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="3a80e-119">Invalid media type.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="3a80e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a80e-120">Remarks</span></span>

<span data-ttu-id="3a80e-121">Diese Funktion ruft [**validatebitmapinfoheader**](validatebitmapinfoheader.md) auf, um die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur im Medientyp zu validieren.</span><span class="sxs-lookup"><span data-stu-id="3a80e-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="3a80e-122">Wenn der Formattyp nicht Format \_ videoinfo ist, gibt die Funktion den VFW \_ E- \_ Typ \_ nicht \_ akzeptiert zurück.</span><span class="sxs-lookup"><span data-stu-id="3a80e-122">If the format type is not FORMAT\_VideoInfo, the function returns VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a80e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a80e-123">Requirements</span></span>



| <span data-ttu-id="3a80e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a80e-124">Requirement</span></span> | <span data-ttu-id="3a80e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3a80e-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a80e-126">Header</span><span class="sxs-lookup"><span data-stu-id="3a80e-126">Header</span></span><br/> | <dl> <span data-ttu-id="3a80e-127"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a80e-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a80e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a80e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a80e-129">Video-und Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="3a80e-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




