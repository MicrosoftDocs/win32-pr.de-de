---
title: Cdrom. Wiedergabeliste
description: Die Wiedergabelisten Eigenschaft ruft ein Wiedergabelisten Objekt ab, das die Spuren auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk oder die Titel Einträge auf der Stamm Ebene für DVD darstellt.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Cdrom. Wiedergabelisten-Fenster Media Player
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345291"
---
# <a name="cdromplaylist"></a><span data-ttu-id="81a91-104">Cdrom. Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="81a91-104">Cdrom.playlist</span></span>

<span data-ttu-id="81a91-105">Die **Wiedergabe** Listen Eigenschaft ruft ein **Wiedergabe** Listen Objekt ab, das die Spuren auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk oder die Titel Einträge auf der Stamm Ebene für DVD darstellt.</span><span class="sxs-lookup"><span data-stu-id="81a91-105">The **playlist** property retrieves a **Playlist** object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a><span data-ttu-id="81a91-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="81a91-106">Possible Values</span></span>

<span data-ttu-id="81a91-107">Diese Eigenschaft ist ein Schreib geschütztes **Wiedergabe** Listen Objekt.</span><span class="sxs-lookup"><span data-stu-id="81a91-107">This property is a read-only **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="81a91-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81a91-108">Remarks</span></span>

<span data-ttu-id="81a91-109">In der Regel sind DVDs in Titeln organisiert.</span><span class="sxs-lookup"><span data-stu-id="81a91-109">Typically, DVDs are organized into titles.</span></span> <span data-ttu-id="81a91-110">Jeder Titel enthält ein oder mehrere Kapitel.</span><span class="sxs-lookup"><span data-stu-id="81a91-110">Each title contains one or more chapters.</span></span> <span data-ttu-id="81a91-111">Jede DVD wird unterschiedlich erstellt, sodass Titel und Kapitel für den Inhalts Autor verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81a91-111">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="81a91-112">Bei der DVD ruft diese Methode eine Wiedergabeliste ab, die als erstes Element ein **Medien** Objekt enthält, das das DVD-Medium darstellt.</span><span class="sxs-lookup"><span data-stu-id="81a91-112">For DVD, this method retrieves a playlist that contains as the first item a **Media** object that represents the DVD media.</span></span> <span data-ttu-id="81a91-113">Die Wiedergabe des Elements führt dazu, dass die DVD von Anfang an wiedergegeben wird, wenn es sich um das erste Mal nach dem Einfügen einer neuen DVD handelt, oder die Wiedergabe wieder aufzunehmen, wenn die DVD mit der letzten angezeigten DVD identisch ist.</span><span class="sxs-lookup"><span data-stu-id="81a91-113">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="81a91-114">Wenn Sie dieses Element während der Wiedergabe als das aktuelle Element festlegen, wird die DVD von Anfang an wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="81a91-114">Setting this item as the current one during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="81a91-115">Zusätzliche Elemente (**Medien** Objekte) in der Wiedergabeliste sind DVD-Titel, die durch in der Liste dargestellte Wiedergabelisten dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="81a91-115">Additional items (**Media** objects) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="81a91-116">Wenn Sie Steuer *Elemente* angeben. das Element, das einem dieser in der Liste eingefügten Wiedergabelisten Elemente entspricht, **wird von Windows** Media Player automatisch die geklickte Wiedergabeliste als *Player* festgelegt. **currentwiedergabe** nach Beginn der Wiedergabe des Kapitels.</span><span class="sxs-lookup"><span data-stu-id="81a91-116">When you specify *Controls*.**currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as *Player*.**currentPlaylist** after chapter playback begins.</span></span> <span data-ttu-id="81a91-117">Sie können dann die Eigenschaften, Methoden und Ereignisse des **currentwiedergabe** -Objekts verwenden, um mit DVD-Kapiteln zu arbeiten, die auch Wiedergabelisten Elemente sind.</span><span class="sxs-lookup"><span data-stu-id="81a91-117">You can then use the **currentPlaylist** object properties, methods, and events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="81a91-118">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="81a91-118">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="81a91-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="81a91-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="81a91-120">**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81a91-120">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="81a91-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81a91-121">Examples</span></span>

<span data-ttu-id="81a91-122">Im folgenden Beispiel wird *CDROM* verwendet. **Wiedergabeliste** zum Ausfüllen eines HTML-Text Elements mit dem Namen "MyText" mit den Titeln der AudioCD, die sich zurzeit auf dem ersten CD-Laufwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="81a91-122">The following example uses *Cdrom*.**playlist** to fill an HTML text element, named myText, with the titles of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="81a91-123">Verwenden Sie *cdromcollection*. **Anzahl, um** die Anzahl der verfügbaren CD-Laufwerke zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="81a91-123">Use *CdromCollection*.**count** to determine the number of available CD drives.</span></span> <span data-ttu-id="81a91-124">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="81a91-124">The **Player** object was created with ID = "Player".</span></span>


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a><span data-ttu-id="81a91-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81a91-125">Requirements</span></span>



| <span data-ttu-id="81a91-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81a91-126">Requirement</span></span> | <span data-ttu-id="81a91-127">Wert</span><span class="sxs-lookup"><span data-stu-id="81a91-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81a91-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81a91-128">Minimum supported client</span></span><br/> | <span data-ttu-id="81a91-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81a91-129">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81a91-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81a91-130">Minimum supported server</span></span><br/> | <span data-ttu-id="81a91-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81a91-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="81a91-132">Version</span><span class="sxs-lookup"><span data-stu-id="81a91-132">Version</span></span><br/>                  | <span data-ttu-id="81a91-133">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="81a91-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="81a91-134">DLL</span><span class="sxs-lookup"><span data-stu-id="81a91-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81a91-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81a91-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81a91-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81a91-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a91-137">**Cdrom-Objekt**</span><span class="sxs-lookup"><span data-stu-id="81a91-137">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="81a91-138">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="81a91-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="81a91-139">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="81a91-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





