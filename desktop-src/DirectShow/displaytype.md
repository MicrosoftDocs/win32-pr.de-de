---
description: Die DisplayType-Funktion sendet Informationen über einen Medientyp an den debugausgabespeicherort. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: DisplayType-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3d83bbe7a24463fc4cfaed4ace3adec9d6fcf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364728"
---
# <a name="displaytype-function"></a><span data-ttu-id="d531c-104">DisplayType-Funktion</span><span class="sxs-lookup"><span data-stu-id="d531c-104">DisplayType function</span></span>

<span data-ttu-id="d531c-105">Die- `DisplayType` Funktion sendet Informationen über einen Medientyp an den debugausgabespeicherort.</span><span class="sxs-lookup"><span data-stu-id="d531c-105">The `DisplayType` function sends information about a media type to the debug output location.</span></span> <span data-ttu-id="d531c-106">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d531c-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="d531c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d531c-107">Syntax</span></span>


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="d531c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d531c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d531c-109">*label*</span><span class="sxs-lookup"><span data-stu-id="d531c-109">*label*</span></span> 
</dt> <dd>

<span data-ttu-id="d531c-110">Eine Zeichenfolge, die eine Meldung enthält, die mit den Medientyp Informationen angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d531c-110">String that contains a message to display with the media type information.</span></span>

</dd> <dt>

<span data-ttu-id="d531c-111">*pmtin*</span><span class="sxs-lookup"><span data-stu-id="d531c-111">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="d531c-112">unterliegt [**der Medientyp Struktur, die \_ \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) den Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="d531c-112">ointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d531c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d531c-113">Return value</span></span>

<span data-ttu-id="d531c-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d531c-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d531c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d531c-115">Remarks</span></span>

<span data-ttu-id="d531c-116">Diese Funktion generiert mehrere Protokoll-Ablauf \_ Verfolgungs Meldungen.</span><span class="sxs-lookup"><span data-stu-id="d531c-116">This function generates several LOG\_TRACE messages.</span></span> <span data-ttu-id="d531c-117">Bei der Protokollierung 2 oder höher zeigt die Funktion den Haupttyp, den Untertyp und den Formattyp sowie die Daten aus dem Format Block an.</span><span class="sxs-lookup"><span data-stu-id="d531c-117">At logging level 2 or higher, the function displays the major type, subtype, and format type, and data from the format block.</span></span> <span data-ttu-id="d531c-118">Bei der Protokollierung 5 oder höher zeigt die Funktion zusätzliche Informationen an, z. b. die Quell-und Ziel Rechtecke für Video Typen.</span><span class="sxs-lookup"><span data-stu-id="d531c-118">At logging level 5 or higher, the function displays additional information, such as the source and target rectangles for video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="d531c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d531c-119">Requirements</span></span>



| <span data-ttu-id="d531c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d531c-120">Requirement</span></span> | <span data-ttu-id="d531c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d531c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d531c-122">Header</span><span class="sxs-lookup"><span data-stu-id="d531c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d531c-123"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d531c-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d531c-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d531c-124">Library</span></span><br/> | <dl> <span data-ttu-id="d531c-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d531c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d531c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d531c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d531c-127">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="d531c-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




