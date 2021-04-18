---
title: Mediacollection. getbyalbum-Methode
description: Die getbyalbum-Methode ruft eine Wiedergabeliste ab, die die Medienelemente aus dem angegebenen Album enthält.
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- getbyalbum-Methode, Windows-Media Player
- getbyalbum-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getbyalbum-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d94cdfa880288893e9659b73b01bc754ac59bbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371652"
---
# <a name="mediacollectiongetbyalbum-method"></a><span data-ttu-id="24192-106">Mediacollection. getbyalbum-Methode</span><span class="sxs-lookup"><span data-stu-id="24192-106">MediaCollection.getByAlbum method</span></span>

<span data-ttu-id="24192-107">Die **getbyalbum** -Methode ruft eine Wiedergabeliste ab, die die Medienelemente aus dem angegebenen Album enthält.</span><span class="sxs-lookup"><span data-stu-id="24192-107">The **GetByAlbum** method retrieves a playlist containing the media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="24192-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="24192-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a><span data-ttu-id="24192-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="24192-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24192-110">*Album* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24192-110">*album* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24192-111">**Zeichenfolge** , die den Namen des Albums enthält.</span><span class="sxs-lookup"><span data-stu-id="24192-111">**String** containing the name of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24192-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24192-112">Return value</span></span>

<span data-ttu-id="24192-113">Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="24192-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="24192-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24192-114">Remarks</span></span>

<span data-ttu-id="24192-115">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="24192-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="24192-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="24192-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="24192-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24192-117">Examples</span></span>

<span data-ttu-id="24192-118">Im folgenden Beispiel wird *mediacollection* verwendet. **getbyalbum** zum Abrufen einer Wiedergabeliste von Medien Elementen.</span><span class="sxs-lookup"><span data-stu-id="24192-118">The following example uses *MediaCollection*.**getByAlbum** to retrieve a playlist of media items.</span></span> <span data-ttu-id="24192-119">Die Wiedergabeliste enthält Elemente mit dem vom Benutzer angegebenen Album in einem HTML-Text Eingabe Element namens getalbum.</span><span class="sxs-lookup"><span data-stu-id="24192-119">The playlist contains items with the album specified by the user in an HTML TEXT input element named GetAlbum.</span></span> <span data-ttu-id="24192-120">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="24192-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="24192-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24192-121">Requirements</span></span>



| <span data-ttu-id="24192-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24192-122">Requirement</span></span> | <span data-ttu-id="24192-123">Wert</span><span class="sxs-lookup"><span data-stu-id="24192-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24192-124">Version</span><span class="sxs-lookup"><span data-stu-id="24192-124">Version</span></span><br/> | <span data-ttu-id="24192-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="24192-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="24192-126">DLL</span><span class="sxs-lookup"><span data-stu-id="24192-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="24192-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24192-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24192-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24192-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24192-129">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="24192-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="24192-130">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="24192-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="24192-131">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="24192-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="24192-132">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="24192-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





