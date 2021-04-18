---
title: Display Artist-Attribut
description: Das displayartist-Attribut ist der Name des Künstlers, der für ein Element angezeigt wird.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- Display Artist-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368510"
---
# <a name="displayartist-attribute"></a><span data-ttu-id="872be-104">Display Artist-Attribut</span><span class="sxs-lookup"><span data-stu-id="872be-104">DisplayArtist Attribute</span></span>

<span data-ttu-id="872be-105">Das **displayartist** -Attribut ist der Name des Künstlers, der für ein Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="872be-105">The **DisplayArtist** attribute is the name of the artist that is displayed for an item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="872be-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="872be-106">Applies To</span></span>

-   [<span data-ttu-id="872be-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="872be-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="872be-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="872be-108">Remarks</span></span>

<span data-ttu-id="872be-109">Im Allgemeinen hat **displayartist** denselben Wert wie das **WM/Album-** Attribut, wenn dieses Attribut festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="872be-109">Generally, **DisplayArtist** will have the same value as the **WM/AlbumArtist** attribute when that attribute is set.</span></span> <span data-ttu-id="872be-110">Andernfalls ist der Wert der Name des Künstlers, der mit dem ersten Titel des Albums verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="872be-110">Otherwise, the value will be the name of the artist that is associated with the first track on the album.</span></span>

<span data-ttu-id="872be-111">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="872be-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="872be-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="872be-112">Requirements</span></span>



| <span data-ttu-id="872be-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="872be-113">Requirement</span></span> | <span data-ttu-id="872be-114">Wert</span><span class="sxs-lookup"><span data-stu-id="872be-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="872be-115">Version</span><span class="sxs-lookup"><span data-stu-id="872be-115">Version</span></span><br/> | <span data-ttu-id="872be-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="872be-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="872be-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="872be-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872be-118">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="872be-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="872be-119">**WM/albumartist-Attribut**</span><span class="sxs-lookup"><span data-stu-id="872be-119">**WM/AlbumArtist Attribute**</span></span>](wm-albumartist-attribute.md)
</dt> </dl>

 

 





