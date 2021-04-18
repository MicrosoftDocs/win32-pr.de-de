---
title: Iwmperroritem ErrorCode-Eigenschaft
description: Die ErrorCode-Eigenschaft ruft den aktuellen Fehlercode ab.
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- Eigenschaften Fenster für ErrorCode-Eigenschaft Media Player
- ErrorCode-Eigenschaft, Windows Media Player, iwmperroritem-Schnittstelle
- Iwmperroritem-Schnittstelle Windows Media Player, ErrorCode-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f284d5655fc1f4007695a1f681c744a9c5c6fc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365646"
---
# <a name="iwmperroritemerrorcode-property"></a><span data-ttu-id="f4f89-106">Iwmperroritem:: ErrorCode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f4f89-106">IWMPErrorItem::errorCode property</span></span>

<span data-ttu-id="f4f89-107">Die **errorCode** -Eigenschaft ruft den aktuellen Fehlercode ab.</span><span class="sxs-lookup"><span data-stu-id="f4f89-107">The **errorCode** property gets the current error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f89-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4f89-108">Syntax</span></span>


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="f4f89-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f4f89-109">Property value</span></span>

<span data-ttu-id="f4f89-110">Ein **System. Int32** , das den Fehlercode ist.</span><span class="sxs-lookup"><span data-stu-id="f4f89-110">A **System.Int32** that is the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4f89-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4f89-111">Remarks</span></span>

<span data-ttu-id="f4f89-112">Sie sollten **iwmpsettings. enableerrordialogs** auf **false** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="f4f89-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="f4f89-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4f89-113">Examples</span></span>

<span data-ttu-id="f4f89-114">Im folgenden Beispiel wird **errorCode** in einem Fehler Ereignishandler verwendet, um den Fehlercode für den Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f4f89-114">The following example uses **errorCode** in an Error event handler to display the error code to the user.</span></span> <span data-ttu-id="f4f89-115">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f4f89-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f4f89-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4f89-116">Requirements</span></span>



| <span data-ttu-id="f4f89-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4f89-117">Requirement</span></span> | <span data-ttu-id="f4f89-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f4f89-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f89-119">Version</span><span class="sxs-lookup"><span data-stu-id="f4f89-119">Version</span></span><br/>   | <span data-ttu-id="f4f89-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="f4f89-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f4f89-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4f89-121">Namespace</span></span><br/> | <span data-ttu-id="f4f89-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f4f89-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f4f89-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="f4f89-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f4f89-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f4f89-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f89-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4f89-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f89-126">**Iwmperroritem-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f4f89-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4f89-127">**Iwmpsettings. enableerrordialogs (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f4f89-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





