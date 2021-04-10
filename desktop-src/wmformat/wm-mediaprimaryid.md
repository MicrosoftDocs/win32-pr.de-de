---
title: WM/mediaclassprimaryid
description: Das WM/mediaclassprimaryid-Attribut enthält die GUID der primären Medienklasse.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- WM/mediaclassprimaryid Windows Media-Format
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857579"
---
# <a name="wmmediaclassprimaryid"></a><span data-ttu-id="c8962-104">WM/mediaclassprimaryid</span><span class="sxs-lookup"><span data-stu-id="c8962-104">WM/MediaClassPrimaryID</span></span>

<span data-ttu-id="c8962-105">Das **WM/mediaclassprimaryid-** Attribut enthält die GUID der primären Medienklasse.</span><span class="sxs-lookup"><span data-stu-id="c8962-105">The **WM/MediaClassPrimaryID** attribute contains the GUID of the primary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c8962-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="c8962-106">Global Constant</span></span>

<span data-ttu-id="c8962-107">g \_ wszwmmediaclassprimaryid</span><span class="sxs-lookup"><span data-stu-id="c8962-107">g\_wszWMMediaClassPrimaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="c8962-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c8962-108">Data Type</span></span>

<span data-ttu-id="c8962-109">**WMT- \_ Typ- \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="c8962-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="c8962-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8962-110">Remarks</span></span>

<span data-ttu-id="c8962-111">Dieses Attribut sollte auf einen der Werte in der folgenden Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c8962-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="c8962-112">GUID der primär Klasse</span><span class="sxs-lookup"><span data-stu-id="c8962-112">Primary class GUID</span></span>                     | <span data-ttu-id="c8962-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8962-113">Description</span></span>                                                  |
|----------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c8962-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span><span class="sxs-lookup"><span data-stu-id="c8962-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span></span> | <span data-ttu-id="c8962-115">Verwenden Sie für Musikdateien.</span><span class="sxs-lookup"><span data-stu-id="c8962-115">Use for music files.</span></span> <span data-ttu-id="c8962-116">Nicht für Audiodaten verwenden, die kein Musik ist.</span><span class="sxs-lookup"><span data-stu-id="c8962-116">Do not use for audio that is not music.</span></span> |
| <span data-ttu-id="c8962-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span><span class="sxs-lookup"><span data-stu-id="c8962-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span></span> | <span data-ttu-id="c8962-118">Verwenden Sie für Videodateien.</span><span class="sxs-lookup"><span data-stu-id="c8962-118">Use for video files.</span></span>                                         |
| <span data-ttu-id="c8962-119">"01cd0f 29-da4e-4157-897b-6275d50c4f"</span><span class="sxs-lookup"><span data-stu-id="c8962-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span></span> | <span data-ttu-id="c8962-120">Verwenden Sie dies für Audiodateien, die keine Musik sind.</span><span class="sxs-lookup"><span data-stu-id="c8962-120">Use for audio files that are not music.</span></span>                      |
| <span data-ttu-id="c8962-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span><span class="sxs-lookup"><span data-stu-id="c8962-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span></span> | <span data-ttu-id="c8962-122">Verwenden Sie für Dateien, die weder Audiodaten noch Videos sind.</span><span class="sxs-lookup"><span data-stu-id="c8962-122">Use for files that are neither audio or video.</span></span>               |



 

<span data-ttu-id="c8962-123">Wenn Sie einen Bezeichner der primären Klasse angeben, sollten Sie auch einen sekundären Klassen Bezeichner festlegen, um den Typ des Inhalts in der Datei zu verdeutlichen.</span><span class="sxs-lookup"><span data-stu-id="c8962-123">When you specify a primary class identifier, you should also set a secondary class identifier to clarify the type of content in the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8962-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8962-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8962-125">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="c8962-125">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="c8962-126">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="c8962-126">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
</dt> </dl>

 

 




