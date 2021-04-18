---
title: IWMPStringCollection2 getattributezähltbytype-Methode
description: Die getattributezähltbytype-Methode gibt die Anzahl der Attribute zurück, die dem angegebenen Zeichen folgen-Sammlungs Index, dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- getattributezähltbytype-Methode, Windows Media Player
- getattributezähltbytype-Methode, Windows Media Player, IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2 Interface Windows Media Player, getattributezähltbytype-Methode
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bb60fdd843fb3f45b6e4e3aff444a8a915fa0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365748"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a>IWMPStringCollection2:: getattributezähltbytype-Methode

Die **getattributezähltbytype** -Methode gibt die Anzahl der Attribute zurück, die dem angegebenen Zeichen folgen-Sammlungs Index, dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lcollectionindex* \[ in\]
</dt> <dd>

Der **System. Int32** -Wert, der den NULL basierten Index des Zeichen folgen-Sammel Elements angibt, aus dem das Attribut abgeleitet werden soll.

</dd> <dt>

*bstrintype* \[ in\]
</dt> <dd>

Die **System. String** -Eigenschaft, die den Namen des Attributs ist.

</dd> <dt>

*bstraulanguage* \[ in\]
</dt> <dd>

Die **System. String** , die den Namen der Sprache hat. Wenn der Wert auf NULL oder auf eine Zeichenfolge der Länge 0 (null) festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der **System. Int32** -Wert, der die Anzahl ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird verwendet, um die Anzahl von Attributen zu ermitteln, die einem bestimmten Attributnamen für ein bestimmtes **StringCollection** -Element entsprechen. Index Nummern können dann an den vierten Parameter der **getItemInfoByType** -Methode übergeben werden.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPStringCollection2-Schnittstelle (VB und c#)**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfoByType (VB und c#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





