---
title: Mediacollection. getbyattribute-Methode
description: Die getbyattribute-Methode ruft eine Wiedergabeliste von Medien Elementen ab, die einen angegebenen Wert für ein angegebenes Attribut enthalten.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- getbyattribute-Methode, Windows-Media Player
- getbyattribute-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getbyattribute-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533823127364416f8f4492c82381e682173c5c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370226"
---
# <a name="mediacollectiongetbyattribute-method"></a><span data-ttu-id="c1e4d-106">Mediacollection. getbyattribute-Methode</span><span class="sxs-lookup"><span data-stu-id="c1e4d-106">MediaCollection.getByAttribute method</span></span>

<span data-ttu-id="c1e4d-107">Die **getbyattribute** -Methode ruft eine Wiedergabeliste von Medien Elementen ab, die einen angegebenen Wert für ein angegebenes Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-107">The **getByAttribute** method retrieves a playlist of media items that contain a specified value for a specified attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e4d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1e4d-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="c1e4d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1e4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e4d-110">*Attribut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1e4d-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e4d-111">**Zeichenfolge** , die den Namen des zu durchsuchenden Attributs angibt.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-111">**String** indicating the name of the attribute to search.</span></span> <span data-ttu-id="c1e4d-112">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1e4d-113">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1e4d-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e4d-114">Eine **Zeichenfolge** , die den Wert angibt, den das Attribut aufweisen sollte.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-114">**String** indicating the value that the attribute should have.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e4d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1e4d-115">Return value</span></span>

<span data-ttu-id="c1e4d-116">Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-116">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e4d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1e4d-117">Remarks</span></span>

<span data-ttu-id="c1e4d-118">Diese Methode kann verwendet werden, um eine generische Abfrage für Medienelemente zu erstellen, die einem Wert für ein Attribut in der Datenbank entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-118">This method can be used to create a generic query for media items that match a value for an attribute in the database.</span></span> <span data-ttu-id="c1e4d-119">Dies ist nützlich für benutzerdefinierte Attribute.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-119">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="c1e4d-120">Wenn das Attribut nicht vorhanden ist, führt dies zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-120">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="c1e4d-121">Mit dieser Methode können Sie alle Medienelemente eines bestimmten Typs abrufen.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-121">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="c1e4d-122">Verwenden Sie den Attributnamen "MediaType" und einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="c1e4d-122">Use the attribute name "MediaType" and one of the following values:</span></span>



| <span data-ttu-id="c1e4d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e4d-123">Value</span></span>    | <span data-ttu-id="c1e4d-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1e4d-124">Description</span></span>                                                |
|----------|------------------------------------------------------------|
| <span data-ttu-id="c1e4d-125">Audio</span><span class="sxs-lookup"><span data-stu-id="c1e4d-125">audio</span></span>    | <span data-ttu-id="c1e4d-126">Musik und andere reine Audioelemente.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-126">Music and other audio-only items.</span></span>                          |
| <span data-ttu-id="c1e4d-127">Abspielen</span><span class="sxs-lookup"><span data-stu-id="c1e4d-127">playlist</span></span> | <span data-ttu-id="c1e4d-128">Wiedergabelisten, die als **Medien** Objekte dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-128">Playlists represented as **Media** objects.</span></span>                |
| <span data-ttu-id="c1e4d-129">radio</span><span class="sxs-lookup"><span data-stu-id="c1e4d-129">radio</span></span>    | <span data-ttu-id="c1e4d-130">Radio Station-Elemente.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-130">Radio station items.</span></span> <span data-ttu-id="c1e4d-131">Wird nicht von Windows Media Player 10 verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-131">Not used by Windows Media Player 10.</span></span>  |
| <span data-ttu-id="c1e4d-132">video</span><span class="sxs-lookup"><span data-stu-id="c1e4d-132">video</span></span>    | <span data-ttu-id="c1e4d-133">Video Elemente.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-133">Video items.</span></span>                                               |
| <span data-ttu-id="c1e4d-134">Foto</span><span class="sxs-lookup"><span data-stu-id="c1e4d-134">photo</span></span>    | <span data-ttu-id="c1e4d-135">Foto Elemente.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-135">Photo items.</span></span> <span data-ttu-id="c1e4d-136">Erfordert Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-136">Requires Windows Media Player 10.</span></span>             |
| <span data-ttu-id="c1e4d-137">andere</span><span class="sxs-lookup"><span data-stu-id="c1e4d-137">other</span></span>    | <span data-ttu-id="c1e4d-138">Andere Elemente, wie z. b. ASF-Dateien oder URLs für Streaming-Medien.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-138">Other items, such as ASF files or URLs to streaming media.</span></span> |



 

<span data-ttu-id="c1e4d-139">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-139">To use this method, read access to the library is required.</span></span> <span data-ttu-id="c1e4d-140">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c1e4d-140">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c1e4d-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1e4d-141">Examples</span></span>

<span data-ttu-id="c1e4d-142">Im folgenden JScript-Beispiel wird *mediacollection* verwendet. " **getbyattribute** ", um den gesamten Inhalt der Bibliothek von der Künstlerin mit dem Namen "48 drei</span><span class="sxs-lookup"><span data-stu-id="c1e4d-142">The following JScript example uses *MediaCollection*.**getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="c1e4d-143">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-143">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="c1e4d-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1e4d-144">Requirements</span></span>



| <span data-ttu-id="c1e4d-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1e4d-145">Requirement</span></span> | <span data-ttu-id="c1e4d-146">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e4d-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e4d-147">Version</span><span class="sxs-lookup"><span data-stu-id="c1e4d-147">Version</span></span><br/> | <span data-ttu-id="c1e4d-148">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c1e4d-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c1e4d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="c1e4d-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="c1e4d-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1e4d-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e4d-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1e4d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e4d-152">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="c1e4d-152">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="c1e4d-153">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="c1e4d-153">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="c1e4d-154">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="c1e4d-154">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c1e4d-155">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="c1e4d-155">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





