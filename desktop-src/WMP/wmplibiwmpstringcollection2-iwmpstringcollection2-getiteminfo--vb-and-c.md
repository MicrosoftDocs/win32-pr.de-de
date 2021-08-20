---
title: IWMPStringCollection2 getItemInfo-Methode
description: Die getItemInfo-Methode gibt die Zeichenfolge zurück, die dem angegebenen Index und Namen des Zeichenfolgensammlungselements entspricht.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- getItemInfo-Windows Media Player
- getItemInfo-Methode Windows Media Player , IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2-Schnittstelle Windows Media Player , getItemInfo-Methode
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
ms.openlocfilehash: 6f3f5371d55384544e4135e702b686cc7ce36707d204529ca7a4e68a3734d8ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899840"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a>IWMPStringCollection2::getItemInfo-Methode

Die **getItemInfo-Methode** gibt die Zeichenfolge zurück, die dem angegebenen Index und Namen des Zeichenfolgensammlungselements entspricht.

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

*lCollectionIndex* \[ In\]
</dt> <dd>

Das **System.Int32-Objekt,** das den nullbasierten Index des Zeichenfolgensammlungselements angibt, aus dem das Attribut erhalten werden soll.

</dd> <dt>

*bstrItemName* \[ In\]
</dt> <dd>

Die **System.String,** die der Attributname ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **System.String,** die der Name des Zeichenfolgensammlungselements ist. Für Attribute, deren zugrunde liegender Wert **System.Boolean** ist, wird die Zeichenfolge "true" oder "false" zurückgegeben.

## <a name="remarks"></a>Hinweise

Verwenden Sie zum Abrufen von Attributen mit mehreren Werten und Attributen mit komplexen Werten die **getItemInfoByType-Methode.**

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPStringCollection2-Schnittstelle**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2.getItemInfoByType (VB und C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





