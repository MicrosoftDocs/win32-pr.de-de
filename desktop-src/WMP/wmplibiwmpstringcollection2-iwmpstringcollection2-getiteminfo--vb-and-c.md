---
title: IWMPStringCollection2 getiteminfo-Methode
description: Die getiteminfo-Methode gibt die Zeichenfolge zurück, die dem angegebenen Index und Namen des Zeichen folgen Auflistungs Elements entspricht.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2 Interface, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4741c4a3ba74b03038974d8b66bc42c23830ebb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372682"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a>IWMPStringCollection2:: getiteminfo-Methode

Die **getiteminfo** -Methode gibt die Zeichenfolge zurück, die dem angegebenen Index und Namen des Zeichen folgen Auflistungs Elements entspricht.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lcollectionindex* \[ in\]
</dt> <dd>

Der **System. Int32** -Wert, der den NULL basierten Index des Zeichen folgen-Sammel Elements angibt, aus dem das Attribut abgeleitet werden soll.

</dd> <dt>

*bstritemname* \[ in\]
</dt> <dd>

Der **System. String** -Wert, der der Attribut Name ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der **System. String** -Wert, der der Name des Zeichen folgen-Sammel Elements ist. Bei Attributen, deren zugrunde liegender Wert **System. Boolean** ist, wird die Zeichenfolge "true" oder "false" zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Um Attribute mit mehreren Werten und Attributen mit komplexen Werten abzurufen, verwenden Sie die **getItemInfoByType** -Methode.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPStringCollection2-Schnittstelle**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfoByType (VB und c#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





