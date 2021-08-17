---
title: IWMPPlaylist getItemInfo-Methode
description: Die getItemInfo-Methode gibt den Wert eines durch den Namen angegebenen Wiedergabelistenattributs zurück.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- getItemInfo-Methode Windows Media Player
- getItemInfo-Methode Windows Media Player , IWMPPlaylist-Schnittstelle
- IWMPPlaylist-Schnittstelle Windows Media Player , getItemInfo-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e3ad24f12333dbc9db5baf977300d1755a9cecc60739504da05478d5acc48e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745752"
---
# <a name="iwmpplaylistgetiteminfo-method"></a>IWMPPlaylist::getItemInfo-Methode

Die **getItemInfo-Methode** gibt den Wert eines durch den Namen angegebenen Wiedergabelistenattributs zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrName* \[ In\]
</dt> <dd>

Eine **System.String,die** der Name des Wiedergabelistenattributs ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String,** die der Wert des Wiedergabelistenattributs ist.

## <a name="remarks"></a>Hinweise

Bevor Sie diese Methode verwenden können, benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Beispielcode, der diese Eigenschaft verwendet, finden Sie in der [attributeCount-Eigenschaft.](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.setItemInfo (VB und C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





