---
title: Mediacollection. getbygenre-Methode
description: Die getbygenre-Methode ruft eine Wiedergabeliste der Medienelemente mit dem angegebenen Genre ab.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- getbygenre-Methode, Windows-Media Player
- getbygenre-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getbygenre-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354127"
---
# <a name="mediacollectiongetbygenre-method"></a><span data-ttu-id="2c7b3-106">Mediacollection. getbygenre-Methode</span><span class="sxs-lookup"><span data-stu-id="2c7b3-106">MediaCollection.getByGenre method</span></span>

<span data-ttu-id="2c7b3-107">Die **getbygenre** -Methode ruft eine Wiedergabeliste der Medienelemente mit dem angegebenen Genre ab.</span><span class="sxs-lookup"><span data-stu-id="2c7b3-107">The **getByGenre** method retrieves a playlist of the media items with the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c7b3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c7b3-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a><span data-ttu-id="2c7b3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c7b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c7b3-110">*Genre* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c7b3-110">*genre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c7b3-111">**Zeichenfolge** , die den Namen des Genres enthält.</span><span class="sxs-lookup"><span data-stu-id="2c7b3-111">**String** containing the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c7b3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c7b3-112">Return value</span></span>

<span data-ttu-id="2c7b3-113">Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="2c7b3-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c7b3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c7b3-114">Remarks</span></span>

<span data-ttu-id="2c7b3-115">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2c7b3-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="2c7b3-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2c7b3-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2c7b3-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c7b3-117">Examples</span></span>

<span data-ttu-id="2c7b3-118">Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **getbygenre** zum Abrufen einer Wiedergabeliste von Medien Elementen.</span><span class="sxs-lookup"><span data-stu-id="2c7b3-118">The following JScript example uses *MediaCollection*.**getByGenre** to retrieve a playlist of media items.</span></span> <span data-ttu-id="2c7b3-119">Die Wiedergabeliste enthält Elemente mit dem vom Benutzer angegebenen Genre in einem HTML-Text Eingabe Element mit dem Namen getgenre.</span><span class="sxs-lookup"><span data-stu-id="2c7b3-119">The playlist contains items with the genre specified by the user in an HTML TEXT input element named GetGenre.</span></span> <span data-ttu-id="2c7b3-120">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c7b3-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="2c7b3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c7b3-121">Requirements</span></span>



| <span data-ttu-id="2c7b3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c7b3-122">Requirement</span></span> | <span data-ttu-id="2c7b3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2c7b3-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7b3-124">Version</span><span class="sxs-lookup"><span data-stu-id="2c7b3-124">Version</span></span><br/> | <span data-ttu-id="2c7b3-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2c7b3-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2c7b3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2c7b3-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c7b3-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c7b3-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c7b3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c7b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c7b3-129">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="2c7b3-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="2c7b3-130">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="2c7b3-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="2c7b3-131">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="2c7b3-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2c7b3-132">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="2c7b3-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





