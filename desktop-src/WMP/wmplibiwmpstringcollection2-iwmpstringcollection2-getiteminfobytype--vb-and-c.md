---
title: IWMPStringCollection2 getItemInfobyType-Methode
description: Die getItemInfoByType-Methode gibt den Wert zurück, der dem angegebenen Index, Namen, der Sprache und dem Attributindex der Zeichenfolgensammlung entspricht.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- getItemInfobyType-Windows Media Player
- getItemInfobyType-Methode Windows Media Player , IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2-Schnittstelle Windows Media Player , getItemInfobyType-Methode
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
ms.openlocfilehash: cc2894faedc8e2573fad5beaa7744216fbb53fbd1b090e4be2122a3194827f43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899760"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a>IWMPStringCollection2::getItemInfobyType-Methode

Die **getItemInfoByType-Methode** gibt den Wert zurück, der dem angegebenen Index, Namen, der Sprache und dem Attributindex der Zeichenfolgensammlung entspricht.

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

*lCollectionIndex* \[ In\]
</dt> <dd>

Das **System.Int32,** das der nullbasierte Index des Zeichenfolgensammlungselements ist, aus dem das Attribut erhalten werden soll.

</dd> <dt>

*bstrType* \[ In\]
</dt> <dd>

Die **System.String,** die der Attributname ist.

</dd> <dt>

*bstrLanguage* \[ In\]
</dt> <dd>

Die **System.String,die** die Sprache angibt. Wenn der Wert auf NULL oder auf eine Zeichenfolge der Länge 0 (null) festgelegt ist (""), wird die aktuelle Locale String verwendet. Andernfalls muss der Wert eine gültige RFC 1766-Sprachzeichenfolge wie "en-us" sein.

</dd> <dt>

*lAttributeIndex* \[ In\]
</dt> <dd>

Ein **System.Int32,** das der nullbasierte Index des Attributs ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System.Object,** das das Zeichenfolgensammlungselement ist.

## <a name="remarks"></a>Hinweise

Diese Methode unterstützt Attribute mit mehreren Werten und Attribute mit komplexen Werten. Die **getItemInfo-Methode** unterstützt keine Attribute mit mehreren Werten oder Attribute mit komplexen Werten.

Durch Übergeben des Werts "ChildList" im *bstrType-Parameter* können Sie eine neue Zeichenfolgensammlung abrufen, die die untergeordneten Elemente eines der Elemente in der übergeordneten Zeichenfolgensammlung enthält. Wenn die übergeordnete Auflistung beispielsweise eine Liste von AlbumIDs enthält, können Sie diese Methode verwenden, um eine untergeordnete Zeichenfolgensammlung zu erhalten, die alle Titel für eines der Albums enthält. Dieser Ansatz ist schneller und effizienter als das zweimalige Aufrufen der **IWMPMediaCollection2.getStringCollectionByQuery-Methode.** einmal, um eine Sammlung von AlbumIDs zu erhalten, und ein zweites Mal, um eine Sammlung von Titeln für eine bestimmte AlbumID zu erhalten. Um ChildList wie oben beschrieben zu verwenden, muss die übergeordnete Zeichenfolgensammlung aus einer Mediensammlung über **IWMPLibraryServices** und nicht mithilfe der **AxWindowsMediaPlayer.mediaCollection-Eigenschaft erhalten** werden.

Übergeben Sie bei Verwendung von ChildList den Wert "ChildList" im *bstrType-Parameter* und den Wert 0 im *Parameter lAttributeIndex.* Anschließend können Sie das -Objekt, das in eine **IWMPStringCollection2-Schnittstelle** zurückgegeben wird, um auf die untergeordnete Liste zu zugreifen.

Um diese Methode verwenden zu können, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AlbumID-Attribut**](albumid-attribute.md)
</dt> <dt>

[**IWMPLibraryServices-Schnittstelle (VB und C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2.getStringCollectionByQuery (VB und C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2-Schnittstelle**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2.getItemInfo (VB und C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





