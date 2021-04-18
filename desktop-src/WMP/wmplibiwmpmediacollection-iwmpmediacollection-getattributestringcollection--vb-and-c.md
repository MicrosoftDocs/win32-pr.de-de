---
title: Iwmpmediacollection getAttributeStringCollection-Methode
description: Die getAttributeStringCollection-Methode gibt eine iwmpstringcollection-Schnittstelle zurück, die den Satz aller Werte für ein angegebenes Attribut innerhalb eines Medientyps darstellt.
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- getAttributeStringCollection-Methode, Windows Media Player
- getAttributeStringCollection-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection-Schnittstelle Windows Media Player, getAttributeStringCollection-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAttributeStringCollection
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef25cd811890e82273fd5d634633e25e7ec460c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365838"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a><span data-ttu-id="18cb8-106">Iwmpmediacollection:: getAttributeStringCollection-Methode</span><span class="sxs-lookup"><span data-stu-id="18cb8-106">IWMPMediaCollection::getAttributeStringCollection method</span></span>

<span data-ttu-id="18cb8-107">Die **getAttributeStringCollection** -Methode gibt eine **iwmpstringcollection** -Schnittstelle zurück, die den Satz aller Werte für ein angegebenes Attribut innerhalb eines Medientyps darstellt.</span><span class="sxs-lookup"><span data-stu-id="18cb8-107">The **getAttributeStringCollection** method returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="18cb8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="18cb8-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getAttributeStringCollection(
  System.String bstrAttribute,
  System.String bstrMediaType
);
```


```VB

Public Function getAttributeStringCollection( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPStringCollection
Implements IWMPMediaCollection.getAttributeStringCollection
```





## <a name="parameters"></a><span data-ttu-id="18cb8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="18cb8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18cb8-110">*bstrattribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18cb8-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18cb8-111">Ein **System. String** -Attribut, das das Attribut ist, für das die Werte abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="18cb8-111">A **System.String** that is the attribute for which the values are retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="18cb8-112">*bstraumediatype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18cb8-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18cb8-113">Eine **System. String** , bei der es sich um den Medientyp handelt, für den die Werte abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="18cb8-113">A **System.String** that is the media type for which the values are retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18cb8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18cb8-114">Return value</span></span>

<span data-ttu-id="18cb8-115">Eine **WMPLib. iwmpstringcollection** -Schnittstelle für die abgerufenen Werte.</span><span class="sxs-lookup"><span data-stu-id="18cb8-115">A **WMPLib.IWMPStringCollection** interface for the retrieved values.</span></span>

## <a name="remarks"></a><span data-ttu-id="18cb8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18cb8-116">Remarks</span></span>

<span data-ttu-id="18cb8-117">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="18cb8-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="18cb8-118">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="18cb8-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="18cb8-119">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="18cb8-119">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="18cb8-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18cb8-120">Examples</span></span>

<span data-ttu-id="18cb8-121">Im folgenden Beispiel wird mit **getAttributeStringCollection** eine Liste von Werten angezeigt, die einem bestimmten Attribut für Audioelemente in der Mediensammlung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="18cb8-121">The following example uses **getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="18cb8-122">Ein Listenfeld ermöglicht dem Benutzer das Auswählen eines Attributs, z. b. "Artist", "Genre" oder "Album", und ein mehrzeilige Textfeld zeigt das Ergebnis an.</span><span class="sxs-lookup"><span data-stu-id="18cb8-122">A list box allows the user to select an attribute, such as Artist, Genre, or Album and a multi-line text box displays the result.</span></span> <span data-ttu-id="18cb8-123">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="18cb8-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void audioAttributes_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Retrieve the attribute type from the ListBox
    string attributeType = (string)((System.Windows.Forms.ListBox)sender).SelectedItem;

    // Get an interface to the mediaCollection.  
    WMPLib.IWMPMediaCollection2 library = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

    // Get an interface to the string collection for the attribute type the user selects.
    WMPLib.IWMPStringCollection2 all = (WMPLib.IWMPStringCollection2)library.getAttributeStringCollection(attributeType, "Audio");

    // Clear the text box of previous results.
    attributeValues.Clear();

    // Create an array to hold the attribute values.
    string[] attributeArray = new string[all.count];
    
    // Loop through the string collection.
    for (int i = 0; i < all.count; i++)
    {
        // Store the items in the array.
        attributeArray[i] = all.Item(i);
    }

    // Display the items in the text box.
    attributeValues.Lines = attributeArray;
}
```


```VB

Public Sub audioAttributes_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles audioAttributes.SelectedIndexChanged

    &#39; Retrieve the attribute type from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim attributeType As String = lb.SelectedItem

    &#39; Get an interface to the mediaCollection.  
    Dim library As WMPLib.IWMPMediaCollection2 = player.mediaCollection

    &#39; Get an interface to the string collection for the attribute type the user selects.
    Dim all As WMPLib.IWMPStringCollection2 = library.getAttributeStringCollection(attributeType, &quot;Audio&quot;)

    &#39; Clear the text box of previous results.
    attributeValues.Clear()

    &#39; Create an array to hold the attribute values.
    Dim attributeArray(all.count) As String

    &#39; Loop through the string collection.
    For i As Integer = 0 To (all.count - 1)

        &#39; Store the items in the array.
        attributeArray(i) = all.Item(i)

    Next i

    &#39; Display the items in the text box.
    attributeValues.Lines = attributeArray

End Sub
```





## <a name="requirements"></a><span data-ttu-id="18cb8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18cb8-124">Requirements</span></span>



| <span data-ttu-id="18cb8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18cb8-125">Requirement</span></span> | <span data-ttu-id="18cb8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="18cb8-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18cb8-127">Version</span><span class="sxs-lookup"><span data-stu-id="18cb8-127">Version</span></span><br/>   | <span data-ttu-id="18cb8-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="18cb8-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="18cb8-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="18cb8-129">Namespace</span></span><br/> | <span data-ttu-id="18cb8-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="18cb8-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="18cb8-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="18cb8-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="18cb8-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="18cb8-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18cb8-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18cb8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18cb8-134">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="18cb8-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18cb8-135">**Iwmpstringcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="18cb8-135">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





