---
title: Iwmpnetwork sourceprotocol (Eigenschaft)
description: Die sourceprotocol-Eigenschaft ruft das Quell Protokoll ab, das zum Empfangen von Daten verwendet wird.
ms.assetid: db1d7651-3f25-4ac9-a3e1-dc3a8ddf8c40
keywords:
- sourceprotocol-Eigenschaften Fenster Media Player
- sourceprotocol-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, sourceprotocol (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.sourceProtocol
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5017e1a053c124a1f7f50668c6f392eb541d57f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369268"
---
# <a name="iwmpnetworksourceprotocol-property"></a><span data-ttu-id="7d1b3-106">Iwmpnetwork:: sourceprotocol (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7d1b3-106">IWMPNetwork::sourceProtocol property</span></span>

<span data-ttu-id="7d1b3-107">Die **sourceprotocol** -Eigenschaft ruft das Quell Protokoll ab, das zum Empfangen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d1b3-107">The **sourceProtocol** property gets the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d1b3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d1b3-108">Syntax</span></span>


```CSharp
public System.String sourceProtocol {get; set;}
```


```VB

Public ReadOnly Property sourceProtocol As System.String
```





## <a name="property-value"></a><span data-ttu-id="7d1b3-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7d1b3-109">Property value</span></span>

<span data-ttu-id="7d1b3-110">Ein **System. String** -Wert, der den Namen des Quell Protokolls ist.</span><span class="sxs-lookup"><span data-stu-id="7d1b3-110">A **System.String** that is the name of the source protocol.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d1b3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d1b3-111">Remarks</span></span>

<span data-ttu-id="7d1b3-112">Diese Eigenschaft erhält eine Zeichenfolge der Länge 0 (null) (""), wenn eine CD oder DVD wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7d1b3-112">This property gets a zero-length string ("") when playing a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="7d1b3-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d1b3-113">Examples</span></span>

<span data-ttu-id="7d1b3-114">Im folgenden Codebeispiel wird **sourceprotocol** verwendet, um das Quell Protokoll anzuzeigen, das zum Empfangen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d1b3-114">The following code example uses **sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="7d1b3-115">Die Informationen werden in einer Bezeichnung als Reaktion auf das **PlayStateChange** -Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d1b3-115">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="7d1b3-116">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7d1b3-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the network source protocol when the player is playing by testing for a 
    // play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3. 
    if (e.newState == 3) 
    {
        sourceProtocolLabel.Text = ("Source protocol: " + player.network.sourceProtocol);
    } 
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the network source protocol when the player is playing by testing for a 
    &#39; play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3.
    If (e.newState = 3) Then

        sourceProtocolLabel.Text = (&quot;Source protocol: &quot; + player.network.sourceProtocol)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="7d1b3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d1b3-117">Requirements</span></span>



| <span data-ttu-id="7d1b3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d1b3-118">Requirement</span></span> | <span data-ttu-id="7d1b3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7d1b3-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d1b3-120">Version</span><span class="sxs-lookup"><span data-stu-id="7d1b3-120">Version</span></span><br/>   | <span data-ttu-id="7d1b3-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="7d1b3-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7d1b3-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d1b3-122">Namespace</span></span><br/> | <span data-ttu-id="7d1b3-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7d1b3-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7d1b3-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="7d1b3-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7d1b3-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7d1b3-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d1b3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d1b3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d1b3-127">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="7d1b3-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





