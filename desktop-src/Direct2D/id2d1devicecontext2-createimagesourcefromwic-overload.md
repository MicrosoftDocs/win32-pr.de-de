---
title: ID2D1DeviceContext2 | ateimagesourcefromwic-Methoden (D2d1 \_ 3. h)
description: Erstellt ein Bild Quell Objekt aus einer WIC-Bitmapquelle und füllt dabei den gesamten Pixel Speicher innerhalb der Bildquelle auf. Das Bild wird bei minimaler Speichermenge geladen und gespeichert.
ms.assetid: af02630d-a9ca-f5b4-6f2a-31a73ef603e5
keywords:
- Methoden von "kreateimagesourcefromwic" Direct2D
topic_type:
- apiref
api_location:
- d2d1_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 20773912886840a185e1b9fc71576f89e9a40fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362134"
---
# <a name="id2d1devicecontext2createimagesourcefromwic-methods"></a><span data-ttu-id="6ced8-105">ID2D1DeviceContext2:: kreateimagesourcefromwic-Methoden</span><span class="sxs-lookup"><span data-stu-id="6ced8-105">ID2D1DeviceContext2::CreateImageSourceFromWic methods</span></span>

<span data-ttu-id="6ced8-106">Erstellt ein Bild Quell Objekt aus einer WIC-Bitmapquelle und füllt dabei den gesamten Pixel Speicher innerhalb der Bildquelle auf.</span><span class="sxs-lookup"><span data-stu-id="6ced8-106">Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.</span></span> <span data-ttu-id="6ced8-107">Das Bild wird bei minimaler Speichermenge geladen und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6ced8-107">The image is loaded and stored while using a minimal amount of memory.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6ced8-108">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="6ced8-108">Overload list</span></span>



| <span data-ttu-id="6ced8-109">Methode</span><span class="sxs-lookup"><span data-stu-id="6ced8-109">Method</span></span>                                                                                                                                                                                       | <span data-ttu-id="6ced8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ced8-110">Description</span></span>                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ced8-111">[**"Kreateimagesourcefromwic" (IWICBitmapSource \* , D2D1 \_ \_ Laden Optionen für Bildquelle \_ \_ , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="6ced8-111">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span></span>                   | <span data-ttu-id="6ced8-112">Version der-Methode, mit der Sie die WIC-Bitmapquelle, das Ausgabe Bild Quell Objekt und die Lade Optionen mit dem standardalphamodus angeben können.</span><span class="sxs-lookup"><span data-stu-id="6ced8-112">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options with default alpha mode.</span></span><br/>   |
| <span data-ttu-id="6ced8-113">[**"Kreateimagesourcefromwic" (IWICBitmapSource \* , D2D1 \_ \_ Laden Optionen für Bildquelle \_ \_ , D2D1 \_ alpha \_ Modus, ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="6ced8-113">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, D2D1\_ALPHA\_MODE, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span></span> | <span data-ttu-id="6ced8-114">Version der-Methode, mit der Sie die WIC-Bitmapquelle, das Ausgabe Bild Quell Objekt und die Lade Optionen sowie den Alpha Modus angeben können.</span><span class="sxs-lookup"><span data-stu-id="6ced8-114">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options, and alpha mode.</span></span><br/>           |
| <span data-ttu-id="6ced8-115">[**"Kreateimagesourcefromwic" (IWICBitmapSource \* , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="6ced8-115">[**CreateImageSourceFromWic (IWICBitmapSource\*, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span></span>                                                          | <span data-ttu-id="6ced8-116">Version der-Methode, mit der Sie die WIC-Bitmapquelle und das Quell Objekt des Ausgabe Bilds mit den standardmäßigen Ladevorgängen und dem Alpha Modus angeben können.</span><span class="sxs-lookup"><span data-stu-id="6ced8-116">Version of the method that allows you to specify the WIC bitmap source and the output image source object with default loading opitons and alpha mode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6ced8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ced8-117">Requirements</span></span>



| <span data-ttu-id="6ced8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ced8-118">Requirement</span></span> | <span data-ttu-id="6ced8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6ced8-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6ced8-120">Header</span><span class="sxs-lookup"><span data-stu-id="6ced8-120">Header</span></span><br/> | <dl> <span data-ttu-id="6ced8-121"><dt>D2d1 \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ced8-121"><dt>D2d1\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ced8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ced8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ced8-123">**ID2D1DeviceContext2**</span><span class="sxs-lookup"><span data-stu-id="6ced8-123">**ID2D1DeviceContext2**</span></span>](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2)
</dt> </dl>

<span data-ttu-id="6ced8-124">�</span><span class="sxs-lookup"><span data-stu-id="6ced8-124">�</span></span>

<span data-ttu-id="6ced8-125">�</span><span class="sxs-lookup"><span data-stu-id="6ced8-125">�</span></span>
