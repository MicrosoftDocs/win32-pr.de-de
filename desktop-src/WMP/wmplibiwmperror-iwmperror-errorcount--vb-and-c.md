---
title: Iwmperror errorCount (Eigenschaft)
description: Die errorCount-Eigenschaft ruft die Anzahl der Fehler in der Fehler Warteschlange ab.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- errorCount-Eigenschaft, Windows Media Player
- errorCount-Eigenschaft, Windows Media Player, iwmperror-Schnittstelle
- Iwmperror-Schnittstelle, Windows Media Player, errorCount (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371308"
---
# <a name="iwmperrorerrorcount-property"></a><span data-ttu-id="51d63-106">Iwmperror:: errorCount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="51d63-106">IWMPError::errorCount property</span></span>

<span data-ttu-id="51d63-107">Die **errorCount** -Eigenschaft ruft die Anzahl der Fehler in der Fehler Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="51d63-107">The **errorCount** property gets the number of errors in the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="51d63-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="51d63-108">Syntax</span></span>


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="51d63-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="51d63-109">Property value</span></span>

<span data-ttu-id="51d63-110">Ein **System. Int32** -Wert, der die Anzahl der Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="51d63-110">A **System.Int32** that is the number of errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="51d63-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51d63-111">Remarks</span></span>

<span data-ttu-id="51d63-112">Sie sollten **iwmpsettings. enableerrordialogs** auf **false** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="51d63-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="51d63-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51d63-113">Examples</span></span>

<span data-ttu-id="51d63-114">Im folgenden Beispiel wird **errorCount** in einem Fehler Ereignishandler verwendet, um den Benutzer über den letzten Fehler in der Fehler Warteschlange zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="51d63-114">The following example uses **errorCount** in an Error event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="51d63-115">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="51d63-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="51d63-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51d63-116">Requirements</span></span>



| <span data-ttu-id="51d63-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51d63-117">Requirement</span></span> | <span data-ttu-id="51d63-118">Wert</span><span class="sxs-lookup"><span data-stu-id="51d63-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51d63-119">Version</span><span class="sxs-lookup"><span data-stu-id="51d63-119">Version</span></span><br/>   | <span data-ttu-id="51d63-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="51d63-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="51d63-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="51d63-121">Namespace</span></span><br/> | <span data-ttu-id="51d63-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="51d63-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="51d63-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="51d63-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="51d63-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="51d63-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51d63-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51d63-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51d63-126">**Iwmperror-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51d63-126">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51d63-127">**Iwmpsettings. enableerrordialogs (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51d63-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





