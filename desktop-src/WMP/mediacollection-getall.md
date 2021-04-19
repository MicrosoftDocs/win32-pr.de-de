---
title: Mediacollection. GetAll-Methode
description: Die GetAll-Methode ruft eine Wiedergabeliste ab, die alle Medienelemente in der Bibliothek enthält.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- GetAll-Methoden Fenster Media Player
- GetAll-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, GetAll-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1681cd533be4084123cb80cdcc199ab5e1ce2981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373868"
---
# <a name="mediacollectiongetall-method"></a><span data-ttu-id="c61a9-106">Mediacollection. GetAll-Methode</span><span class="sxs-lookup"><span data-stu-id="c61a9-106">MediaCollection.getAll method</span></span>

<span data-ttu-id="c61a9-107">Die **GetAll** -Methode ruft eine Wiedergabeliste ab, die alle Medienelemente in der Bibliothek enthält.</span><span class="sxs-lookup"><span data-stu-id="c61a9-107">The **getAll** method retrieves a playlist containing all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="c61a9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c61a9-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a><span data-ttu-id="c61a9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c61a9-109">Parameters</span></span>

<span data-ttu-id="c61a9-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c61a9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c61a9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c61a9-111">Return value</span></span>

<span data-ttu-id="c61a9-112">Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c61a9-112">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c61a9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c61a9-113">Remarks</span></span>

<span data-ttu-id="c61a9-114">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c61a9-114">To use this method, read access to the library is required.</span></span> <span data-ttu-id="c61a9-115">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c61a9-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c61a9-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c61a9-116">Examples</span></span>

<span data-ttu-id="c61a9-117">Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **GetAll** zum Zufalls Spiel der Medienelemente aus der Mediensammlung.</span><span class="sxs-lookup"><span data-stu-id="c61a9-117">The following JScript example uses *MediaCollection*.**getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="c61a9-118">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c61a9-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="c61a9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c61a9-119">Requirements</span></span>



| <span data-ttu-id="c61a9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c61a9-120">Requirement</span></span> | <span data-ttu-id="c61a9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c61a9-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c61a9-122">Version</span><span class="sxs-lookup"><span data-stu-id="c61a9-122">Version</span></span><br/> | <span data-ttu-id="c61a9-123">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c61a9-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c61a9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c61a9-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c61a9-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c61a9-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c61a9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c61a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61a9-127">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="c61a9-127">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="c61a9-128">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="c61a9-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="c61a9-129">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="c61a9-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c61a9-130">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="c61a9-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





