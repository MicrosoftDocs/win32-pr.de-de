---
title: Iwmpcontrols-PlayItem-Methode
description: Die PlayItem-Methode gibt das angegebene Medien Element wieder. | Iwmpcontrols-PlayItem-Methode
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- PlayItem-Methoden Fenster Media Player
- PlayItem-Methode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols-Schnittstelle, Windows Media Player, PlayItem-Methode
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371311"
---
# <a name="iwmpcontrolsplayitem-method"></a><span data-ttu-id="dced3-107">Iwmpcontrols::p layitem-Methode</span><span class="sxs-lookup"><span data-stu-id="dced3-107">IWMPControls::playItem method</span></span>

<span data-ttu-id="dced3-108">Die **PlayItem** -Methode gibt das angegebene Medien Element wieder.</span><span class="sxs-lookup"><span data-stu-id="dced3-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="dced3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dced3-109">Syntax</span></span>


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a><span data-ttu-id="dced3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dced3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dced3-111">*piwmpmedia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dced3-111">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dced3-112">Eine **WMPLib. iwmpmedia** -Schnittstelle für das Medien Element.</span><span class="sxs-lookup"><span data-stu-id="dced3-112">A **WMPLib.IWMPMedia** interface to the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dced3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dced3-113">Return value</span></span>

<span data-ttu-id="dced3-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dced3-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dced3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dced3-115">Remarks</span></span>

<span data-ttu-id="dced3-116">Das Medien Element wird unabhängig vom Wert der **iwmpsettings. Autostart** -Eigenschaft automatisch geladen und abgespielt.</span><span class="sxs-lookup"><span data-stu-id="dced3-116">The media item will load and play automatically, regardless of the value of the **IWMPSettings.autoStart** property.</span></span> <span data-ttu-id="dced3-117">Wenn Sie ein Element ohne automatische Wiedergabe laden möchten, legen Sie " **iwmpsettings. Autostart** " auf " **false** " fest, und weisen Sie " **AxWindowsMediaPlayer. URL**" einen Wert zu, nachdem " **iwmpcontrols. Play** " aufgerufen werden kann, um die Wiedergabe des Elements</span><span class="sxs-lookup"><span data-stu-id="dced3-117">To load an item without playing it automatically, set **IWMPSettings.autoStart** to **false** and assign a value to **AxWindowsMediaPlayer.URL**, after which **IWMPControls.play** can be called to start playing the item.</span></span>

<span data-ttu-id="dced3-118">Hinweis</span><span class="sxs-lookup"><span data-stu-id="dced3-118">Note</span></span>

<span data-ttu-id="dced3-119">**PlayItem** funktioniert nur mit Elementen in **AxWindowsMediaPlayer. currentwiedergabe**.</span><span class="sxs-lookup"><span data-stu-id="dced3-119">**playItem** works only with items in **AxWindowsMediaPlayer.currentPlaylist**.</span></span> <span data-ttu-id="dced3-120">Das Aufrufen von **PlayItem** mit einem Verweis auf ein gespeichertes Medien Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dced3-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="dced3-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dced3-121">Examples</span></span>

<span data-ttu-id="dced3-122">Im folgenden Beispiel wird **PlayItem** verwendet, um ein Medien Element aus der aktuellen Wiedergabeliste wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="dced3-122">The following example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="dced3-123">Das Element, das abgespielt werden soll, wird basierend auf seiner Position in der Wiedergabeliste ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="dced3-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="dced3-124">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="dced3-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a><span data-ttu-id="dced3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dced3-125">Requirements</span></span>



| <span data-ttu-id="dced3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dced3-126">Requirement</span></span> | <span data-ttu-id="dced3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="dced3-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dced3-128">Version</span><span class="sxs-lookup"><span data-stu-id="dced3-128">Version</span></span><br/>   | <span data-ttu-id="dced3-129">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="dced3-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dced3-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="dced3-130">Namespace</span></span><br/> | <span data-ttu-id="dced3-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dced3-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dced3-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="dced3-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dced3-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dced3-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dced3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dced3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dced3-135">**AxWindowsMediaPlayer. currentwiedergabe (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="dced3-135">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dced3-136">**AxWindowsMediaPlayer. URL (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="dced3-136">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dced3-137">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="dced3-137">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dced3-138">**Iwmpcontrols. Play (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="dced3-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dced3-139">**Iwmpwiedergabe. Item (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="dced3-139">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dced3-140">**Iwmpsettings. Autostart (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="dced3-140">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





