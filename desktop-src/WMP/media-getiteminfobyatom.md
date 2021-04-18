---
title: Media. getiteminfobyatom-Methode
description: Die getiteminfobyatom-Methode ruft den Wert des Attributs mit der angegebenen Indexnummer ab.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- getiteminfobyatom-Methode, Windows Media Player
- getiteminfobyatom-Methode, Windows Media Player, Medienklasse
- Medienklasse, Windows Media Player, getiteminfobyatom-Methode
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372462"
---
# <a name="mediagetiteminfobyatom-method"></a><span data-ttu-id="0439a-106">Media. getiteminfobyatom-Methode</span><span class="sxs-lookup"><span data-stu-id="0439a-106">Media.getItemInfoByAtom method</span></span>

<span data-ttu-id="0439a-107">Die **getiteminfobyatom** -Methode ruft den Wert des Attributs mit der angegebenen Indexnummer ab.</span><span class="sxs-lookup"><span data-stu-id="0439a-107">The **getItemInfoByAtom** method retrieves the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="0439a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0439a-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="0439a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0439a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0439a-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0439a-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0439a-111">**Number** (**Long**), der den Index angibt, an dem sich ein bestimmtes Attribut innerhalb des Satzes verfügbarer Attribute befindet.</span><span class="sxs-lookup"><span data-stu-id="0439a-111">**Number** (**long**) specifying the index at which a given attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0439a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0439a-112">Return value</span></span>

<span data-ttu-id="0439a-113">Diese Methode gibt eine **Zeichenfolge** zurück, die den Wert des angegebenen Attributs darstellt.</span><span class="sxs-lookup"><span data-stu-id="0439a-113">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="0439a-114">Bei Attributen, deren zugrunde liegender Wert **boolescher** Wert ist, wird die Zeichenfolge "true" oder "false" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0439a-114">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="0439a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0439a-115">Remarks</span></span>

<span data-ttu-id="0439a-116">Diese Methode kann verwendet werden, um Metadaten für ein bestimmtes digitales Medien Element mithilfe einer Attribut Indexnummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0439a-116">This method can be used to retrieve metadata for a specific digital media item by using an attribute index number.</span></span> <span data-ttu-id="0439a-117">Die **AttributeCount** -Eigenschaft kann verwendet werden, um die Anzahl der für das Medien Element verfügbaren Attribute zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="0439a-117">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="0439a-118">Die **getmediaatom** -Methode des **mediacollection** -Objekts kann auch verwendet werden, um den Index eines bestimmten Attributs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0439a-118">The **getMediaAtom** method of the **MediaCollection** object can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="0439a-119">Diese Technik ist im Allgemeinen effizienter als die **getiteminfo** -Methode oder die **getItemInfoByType** -Methode bei der Arbeit mit großen Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="0439a-119">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="0439a-120">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0439a-120">To use this method, read access to the library is required.</span></span> <span data-ttu-id="0439a-121">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0439a-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="0439a-122">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="0439a-122">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="0439a-123">**Windows Media Player 10 Mobile:** Attribute für ein Medien Element sind nur während der Wiedergabe verfügbar, es sei denn, Sie werden über die Medien Auflistung aus dem Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0439a-123">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="0439a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0439a-124">Requirements</span></span>



| <span data-ttu-id="0439a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0439a-125">Requirement</span></span> | <span data-ttu-id="0439a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0439a-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0439a-127">Version</span><span class="sxs-lookup"><span data-stu-id="0439a-127">Version</span></span><br/> | <span data-ttu-id="0439a-128">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0439a-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0439a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0439a-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="0439a-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0439a-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0439a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0439a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0439a-132">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="0439a-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="0439a-133">**Media. AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="0439a-133">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="0439a-134">**Media. getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="0439a-134">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="0439a-135">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="0439a-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="0439a-136">**"Media. mentiteminfo"**</span><span class="sxs-lookup"><span data-stu-id="0439a-136">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="0439a-137">**Mediacollection. getmediaatom**</span><span class="sxs-lookup"><span data-stu-id="0439a-137">**MediaCollection.getMediaAtom**</span></span>](mediacollection-getmediaatom.md)
</dt> <dt>

[<span data-ttu-id="0439a-138">**Lesen von Attributwerten**</span><span class="sxs-lookup"><span data-stu-id="0439a-138">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="0439a-139">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="0439a-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0439a-140">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="0439a-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





