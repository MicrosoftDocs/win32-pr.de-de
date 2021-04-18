---
title: Iwmpmedia durationString-Eigenschaft
description: Die durationString-Eigenschaft ruft eine Zeichenfolge ab, die die Dauer des aktuellen Medien Elements im hh mm ss-Format angibt.
ms.assetid: de33c737-d73e-41f0-9c1b-944279194738
keywords:
- durationString-Eigenschaft, Fenster Media Player
- durationString-Eigenschaft, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, durationString (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPMedia.durationString
- IWMPMedia.get_durationString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e6bc732388036aa9e79aeedd988de94fa263bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358746"
---
# <a name="iwmpmediadurationstring-property"></a><span data-ttu-id="960ca-106">Iwmpmedia::d urationstring-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="960ca-106">IWMPMedia::durationString property</span></span>

<span data-ttu-id="960ca-107">Die **durationString** -Eigenschaft ruft eine Zeichenfolge ab, die die Dauer des aktuellen Medien Elements im Format "hh: mm: SS" angibt.</span><span class="sxs-lookup"><span data-stu-id="960ca-107">The **durationString** property gets a string indicating the duration of the current media item in HH:MM:SS format.</span></span>

<span data-ttu-id="960ca-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="960ca-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="960ca-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="960ca-109">Syntax</span></span>


```CSharp
public System.String durationString {get;}
```


```VB

Public ReadOnly Property durationString As System.String
```





## <a name="property-value"></a><span data-ttu-id="960ca-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="960ca-110">Property value</span></span>

<span data-ttu-id="960ca-111">Ein **System. String** -Wert, der die Dauer ist.</span><span class="sxs-lookup"><span data-stu-id="960ca-111">A **System.String** that is the duration.</span></span>

## <a name="remarks"></a><span data-ttu-id="960ca-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="960ca-112">Remarks</span></span>

<span data-ttu-id="960ca-113">Wenn diese Eigenschaft mit einem anderen als dem in AxWindowsMediaPlayer. currentMedia angegebenen Medien Element verwendet wird, enthält Sie möglicherweise keinen gültigen Wert.</span><span class="sxs-lookup"><span data-stu-id="960ca-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span> <span data-ttu-id="960ca-114">Wenn das Medien Element weniger als eine Stunde lang ist, wird der Stunden Teil des Rückgabewerts ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="960ca-114">If the media item is less than an hour long, the hours portion of the return value is omitted.</span></span>

<span data-ttu-id="960ca-115">Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="960ca-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="960ca-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="960ca-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="960ca-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="960ca-117">Examples</span></span>

<span data-ttu-id="960ca-118">Im folgenden Beispiel wird **durationString** verwendet, um die Dauer des aktuellen Medien Elements als formatierten Text in einer Bezeichnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="960ca-118">The following example uses **durationString** to display the duration of the current media item as formatted text in a label.</span></span> <span data-ttu-id="960ca-119">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="960ca-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Display the formatted duration string in the label.
         mediaDuration.Text = player.currentMedia.durationString;
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = 13) Then

        &#39; Display the formatted duration string in the label.
        mediaDuration.Text = player.currentMedia.durationString

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="960ca-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="960ca-120">Requirements</span></span>



| <span data-ttu-id="960ca-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="960ca-121">Requirement</span></span> | <span data-ttu-id="960ca-122">Wert</span><span class="sxs-lookup"><span data-stu-id="960ca-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="960ca-123">Version</span><span class="sxs-lookup"><span data-stu-id="960ca-123">Version</span></span><br/>   | <span data-ttu-id="960ca-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="960ca-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="960ca-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="960ca-125">Namespace</span></span><br/> | <span data-ttu-id="960ca-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="960ca-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="960ca-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="960ca-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="960ca-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="960ca-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="960ca-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="960ca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="960ca-130">**AxWindowsMediaPlayer. currentMedia (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="960ca-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="960ca-131">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="960ca-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="960ca-132">**Iwmpmedia. Duration (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="960ca-132">**IWMPMedia.duration (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)
</dt> </dl>

 

 





