---
title: Iwmpcontrols currentmarker (Eigenschaft)
description: Die currentmarker-Eigenschaft ruft die aktuelle Markernummer ab oder legt Sie fest.
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- currentmarker-Eigenschaft, Fenster Media Player
- currentmarker-Eigenschaft, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, currentmarker (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372459"
---
# <a name="iwmpcontrolscurrentmarker-property"></a><span data-ttu-id="87e95-106">Iwmpcontrols:: currentmarker (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="87e95-106">IWMPControls::currentMarker property</span></span>

<span data-ttu-id="87e95-107">Die **currentmarker** -Eigenschaft ruft die aktuelle Markernummer ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="87e95-107">The **currentMarker** property gets or sets the current marker number.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e95-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="87e95-108">Syntax</span></span>


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="87e95-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="87e95-109">Property value</span></span>

<span data-ttu-id="87e95-110">Ein **System. Int32** -Wert, der die Markernummer ist.</span><span class="sxs-lookup"><span data-stu-id="87e95-110">A **System.Int32** that is the marker number.</span></span>

## <a name="remarks"></a><span data-ttu-id="87e95-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87e95-111">Remarks</span></span>

<span data-ttu-id="87e95-112">Das Festlegen von **currentmarker** bewirkt, dass die Wiedergabe vom angegebenen Marker gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="87e95-112">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="87e95-113">Stellen Sie vor dem Festlegen von **currentmarker** fest, ob eine Datei Marker hat und wie viele diese mithilfe von **iwmpmedia. markercount** hat.</span><span class="sxs-lookup"><span data-stu-id="87e95-113">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **IWMPMedia.markerCount**.</span></span> <span data-ttu-id="87e95-114">Wenn eine Datei keine Marker hat, führt die Festlegung von **currentmarker** auf alles, aber auf 0 (null) zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="87e95-114">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="87e95-115">Wenn **currentmarker** auf eine Zahl höher als **markercount** festgelegt wird, führt dies ebenfalls zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="87e95-115">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="87e95-116">Die **currentmarker** -Eigenschaft gibt immer den aktuellen oder den letzten Marker zurück. Dies bedeutet, dass sich die tatsächliche Dateiposition entweder am aktuellen Marker oder vor dem nächsten Marker befinden kann.</span><span class="sxs-lookup"><span data-stu-id="87e95-116">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="87e95-117">Marker werden beginnend mit 1 nummeriert. Wenn also eine Datei Marker enthält, können Sie **currentmarker** auf NULL festlegen, um die Dateiposition in NULL zu ändern.</span><span class="sxs-lookup"><span data-stu-id="87e95-117">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="87e95-118">Bis das aktuelle Medien Element festgelegt ist (mithilfe von **AxWindowsMediaPlayer. URL** oder **AxWindowsMediaPlayer. currentMedia**), gibt **currentmarker** 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="87e95-118">Until the current media item is set (using **AxWindowsMediaPlayer.URL** or **AxWindowsMediaPlayer.currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="87e95-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87e95-119">Examples</span></span>

<span data-ttu-id="87e95-120">Im folgenden Beispiel wird **currentmarker** verwendet, um die Videowiedergabe von dem Marker zu starten, der der SelectedIndex-Eigenschaft eines Listen Felds entspricht, das mit markerbezeichlern gefüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="87e95-120">The following example uses **currentMarker** to start video playback from the marker that corresponds to the SelectedIndex property of a list box which has been filled with marker identifiers.</span></span> <span data-ttu-id="87e95-121">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="87e95-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

End Sub
```





## <a name="requirements"></a><span data-ttu-id="87e95-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87e95-122">Requirements</span></span>



| <span data-ttu-id="87e95-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87e95-123">Requirement</span></span> | <span data-ttu-id="87e95-124">Wert</span><span class="sxs-lookup"><span data-stu-id="87e95-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87e95-125">Version</span><span class="sxs-lookup"><span data-stu-id="87e95-125">Version</span></span><br/>   | <span data-ttu-id="87e95-126">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="87e95-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="87e95-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="87e95-127">Namespace</span></span><br/> | <span data-ttu-id="87e95-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="87e95-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="87e95-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="87e95-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="87e95-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="87e95-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87e95-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87e95-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e95-132">**AxWindowsMediaPlayer. currentMedia (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="87e95-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="87e95-133">**AxWindowsMediaPlayer. URL (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="87e95-133">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="87e95-134">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="87e95-134">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="87e95-135">**Iwmpmedia. markercount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="87e95-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





