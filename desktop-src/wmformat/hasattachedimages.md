---
title: Hasattachedimages
description: Das hasattachedimages-Attribut ist ein Attribut auf Dateiebene, das angibt, ob es sich bei der Datei um eine MP3-Datei mit angefügten apischen ID3-Frames handelt
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- Hasattachedimages Windows Media-Format
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339042"
---
# <a name="hasattachedimages"></a><span data-ttu-id="545d5-104">Hasattachedimages</span><span class="sxs-lookup"><span data-stu-id="545d5-104">HasAttachedImages</span></span>

<span data-ttu-id="545d5-105">Das **hasattachedimages** -Attribut ist ein Attribut auf Dateiebene, das angibt, ob es sich bei der Datei um eine MP3-Datei mit angefügten apischen ID3-Frames handelt</span><span class="sxs-lookup"><span data-stu-id="545d5-105">The **HasAttachedImages** attribute is a file-level attribute specifying whether the file is an MP3 file with attached APIC ID3 frames.</span></span>

## <a name="global-constant"></a><span data-ttu-id="545d5-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="545d5-106">Global Constant</span></span>

<span data-ttu-id="545d5-107">g \_ wszwmhasattachedimages</span><span class="sxs-lookup"><span data-stu-id="545d5-107">g\_wszWMHasAttachedImages</span></span>

## <a name="data-type"></a><span data-ttu-id="545d5-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="545d5-108">Data Type</span></span>

<span data-ttu-id="545d5-109">**WMT- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="545d5-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="545d5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="545d5-110">Remarks</span></span>

<span data-ttu-id="545d5-111">Dies ist ein codiertes Attribut.</span><span class="sxs-lookup"><span data-stu-id="545d5-111">This is a coded attribute.</span></span>

<span data-ttu-id="545d5-112">Dieses Attribut kann nicht auf Dateiebene dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="545d5-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="545d5-113">Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.</span><span class="sxs-lookup"><span data-stu-id="545d5-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="545d5-114">**Hasattachedimages** wurde entwickelt, um eine Anwendung darüber zu informieren, dass Bilder vorhanden waren, damit Sie mithilfe der [**iwmimageingefo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) -Schnittstelle abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="545d5-114">**HasAttachedImages** was designed to inform an application that images were present so that they could be retrieved using the [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) interface.</span></span> <span data-ttu-id="545d5-115">Da nun Images mit dem [**WM/Bild-**](wmpicture.md) Attribut unterstützt werden, wird **hasattachedimages** nicht mehr benötigt.</span><span class="sxs-lookup"><span data-stu-id="545d5-115">Now that images are supported using the [**WM/Picture**](wmpicture.md) attribute, **HasAttachedImages** is no longer needed.</span></span>

<span data-ttu-id="545d5-116">Um zu ermitteln, ob eine Datei Bilder enthält, können Sie [**IWMHeaderInfo3:: getattributeindices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) aufrufen, die das **WM/Bild-** Attribut angeben.</span><span class="sxs-lookup"><span data-stu-id="545d5-116">To determine whether a file contains images, call [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) specifying the **WM/Picture** attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="545d5-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="545d5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="545d5-118">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="545d5-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




