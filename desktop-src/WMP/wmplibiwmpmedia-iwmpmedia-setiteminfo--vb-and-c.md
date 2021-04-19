---
title: Iwmpmedia-Methode "* titeminfo"
description: Die setiteminfo-Methode legt den Wert des angegebenen Attributs für das Medien Element fest.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- Media Player der Methode "stiteminfo"
- Methode "stiteminfo", Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, Methode "stiteminfo"
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6702c80c13090a370e2922ccecade49bc06645de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356499"
---
# <a name="iwmpmediasetiteminfo-method"></a><span data-ttu-id="1e72d-106">Iwmpmedia:: abtiteminfo-Methode</span><span class="sxs-lookup"><span data-stu-id="1e72d-106">IWMPMedia::setItemInfo method</span></span>

<span data-ttu-id="1e72d-107">Die **setiteminfo** -Methode legt den Wert des angegebenen Attributs für das Medien Element fest.</span><span class="sxs-lookup"><span data-stu-id="1e72d-107">The **setItemInfo** method sets the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e72d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e72d-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="1e72d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e72d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e72d-110">*bstritemname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e72d-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e72d-111">Ein **System. String** -Wert, der der Attribut Name ist.</span><span class="sxs-lookup"><span data-stu-id="1e72d-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="1e72d-112">*bstrauval* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e72d-112">*bstrVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e72d-113">Ein **System. String** -Wert, der der neue Wert ist.</span><span class="sxs-lookup"><span data-stu-id="1e72d-113">A **System.String** that is the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e72d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e72d-114">Return value</span></span>

<span data-ttu-id="1e72d-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1e72d-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e72d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e72d-116">Remarks</span></span>

<span data-ttu-id="1e72d-117">Die **AttributeCount** -Eigenschaft ruft die Anzahl der für ein bestimmtes Medien Element verfügbaren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="1e72d-117">The **attributeCount** property gets the number of attributes available for a given media item.</span></span> <span data-ttu-id="1e72d-118">Index Nummern können dann mit der **GetAttributeName** -Methode verwendet werden, um die Namen der integrierten Attribute zu bestimmen, die mit dieser Methode verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1e72d-118">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="1e72d-119">Verwenden Sie vor der Verwendung dieser Methode die **isread onlyitem** -Methode, um zu ermitteln, ob ein bestimmtes Attribut festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1e72d-119">Before using this method, use the **isReadOnlyItem** method to discover whether a particular attribute can be set.</span></span>

<span data-ttu-id="1e72d-120">Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="1e72d-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="1e72d-121">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1e72d-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="1e72d-122">Hinweis</span><span class="sxs-lookup"><span data-stu-id="1e72d-122">Note</span></span>

<span data-ttu-id="1e72d-123">Wenn Sie das Windows Media Player-Steuerelement in Ihre Anwendung einbetten, werden Dateiattribute, die Sie ändern, erst dann in die digitale Mediendatei geschrieben, wenn der Benutzer Windows Media Player ausführt.</span><span class="sxs-lookup"><span data-stu-id="1e72d-123">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="1e72d-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e72d-124">Examples</span></span>

<span data-ttu-id="1e72d-125">Im folgenden Beispiel wird der Wert des Genre-Attributs für das aktuelle Medien Element mithilfe von " **sminfo** " geändert.</span><span class="sxs-lookup"><span data-stu-id="1e72d-125">The following example uses **setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="1e72d-126">Ein Textfeld ermöglicht dem Benutzer die Eingabe einer Zeichenfolge, die dann verwendet wird, um die Attributinformationen als Reaktion auf das Click-Ereignis einer Schaltfläche zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1e72d-126">A text box allows the user to enter a string, which is then used to change the attribute information in response to the Click event of a button.</span></span> <span data-ttu-id="1e72d-127">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1e72d-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1e72d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e72d-128">Requirements</span></span>



| <span data-ttu-id="1e72d-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e72d-129">Requirement</span></span> | <span data-ttu-id="1e72d-130">Wert</span><span class="sxs-lookup"><span data-stu-id="1e72d-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e72d-131">Version</span><span class="sxs-lookup"><span data-stu-id="1e72d-131">Version</span></span><br/>   | <span data-ttu-id="1e72d-132">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="1e72d-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1e72d-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e72d-133">Namespace</span></span><br/> | <span data-ttu-id="1e72d-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1e72d-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1e72d-135">Assembly</span><span class="sxs-lookup"><span data-stu-id="1e72d-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1e72d-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1e72d-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e72d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e72d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e72d-138">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1e72d-138">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1e72d-139">**Iwmpmedia. AttributeCount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1e72d-139">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1e72d-140">**Iwmpmedia. GetAttributeName (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1e72d-140">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1e72d-141">**Iwmpmedia. isleseronlyitem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1e72d-141">**IWMPMedia.isReadOnlyItem (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





