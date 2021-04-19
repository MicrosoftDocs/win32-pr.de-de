---
title: Iwmpcdrom-Wiedergabelisten Eigenschaft
description: Die Wiedergabeliste Ruft eine iwmpwiedergabe-Schnittstelle ab, die die Spuren auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk oder die Titel Einträge auf der Stamm Ebene einer DVD befinden.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Wiedergabelisten Eigenschaften Fenster Media Player
- Wiedergabelisten Eigenschaft, Windows Media Player, iwmpcdrom-Schnittstelle
- Iwmpcdrom-Schnittstelle, Windows Media Player, Wiedergabelisten Eigenschaft
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359629"
---
# <a name="iwmpcdromplaylist-property"></a><span data-ttu-id="df0e8-106">Iwmpcdrom::P laylist-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df0e8-106">IWMPCdrom::Playlist property</span></span>

<span data-ttu-id="df0e8-107">Die **Wiedergabeliste** Ruft eine **iwmpwiedergabe** -Schnittstelle ab, die die Spuren auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk oder die Titel Einträge auf der Stamm Ebene einer DVD befinden.</span><span class="sxs-lookup"><span data-stu-id="df0e8-107">The **Playlist** property gets an **IWMPPlaylist** interface representing the tracks on the CD currently in the CD drive or the root-level title entries for a DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="df0e8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="df0e8-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="df0e8-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="df0e8-109">Property value</span></span>

<span data-ttu-id="df0e8-110">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="df0e8-110">A **WMPLib.IWMPPlaylist** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="df0e8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df0e8-111">Remarks</span></span>

<span data-ttu-id="df0e8-112">In der Regel ist der DVD-basierte Inhalt in Titel gegliedert.</span><span class="sxs-lookup"><span data-stu-id="df0e8-112">Typically, DVD-based content organized into titles.</span></span> <span data-ttu-id="df0e8-113">Jeder Titel enthält ein oder mehrere Kapitel.</span><span class="sxs-lookup"><span data-stu-id="df0e8-113">Each title contains one or more chapters.</span></span> <span data-ttu-id="df0e8-114">Jede DVD wird unterschiedlich erstellt, sodass Titel und Kapitel für den Inhalts Autor verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df0e8-114">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="df0e8-115">Für eine DVD erhält diese Eigenschaft eine Wiedergabeliste, die als erstes Element eine **iwmpmedia** -Schnittstelle mit dem Namen "DVD" enthält.</span><span class="sxs-lookup"><span data-stu-id="df0e8-115">For a DVD, this property gets a playlist that contains as the first item an **IWMPMedia** interface named "DVD".</span></span> <span data-ttu-id="df0e8-116">Diese Schnittstelle stellt das DVD-Medium dar.</span><span class="sxs-lookup"><span data-stu-id="df0e8-116">This interface represents the DVD media.</span></span> <span data-ttu-id="df0e8-117">Die Wiedergabe des Elements führt dazu, dass die DVD von Anfang an wiedergegeben wird, wenn es sich um das erste Mal nach dem Einfügen einer neuen DVD handelt, oder die Wiedergabe wieder aufzunehmen, wenn die DVD mit der letzten angezeigten DVD identisch ist.</span><span class="sxs-lookup"><span data-stu-id="df0e8-117">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="df0e8-118">Das Festlegen dieses Elements als Aktuelles Element während der Wiedergabe führt dazu, dass die DVD von Anfang an wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="df0e8-118">Setting this item as the current item during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="df0e8-119">Zusätzliche Elemente (die durch **iwmpmedia** -Schnittstellen dargestellt werden) in der Wiedergabeliste sind DVD-Titel, die durch eine Liste von in einer Liste dargestellten Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="df0e8-119">Additional items (represented by **IWMPMedia** interfaces) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="df0e8-120">Wenn Sie **iwmpcontrols.** Currency Item auf eine dieser geklickte Wiedergabelisten Elemente festlegen, legt Windows Media Player die geklickte Wiedergabeliste automatisch als aktuelle Wiedergabeliste fest, nachdem die Kapitel Wiedergabe begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="df0e8-120">When you set **IWMPControls.currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as the current playlist after chapter playback begins.</span></span> <span data-ttu-id="df0e8-121">Sie können dann die Eigenschaften, Methoden und zugehörige Ereignisse der **iwmpwiedergabe** -Schnittstelle verwenden, um mit DVD-Kapiteln zu arbeiten, die auch Wiedergabelisten Elemente sind.</span><span class="sxs-lookup"><span data-stu-id="df0e8-121">You can then use the **IWMPPlaylist** interface properties, methods and associated events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="df0e8-122">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="df0e8-122">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="df0e8-123">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="df0e8-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="df0e8-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df0e8-124">Examples</span></span>

<span data-ttu-id="df0e8-125">Im folgenden Beispiel wird die **Wiedergabe** Liste verwendet, um ein mehrzeilige Textfeld mit dem Namen MyText mit der Trackliste der AudioCD auszufüllen, die sich zurzeit auf dem ersten CD-Laufwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="df0e8-125">The following example uses **Playlist** to fill a multi-line text box, named myText, with the track list of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="df0e8-126">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="df0e8-126">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a><span data-ttu-id="df0e8-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df0e8-127">Requirements</span></span>



| <span data-ttu-id="df0e8-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df0e8-128">Requirement</span></span> | <span data-ttu-id="df0e8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="df0e8-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df0e8-130">Version</span><span class="sxs-lookup"><span data-stu-id="df0e8-130">Version</span></span><br/>   | <span data-ttu-id="df0e8-131">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="df0e8-131">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="df0e8-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="df0e8-132">Namespace</span></span><br/> | <span data-ttu-id="df0e8-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="df0e8-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="df0e8-134">Assembly</span><span class="sxs-lookup"><span data-stu-id="df0e8-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="df0e8-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="df0e8-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df0e8-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df0e8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df0e8-137">**Iwmpcdrom-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="df0e8-137">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="df0e8-138">**Iwmpcontrols. Currency Item (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="df0e8-138">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="df0e8-139">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="df0e8-139">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="df0e8-140">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="df0e8-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="df0e8-141">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="df0e8-141">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="df0e8-142">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="df0e8-142">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





