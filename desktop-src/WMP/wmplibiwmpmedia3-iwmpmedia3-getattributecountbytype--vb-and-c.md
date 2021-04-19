---
title: IWMPMedia3 getattributezähltbytype-Methode
description: Die getattributezähltbytype-Methode gibt die Anzahl der Attribute zurück, die dem angegebenen Attributtyp zugeordnet sind.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- getattributezähltbytype-Methode, Windows Media Player
- getattributezähltbytype-Methode, Windows Media Player, IWMPMedia3-Schnittstelle
- IWMPMedia3 Interface Windows Media Player, getattributezähltbytype-Methode
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357321"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a>IWMPMedia3:: getattributezähltbytype-Methode

Die **getattributezähltbytype** -Methode gibt die Anzahl der Attribute zurück, die dem angegebenen Attributtyp zugeordnet sind.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrintype* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Attributtyp ist.

</dd> <dt>

*bstraulanguage* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der die Sprache ist. Wenn der Wert auf NULL oder eine Zeichenfolge der Länge 0 (null) ("") festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Int32** -Wert, der die Anzahl der Attribute ist, die dem Typ zugeordnet sind.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird verwendet, um die Anzahl von Attributen zu ermitteln, die einem bestimmten Attributnamen für ein bestimmtes Medien Element entsprechen. Index Nummern können dann an die **getItemInfoByType** -Methode weitergegeben werden. Dies ist beispielsweise hilfreich, wenn ein Medien Element unter mehreren Genres kategorisiert wurde.

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMedia3-Schnittstelle (VB und c#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB und c#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





