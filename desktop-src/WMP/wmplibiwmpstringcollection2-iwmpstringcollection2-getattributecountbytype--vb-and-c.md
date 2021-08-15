---
title: IWMPStringCollection2 getAttributeCountByType-Methode
description: Die getAttributeCountByType-Methode gibt die Anzahl der Attribute zurück, die dem angegebenen Zeichenfolgensammlungsindex, Attributnamen und der angegebenen Sprache zugeordnet sind.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- getAttributeCountByType-Windows Media Player
- getAttributeCountByType-Methode Windows Media Player , IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2-Schnittstelle Windows Media Player , getAttributeCountByType-Methode
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
ms.openlocfilehash: c236d03cad0612d8306b8ccde370136cb9b31acca82e0aa52761ed56fb4b9bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330914"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a>IWMPStringCollection2::getAttributeCountByType-Methode

Die **getAttributeCountByType-Methode** gibt die Anzahl der Attribute zurück, die dem angegebenen Zeichenfolgensammlungsindex, Attributnamen und der angegebenen Sprache zugeordnet sind.

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

*lCollectionIndex* \[ In\]
</dt> <dd>

Das **System.Int32-Objekt,** das den nullbasierten Index des Zeichenfolgensammlungselements angibt, aus dem das Attribut erhalten werden soll.

</dd> <dt>

*bstrType* \[ In\]
</dt> <dd>

Die **System.String,** die der Name des Attributs ist.

</dd> <dt>

*bstrLanguage* \[ In\]
</dt> <dd>

Die **System.String,** die der Name der Sprache ist. Wenn der Wert auf NULL oder auf eine Zeichenfolge der Länge 0 (null) festgelegt ist (""), wird die aktuelle Locale String verwendet. Andernfalls muss der Wert eine gültige RFC 1766-Sprachzeichenfolge wie "en-us" sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Das **System.Int32,** das die Anzahl ist.

## <a name="remarks"></a>Hinweise

Diese Methode wird verwendet, um die Anzahl von Attributen zu finden, die einem bestimmten Attributnamen für ein bestimmtes **StringCollection-Element** entspricht. Indexnummern können dann an den vierten Parameter der **getItemInfoByType-Methode übergeben** werden.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPStringCollection2-Schnittstelle (VB und C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2.getItemInfoByType (VB und C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





