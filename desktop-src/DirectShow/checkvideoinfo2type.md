---
description: Die CheckVideoInfo2Type-Funktion überprüft einen Medientyp, der eine VIDEOINFOHEADER2-Format Struktur enthält, für bestimmte häufige Fehler, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: CheckVideoInfo2Type-Funktion (checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 5ec092bdea1e3dd00de36893d1816f70ca6d7945
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369136"
---
# <a name="checkvideoinfo2type-function"></a><span data-ttu-id="b041c-103">CheckVideoInfo2Type-Funktion</span><span class="sxs-lookup"><span data-stu-id="b041c-103">CheckVideoInfo2Type function</span></span>

<span data-ttu-id="b041c-104">Die- `CheckVideoInfo2Type` Funktion überprüft einen Medientyp, der eine [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format Struktur für bestimmte häufige Fehler enthält, die Pufferüberläufe oder ganzzahlige über Läufe verursachen können.</span><span class="sxs-lookup"><span data-stu-id="b041c-104">The `CheckVideoInfo2Type` function checks a media type that contains a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="b041c-105">Diese Funktion garantiert nicht, dass der Medientyp gültig ist oder dass der Code, der die Struktur verwendet, sicher ist.</span><span class="sxs-lookup"><span data-stu-id="b041c-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b041c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b041c-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="b041c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b041c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b041c-108">*PMT*</span><span class="sxs-lookup"><span data-stu-id="b041c-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b041c-109">Zeiger auf die zu validierende [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.</span><span class="sxs-lookup"><span data-stu-id="b041c-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b041c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b041c-110">Return value</span></span>

<span data-ttu-id="b041c-111">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="b041c-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="b041c-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b041c-112">Return code</span></span>                                                                                                | <span data-ttu-id="b041c-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b041c-113">Description</span></span>                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="b041c-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b041c-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="b041c-115">Erfolg</span><span class="sxs-lookup"><span data-stu-id="b041c-115">Success</span></span><br/>                |
| <dl> <span data-ttu-id="b041c-116"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="b041c-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="b041c-117">**Null** -Zeiger Wert</span><span class="sxs-lookup"><span data-stu-id="b041c-117">**NULL** pointer value</span></span><br/> |
| <dl> <span data-ttu-id="b041c-118"><dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt></span><span class="sxs-lookup"><span data-stu-id="b041c-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="b041c-119">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="b041c-119">Invalid media type</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="b041c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b041c-120">Remarks</span></span>

<span data-ttu-id="b041c-121">Diese Funktion ruft [**validatebitmapinfoheader**](validatebitmapinfoheader.md) auf, um die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur im Medientyp zu validieren.</span><span class="sxs-lookup"><span data-stu-id="b041c-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="b041c-122">Wenn der Formattyp nicht " **Format \_ VideoInfo2**" ist, gibt die Funktion " **VFW \_ E \_ Type \_ Not \_ Accepted**" zurück.</span><span class="sxs-lookup"><span data-stu-id="b041c-122">If the format type is not **FORMAT\_VideoInfo2**, the function returns **VFW\_E\_TYPE\_NOT\_ACCEPTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b041c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b041c-123">Requirements</span></span>



| <span data-ttu-id="b041c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b041c-124">Requirement</span></span> | <span data-ttu-id="b041c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b041c-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b041c-126">Header</span><span class="sxs-lookup"><span data-stu-id="b041c-126">Header</span></span><br/> | <dl> <span data-ttu-id="b041c-127"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b041c-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b041c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b041c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b041c-129">Video-und Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="b041c-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




