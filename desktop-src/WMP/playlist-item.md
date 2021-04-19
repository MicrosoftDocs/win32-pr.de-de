---
title: Wiedergabe. Item-Methode
description: Die Item-Methode ruft das Medien Element am angegebenen Index ab.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367797"
---
# <a name="playlistitem-method"></a><span data-ttu-id="40cb0-106">Wiedergabe. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="40cb0-106">Playlist.item method</span></span>

<span data-ttu-id="40cb0-107">Die **Item** -Methode ruft das Medien Element am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="40cb0-107">The **item** method retrieves the media item at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="40cb0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="40cb0-108">Syntax</span></span>


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="40cb0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="40cb0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40cb0-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40cb0-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40cb0-111">**Zahl** (**Long**), die den Index des abzurufenden Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="40cb0-111">**Number** (**long**) containing the index of the item to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40cb0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40cb0-112">Return value</span></span>

<span data-ttu-id="40cb0-113">Diese Methode gibt ein **Medien** Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="40cb0-113">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="40cb0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40cb0-114">Remarks</span></span>

<span data-ttu-id="40cb0-115">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="40cb0-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="40cb0-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="40cb0-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="40cb0-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40cb0-117">Examples</span></span>

<span data-ttu-id="40cb0-118">Im folgenden JScript-Beispiel wird die *Wiedergabeliste* verwendet. **Element** zum Abrufen eines Medien Elements aus der aktuellen Wiedergabeliste basierend auf einer Benutzer Auswahl.</span><span class="sxs-lookup"><span data-stu-id="40cb0-118">The following JScript example uses *Playlist*.**item** to retrieve a media item from the current playlist based on a user selection.</span></span> <span data-ttu-id="40cb0-119">Es wurde ein HTML-SELECT-Element mit dem Namen "weblist" erstellt und mit den Titeln aus der aktuellen Wiedergabeliste gefüllt.</span><span class="sxs-lookup"><span data-stu-id="40cb0-119">An HTML SELECT element was created with name "weblist", and filled with the titles from the current playlist.</span></span> <span data-ttu-id="40cb0-120">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="40cb0-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

```



## <a name="requirements"></a><span data-ttu-id="40cb0-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40cb0-121">Requirements</span></span>



| <span data-ttu-id="40cb0-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40cb0-122">Requirement</span></span> | <span data-ttu-id="40cb0-123">Wert</span><span class="sxs-lookup"><span data-stu-id="40cb0-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40cb0-124">Version</span><span class="sxs-lookup"><span data-stu-id="40cb0-124">Version</span></span><br/> | <span data-ttu-id="40cb0-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="40cb0-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="40cb0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="40cb0-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="40cb0-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40cb0-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40cb0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40cb0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40cb0-129">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="40cb0-129">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="40cb0-130">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="40cb0-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="40cb0-131">**Wiedergabeliste. InsertItem**</span><span class="sxs-lookup"><span data-stu-id="40cb0-131">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="40cb0-132">**Wiedergabeliste. RemoveItem**</span><span class="sxs-lookup"><span data-stu-id="40cb0-132">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="40cb0-133">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="40cb0-133">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="40cb0-134">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="40cb0-134">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





