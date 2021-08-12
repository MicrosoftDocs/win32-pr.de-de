---
title: IWMPPlaylist setItemInfo-Methode
description: Die setItemInfo-Methode legt den Wert eines Attributs der aktuellen Wiedergabeliste fest.
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- setItemInfo-Methode Windows Media Player
- setItemInfo-Methode Windows Media Player , IWMPPlaylist-Schnittstelle
- IWMPPlaylist-Schnittstelle Windows Media Player , setItemInfo-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcd4bf2d90b90a825942c5634b2b2cde3bb82e7806fe62ecd5e7d298cd191997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568705"
---
# <a name="iwmpplaylistsetiteminfo-method"></a>IWMPPlaylist::setItemInfo-Methode

Die **setItemInfo-Methode** legt den Wert eines Attributs der aktuellen Wiedergabeliste fest.

## <a name="syntax"></a>Syntax


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrName* \[ In\]
</dt> <dd>

Eine **System.String,die** der Attributname ist.

</dd> <dt>

*bstrValue* \[ In\]
</dt> <dd>

Eine **System.String,die** der Attributwert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Vor dem Aufrufen dieser Methode benötigen Sie Vollzugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Beispielcode, der diese Eigenschaft verwendet, finden Sie in der [attributeCount-Eigenschaft.](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.getItemInfo (VB und C#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





