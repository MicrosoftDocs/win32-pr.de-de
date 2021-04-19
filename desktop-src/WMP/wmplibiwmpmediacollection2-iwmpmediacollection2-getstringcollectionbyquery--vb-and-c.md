---
title: IWMPMediaCollection2 getstringcollectionbyquery-Methode
description: Die getstringcollectionbyquery-Methode gibt eine iwmpstringcollection-Schnittstelle zurück, die Zugriff auf den Satz aller Zeichen folgen Werte für ein angegebenes Attribut bietet, die den Abfragebedingungen entsprechen.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- getstringcollectionbyquery-Methode, Windows-Media Player
- getstringcollectionbyquery-Methode, Windows Media Player, IWMPMediaCollection2-Schnittstelle
- IWMPMediaCollection2 Interface, Windows Media Player, getstringcollectionbyquery-Methode
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
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366729"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a>IWMPMediaCollection2:: getstringcollectionbyquery-Methode

Die- `getStringCollectionByQuery` Methode gibt eine **iwmpstringcollection** -Schnittstelle zurück, die Zugriff auf den Satz aller Zeichen folgen Werte für ein angegebenes Attribut bietet, die den Abfragebedingungen entsprechen.

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

*bstrattribute* \[ in\]
</dt> <dd>

Der **System. String** -Wert, der der Attribut Name ist.

</dd> <dt>

*pquery* \[ in\]
</dt> <dd>

Die **WMPLib. iwmpquery** -Schnittstelle, bei der es sich um die Abfrage handelt, die die zum Abrufen der Zeichen folgen Auflistung verwendeten Bedingungen definiert.

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

Der **System. Boolean** -Wert, der angibt, ob der Satz von Zeichen folgen Werten in aufsteigender Reihenfolge sortiert werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpstringcollection** -Schnittstelle für den abgerufenen Satz von Zeichen folgen Werten.

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

[**Iwmpquery-Schnittstelle (VB und c#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Iwmpstringcollection-Schnittstelle (VB und c#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**MediaType-Attribut**](mediatype-attribute.md)
</dt> </dl>

 

 





