---
title: "' Iwmpmediacollection ' getbyattribute-Methode"
description: Die getbyattribute-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die dem angegebenen Attribut mit dem angegebenen Wert entspricht.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- getbyattribute-Methode, Windows-Media Player
- getbyattribute-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection-Schnittstelle, Windows Media Player, getbyattribute-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370856"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a><span data-ttu-id="f18f9-106">Iwmpmediacollection:: getbyattribute-Methode</span><span class="sxs-lookup"><span data-stu-id="f18f9-106">IWMPMediaCollection::getByAttribute method</span></span>

<span data-ttu-id="f18f9-107">Die **getbyattribute** -Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die dem angegebenen Attribut mit dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="f18f9-107">The **getByAttribute** method returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f18f9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f18f9-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a><span data-ttu-id="f18f9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f18f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f18f9-110">*bstrattribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f18f9-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f18f9-111">Die **System. String** -Eigenschaft, die das angegebene Attribut ist.</span><span class="sxs-lookup"><span data-stu-id="f18f9-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="f18f9-112">*bstrauvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f18f9-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f18f9-113">Die **System. String** , die den angegebenen Wert ist.</span><span class="sxs-lookup"><span data-stu-id="f18f9-113">The **System.String** that is the specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f18f9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f18f9-114">Return value</span></span>

<span data-ttu-id="f18f9-115">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufenen Medienelemente.</span><span class="sxs-lookup"><span data-stu-id="f18f9-115">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="f18f9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f18f9-116">Remarks</span></span>

<span data-ttu-id="f18f9-117">Diese Methode kann verwendet werden, um eine generische Abfrage für Medienelemente zu erstellen, die einem Wert für ein Attribut in der Bibliothek entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f18f9-117">This method can be used to create a generic query for media items that match a value for an attribute in the library.</span></span> <span data-ttu-id="f18f9-118">Dies ist nützlich für benutzerdefinierte Attribute.</span><span class="sxs-lookup"><span data-stu-id="f18f9-118">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="f18f9-119">Wenn das Attribut nicht vorhanden ist, führt dies zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="f18f9-119">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="f18f9-120">Mit dieser Methode können Sie alle Medienelemente eines bestimmten Typs abrufen.</span><span class="sxs-lookup"><span data-stu-id="f18f9-120">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="f18f9-121">Verwenden Sie den Attributnamen " **mediaType** " und einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="f18f9-121">Use the attribute name **MediaType** and one of the following values.</span></span>



| <span data-ttu-id="f18f9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f18f9-122">Value</span></span>    | <span data-ttu-id="f18f9-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f18f9-123">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="f18f9-124">Audio</span><span class="sxs-lookup"><span data-stu-id="f18f9-124">audio</span></span>    | <span data-ttu-id="f18f9-125">Musik und andere reine Audioelemente</span><span class="sxs-lookup"><span data-stu-id="f18f9-125">Music and other audio-only items</span></span>                          |
| <span data-ttu-id="f18f9-126">andere</span><span class="sxs-lookup"><span data-stu-id="f18f9-126">other</span></span>    | <span data-ttu-id="f18f9-127">Andere Elemente, wie z. b. eine. ASF-Datei oder die URL eines Streams.</span><span class="sxs-lookup"><span data-stu-id="f18f9-127">Other items, such as an .asf file or the URL of a stream.</span></span> |
| <span data-ttu-id="f18f9-128">Foto</span><span class="sxs-lookup"><span data-stu-id="f18f9-128">photo</span></span>    | <span data-ttu-id="f18f9-129">Foto Elemente.</span><span class="sxs-lookup"><span data-stu-id="f18f9-129">Photo items.</span></span> <span data-ttu-id="f18f9-130">Erfordert Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="f18f9-130">Requires Windows Media Player 10.</span></span>            |
| <span data-ttu-id="f18f9-131">Abspielen</span><span class="sxs-lookup"><span data-stu-id="f18f9-131">playlist</span></span> | <span data-ttu-id="f18f9-132">Wiedergabelisten, die als Medienelemente dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f18f9-132">Playlists represented as media items.</span></span>                     |
| <span data-ttu-id="f18f9-133">radio</span><span class="sxs-lookup"><span data-stu-id="f18f9-133">radio</span></span>    | <span data-ttu-id="f18f9-134">Radio Station-Elemente.</span><span class="sxs-lookup"><span data-stu-id="f18f9-134">Radio station items.</span></span> <span data-ttu-id="f18f9-135">Wird nicht von Windows Media Player 10 verwendet.</span><span class="sxs-lookup"><span data-stu-id="f18f9-135">Not used by Windows Media Player 10.</span></span> |
| <span data-ttu-id="f18f9-136">video</span><span class="sxs-lookup"><span data-stu-id="f18f9-136">video</span></span>    | <span data-ttu-id="f18f9-137">Video Elemente.</span><span class="sxs-lookup"><span data-stu-id="f18f9-137">Video items.</span></span>                                              |



 

<span data-ttu-id="f18f9-138">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="f18f9-138">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="f18f9-139">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f18f9-139">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f18f9-140">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f18f9-140">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="f18f9-141">Es gibt zwei Möglichkeiten, wie Sie eine **iwmpmediacollection** -Schnittstelle abrufen können, und das Verhalten der **getbyattribute** -Methode hängt davon ab, welche dieser beiden Methoden Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="f18f9-141">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAttribute** method depends on which of those two ways you use.</span></span> <span data-ttu-id="f18f9-142">Wenn Sie die Schnittstelle abrufen, indem Sie [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)aufrufen, gibt die **getbyattribute** -Methode alle Medienelemente in der Bibliothek zurück.</span><span class="sxs-lookup"><span data-stu-id="f18f9-142">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAttribute** method returns all the media items in the library.</span></span> <span data-ttu-id="f18f9-143">Wenn Sie jedoch die Schnittstelle abrufen, indem Sie [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)aufrufen, gibt die **getbyattribute** -Methode nur die Audioelemente in der Bibliothek zurück, die über das angegebene Attribut und den angegebenen Wert verfügen.</span><span class="sxs-lookup"><span data-stu-id="f18f9-143">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAttribute** method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="f18f9-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f18f9-144">Examples</span></span>

<span data-ttu-id="f18f9-145">Im folgenden Codebeispiel wird **getbyattribute** verwendet, um den gesamten Inhalt der Bibliothek von der Künstlerin mit dem Namen "testode 48" wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="f18f9-145">The following code example uses **getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="f18f9-146">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f18f9-146">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="f18f9-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f18f9-147">Requirements</span></span>



| <span data-ttu-id="f18f9-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f18f9-148">Requirement</span></span> | <span data-ttu-id="f18f9-149">Wert</span><span class="sxs-lookup"><span data-stu-id="f18f9-149">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f18f9-150">Version</span><span class="sxs-lookup"><span data-stu-id="f18f9-150">Version</span></span><br/>   | <span data-ttu-id="f18f9-151">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="f18f9-151">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f18f9-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="f18f9-152">Namespace</span></span><br/> | <span data-ttu-id="f18f9-153">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f18f9-153">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f18f9-154">Assembly</span><span class="sxs-lookup"><span data-stu-id="f18f9-154">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f18f9-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f18f9-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f18f9-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f18f9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18f9-157">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f18f9-157">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f18f9-158">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f18f9-158">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f18f9-159">**Iwmpplaylistcollection. GetAll (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f18f9-159">**IWMPPlaylistCollection.getAll (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





