---
title: Wiedergabeliste. itemmedia
description: Das itemmedia-Attribut ruft das Medienobjekt ab, das dem angegebenen Index im Wiedergabelisten Element entspricht.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- Wiedergabeliste. itemmedia Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360417"
---
# <a name="playlistitemmedia"></a><span data-ttu-id="f5949-104">Wiedergabeliste. itemmedia</span><span class="sxs-lookup"><span data-stu-id="f5949-104">PLAYLIST.itemMedia</span></span>

<span data-ttu-id="f5949-105">Das **itemmedia** -Attribut ruft das **Medien** Objekt ab, das dem angegebenen Index im **Wiedergabe** Listenelement entspricht.</span><span class="sxs-lookup"><span data-stu-id="f5949-105">The **itemMedia** attribute retrieves the **Media** object corresponding to the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a><span data-ttu-id="f5949-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f5949-106">Possible Values</span></span>

<span data-ttu-id="f5949-107">Dieses Attribut ist ein Schreib geschütztes **Medien** Objekt.</span><span class="sxs-lookup"><span data-stu-id="f5949-107">This attribute is a read-only **Media** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5949-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5949-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5949-109"><span id="index"></span><span id="INDEX"></span>*Sin*</span><span class="sxs-lookup"><span data-stu-id="f5949-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="f5949-110">**Zahl**(**Long**), die den Index eines Wiedergabelisten Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="f5949-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5949-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5949-111">Remarks</span></span>

<span data-ttu-id="f5949-112">Die **itemmedia** -Eigenschaft gibt Medienobjekte zurück, die im **Wiedergabe** Listenelement erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="f5949-112">The **itemMedia** property will return media objects that are expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="f5949-113">Wenn beispielsweise eine Wiedergabeliste mit drei Medienclips vorhanden ist, die nicht im **Wiedergabe** Listenelement erweitert werden, gibt **itemmedia**(0) die Wiedergabeliste als Medienobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f5949-113">For example, if there is a playlist that contains three media clips that is not expanded in the **PLAYLIST** element, **itemMedia**(0) will return the playlist as the media object.</span></span> <span data-ttu-id="f5949-114">Wenn die Wiedergabeliste erweitert ist, gibt **itemmedia**(0) den ersten Medien Clip in der Wiedergabeliste zurück.</span><span class="sxs-lookup"><span data-stu-id="f5949-114">If the playlist is expanded, **itemMedia**(0) will return the first media clip in the playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5949-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5949-115">Requirements</span></span>



| <span data-ttu-id="f5949-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5949-116">Requirement</span></span> | <span data-ttu-id="f5949-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f5949-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="f5949-118">Version</span><span class="sxs-lookup"><span data-stu-id="f5949-118">Version</span></span><br/> | <span data-ttu-id="f5949-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="f5949-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5949-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5949-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5949-121">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="f5949-121">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f5949-122">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="f5949-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





