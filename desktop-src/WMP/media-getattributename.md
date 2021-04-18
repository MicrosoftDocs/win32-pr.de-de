---
title: Media. GetAttributeName-Methode
description: Die GetAttributeName-Methode ruft den Namen des Attributs ab, das dem angegebenen Index entspricht.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- GetAttributeName-Methode, Windows-Media Player
- GetAttributeName-Methode, Windows Media Player, Medienklasse
- Medienklasse Windows Media Player, GetAttributeName-Methode
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7134b68837a7a5d1b765c64320ae68c56c6fc56
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357591"
---
# <a name="mediagetattributename-method"></a><span data-ttu-id="be3b2-106">Media. GetAttributeName-Methode</span><span class="sxs-lookup"><span data-stu-id="be3b2-106">Media.getAttributeName method</span></span>

<span data-ttu-id="be3b2-107">Die **GetAttributeName** -Methode ruft den Namen des Attributs ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="be3b2-107">The **getAttributeName** method retrieves the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="be3b2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="be3b2-108">Syntax</span></span>


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="be3b2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="be3b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be3b2-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be3b2-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be3b2-111">Die **Zahl** (**Long**), die den Index des Attributs enthält.</span><span class="sxs-lookup"><span data-stu-id="be3b2-111">**Number** (**long**) containing the index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be3b2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be3b2-112">Return value</span></span>

<span data-ttu-id="be3b2-113">Diese Methode gibt eine **Zeichenfolge** zurück, die den Namen des Attributs angibt.</span><span class="sxs-lookup"><span data-stu-id="be3b2-113">This method returns a **String** specifying the name of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="be3b2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be3b2-114">Remarks</span></span>

<span data-ttu-id="be3b2-115">Der zurückgegebene Attribut Name kann in Verbindung mit **getiteminfo** verwendet werden, um den Wert für ein bestimmtes benanntes Attribut abzurufen.</span><span class="sxs-lookup"><span data-stu-id="be3b2-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="be3b2-116">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="be3b2-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="be3b2-117">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="be3b2-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="be3b2-118">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="be3b2-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="be3b2-119">**Windows Media Player 10 Mobile:** Attribute für ein Medien Element sind nur während der Wiedergabe verfügbar, es sei denn, Sie werden über die Medien Auflistung aus dem Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="be3b2-119">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="be3b2-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be3b2-120">Examples</span></span>

<span data-ttu-id="be3b2-121">Im folgenden JScript-Beispiel werden *Medien* verwendet. **GetAttributeName** zum Ausfüllen eines HTML-Text Bereichs namens MyText mit dem Index und dem Namen der einzelnen Attribute für das aktuelle Medien Element.</span><span class="sxs-lookup"><span data-stu-id="be3b2-121">The following JScript example uses *Media*.**getAttributeName** to fill an HTML text area named myText with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="be3b2-122">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="be3b2-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="be3b2-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be3b2-123">Requirements</span></span>



| <span data-ttu-id="be3b2-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be3b2-124">Requirement</span></span> | <span data-ttu-id="be3b2-125">Wert</span><span class="sxs-lookup"><span data-stu-id="be3b2-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be3b2-126">Version</span><span class="sxs-lookup"><span data-stu-id="be3b2-126">Version</span></span><br/> | <span data-ttu-id="be3b2-127">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="be3b2-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="be3b2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="be3b2-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="be3b2-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be3b2-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be3b2-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be3b2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be3b2-131">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="be3b2-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="be3b2-132">**Media. AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="be3b2-132">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="be3b2-133">**Media. getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="be3b2-133">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="be3b2-134">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="be3b2-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="be3b2-135">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="be3b2-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





