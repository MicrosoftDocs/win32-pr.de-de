---
title: IWMPMediaCollection getAttributeStringCollection-Methode
description: Die getAttributeStringCollection-Methode gibt eine IWMPStringCollection-Schnittstelle zurück, die den Satz aller Werte für ein angegebenes Attribut innerhalb eines Medientyps darstellt.
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- getAttributeStringCollection-Methode Windows Media Player
- getAttributeStringCollection-Methode Windows Media Player , IWMPMediaCollection-Schnittstelle
- IWMPMediaCollection-Schnittstelle Windows Media Player , getAttributeStringCollection-Methode
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
ms.openlocfilehash: 508630ee8a377e1542f823c1afb21521206369aa3ce489c58afae47efa268880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331942"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a>IWMPMediaCollection::getAttributeStringCollection-Methode

Die **getAttributeStringCollection-Methode** gibt eine **IWMPStringCollection-Schnittstelle** zurück, die den Satz aller Werte für ein angegebenes Attribut innerhalb eines Medientyps darstellt.

## <a name="syntax"></a>Syntax


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





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrAttribute* \[ In\]
</dt> <dd>

Eine **System.String,** die das Attribut ist, für das die Werte abgerufen werden.

</dd> <dt>

*bstrMediaType* \[ In\]
</dt> <dd>

Eine **System.String-Datei,** bei der es sich um den Medientyp handelt, für den die Werte abgerufen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPStringCollection-Schnittstelle** für die abgerufenen Werte.

## <a name="remarks"></a>Hinweise

Vor dem Aufrufen dieser Methode benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Informationen zu den attributen, die von Windows Media Player unterstützt werden, finden Sie unter [Attributverweis.](attribute-reference.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **getAttributeStringCollection** verwendet, um eine Liste von Werten anzuzeigen, die einem bestimmten Attribut für Audioelemente in der Medienauflistung entsprechen. Mit einem Listenfeld kann der Benutzer ein Attribut auswählen, z. B. Interpret, Genre oder Album, und ein mehrzeiliges Textfeld zeigt das Ergebnis an. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection-Schnittstelle (VB und C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





