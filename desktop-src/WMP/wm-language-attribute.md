---
title: WM/Language-Attribut
description: Das WM/Language-Attribut ist die Sprache des Elements.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- WM/sprach Attribut Fenster Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359320"
---
# <a name="wmlanguage-attribute"></a><span data-ttu-id="42827-104">WM/Language-Attribut</span><span class="sxs-lookup"><span data-stu-id="42827-104">WM/Language Attribute</span></span>

<span data-ttu-id="42827-105">Das **WM/Language-** Attribut ist die Sprache des Elements.</span><span class="sxs-lookup"><span data-stu-id="42827-105">The **WM/Language** attribute is the language of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="42827-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="42827-106">Applies To</span></span>

-   [<span data-ttu-id="42827-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="42827-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="42827-108">Häufig verwendete Windows Media-Dateiattribute</span><span class="sxs-lookup"><span data-stu-id="42827-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="42827-109">Options Felder</span><span class="sxs-lookup"><span data-stu-id="42827-109">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="42827-110">Video Elemente</span><span class="sxs-lookup"><span data-stu-id="42827-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="42827-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42827-111">Remarks</span></span>

<span data-ttu-id="42827-112">Dieses Attribut ist sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="42827-112">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="42827-113">Dieses Attribut kann mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="42827-113">This attribute may have multiple values.</span></span> <span data-ttu-id="42827-114">Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die Media. **getItemInfoByType** -Methode und nicht die **Media. getiteminfo** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="42827-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="42827-115">**Language** ist ein Alias für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="42827-115">**Language** is an alias for this attribute.</span></span>

<span data-ttu-id="42827-116">Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmlanguage.</span><span class="sxs-lookup"><span data-stu-id="42827-116">The Windows Media Format SDK constant for this attribute is g\_wszWMLanguage.</span></span>

<span data-ttu-id="42827-117">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="42827-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="42827-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42827-118">Requirements</span></span>



| <span data-ttu-id="42827-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42827-119">Requirement</span></span> | <span data-ttu-id="42827-120">Wert</span><span class="sxs-lookup"><span data-stu-id="42827-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42827-121">Version</span><span class="sxs-lookup"><span data-stu-id="42827-121">Version</span></span><br/> | <span data-ttu-id="42827-122">Windows Media Player 9-Serie oder höher (das Optionsfeld wird nur in Windows Media Player 9-Serie unterstützt)</span><span class="sxs-lookup"><span data-stu-id="42827-122">Windows Media Player 9 Series or later (The radio item is supported only in Windows Media Player 9 Series)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42827-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42827-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42827-124">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="42827-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="42827-125">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="42827-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





