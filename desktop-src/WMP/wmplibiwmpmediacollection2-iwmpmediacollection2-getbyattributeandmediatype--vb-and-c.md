---
title: IWMPMediaCollection2 getbyattributeandmediatype-Methode
description: Die getbyattributeandmediatype-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die den Zugriff auf Medienelemente mit einem angegebenen Attribut und Medientyp ermöglicht.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- getbyattributeandmediatype-Methode, Windows Media Player
- getbyattributeandmediatype-Methode, Windows Media Player, IWMPMediaCollection2-Schnittstelle
- IWMPMediaCollection2 Interface, Windows Media Player, getbyattributeandmediatype-Methode
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
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365405"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a>IWMPMediaCollection2:: getbyattributeandmediatype-Methode

Die- `getByAttributeAndMediaType` Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente mit einem angegebenen Attribut und Medientyp ermöglicht.

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

*bstrattribute* \[ in\]
</dt> <dd>

Die **System. String** -Eigenschaft, die das angegebene Attribut ist.

</dd> <dt>

*bstrauvalue* \[ in\]
</dt> <dd>

Die **System. String** , die den angegebenen Wert für das in *bstrattribute* angegebene Attribut ist.

</dd> <dt>

*bstraumediatype* \[ in\]
</dt> <dd>

Die **System. String** , die den angegebenen Medientyp ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufene Wiedergabeliste.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMediaCollection2-Schnittstelle (VB und c#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





