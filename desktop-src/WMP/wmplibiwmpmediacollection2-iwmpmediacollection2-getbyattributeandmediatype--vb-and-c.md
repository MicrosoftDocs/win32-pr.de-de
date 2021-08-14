---
title: IWMPMediaCollection2 getByAttributeAndMediaType-Methode
description: Die getByAttributeAndMediaType-Methode gibt eine IWMPPlaylist-Schnittstelle zurück, die Zugriff auf Medienelemente mit einem angegebenen Attribut und Medientyp bietet.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- getByAttributeAndMediaType-Methode Windows Media Player
- getByAttributeAndMediaType-Methode Windows Media Player , IWMPMediaCollection2-Schnittstelle
- IWMPMediaCollection2-Schnittstelle Windows Media Player , getByAttributeAndMediaType-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e08d38954dd24246b4d35b7842f890caba6eea94868901a528396e9a22b38c1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246430"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a>IWMPMediaCollection2::getByAttributeAndMediaType-Methode

Die `getByAttributeAndMediaType` -Methode gibt eine **IWMPPlaylist-Schnittstelle** zurück, die Zugriff auf Medienelemente mit einem angegebenen Attribut und Medientyp bietet.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrAttribute* \[ In\]
</dt> <dd>

Die **System.String,** die das angegebene Attribut ist.

</dd> <dt>

*bstrValue* \[ In\]
</dt> <dd>

Die **System.String,** die der angegebene Wert für das Attribut ist, das in *bstrAttribute angegeben ist.*

</dd> <dt>

*bstrMediaType* \[ In\]
</dt> <dd>

Die **System.String,** die der angegebene Medientyp ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die abgerufene Wiedergabeliste.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPMediaCollection2-Schnittstelle (VB und C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





