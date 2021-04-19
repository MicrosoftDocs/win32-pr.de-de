---
title: AxWindowsMediaPlayer. FullScreen-Eigenschaft
description: Mit der FullScreen-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob Videoinhalte im Vollbildmodus abgespielt werden.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- Vollbild-Eigenschaften Fenster Media Player
- Vollbild-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, FullScreen-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355878"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a><span data-ttu-id="35a15-106">AxWindowsMediaPlayer. FullScreen-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="35a15-106">AxWindowsMediaPlayer.fullScreen property</span></span>

<span data-ttu-id="35a15-107">Mit der FullScreen-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob Videoinhalte im Vollbildmodus abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="35a15-107">The fullScreen property gets or sets a value indicating whether video content is played in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a15-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="35a15-108">Syntax</span></span>


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="35a15-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="35a15-109">Property value</span></span>

<span data-ttu-id="35a15-110">Ein System. Boolean-Wert, der angibt, ob der Inhalt im Vollbildmodus wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="35a15-110">A System.Boolean value that indicates whether content is played in full-screen mode.</span></span> <span data-ttu-id="35a15-111">Der Standardwert ist „FALSE“.</span><span class="sxs-lookup"><span data-stu-id="35a15-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a15-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35a15-112">Remarks</span></span>

<span data-ttu-id="35a15-113">Damit der Vollbildmodus beim Einbetten des Windows Media Player-Steuer Elements ordnungsgemäß funktioniert, muss der Videoanzeige Bereich eine Höhe und Breite von mindestens einem Pixel aufweisen.</span><span class="sxs-lookup"><span data-stu-id="35a15-113">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="35a15-114">Wenn **uiMode** auf "Mini" oder "Full" festgelegt ist, muss die Höhe des Steuer Elements auf 65 oder höher festgelegt sein, um zusätzlich zur Benutzeroberfläche den Videoanzeige Bereich aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="35a15-114">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="35a15-115">Wenn **uiMode** auf "unsichtbar" festgelegt ist, löst das Festlegen dieser Eigenschaft auf true einen Fehler aus und wirkt sich nicht auf das Verhalten des Steuer Elements aus.</span><span class="sxs-lookup"><span data-stu-id="35a15-115">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="35a15-116">Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn [enablecontextmenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) den Wert false hat und **uiMode** den Wert "None" hat.</span><span class="sxs-lookup"><span data-stu-id="35a15-116">During full-screen playback, Windows Media Player hides the mouse cursor when [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="35a15-117">Wenn **uiMode** auf "Full" oder "Mini" festgelegt ist, zeigt Windows Media Player Transport Steuerelemente im Vollbildmodus an, wenn der Mauszeiger bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="35a15-117">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="35a15-118">Nach einem kurzen Intervall ohne Mausbewegung werden die Transport Steuerelemente ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="35a15-118">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="35a15-119">Wenn **uiMode** auf "None" festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35a15-119">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="35a15-120">Zum Anzeigen von Transport Steuerelementen im Vollbildmodus ist das Betriebssystem Windows XP erforderlich.</span><span class="sxs-lookup"><span data-stu-id="35a15-120">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

 

<span data-ttu-id="35a15-121">Wenn Transport Steuerelemente nicht im Vollbildmodus angezeigt werden, beendet Windows Media Player den Vollbildmodus automatisch, wenn die Wiedergabe angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="35a15-121">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

## <a name="examples"></a><span data-ttu-id="35a15-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35a15-122">Examples</span></span>

<span data-ttu-id="35a15-123">Im folgenden Beispiel wird eine Schaltfläche erstellt, die die FullScreen-Eigenschaft verwendet, um ein eingebettetes Player-Objekt in den Vollbildmodus zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="35a15-123">The following example creates a button that uses the fullScreen property to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="35a15-124">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="35a15-124">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="35a15-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35a15-125">Requirements</span></span>



| <span data-ttu-id="35a15-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35a15-126">Requirement</span></span> | <span data-ttu-id="35a15-127">Wert</span><span class="sxs-lookup"><span data-stu-id="35a15-127">Value</span></span> |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a15-128">Version</span><span class="sxs-lookup"><span data-stu-id="35a15-128">Version</span></span><br/>   | <span data-ttu-id="35a15-129">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="35a15-129">Windows Media Player 9 Series or later</span></span><br/>                                                                  |
| <span data-ttu-id="35a15-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="35a15-130">Namespace</span></span><br/> | <span data-ttu-id="35a15-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="35a15-131">**AxWMPLib**</span></span><br/>                                                                                            |
| <span data-ttu-id="35a15-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="35a15-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="35a15-133"><dt>AxInterop. WMPLib (AxInterop.WMPLib.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="35a15-133"><dt>AxInterop.WMPLib (AxInterop.WMPLib.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a15-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35a15-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a15-135">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="35a15-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="35a15-136">**AxWindowsMediaPlayer. uiMode (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="35a15-136">**AxWindowsMediaPlayer.uiMode (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





