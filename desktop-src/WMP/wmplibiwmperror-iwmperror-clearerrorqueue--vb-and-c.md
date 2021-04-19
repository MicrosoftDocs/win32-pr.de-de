---
title: Iwmperror clearerrorqueue-Methode
description: Mit der clearerrorqueue-Methode werden die Fehler in der Fehler Warteschlange gelöscht. | Iwmperror clearerrorqueue-Methode
ms.assetid: a8e8e666-56e4-4e75-9ed5-2714d272ce7c
keywords:
- clearerrorqueue-Methode, Windows Media Player
- clearerrorqueue-Methode, Windows Media Player, iwmperror-Schnittstelle
- Iwmperror-Schnittstelle, Windows Media Player, clearerrorqueue-Methode
topic_type:
- apiref
api_name:
- IWMPError.clearErrorQueue
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c3f422a9bc32049106d83c970bd8d2c9b2110f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367091"
---
# <a name="iwmperrorclearerrorqueue-method"></a><span data-ttu-id="64f53-107">Iwmperror:: clearerrorqueue-Methode</span><span class="sxs-lookup"><span data-stu-id="64f53-107">IWMPError::clearErrorQueue method</span></span>

<span data-ttu-id="64f53-108">Mit der **clearerrorqueue** -Methode werden die Fehler in der Fehler Warteschlange gelöscht.</span><span class="sxs-lookup"><span data-stu-id="64f53-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="64f53-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="64f53-109">Syntax</span></span>


```CSharp
public void clearErrorQueue();
```


```VB

Public Sub clearErrorQueue()
Implements IWMPError.clearErrorQueue
```





## <a name="parameters"></a><span data-ttu-id="64f53-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64f53-110">Parameters</span></span>

<span data-ttu-id="64f53-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="64f53-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64f53-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64f53-112">Return value</span></span>

<span data-ttu-id="64f53-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="64f53-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64f53-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64f53-114">Remarks</span></span>

<span data-ttu-id="64f53-115">Verwenden Sie diese Methode, um die Fehler Warteschlange zu löschen, nachdem eine Reihe von Fehlern verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="64f53-115">Use this method to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="64f53-116">Sie sollten **iwmpsettings. enableerrordialogs** auf **false** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="64f53-116">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="64f53-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64f53-117">Examples</span></span>

<span data-ttu-id="64f53-118">Im folgenden Beispiel wird **clearerrorqueue** in einem Fehler Ereignishandler verwendet, um die Fehler Warteschlange zu leeren, nachdem alle Fehlerbeschreibungen angezeigt wurden.</span><span class="sxs-lookup"><span data-stu-id="64f53-118">The following example uses **clearErrorQueue** in an Error event handler to empty the error queue after all error descriptions have been displayed.</span></span> <span data-ttu-id="64f53-119">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="64f53-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_clearErrorQueue(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Loop through the list of errors.
    for (int i = 0; i < max; i++)
    {
        // Get the description for this error.
        string errDesc = player.Error.get_Item(i).errorDescription;

        // Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc);
    }

    // Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue();
}
```


```VB

Public Sub player_ErrorEvent_clearErrorQueue(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Loop through the list of errors.
    For i As Integer = 0 To (max - 1)

        &#39; Get the description for this error.
        Dim errDesc As String = player.Error.Item(i).errorDescription

        &#39; Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc)

    Next i

    &#39; Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="64f53-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64f53-120">Requirements</span></span>



| <span data-ttu-id="64f53-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64f53-121">Requirement</span></span> | <span data-ttu-id="64f53-122">Wert</span><span class="sxs-lookup"><span data-stu-id="64f53-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64f53-123">Version</span><span class="sxs-lookup"><span data-stu-id="64f53-123">Version</span></span><br/>   | <span data-ttu-id="64f53-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="64f53-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="64f53-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="64f53-125">Namespace</span></span><br/> | <span data-ttu-id="64f53-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="64f53-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="64f53-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="64f53-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="64f53-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="64f53-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64f53-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64f53-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f53-130">**Iwmperror-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="64f53-130">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="64f53-131">**Iwmpsettings. enableerrordialogs (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="64f53-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





