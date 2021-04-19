---
description: Die folgenden Untertypen werden von Decodern verwendet, die DirectX Video Acceleration (DXVA) verwenden.
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Video-Untertypen der DirectX-Videobeschleunigung (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361935"
---
# <a name="directx-video-acceleration-video-subtypes"></a><span data-ttu-id="f18b4-103">Video-Untertypen der DirectX-Videobeschleunigung</span><span class="sxs-lookup"><span data-stu-id="f18b4-103">DirectX Video Acceleration Video Subtypes</span></span>

<span data-ttu-id="f18b4-104">Die folgenden Untertypen werden von Decodern verwendet, die DirectX Video Acceleration (DXVA) verwenden.</span><span class="sxs-lookup"><span data-stu-id="f18b4-104">The following subtypes are used by decoders that are using DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="f18b4-105">AI44 und IA44 sind Flächen mit einem Bits-pro-Pixel-Wert von 8.</span><span class="sxs-lookup"><span data-stu-id="f18b4-105">AI44 and IA44 are surfaces with a bits-per-pixel value of 8.</span></span> <span data-ttu-id="f18b4-106">Es gibt vier *Bits von I* und 4 Bits von. *Ich Stelle* einen Index in einer 16-Eintrag-YUV-Palette dar.</span><span class="sxs-lookup"><span data-stu-id="f18b4-106">There are 4 bits of I and 4 bits of *A*. *I* represents an index into a 16-entry YUV palette.</span></span> <span data-ttu-id="f18b4-107">*Ein* stellt vier Bits von Transparenz Informationen dar (auch als pro Pixel-Alpha bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="f18b4-107">*A* represents 4 bits of transparency information (also known as per-pixel-alpha).</span></span> <span data-ttu-id="f18b4-108">Daher ermöglichen AI44-und IA44-Oberflächen 16 verschiedene Farben bei 16 verschiedenen Transparenz Werten oder 256 verschiedene Pixel Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="f18b4-108">Therefore, AI44 and IA44 surfaces allow for 16 different colors at 16 different transparency values, or 256 different pixel representations.</span></span> <span data-ttu-id="f18b4-109">Mit AI44 wird das Alpha in "Hi-Nibble" gespeichert, in IA44 wird das Alpha in "Lo-Nibble" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f18b4-109">With AI44 the alpha is stored in the hi-nibble, in IA44 the alpha is stored in the lo-nibble.</span></span> <span data-ttu-id="f18b4-110">Beide Formate sind für DVD-unter Bild Bilder und Line21-und Teletext-Bilder sehr nützlich.</span><span class="sxs-lookup"><span data-stu-id="f18b4-110">Both formats are very useful for DVD sub-picture images and Line21 and Teletext images.</span></span> <span data-ttu-id="f18b4-111">Microsoft bevorzugt die AI44-Version, da es etwas einfacher ist, Text mit diesem Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="f18b4-111">Microsoft prefers the AI44 version because it is slightly easier to generate text using this format.</span></span>

| <span data-ttu-id="f18b4-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="f18b4-112">Subtype</span></span>            | <span data-ttu-id="f18b4-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f18b4-113">Description</span></span>                                                 |
|--------------------|-------------------------------------------------------------|
| <span data-ttu-id="f18b4-114">Mediasubtype \_ AI44</span><span class="sxs-lookup"><span data-stu-id="f18b4-114">MEDIASUBTYPE\_AI44</span></span> | <span data-ttu-id="f18b4-115">Für untergeordnete Bild-und Text Überlagerungen.</span><span class="sxs-lookup"><span data-stu-id="f18b4-115">For subpicture and text overlays.</span></span> <span data-ttu-id="f18b4-116">Siehe vorherige Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="f18b4-116">See previous description.</span></span> |
| <span data-ttu-id="f18b4-117">Mediasubtype \_ IA44</span><span class="sxs-lookup"><span data-stu-id="f18b4-117">MEDIASUBTYPE\_IA44</span></span> | <span data-ttu-id="f18b4-118">Für untergeordnete Bild-und Text Überlagerungen.</span><span class="sxs-lookup"><span data-stu-id="f18b4-118">For subpicture and text overlays.</span></span> <span data-ttu-id="f18b4-119">Siehe vorherige Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="f18b4-119">See previous description.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f18b4-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f18b4-120">Requirements</span></span>



| <span data-ttu-id="f18b4-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f18b4-121">Requirement</span></span> | <span data-ttu-id="f18b4-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f18b4-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f18b4-123">Header</span><span class="sxs-lookup"><span data-stu-id="f18b4-123">Header</span></span><br/> | <dl> <span data-ttu-id="f18b4-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="f18b4-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f18b4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f18b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18b4-126">Video Untertypen</span><span class="sxs-lookup"><span data-stu-id="f18b4-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




