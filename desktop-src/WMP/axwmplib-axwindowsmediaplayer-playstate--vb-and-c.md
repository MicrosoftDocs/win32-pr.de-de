---
title: AxWindowsMediaPlayer. playstate (Eigenschaft)
description: Die playstate-Eigenschaft ruft einen Enumerationswert ab, der den Zustand des Windows-Media Player Vorgangs angibt.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- playstate-Eigenschaften Fenster Media Player
- playstate-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, playstate (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370310"
---
# <a name="axwindowsmediaplayerplaystate-property"></a><span data-ttu-id="0f412-106">AxWindowsMediaPlayer. playstate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0f412-106">AxWindowsMediaPlayer.playState property</span></span>

<span data-ttu-id="0f412-107">Die playstate-Eigenschaft ruft einen Enumerationswert ab, der den Zustand des Windows-Media Player Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="0f412-107">The playState property gets an enumeration value indicating the state of the Windows Media Player operation.</span></span>

<span data-ttu-id="0f412-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0f412-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f412-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f412-109">Syntax</span></span>


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a><span data-ttu-id="0f412-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0f412-110">Property value</span></span>

<span data-ttu-id="0f412-111">Der WMPLib. WMPPlayState-Enumerationswert.</span><span class="sxs-lookup"><span data-stu-id="0f412-111">The WMPLib.WMPPlayState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f412-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f412-112">Remarks</span></span>

<span data-ttu-id="0f412-113">Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten.</span><span class="sxs-lookup"><span data-stu-id="0f412-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="0f412-114">Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf.</span><span class="sxs-lookup"><span data-stu-id="0f412-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="0f412-115">Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.</span><span class="sxs-lookup"><span data-stu-id="0f412-115">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="0f412-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f412-116">Examples</span></span>

<span data-ttu-id="0f412-117">Im folgenden Beispiel wird die playstate-Eigenschaft verwendet, um den aktuellen Wiedergabe Status des Players in einer Bezeichnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0f412-117">The following example uses the playState property to display the current playing status of the player in a label.</span></span> <span data-ttu-id="0f412-118">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0f412-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





## <a name="requirements"></a><span data-ttu-id="0f412-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f412-119">Requirements</span></span>



| <span data-ttu-id="0f412-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f412-120">Requirement</span></span> | <span data-ttu-id="0f412-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0f412-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f412-122">Version</span><span class="sxs-lookup"><span data-stu-id="0f412-122">Version</span></span><br/>   | <span data-ttu-id="0f412-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0f412-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="0f412-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f412-124">Namespace</span></span><br/> | <span data-ttu-id="0f412-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="0f412-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="0f412-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="0f412-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0f412-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0f412-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f412-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f412-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f412-129">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0f412-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0f412-130">**AxWindowsMediaPlayer. PlayStateChange-Ereignis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0f412-130">**AxWindowsMediaPlayer.PlayStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="0f412-131">**WMPPlayState**</span><span class="sxs-lookup"><span data-stu-id="0f412-131">**WMPPlayState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





