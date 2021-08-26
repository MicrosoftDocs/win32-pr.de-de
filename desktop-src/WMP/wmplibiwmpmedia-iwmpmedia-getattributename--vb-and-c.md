---
title: IWMPMedia getAttributeName-Methode
description: Die getAttributeName-Methode gibt den Namen des Attributs zurück, das dem angegebenen Index entspricht.
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- getAttributeName-Windows Media Player
- getAttributeName-Methode Windows Media Player , IWMPMedia-Schnittstelle
- IWMPMedia-Schnittstelle Windows Media Player , getAttributeName-Methode
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
ms.openlocfilehash: 6ad61be7a611eefc18f408f3f325a45b5f5952e81d53279f04f002f8d87dc2f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031060"
---
# <a name="iwmpmediagetattributename-method"></a>IWMPMedia::getAttributeName-Methode

Die **getAttributeName-Methode** gibt den Namen des Attributs zurück, das dem angegebenen Index entspricht.

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

*lIndex* \[ In\]
</dt> <dd>

Ein **System.Int32,** das der Index ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String,** die der Attributname ist.

## <a name="remarks"></a>Hinweise

Der zurückgegebene Attributname kann in Verbindung mit **getItemInfo** verwendet werden, um den Wert für ein bestimmtes benanntes Attribut abzurufen.

Bevor Sie diese Methode aufrufen, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attributreferenz.](attribute-reference.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **getAttributeName** verwendet, um ein mehrzeilenbasiertes Textfeld mit dem Index und Namen jedes Attributs für das aktuelle Medienelement zu füllen. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getItemInfo (VB und C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





