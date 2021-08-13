---
title: IWMPMedia isReadOnlyItem-Methode
description: Die isReadOnlyItem-Methode gibt einen Wert zurück, der angibt, ob die Attribute des angegebenen Medienelements bearbeitet werden können.
ms.assetid: c810c5c1-8cb9-4ac7-ac49-1ebdc86f5d7f
keywords:
- isReadOnlyItem-Methode Windows Media Player
- isReadOnlyItem-Methode Windows Media Player , IWMPMedia-Schnittstelle
- IWMPMedia-Schnittstelle Windows Media Player , isReadOnlyItem-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.isReadOnlyItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcfd6ef631ed1a3e8159c91bd26e637fc9f22c9b3aa61594555ce1e5ede9c81f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464990"
---
# <a name="iwmpmediaisreadonlyitem-method"></a>IWMPMedia::isReadOnlyItem-Methode

Die **isReadOnlyItem-Methode** gibt einen Wert zurück, der angibt, ob die Attribute des angegebenen Medienelements bearbeitet werden können.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean isReadOnlyItem(
  System.String bstrItemName
);
```


```VB

Public Function isReadOnlyItem( _
  ByVal bstrItemName As System.String _
) As System.Boolean
Implements IWMPMedia.isReadOnlyItem
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrItemName* \[ In\]
</dt> <dd>

Eine **System.String,** die der Name des Medienelements ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System.Boolean-Wert,** der angibt, ob die Attribute schreibgeschützt sind.

## <a name="remarks"></a>Hinweise

Wenn ein Attribut schreibgeschützt ist, kann es nicht mit der **setItemInfo-Methode** festgelegt werden. Beachten Sie, dass diese Methode möglicherweise unterschiedliche Werte für ein bestimmtes Attribut zurückgibt, wenn sie mit verschiedenen Versionen von Windows Media Player verwendet wird.

Vor dem Aufrufen dieser Methode benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel **wird isReadOnlyItem** verwendet, um ein mehrzeiliges Textfeld mit Informationen zum aktuellen Medienelement auszufüllen. Der Code zeigt jedes Attribut des aktuellen Medienelements zusammen mit Text an, der angibt, ob das Attribut schreibgeschützt oder lese-/schreibgeschützt ist. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Store a WMPLib.IWMPMedia3 interface to the current media item.
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes in the current media item.
int attCount = player.currentMedia.attributeCount;

// Create an array to store the list of attribute information.
string[] atInfo = new string[attCount];

// Create a variable to hold each attribute name.
string atName;

// Loop through the attribute list.
for (int i = 0; i < cm.attributeCount; i++)
{
    // Get the attribute name.
    atName = cm.getAttributeName(i);

    // Test whether the attribute is read-only.
    string test = ((cm.isReadOnlyItem(atName)) ? "Read-Only" : "Read/Write");

    // Store the attribute information in the array.
    atInfo[i] = (atName + " is " + test);
}

// Display the attribute information in the text box.
rwText.Lines = atInfo;
```


```VB

' Store a WMPLib.IWMPMedia3 interface to the current media item.
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes in the current media item.
Dim attCount As Integer = player.currentMedia.attributeCount

&#39; Create an array to store the list of attribute information.
Dim atInfo(attCount) As String

&#39; Create a variable to hold each attribute name.
Dim atName As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (cm.attributeCount - 1)

    &#39; Get the attribute name.
    atName = cm.getAttributeName(i)

    &#39; Test whether the attribute is read-only.
    If (cm.isReadOnlyItem(atName)) Then

        atInfo(i) = (atName + &quot; is Read-Only&quot;)

    Else

        atInfo(i) = (atName + &quot; is Read/Write&quot;)

    End If

Next i

&#39; Display the attribute information in the text box.
rwText.Lines = atInfo
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.setItemInfo (VB und C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





