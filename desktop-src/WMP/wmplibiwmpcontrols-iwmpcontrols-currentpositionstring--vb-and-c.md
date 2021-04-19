---
title: Iwmpcontrols currentpositionstring (Eigenschaft)
description: Die currentpositionstring-Eigenschaft ruft die aktuelle Position im Medien Element als Zeichenfolge ab, die als hh mm SS (Stunden, Minuten und Sekunden) formatiert ist.
ms.assetid: cd28dafa-b6a4-4bed-aa5d-7e7be6af1426
keywords:
- currentpositionstring-Eigenschaft, Windows-Media Player
- currentpositionstring-Eigenschaft, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, currentpositionstring (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPControls.currentPositionString
- IWMPControls.get_currentPositionString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e941fceb61e4f00393b05f96489ec7ac8e950f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370316"
---
# <a name="iwmpcontrolscurrentpositionstring-property"></a><span data-ttu-id="45859-106">Iwmpcontrols:: currentpositionstring (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="45859-106">IWMPControls::currentPositionString property</span></span>

<span data-ttu-id="45859-107">Die **currentpositionstring** -Eigenschaft ruft die aktuelle Position im Medien Element als Zeichenfolge ab, die als hh: mm: SS (Stunden, Minuten und Sekunden) formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="45859-107">The **currentPositionString** property gets the current position in the media item as a string formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

<span data-ttu-id="45859-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="45859-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="45859-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="45859-109">Syntax</span></span>


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a><span data-ttu-id="45859-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="45859-110">Property value</span></span>

<span data-ttu-id="45859-111">Ein formatiertes **System. String** -Wert, der die aktuelle Position ist.</span><span class="sxs-lookup"><span data-stu-id="45859-111">A formatted **System.String** that is the current position.</span></span>

## <a name="remarks"></a><span data-ttu-id="45859-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45859-112">Remarks</span></span>

<span data-ttu-id="45859-113">Wenn das Medien Element weniger als eine Stunde lang ist, wird die aktuelle Position als mm: SS (Minuten und Sekunden) formatiert.</span><span class="sxs-lookup"><span data-stu-id="45859-113">If the media item is less than an hour long, the current position is formatted as MM:SS (minutes and seconds).</span></span>

## <a name="examples"></a><span data-ttu-id="45859-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45859-114">Examples</span></span>

<span data-ttu-id="45859-115">Im folgenden Beispiel wird ein Timer gestartet, der ein Ereignis in Intervallen von einer Sekunde auslöst.</span><span class="sxs-lookup"><span data-stu-id="45859-115">The following example starts a timer that triggers an event at one-second intervals.</span></span> <span data-ttu-id="45859-116">Im Timer-Ereignishandler wird eine Bezeichnung mit **currentpositionstring** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="45859-116">In the timer event handler, a label is updated with the **currentPositionString**.</span></span> <span data-ttu-id="45859-117">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="45859-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 
   
// Update the text of the label with the currentPositionString.
private void TimerEventProcessor(object sender, System.EventArgs e)
{
    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString;
}
```


```VB

' Set the timer to fire an event every second and start the timer.
timer.Interval = 1000
timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
&#39; determine when to start and stop the timer. 

&#39; Update the text of the label with the currentPositionString.
Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString

End Sub
```





## <a name="requirements"></a><span data-ttu-id="45859-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45859-118">Requirements</span></span>



| <span data-ttu-id="45859-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45859-119">Requirement</span></span> | <span data-ttu-id="45859-120">Wert</span><span class="sxs-lookup"><span data-stu-id="45859-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45859-121">Version</span><span class="sxs-lookup"><span data-stu-id="45859-121">Version</span></span><br/>   | <span data-ttu-id="45859-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="45859-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="45859-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="45859-123">Namespace</span></span><br/> | <span data-ttu-id="45859-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="45859-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="45859-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="45859-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="45859-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="45859-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45859-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45859-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45859-128">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="45859-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="45859-129">**Iwmpcontrols. CurrentPosition (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="45859-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





