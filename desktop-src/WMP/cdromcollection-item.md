---
title: Cdromcollection. Item-Methode
description: Die Item-Methode ruft das CDROM-Objekt am angegebenen Index ab.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, cdromcollection-Klasse
- Cdromcollection-Klasse, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365812"
---
# <a name="cdromcollectionitem-method"></a><span data-ttu-id="dbeba-106">Cdromcollection. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="dbeba-106">CdromCollection.item method</span></span>

<span data-ttu-id="dbeba-107">Die **Item** -Methode ruft das **CDROM** -Objekt am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="dbeba-107">The **item** method retrieves the **Cdrom** object at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbeba-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbeba-108">Syntax</span></span>


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="dbeba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbeba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbeba-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbeba-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbeba-111">Die **Zahl** (**Long**), die den Index enthält.</span><span class="sxs-lookup"><span data-stu-id="dbeba-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbeba-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbeba-112">Return value</span></span>

<span data-ttu-id="dbeba-113">Diese Methode gibt ein **CDROM** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="dbeba-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbeba-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbeba-114">Remarks</span></span>

<span data-ttu-id="dbeba-115">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dbeba-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="dbeba-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="dbeba-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="dbeba-117">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dbeba-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="dbeba-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbeba-118">Examples</span></span>

<span data-ttu-id="dbeba-119">Im folgenden JScript-Beispiel wird *cdromcollection* verwendet. **Element** , mit dem der Wiedergabelisten Name der einzelnen auf dem Computer verfügbaren CD gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbeba-119">The following JScript example uses *CdromCollection*.**item** to print the playlist name from each CD available on the computer.</span></span> <span data-ttu-id="dbeba-120">Wenn das Laufwerk tatsächlich DVD-Inhalte enthält, ist Windows XP oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dbeba-120">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="dbeba-121">Ein HTML-TEXTAREA-Element wurde mit ID = "Playlists" erstellt.</span><span class="sxs-lookup"><span data-stu-id="dbeba-121">An HTML TextArea element was created with ID = "playlists".</span></span> <span data-ttu-id="dbeba-122">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="dbeba-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="dbeba-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbeba-123">Requirements</span></span>



| <span data-ttu-id="dbeba-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbeba-124">Requirement</span></span> | <span data-ttu-id="dbeba-125">Wert</span><span class="sxs-lookup"><span data-stu-id="dbeba-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dbeba-126">Version</span><span class="sxs-lookup"><span data-stu-id="dbeba-126">Version</span></span><br/> | <span data-ttu-id="dbeba-127">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="dbeba-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="dbeba-128">DLL</span><span class="sxs-lookup"><span data-stu-id="dbeba-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="dbeba-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbeba-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbeba-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbeba-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbeba-131">**Cdrom. drivespecifier**</span><span class="sxs-lookup"><span data-stu-id="dbeba-131">**Cdrom.driveSpecifier**</span></span>](cdrom-drivespecifier.md)
</dt> <dt>

[<span data-ttu-id="dbeba-132">**Cdromcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="dbeba-132">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="dbeba-133">**Cdromcollection. Count**</span><span class="sxs-lookup"><span data-stu-id="dbeba-133">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="dbeba-134">**Playlist.name**</span><span class="sxs-lookup"><span data-stu-id="dbeba-134">**Playlist.name**</span></span>](playlist-name.md)
</dt> <dt>

[<span data-ttu-id="dbeba-135">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="dbeba-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="dbeba-136">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="dbeba-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





