---
title: Iwmpnetwork, lostpakete (Eigenschaft)
description: Die lostpaketen-Eigenschaft ruft die Anzahl der verlorenen Pakete ab.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- Eigenschaften Fenster von "lostpakete" Media Player
- lostpaketen-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, lostpakete (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1adac5f4aa8b1f58c023a556af04b8eae4bd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361337"
---
# <a name="iwmpnetworklostpackets-property"></a><span data-ttu-id="3e2bd-106">Iwmpnetwork:: lostpakete (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3e2bd-106">IWMPNetwork::lostPackets property</span></span>

<span data-ttu-id="3e2bd-107">Die **lostpaketen** -Eigenschaft ruft die Anzahl der verlorenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="3e2bd-107">The **lostPackets** property gets the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e2bd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e2bd-108">Syntax</span></span>


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="3e2bd-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3e2bd-109">Property value</span></span>

<span data-ttu-id="3e2bd-110">Ein **System. Int32** -Wert, der die Anzahl verlorener Pakete ist.</span><span class="sxs-lookup"><span data-stu-id="3e2bd-110">A **System.Int32** that is the number of lost packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e2bd-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e2bd-111">Remarks</span></span>

<span data-ttu-id="3e2bd-112">Diese Eigenschaft umfasst nur das Streaming von Medien Paketen und gibt 0 (null) zurück, wenn das HTTP-Protokoll verwendet wird, das verlustfrei ist.</span><span class="sxs-lookup"><span data-stu-id="3e2bd-112">This property includes streaming media packets only, and will return zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="3e2bd-113">Pakete können aus verschiedenen Gründen verloren gehen, z. b. Art und Qualität der Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="3e2bd-113">Packets can be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="3e2bd-114">Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3e2bd-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="3e2bd-115">Der Wert wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="3e2bd-115">The value is not reset if playback is paused.</span></span> <span data-ttu-id="3e2bd-116">Diese Eigenschaft ruft nur während der Laufzeit gültige Informationen ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer. URL** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3e2bd-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="3e2bd-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e2bd-117">Examples</span></span>

<span data-ttu-id="3e2bd-118">Im folgenden Codebeispiel wird **lostpakete** verwendet, um die Gesamtanzahl der während der Wiedergabe verlorenen Pakete anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3e2bd-118">The following code example uses **lostPackets** to display the total number of packets lost during playback.</span></span> <span data-ttu-id="3e2bd-119">Die Informationen werden in einer Bezeichnung angezeigt, wenn der Benutzer auf eine Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="3e2bd-119">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="3e2bd-120">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3e2bd-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3e2bd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e2bd-121">Requirements</span></span>



| <span data-ttu-id="3e2bd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e2bd-122">Requirement</span></span> | <span data-ttu-id="3e2bd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3e2bd-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e2bd-124">Version</span><span class="sxs-lookup"><span data-stu-id="3e2bd-124">Version</span></span><br/>   | <span data-ttu-id="3e2bd-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="3e2bd-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3e2bd-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e2bd-126">Namespace</span></span><br/> | <span data-ttu-id="3e2bd-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3e2bd-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3e2bd-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="3e2bd-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3e2bd-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3e2bd-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e2bd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e2bd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e2bd-131">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3e2bd-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3e2bd-132">**AxWindowsMediaPlayer. URL (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3e2bd-132">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





