---
title: Iwmperror. Item (VB und C)
description: Die Item-Eigenschaft (die get \_ Item-Methode in C \) Ruft eine iwmperroritem-Schnittstelle am angegebenen Index in der Fehler Warteschlange ab.
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- Iwmperror. Item (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9217ec772512171c828dd0dad06ec8fe3704dba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370149"
---
# <a name="iwmperroritem-vb-and-c"></a><span data-ttu-id="670c2-104">Iwmperror. Item (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="670c2-104">IWMPError.Item (VB and C#)</span></span>

<span data-ttu-id="670c2-105">Die **Item** -Eigenschaft (die **get \_ Item** -Methode in c#) Ruft eine **iwmperroritem** -Schnittstelle am angegebenen Index in der Fehler Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="670c2-105">The **Item** property (the **get\_Item** method in C#) gets an **IWMPErrorItem** interface at the specified index in the error queue.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="670c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="670c2-106">Parameters</span></span>

<span data-ttu-id="670c2-107">*dwIndex*</span><span class="sxs-lookup"><span data-stu-id="670c2-107">*dwIndex*</span></span>

<span data-ttu-id="670c2-108">Ein **System. Int32** -Wert, der der null basierte Index einer **iwmperroritem** -Schnittstelle in der Fehler Warteschlange ist.</span><span class="sxs-lookup"><span data-stu-id="670c2-108">A **System.Int32** that is the zero-based index of an **IWMPErrorItem** interface in the error queue.</span></span>

## <a name="property-value"></a><span data-ttu-id="670c2-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="670c2-109">Property Value</span></span>

<span data-ttu-id="670c2-110">Eine **WMPLib. iwmperroritem** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="670c2-110">A **WMPLib.IWMPErrorItem** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="670c2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="670c2-111">Remarks</span></span>

<span data-ttu-id="670c2-112">Windows Media Player kann als Reaktion auf eine Fehlerbedingung eine Reihe von Fehlern generieren.</span><span class="sxs-lookup"><span data-stu-id="670c2-112">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="670c2-113">Diese Eigenschaft ruft einen bestimmten Fehler in der Warteschlange mit einer Indexnummer ab.</span><span class="sxs-lookup"><span data-stu-id="670c2-113">This property gets a specific error in the queue by using an index number.</span></span> <span data-ttu-id="670c2-114">Die Indexnummern für die Fehler Warteschlange beginnen mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="670c2-114">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="670c2-115">Sie sollten **iwmpsettings. enableerrordialogs** auf **false** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="670c2-115">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="670c2-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="670c2-116">Examples</span></span>

<span data-ttu-id="670c2-117">Im folgenden Beispiel wird die **Item** -Eigenschaft (die **get \_ Item** -Methode in c#) in einem Fehler Ereignishandler verwendet, um Informationen zum letzten Fehler in der Fehler Warteschlange abzurufen und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="670c2-117">The following example uses the **Item** property (the **get\_Item** method in C#) in an Error event handler to retrieve and display information about the most recent error in the error queue.</span></span> <span data-ttu-id="670c2-118">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="670c2-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="670c2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="670c2-119">Requirements</span></span>



| <span data-ttu-id="670c2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="670c2-120">Requirement</span></span> | <span data-ttu-id="670c2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="670c2-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="670c2-122">Version</span><span class="sxs-lookup"><span data-stu-id="670c2-122">Version</span></span><br/>   | <span data-ttu-id="670c2-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="670c2-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="670c2-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="670c2-124">Namespace</span></span><br/> | <span data-ttu-id="670c2-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="670c2-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="670c2-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="670c2-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="670c2-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="670c2-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670c2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="670c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670c2-129">**Iwmperror-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="670c2-129">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="670c2-130">**Iwmperroritem-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="670c2-130">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="670c2-131">**Iwmpsettings. enableerrordialogs (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="670c2-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





