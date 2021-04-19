---
title: Iwmpnetwork bufferingcount (Eigenschaft)
description: Die bufferingcount-Eigenschaft ruft die Häufigkeit ab, mit der die Pufferung während der Wiedergabe aufgetreten ist.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- bufferingcount-Eigenschaft, Windows-Media Player
- bufferingcount-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, bufferingcount (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4958892dd9784ee72b51adfedbbcdee81817b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373660"
---
# <a name="iwmpnetworkbufferingcount-property"></a><span data-ttu-id="5548f-106">Iwmpnetwork:: bufferingcount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5548f-106">IWMPNetwork::bufferingCount property</span></span>

<span data-ttu-id="5548f-107">Die **bufferingcount** -Eigenschaft ruft die Häufigkeit ab, mit der die Pufferung während der Wiedergabe aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5548f-107">The **bufferingCount** property gets the number of times buffering occurred during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="5548f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5548f-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="5548f-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5548f-109">Property value</span></span>

<span data-ttu-id="5548f-110">Ein **System. Int32** -Wert, der die Puffer Anzahl ist.</span><span class="sxs-lookup"><span data-stu-id="5548f-110">A **System.Int32** that is the buffering count.</span></span>

## <a name="remarks"></a><span data-ttu-id="5548f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5548f-111">Remarks</span></span>

<span data-ttu-id="5548f-112">Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5548f-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="5548f-113">Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5548f-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="5548f-114">Die Pufferung gilt nur für Streaminginhalte.</span><span class="sxs-lookup"><span data-stu-id="5548f-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="5548f-115">Diese Eigenschaft ruft nur während der Laufzeit gültige Informationen ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer. URL** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5548f-115">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="5548f-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5548f-116">Examples</span></span>

<span data-ttu-id="5548f-117">Im folgenden Beispiel wird *bufferingcount* verwendet, um anzuzeigen, wie oft Pufferung während der Wiedergabe auftritt.</span><span class="sxs-lookup"><span data-stu-id="5548f-117">The following example uses *bufferingCount* to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="5548f-118">Die Informationen werden in einer Bezeichnung als Reaktion auf das Puffer Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5548f-118">The information is displayed in a label in response to the Buffering Event.</span></span> <span data-ttu-id="5548f-119">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5548f-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="5548f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5548f-120">Requirements</span></span>



| <span data-ttu-id="5548f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5548f-121">Requirement</span></span> | <span data-ttu-id="5548f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5548f-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5548f-123">Version</span><span class="sxs-lookup"><span data-stu-id="5548f-123">Version</span></span><br/>   | <span data-ttu-id="5548f-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="5548f-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5548f-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="5548f-125">Namespace</span></span><br/> | <span data-ttu-id="5548f-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5548f-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5548f-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="5548f-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5548f-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5548f-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5548f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5548f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5548f-130">**AxWindowsMediaPlayer. URL (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5548f-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5548f-131">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5548f-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





