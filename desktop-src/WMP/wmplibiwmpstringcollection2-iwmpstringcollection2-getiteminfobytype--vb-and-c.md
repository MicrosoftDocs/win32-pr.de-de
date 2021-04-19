---
title: IWMPStringCollection2 getItemInfoByType-Methode
description: Die getItemInfoByType-Methode gibt den Wert zurück, der dem angegebenen Index, dem Namen, der Sprache und dem Attribut Index für Zeichen folgen Auflistungs Elemente entspricht.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- getItemInfoByType-Methode, Windows Media Player
- getItemInfoByType-Methode, Windows Media Player, IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2 Interface, Windows Media Player, getItemInfoByType-Methode
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366851"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a>IWMPStringCollection2:: getItemInfoByType-Methode

Die **getItemInfoByType** -Methode gibt den Wert zurück, der dem angegebenen Index, dem Namen, der Sprache und dem Attribut Index für Zeichen folgen Auflistungs Elemente entspricht.

## <a name="syntax"></a>Syntax


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lcollectionindex* \[ in\]
</dt> <dd>

Der **System. Int32** -Wert, der der null basierte Index des Zeichen folgen-Sammel Elements ist, aus dem das Attribut abgeleitet werden soll.

</dd> <dt>

*bstrintype* \[ in\]
</dt> <dd>

Der **System. String** -Wert, der der Attribut Name ist.

</dd> <dt>

*bstraulanguage* \[ in\]
</dt> <dd>

Die **System. String** -Wert, der die Sprache angibt. Wenn der Wert auf NULL oder auf eine Zeichenfolge der Länge 0 (null) festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".

</dd> <dt>

*lattributeindex* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der der null basierte Index des Attributs ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Object** , das das Zeichen folgen Auflistungs Element ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode unterstützt Attribute mit mehreren Werten und Attributen mit komplexen Werten. Die **getiteminfo** -Methode unterstützt keine Attribute mit mehreren Werten oder Attributen mit komplexen Werten.

Durch Übergeben des Werts "childlist" im *bstrintype* -Parameter können Sie eine neue Zeichen folgen Auflistung abrufen, die die untergeordneten Elemente eines der Elemente in der übergeordneten Zeichen folgen Auflistung enthält. Wenn die übergeordnete Auflistung z. b. eine Liste von albumids enthält, können Sie mit dieser Methode eine untergeordnete Zeichen folgen Auflistung abrufen, die alle Spuren für eines der Alben enthält. Diese Vorgehensweise ist schneller und effizienter als das doppelte Aufrufen der **IWMPMediaCollection2. getstringcollectionbyquery** -Methode. einmal, um eine Auflistung von albumids zu erhalten, und ein zweites Mal, um eine Sammlung von Spuren für eine bestimmte albumId zu erhalten. Um childlist auf die soeben beschriebene Weise zu verwenden, muss die übergeordnete Zeichen folgen Auflistung aus einer Mediensammlung über **iwmplibraryservices** abgerufen werden, und nicht mithilfe der **AxWindowsMediaPlayer. mediacollection** -Eigenschaft.

Wenn Sie childlist verwenden, übergeben Sie den Wert "childlist" im *bstrintype* -Parameter und den Wert "0" im Parameter " *lattributeindex* ". Anschließend können Sie das zurückgegebene-Objekt in eine **IWMPStringCollection2** -Schnittstelle umwandeln, um auf die untergeordnete Liste zuzugreifen.

Um diese Methode verwenden zu können, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AlbumId-Attribut**](albumid-attribute.md)
</dt> <dt>

[**Iwmplibraryservices-Schnittstelle (VB und c#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getstringcollectionbyquery (VB und c#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2-Schnittstelle**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getiteminfo (VB und c#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





