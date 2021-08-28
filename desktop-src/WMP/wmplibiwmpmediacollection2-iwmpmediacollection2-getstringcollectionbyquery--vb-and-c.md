---
title: IWMPMediaCollection2 getStringCollectionByQuery-Methode
description: Die getStringCollectionByQuery-Methode gibt eine IWMPStringCollection-Schnittstelle zurück, die Zugriff auf den Satz aller Zeichenfolgenwerte für ein angegebenes Attribut bietet, die den Abfragebedingungen entsprechen.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- getStringCollectionByQuery-Windows Media Player
- getStringCollectionByQuery-Methode Windows Media Player , IWMPMediaCollection2-Schnittstelle
- IWMPMediaCollection2-Schnittstelle Windows Media Player , getStringCollectionByQuery-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 054dd5b76cb6dcf3e6cb29ba624cd1f5c0f281d69c4b2b5e5125f5de9b4e7b04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745968"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a>IWMPMediaCollection2::getStringCollectionByQuery-Methode

Die `getStringCollectionByQuery` -Methode gibt eine **IWMPStringCollection-Schnittstelle** zurück, die Zugriff auf den Satz aller Zeichenfolgenwerte für ein angegebenes Attribut bietet, die den Abfragebedingungen entsprechen.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrAttribute* \[ In\]
</dt> <dd>

Die **System.String,** die der Attributname ist.

</dd> <dt>

*pQuery* \[ In\]
</dt> <dd>

Die **WMPLib.IWMPQuery-Schnittstelle,** die die Abfrage ist, die die Bedingungen definiert, die zum Abrufen der Zeichenfolgensammlung verwendet werden.

</dd> <dt>

*bstrMediaType* \[ In\]
</dt> <dd>

Die **System.String,** die den Medientyp ist. Muss einen der folgenden Werte enthalten: "audio", "video", "photo", "playlist" oder "other".

</dd> <dt>

*bstrSortAttribute* \[ In\]
</dt> <dd>

Das **System.String-Attribut,** das für die Sortierung verwendet wird. Eine Zeichenfolge der Länge 0 (null) ("") bedeutet, dass keine Sortierung angewendet wird.

</dd> <dt>

*fSortAscending* \[ In\]
</dt> <dd>

Der **System.Boolean-Wert,** der angibt, ob der Satz von Zeichenfolgenwerten in aufsteigender Reihenfolge sortiert werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPStringCollection-Schnittstelle** für den abgerufenen Satz von Zeichenfolgenwerten.

## <a name="remarks"></a>Hinweise

Bei zusammengesetzten Abfragen, **die IWMPQuery verwenden,** wird die Kleinschreibung nicht beachtet.

Wenn die durch den *pQuery-Parameter* angegebene Verbundabfrage eine Bedingung enthält, die auf dem **MediaType-Attribut** basiert, wird diese Bedingung ignoriert. Der Wert für den *bstrMediaType-Parameter* wird immer verwendet. Wenn die Verbundabfrage beispielsweise die Bedingung "MediaType Gleich Audio" enthält und der Wert für den *bstrMediaType-Parameter* "video" ist, enthält die resultierende Wiedergabeliste nur Videoelemente.

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

[**IWMPQuery-Schnittstelle (VB und C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection-Schnittstelle (VB und C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**MediaType-Attribut**](mediatype-attribute.md)
</dt> </dl>

 

 





