---
title: IWMPMediaCollection2 getplaylistbyquery-Methode
description: Die getplaylistbyquery-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die Zugriff auf Medienelemente bietet, die den Abfragebedingungen entsprechen.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- getplaylistbyquery-Methode, Windows-Media Player
- getplaylistbyquery-Methode, Windows Media Player, IWMPMediaCollection2-Schnittstelle
- IWMPMediaCollection2 Interface, Windows Media Player, getplaylistbyquery-Methode
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
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370745"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a>IWMPMediaCollection2:: getplaylistbyquery-Methode

Die- `getPlaylistByQuery` Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die Zugriff auf Medienelemente bietet, die den Abfragebedingungen entsprechen.

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

*pquery* \[ in\]
</dt> <dd>

Die **WMPLib. iwmpquery** -Schnittstelle, die die Abfrage darstellt.

</dd> <dt>

*bstraumediatype* \[ in\]
</dt> <dd>

Die **System. String** , die den Medientyp ist. Muss einen der folgenden Werte enthalten: "Audiodatei", "Video", "Photo", "Wiedergabeliste" oder "Other".

</dd> <dt>

*bstrausortattribute* \[ in\]
</dt> <dd>

Die **System. String** , die der für die Sortierung verwendete Attribut Name ist. Eine Zeichenfolge der Länge 0 (null) bedeutet, dass keine Sortierung angewendet wird.

</dd> <dt>

*fsortascending* \[ in\]
</dt> <dd>

Der **System. Boolean** -Wert, der angibt, ob die Wiedergabeliste in aufsteigender Reihenfolge sortiert werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufene Wiedergabeliste.

## <a name="remarks"></a>Bemerkungen

Bei Verbund Abfragen mit **iwmpquery** wird die Groß-/Kleinschreibung nicht beachtet

Wenn die durch den *pquery* -Parameter angegebene Verbund Abfrage eine Bedingung enthält, die auf dem **mediaType** -Attribut basiert, wird diese Bedingung ignoriert. Der Wert für den *bstraumediatype* -Parameter wird immer verwendet. Wenn die Verbund Abfrage z. b. die Bedingung "MediaType ist mit Audiodaten" enthält und der Wert für den *botmediatype* -Parameter "Video" ist, enthält die resultierende Wiedergabeliste nur Video Elemente.

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
</dt> <dt>

[**Iwmpquery-Schnittstelle (VB und c#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**MediaType-Attribut**](mediatype-attribute.md)
</dt> </dl>

 

 





