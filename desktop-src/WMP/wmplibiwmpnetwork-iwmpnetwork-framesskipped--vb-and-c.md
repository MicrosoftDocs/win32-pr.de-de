---
title: Iwmpnetwork-framesskipped (Eigenschaft)
description: Die framesskipped-Eigenschaft ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- Eigenschaften Fenster für "framesskipped" Media Player
- framesskipped-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, framesskipped (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366699"
---
# <a name="iwmpnetworkframesskipped-property"></a><span data-ttu-id="34937-106">Iwmpnetwork:: framesskipped (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="34937-106">IWMPNetwork::framesSkipped property</span></span>

<span data-ttu-id="34937-107">Die **framesskipped** -Eigenschaft ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.</span><span class="sxs-lookup"><span data-stu-id="34937-107">The **framesSkipped** property gets the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="34937-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="34937-108">Syntax</span></span>


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="34937-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="34937-109">Property value</span></span>

<span data-ttu-id="34937-110">Ein **System. Int32** -Wert, der die Anzahl der übersprungenen Frames ist.</span><span class="sxs-lookup"><span data-stu-id="34937-110">A **System.Int32** that is the number of frames skipped.</span></span>

## <a name="examples"></a><span data-ttu-id="34937-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34937-111">Examples</span></span>

<span data-ttu-id="34937-112">Im folgenden Codebeispiel wird **framesskipped** verwendet, um die Gesamtzahl der Rahmen anzuzeigen, die während der Wiedergabe ausgelassen wurden.</span><span class="sxs-lookup"><span data-stu-id="34937-112">The following code example uses **framesSkipped** to display the total number of frames skipped during playback.</span></span> <span data-ttu-id="34937-113">Die Informationen werden in einer Bezeichnung angezeigt, wenn der Benutzer auf eine Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="34937-113">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="34937-114">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34937-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="34937-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34937-115">Requirements</span></span>



| <span data-ttu-id="34937-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34937-116">Requirement</span></span> | <span data-ttu-id="34937-117">Wert</span><span class="sxs-lookup"><span data-stu-id="34937-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34937-118">Version</span><span class="sxs-lookup"><span data-stu-id="34937-118">Version</span></span><br/>   | <span data-ttu-id="34937-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="34937-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="34937-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="34937-120">Namespace</span></span><br/> | <span data-ttu-id="34937-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="34937-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="34937-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="34937-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="34937-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="34937-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34937-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34937-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34937-125">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="34937-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





