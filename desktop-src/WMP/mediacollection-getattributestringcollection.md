---
title: Mediacollection. getAttributeStringCollection-Methode
description: Die getAttributeStringCollection-Methode ruft ein StringCollection-Objekt ab, das den Satz aller Werte für ein angegebenes Attribut innerhalb eines angegebenen Medientyps darstellt.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- getAttributeStringCollection-Methode, Windows Media Player
- getAttributeStringCollection-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getAttributeStringCollection-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352024"
---
# <a name="mediacollectiongetattributestringcollection-method"></a><span data-ttu-id="0faf7-106">Mediacollection. getAttributeStringCollection-Methode</span><span class="sxs-lookup"><span data-stu-id="0faf7-106">MediaCollection.getAttributeStringCollection method</span></span>

<span data-ttu-id="0faf7-107">Die **getAttributeStringCollection** -Methode ruft ein **StringCollection** -Objekt ab, das den Satz aller Werte für ein angegebenes Attribut innerhalb eines angegebenen Medientyps darstellt.</span><span class="sxs-lookup"><span data-stu-id="0faf7-107">The **getAttributeStringCollection** method retrieves a **StringCollection** object representing the set of all values for a specified attribute within a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0faf7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0faf7-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="0faf7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0faf7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0faf7-110">*Attribut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0faf7-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0faf7-111">**Zeichenfolge** , die das Attribut angibt.</span><span class="sxs-lookup"><span data-stu-id="0faf7-111">**String** specifying the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="0faf7-112">*mediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0faf7-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0faf7-113">**Zeichenfolge** , die den Medientyp darstellt.</span><span class="sxs-lookup"><span data-stu-id="0faf7-113">**String** representing the media type.</span></span> <span data-ttu-id="0faf7-114">Enthält einen der folgenden Werte: "Audiodatei", "Video", "Wiedergabeliste" oder "andere".</span><span class="sxs-lookup"><span data-stu-id="0faf7-114">Contains one of the following values: "Audio", "Video", "Playlist", or "Other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0faf7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0faf7-115">Return value</span></span>

<span data-ttu-id="0faf7-116">Diese Methode gibt ein **StringCollection** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0faf7-116">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0faf7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0faf7-117">Remarks</span></span>

<span data-ttu-id="0faf7-118">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0faf7-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="0faf7-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0faf7-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="0faf7-120">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie im Abschnitt [Attribut Verweis](attribute-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="0faf7-120">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md) section.</span></span>

## <a name="examples"></a><span data-ttu-id="0faf7-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0faf7-121">Examples</span></span>

<span data-ttu-id="0faf7-122">Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **getAttributeStringCollection** zum Anzeigen einer Liste von Werten, die einem bestimmten Attribut für Audioelemente in der Mediensammlung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0faf7-122">The following JScript example uses *MediaCollection*.**getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="0faf7-123">Ein HTML SELECT-Element, das mit ID = "Attribute" erstellt wurde, ermöglicht dem Benutzer die Auswahl eines Attributs, z. b. eines Künstlers, Genres oder Albums.</span><span class="sxs-lookup"><span data-stu-id="0faf7-123">An HTML SELECT element, created with ID = "Attribute", allows the user to select an attribute, such as Artist, Genre, or Album.</span></span> <span data-ttu-id="0faf7-124">Mit einem HTML-TEXTAREA-Element, das mit ID = "attributevals" erstellt wurde, wird das Ergebnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0faf7-124">An HTML TEXTAREA element, created with ID = "AttributeVals", displays the result.</span></span> <span data-ttu-id="0faf7-125">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0faf7-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="0faf7-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0faf7-126">Requirements</span></span>



| <span data-ttu-id="0faf7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0faf7-127">Requirement</span></span> | <span data-ttu-id="0faf7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0faf7-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0faf7-129">Version</span><span class="sxs-lookup"><span data-stu-id="0faf7-129">Version</span></span><br/> | <span data-ttu-id="0faf7-130">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0faf7-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0faf7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0faf7-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="0faf7-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0faf7-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0faf7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0faf7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0faf7-134">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="0faf7-134">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="0faf7-135">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="0faf7-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0faf7-136">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="0faf7-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0faf7-137">**StringCollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="0faf7-137">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





