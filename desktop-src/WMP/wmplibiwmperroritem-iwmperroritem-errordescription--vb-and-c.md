---
title: Iwmperroritem ErrorDescription-Eigenschaft
description: Die ErrorDescription-Eigenschaft ruft eine Beschreibung des Fehlers ab.
ms.assetid: a9914c24-1d10-422a-bcba-80be9fb85108
keywords:
- ErrorDescription-Eigenschaft, Windows-Media Player
- ErrorDescription-Eigenschaft, Windows Media Player, iwmperroritem-Schnittstelle
- Iwmperroritem-Schnittstelle Windows Media Player, ErrorDescription-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8725099d1ce49eae8f378b2571dc4030f60611e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373970"
---
# <a name="iwmperroritemerrordescription-property"></a><span data-ttu-id="5c33a-106">Iwmperroritem:: ErrorDescription-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5c33a-106">IWMPErrorItem::errorDescription property</span></span>

<span data-ttu-id="5c33a-107">Die **ErrorDescription** -Eigenschaft ruft eine Beschreibung des Fehlers ab.</span><span class="sxs-lookup"><span data-stu-id="5c33a-107">The **errorDescription** property gets a description of the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c33a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c33a-108">Syntax</span></span>


```CSharp
public System.String errorDescription {get; set;}
```


```VB

Public ReadOnly Property errorDescription As System.String
```





## <a name="property-value"></a><span data-ttu-id="5c33a-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5c33a-109">Property value</span></span>

<span data-ttu-id="5c33a-110">Ein **System. String** -Wert, der die Fehlerbeschreibung ist.</span><span class="sxs-lookup"><span data-stu-id="5c33a-110">A **System.String** that is the error description.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c33a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c33a-111">Remarks</span></span>

<span data-ttu-id="5c33a-112">Sie sollten **iwmpsettings. enableerrordialogs** auf **false** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="5c33a-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="5c33a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c33a-113">Examples</span></span>

<span data-ttu-id="5c33a-114">Im folgenden Beispiel wird **ErrorDescription** in einem Fehler Ereignishandler verwendet, um die Fehlerbeschreibung für den Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5c33a-114">The following example uses **errorDescription** in an Error event handler to display the error description to the user.</span></span> <span data-ttu-id="5c33a-115">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5c33a-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorDescription(object sender, System.EventArgs e)
{
    // Get the error description for the first error item.
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show("Error: " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorDescription(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error description for the first error item.
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(&quot;Error: &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="5c33a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c33a-116">Requirements</span></span>



| <span data-ttu-id="5c33a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c33a-117">Requirement</span></span> | <span data-ttu-id="5c33a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5c33a-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c33a-119">Version</span><span class="sxs-lookup"><span data-stu-id="5c33a-119">Version</span></span><br/>   | <span data-ttu-id="5c33a-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="5c33a-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5c33a-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c33a-121">Namespace</span></span><br/> | <span data-ttu-id="5c33a-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5c33a-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5c33a-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="5c33a-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5c33a-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5c33a-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c33a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c33a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c33a-126">**Iwmperroritem-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5c33a-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5c33a-127">**Iwmpsettings. enableerrordialogs (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5c33a-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





