---
title: IWMPMediaCollection2 getPlaylistByQuery-Methode
description: Die getPlaylistByQuery-Methode gibt eine IWMPPlaylist-Schnittstelle zurück, die Zugriff auf Medienelemente bereitstellt, die den Abfragebedingungen entsprechen.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- getPlaylistByQuery-Methode Windows Media Player
- getPlaylistByQuery-Methode Windows Media Player , IWMPMediaCollection2-Schnittstelle
- IWMPMediaCollection2-Schnittstelle Windows Media Player , getPlaylistByQuery-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd80467c78aac832c5ac2784281abcf07975a1956ee304c734b2b45b82901fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053578"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a>IWMPMediaCollection2::getPlaylistByQuery-Methode

Die `getPlaylistByQuery` -Methode gibt eine **IWMPPlaylist-Schnittstelle** zurück, die Zugriff auf Medienelemente bereitstellt, die den Abfragebedingungen entsprechen.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*pQuery* \[ In\]
</dt> <dd>

Die **WMPLib.IWMPQuery-Schnittstelle,** die die Abfrage darstellt.

</dd> <dt>

*bstrMediaType* \[ In\]
</dt> <dd>

Die **System.String,** bei der es sich um den Medientyp handelt. Muss einen der folgenden Werte enthalten: "audio", "video", "photo", "playlist" oder "other".

</dd> <dt>

*bstrSortAttribute* \[ In\]
</dt> <dd>

Die **System.String,** bei der es sich um den Attributnamen handelt, der für die Sortierung verwendet wird. Eine Zeichenfolge der Länge 0 (null) bedeutet, dass keine Sortierung angewendet wird.

</dd> <dt>

*fSortAscending* \[ In\]
</dt> <dd>

Der **System.Boolean-Wert,** der angibt, ob die Wiedergabeliste in aufsteigender Reihenfolge sortiert werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die abgerufene Wiedergabeliste.

## <a name="remarks"></a>Hinweise

Bei zusammengesetzten Abfragen, die **IWMPQuery** verwenden, wird die Groß-/Kleinschreibung nicht beachtet.

Wenn die vom *pQuery-Parameter* angegebene Verbundabfrage eine Bedingung enthält, die auf dem **MediaType-Attribut** basiert, wird diese Bedingung ignoriert. Der Wert für den *bstrMediaType-Parameter* wird immer verwendet. Wenn die Verbundabfrage beispielsweise die Bedingung "MediaType Equals audio" enthält und der Wert für den *bstrMediaType-Parameter* "video" ist, enthält die resultierende Wiedergabeliste nur Videoelemente.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMediaCollection2-Schnittstelle (VB und C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPQuery-Schnittstelle (VB und C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**MediaType-Attribut**](mediatype-attribute.md)
</dt> </dl>

 

 





