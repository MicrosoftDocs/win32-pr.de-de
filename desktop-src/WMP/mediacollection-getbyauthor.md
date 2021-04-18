---
title: Mediacollection. getbyauthor-Methode
description: Die getbyauthor-Methode ruft eine Wiedergabeliste der Medienelemente vom angegebenen Autor ab.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- getbyauthor-Methode, Windows-Media Player
- getbyauthor-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getbyauthor-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eae0928250e37e76bf3a39f38b43bef8a5691c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365181"
---
# <a name="mediacollectiongetbyauthor-method"></a><span data-ttu-id="64a44-106">Mediacollection. getbyauthor-Methode</span><span class="sxs-lookup"><span data-stu-id="64a44-106">MediaCollection.getByAuthor method</span></span>

<span data-ttu-id="64a44-107">Die **getbyauthor** -Methode ruft eine Wiedergabeliste der Medienelemente vom angegebenen Autor ab.</span><span class="sxs-lookup"><span data-stu-id="64a44-107">The **getByAuthor** method retrieves a playlist of the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="64a44-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="64a44-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a><span data-ttu-id="64a44-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="64a44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64a44-110">*Autor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64a44-110">*author* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64a44-111">**Zeichenfolge** , die den Namen des Autors enthält.</span><span class="sxs-lookup"><span data-stu-id="64a44-111">**String** containing the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64a44-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64a44-112">Return value</span></span>

<span data-ttu-id="64a44-113">Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="64a44-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="64a44-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64a44-114">Remarks</span></span>

<span data-ttu-id="64a44-115">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="64a44-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="64a44-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="64a44-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="64a44-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64a44-117">Examples</span></span>

<span data-ttu-id="64a44-118">Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **getbyauthor** zum Abrufen einer Wiedergabeliste von Medien Elementen.</span><span class="sxs-lookup"><span data-stu-id="64a44-118">The following JScript example uses *MediaCollection*.**getByAuthor** to retrieve a playlist of media items.</span></span> <span data-ttu-id="64a44-119">Die Wiedergabeliste enthält Elemente, die mit dem vom Benutzer angegebenen Autor in einem HTML-Text Eingabe Element namens getauthor übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="64a44-119">The playlist contains items matching the author specified by the user in an HTML TEXT input element named GetAuthor.</span></span> <span data-ttu-id="64a44-120">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="64a44-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
               Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="64a44-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64a44-121">Requirements</span></span>



| <span data-ttu-id="64a44-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64a44-122">Requirement</span></span> | <span data-ttu-id="64a44-123">Wert</span><span class="sxs-lookup"><span data-stu-id="64a44-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64a44-124">Version</span><span class="sxs-lookup"><span data-stu-id="64a44-124">Version</span></span><br/> | <span data-ttu-id="64a44-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="64a44-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="64a44-126">DLL</span><span class="sxs-lookup"><span data-stu-id="64a44-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="64a44-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64a44-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64a44-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64a44-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64a44-129">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="64a44-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="64a44-130">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="64a44-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="64a44-131">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="64a44-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="64a44-132">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="64a44-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





