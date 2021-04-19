---
title: Iwmpmedia GetAttributeName-Methode
description: Die GetAttributeName-Methode gibt den Namen des Attributs zurück, das dem angegebenen Index entspricht.
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- GetAttributeName-Methode, Windows-Media Player
- GetAttributeName-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, GetAttributeName-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb40ef8c0c984258dc11dd00c80807db2f4eb64a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362095"
---
# <a name="iwmpmediagetattributename-method"></a>Iwmpmedia:: GetAttributeName-Methode

Die **GetAttributeName** -Methode gibt den Namen des Attributs zurück, das dem angegebenen Index entspricht.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*Lindex* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der der Index ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. String** -Wert, der der Attribut Name ist.

## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Attribut Name kann in Verbindung mit **getiteminfo** verwendet werden, um den Wert für ein bestimmtes benanntes Attribut abzurufen.

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **GetAttributeName** verwendet, um ein mehr zeitiges Textfeld mit dem Index und dem Namen der einzelnen Attribute für das aktuelle Medien Element auszufüllen. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. getiteminfo (VB und c#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





