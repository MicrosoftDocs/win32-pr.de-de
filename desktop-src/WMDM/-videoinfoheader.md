---
title: _VIDEOINFOHEADER Struktur
description: Die \_ videoinfoheader-Struktur enthält Informationen zu einem Videostream und enthält eine \_ BITMAPINFOHEADER-Struktur, die das Format eines einzelnen Frames definiert.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- _VIDEOINFOHEADER Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365892"
---
# <a name="_videoinfoheader-structure"></a><span data-ttu-id="baa20-104">\_Videoinfoheader-Struktur</span><span class="sxs-lookup"><span data-stu-id="baa20-104">\_VIDEOINFOHEADER structure</span></span>

<span data-ttu-id="baa20-105">Die **\_ videoinfoheader** -Struktur enthält Informationen zu einem Videostream und enthält eine **\_ BITMAPINFOHEADER** -Struktur, die das Format eines einzelnen Frames definiert.</span><span class="sxs-lookup"><span data-stu-id="baa20-105">The **\_VIDEOINFOHEADER** structure contains information about a video stream and includes a **\_BITMAPINFOHEADER** structure that defines the format of an individual frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="baa20-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="baa20-106">Syntax</span></span>


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="baa20-107">Member</span><span class="sxs-lookup"><span data-stu-id="baa20-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="baa20-108">**rcSource**</span><span class="sxs-lookup"><span data-stu-id="baa20-108">**rcSource**</span></span>
</dt> <dd>

<span data-ttu-id="baa20-109">**Rect** -Struktur, die das Quellvideo Fenster angibt.</span><span class="sxs-lookup"><span data-stu-id="baa20-109">**RECT** structure that specifies the source video window.</span></span>

</dd> <dt>

<span data-ttu-id="baa20-110">**rctarget**</span><span class="sxs-lookup"><span data-stu-id="baa20-110">**rcTarget**</span></span>
</dt> <dd>

<span data-ttu-id="baa20-111">**Rect** -Struktur, die das Ziel Videofenster angibt.</span><span class="sxs-lookup"><span data-stu-id="baa20-111">**RECT** structure that specifies the destination video window.</span></span>

</dd> <dt>

<span data-ttu-id="baa20-112">**dwbitrate**</span><span class="sxs-lookup"><span data-stu-id="baa20-112">**dwBitRate**</span></span>
</dt> <dd>

<span data-ttu-id="baa20-113">**DWORD** -Wert, der die ungefähre Datenrate des Videostreams in Bits pro Sekunde angibt.</span><span class="sxs-lookup"><span data-stu-id="baa20-113">**DWORD** value that specifies the video stream's approximate data rate, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="baa20-114">**dwbiterrorrate**</span><span class="sxs-lookup"><span data-stu-id="baa20-114">**dwBitErrorRate**</span></span>
</dt> <dd>

<span data-ttu-id="baa20-115">**DWORD** -Wert, der die Datenfehler Rate des Videostreams in Bitfehlern pro Sekunde angibt.</span><span class="sxs-lookup"><span data-stu-id="baa20-115">**DWORD** value that specifies the video stream's data error rate, in bit errors per second.</span></span>

</dd> <dt>

<span data-ttu-id="baa20-116">**Avgtimeperframe**</span><span class="sxs-lookup"><span data-stu-id="baa20-116">**AvgTimePerFrame**</span></span>
</dt> <dd>

<span data-ttu-id="baa20-117">**Verweis \_ Der Zeitwert** , der die durchschnittliche Anzeigezeit des Video Frames in 100-Nanosecond-Einheiten angibt.</span><span class="sxs-lookup"><span data-stu-id="baa20-117">**REFERENCE\_TIME** value that specifies the video frame's average display time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="baa20-118">**bmiheader**</span><span class="sxs-lookup"><span data-stu-id="baa20-118">**bmiHeader**</span></span>
</dt> <dd>

<span data-ttu-id="baa20-119">Win32- **\_ BITMAPINFOHEADER** -Struktur, die Farb-und Dimensions Informationen für die Video Bild-Bitmap enthält.</span><span class="sxs-lookup"><span data-stu-id="baa20-119">Win32 **\_BITMAPINFOHEADER** structure that contains color and dimension information for the video image bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="baa20-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="baa20-120">Requirements</span></span>



| <span data-ttu-id="baa20-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="baa20-121">Requirement</span></span> | <span data-ttu-id="baa20-122">Wert</span><span class="sxs-lookup"><span data-stu-id="baa20-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="baa20-123">Header</span><span class="sxs-lookup"><span data-stu-id="baa20-123">Header</span></span><br/> | <dl> <span data-ttu-id="baa20-124"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="baa20-124"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baa20-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baa20-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa20-126">**\_BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="baa20-126">**\_BITMAPINFOHEADER**</span></span>](-bitmapinfoheader.md)
</dt> <dt>

[<span data-ttu-id="baa20-127">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="baa20-127">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





