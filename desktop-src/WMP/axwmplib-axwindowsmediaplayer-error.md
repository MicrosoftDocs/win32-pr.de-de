---
title: Fehler Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Error-Ereignis tritt auf, wenn das Windows Media Player-Steuerelement einen Fehlerzustand aufweist.
ms.assetid: d28c18a9-c650-4169-989b-8727b7a5a831
keywords:
- Fehler Ereignis der "AxWindowsMediaPlayer"-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- Error Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfd3571538aa2cdd263a9f5d57e479e73818806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353803"
---
# <a name="error-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="6a33f-104">Fehler Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="6a33f-104">Error Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="6a33f-105">Das Error-Ereignis tritt auf, wenn das Windows Media Player-Steuerelement einen Fehlerzustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="6a33f-105">The Error event occurs when the Windows Media Player control has an error condition.</span></span>

``` syntax
[C#]
private void player_ErrorEvent(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_ErrorEvent(  
  sender As Object,  
  e As System.EventArgs
) Handles player.ErrorEvent
```

## <a name="event-data"></a><span data-ttu-id="6a33f-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="6a33f-106">Event Data</span></span>

<span data-ttu-id="6a33f-107">Dieses Ereignis enthält keine Daten.</span><span class="sxs-lookup"><span data-stu-id="6a33f-107">This event does not contain data.</span></span>

## <a name="examples"></a><span data-ttu-id="6a33f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a33f-108">Examples</span></span>

<span data-ttu-id="6a33f-109">Im folgenden Beispiel wird ein Ereignishandler für das Fehler Ereignis erstellt, um den Beschreibungstext für den ersten Fehler in der Fehler Warteschlange anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6a33f-109">The following example creates an event handler for the Error event to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="6a33f-110">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6a33f-110">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Error event.
player.ErrorEvent += new EventHandler(player_ErrorEvent);

private void player_ErrorEvent(object sender, System.EventArgs e)
{
    // Get the description of the first error. 
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the description of the first error. 
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6a33f-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a33f-111">Requirements</span></span>



| <span data-ttu-id="6a33f-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a33f-112">Requirement</span></span> | <span data-ttu-id="6a33f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6a33f-113">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a33f-114">Version</span><span class="sxs-lookup"><span data-stu-id="6a33f-114">Version</span></span><br/>   | <span data-ttu-id="6a33f-115">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="6a33f-115">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="6a33f-116">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a33f-116">Namespace</span></span><br/> | <span data-ttu-id="6a33f-117">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="6a33f-117">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="6a33f-118">Assembly</span><span class="sxs-lookup"><span data-stu-id="6a33f-118">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6a33f-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6a33f-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a33f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a33f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a33f-121">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6a33f-121">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6a33f-122">**Iwmperror. Item (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6a33f-122">**IWMPError.Item (VB and C#)**</span></span>](iwmperror-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6a33f-123">**Iwmperroritem. ErrorDescription (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6a33f-123">**IWMPErrorItem.errorDescription (VB and C#)**</span></span>](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md)
</dt> </dl>

 

 





