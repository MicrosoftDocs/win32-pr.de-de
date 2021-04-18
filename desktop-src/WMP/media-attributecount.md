---
title: Media. AttributeCount
description: Die AttributeCount-Eigenschaft ruft die Anzahl der Attribute ab, die abgefragt und/oder für das Medien Element festgelegt werden können.
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- Media. AttributeCount-Windows-Media Player
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4979f670cdd6a79b1b309bc3eceff5a2798223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368691"
---
# <a name="mediaattributecount"></a><span data-ttu-id="97c49-104">Media. AttributeCount</span><span class="sxs-lookup"><span data-stu-id="97c49-104">Media.attributeCount</span></span>

<span data-ttu-id="97c49-105">Die **AttributeCount** -Eigenschaft ruft die Anzahl der Attribute ab, die abgefragt und/oder für das Medien Element festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="97c49-105">The **attributeCount** property retrieves the number of attributes that can be queried and/or set for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c49-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="97c49-106">Syntax</span></span>

<span data-ttu-id="97c49-107">*Player*. *currentMedia*. **AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="97c49-107">*player*.*currentMedia*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="97c49-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="97c49-108">Possible Values</span></span>

<span data-ttu-id="97c49-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="97c49-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="97c49-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97c49-110">Remarks</span></span>

<span data-ttu-id="97c49-111">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="97c49-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="97c49-112">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="97c49-112">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="97c49-113">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="97c49-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="97c49-114">**Windows Media Player 10 Mobile:** Attribute für ein Medien Element sind nur während der Wiedergabe verfügbar, es sei denn, Sie werden über die Medien Auflistung aus dem Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="97c49-114">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="97c49-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97c49-115">Examples</span></span>

<span data-ttu-id="97c49-116">Im folgenden JScript-Beispiel werden *Medien* verwendet. **AttributeCount** , um die Anzahl der Attribute zu bestimmen, die im aktuellen Medien Element verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="97c49-116">The following JScript example uses *Media*.**attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="97c49-117">Der Code verwendet diesen Wert, um eine Liste der Attributnamen und-Werte in einem HTML-Textbereich mit dem Namen MyText auszugeben.</span><span class="sxs-lookup"><span data-stu-id="97c49-117">The code uses that value to print a list of attribute names and values in an HTML text area, named myText.</span></span> <span data-ttu-id="97c49-118">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="97c49-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="97c49-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97c49-119">Requirements</span></span>



| <span data-ttu-id="97c49-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97c49-120">Requirement</span></span> | <span data-ttu-id="97c49-121">Wert</span><span class="sxs-lookup"><span data-stu-id="97c49-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97c49-122">Version</span><span class="sxs-lookup"><span data-stu-id="97c49-122">Version</span></span><br/> | <span data-ttu-id="97c49-123">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="97c49-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="97c49-124">DLL</span><span class="sxs-lookup"><span data-stu-id="97c49-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="97c49-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97c49-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97c49-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97c49-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c49-127">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="97c49-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="97c49-128">**Media. GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="97c49-128">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="97c49-129">**Media. getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="97c49-129">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="97c49-130">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="97c49-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="97c49-131">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="97c49-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





