---
title: Iwmpwiedergabe. AttributeName (VB und C)
description: Die AttributeName-Eigenschaft (die get \_ attributeName-Methode in C \) Ruft den Namen eines durch einen Index angegebenen Wiedergabelisten Attributs ab.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- Iwmpwiedergabe. AttributeName (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364414"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a>Iwmpwiedergabe. AttributeName (VB und c#)

Die **attributeName** -Eigenschaft (die **get \_ attributeName** -Methode in c#) Ruft den Namen eines durch einen Index angegebenen Wiedergabelisten Attributs ab.


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a>Parameter

*Lindex*

Ein **System. Int32** -Wert, der den Index des Wiedergabelisten Attributs ist.

## <a name="return-value"></a>Rückgabewert

Ein **System. String** -Wert, der der Name des Wiedergabelisten Attributs ist.

## <a name="remarks"></a>Bemerkungen

**Iwmpwiedergabe. AttributeName** ist eine schreibgeschützte Eigenschaft in Visual Basic, die einen-Parameter annimmt, während in c# als **iwmpwiedergabe. get \_ attributeName** -Methode bezeichnet wird.

Die Anzahl der einer Wiedergabeliste zugeordneten Attribute wird von der **iwmpwiedergabe. AttributeCount** -Eigenschaft zurückgegeben.

Der Name, der von dieser Eigenschaft zurückgegeben wird, kann an die Methoden " **ctiteminfo** " oder " **getiteminfo** " übergeben werden, um einen Wert für das benannte Attribut anzugeben oder abzurufen.

Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Weitere Informationen zu Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).

## <a name="examples"></a>Beispiele

Einen Beispielcode, der diese Eigenschaft verwendet, finden Sie unter der [AttributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) -Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. AttributeCount (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. getiteminfo (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. Einstellungs Verzeichnis (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





