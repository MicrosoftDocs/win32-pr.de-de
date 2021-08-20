---
title: IWMPMedia3 getItemInfoByType-Methode
description: Die getItemInfoByType-Methode gibt den Wert des Attributs zurück, das dem angegebenen Attributtyp und Index entspricht.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- getItemInfoByType-Windows Media Player
- getItemInfoByType-Methode Windows Media Player , IWMPMedia3-Schnittstelle
- IWMPMedia3-Schnittstelle Windows Media Player , getItemInfoByType-Methode
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdcfd965af6ac6201687ca8c7ecc7584085b7810a2c0ca11bbc70c1b04403c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929864"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a>IWMPMedia3::getItemInfoByType-Methode

Die **getItemInfoByType-Methode** gibt den Wert des Attributs zurück, das dem angegebenen Attributtyp und Index entspricht.

## <a name="syntax"></a>Syntax


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrType* \[ In\]
</dt> <dd>

Eine **System.String,die** den Attributtyp ist.

</dd> <dt>

*bstrLanguage* \[ In\]
</dt> <dd>

Eine **System.String-,** die die Sprache ist. Wenn der Wert auf NULL oder eine Zeichenfolge der Länge 0 (null) festgelegt ist (""), wird die aktuelle Locale String verwendet. Andernfalls muss der Wert eine gültige RFC 1766-Sprachzeichenfolge wie "en-us" sein.

</dd> <dt>

*lIndex* \[ In\]
</dt> <dd>

Ein **System.Int32,** das der Attributindex ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System.Object,** das der Wert des Attributs ist. Der Typ, in den dieses Objekt umtabellet werden soll, hängt vom Typ des Attributs ab.

## <a name="remarks"></a>Hinweise

Diese Methode gibt die Metadaten für ein einzelnes digitales Medienelement oder ein Medienelement zurück, das Teil einer Wiedergabeliste ist.

Diese Methode unterstützt Attribute mit mehreren Werten und Attribute mit komplexen Werten. Die **getItemInfo-Methode** unterstützt keine Attribute mit mehreren Werten und Attribute mit komplexen Werten.

Die **attributeCount-Eigenschaft** ruft die Anzahl der Attributnamen ab, die für ein bestimmtes Medienelement verfügbar sind. Indexnummern können dann mit der **getAttributeName-Methode** verwendet werden, um den Namen jedes verfügbaren Attributs zu bestimmen. Einzelne Attributnamen können an den *Name-Parameter* von **getItemInfoByType übergeben werden.**

Die **getAttributeCountByType-Methode** gibt die Anzahl von Attributen zurück, die einem bestimmten Attributnamen für ein bestimmtes Medienelement entsprechen. Indexnummern können dann an  den Indexparameter von **getItemInfoByType übergeben werden.** Dies ist nützlich, wenn ein Medienelement beispielsweise unter mehreren Genren kategorisiert wurde.

Wenn das Medienelement aus einer Bibliothek stammt, die durch Aufrufen von [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)abgerufen wurde, unterscheiden sich die verfügbaren Attribute von den Attributen, die von der lokalen Bibliothek abgefragt werden können, die durch Aufrufen von [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)abgerufen wird. Beispielsweise sind die attributes, die aus der lokalen Bibliothek verfügbar sind, die mithilfe von **IWMPLibrary** abgerufen wurde, eine Teilmenge der Attribute, die aus der lokalen Bibliothek verfügbar sind, die mit **AxWindowsMediaPlayer** abgerufen wurde. Der Satz von Attributen, die aus anderen Quellen (Remotebibliotheken, portable Geräte oder CDs) verfügbar sind, wird von den anderen Quellen definiert.

Bevor Sie diese Methode aufrufen, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMedia3-Schnittstelle (VB und C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.attributeCount (VB und C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getAttributeName (VB und C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getItemInfo (VB und C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getAttributeCountByType (VB und C#)**](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





