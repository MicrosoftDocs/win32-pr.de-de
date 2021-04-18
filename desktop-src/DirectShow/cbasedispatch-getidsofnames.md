---
description: Die GetIDsOfNames-Methode ordnet einem entsprechenden Satz von DISPIDs einen Satz von Namen zu.
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: Cbasedispatch. GetIDsOfNames-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf11e4aa298f924b69c299c2f411dde88e28e5b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368301"
---
# <a name="cbasedispatchgetidsofnames-method"></a>Cbasedispatch. GetIDsOfNames-Methode

Die-Methode ordnet einem `GetIDsOfNames` entsprechenden Satz von DISPIDs einen Satz von Namen zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* 
</dt> <dd>

Verweis auf einen Schnittstellen Bezeichner (IID), der die-Schnittstelle angibt.

</dd> <dt>

*rgsznames* 
</dt> <dd>

Adresse eines Arrays von breit Zeichen-Zeichen folgen, die die Namen enthalten, die zugeordnet werden sollen.

</dd> <dt>

*CNAMES* 
</dt> <dd>

Größe des Arrays, das vom *rgsznames* -Parameter angegeben wird.

</dd> <dt>

*lcid* 
</dt> <dd>

Der Gebiets Schema Kontext, in dem die Namen interpretiert werden sollen. Kann **null** sein.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Zeiger auf ein Array, das die DISPIDs empfängt. Jedes Element von empfängt einen Bezeichner, der einem der im *rgsznames* -Parameter übergebenen Namen entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                         | Beschreibung                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Erfolg.<br/>                                 |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>       | Nicht genügend Arbeitsspeicher.<br/>                     |
| <dl> <dt>**DISP \_ E \_ unknownname**</dt> </dl> | Mindestens ein Name ist nicht bekannt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode verhält sich wie die **IDispatch:: GetIDsOfNames** -Methode, aber der *riid* -Parameter gibt die Schnittstelle an, auf der DispIds abgerufen werden sollen. (In der **IDispatch** -Version ist der *riid* -Parameter reserviert.)

Wenn die Methode DISP \_ E \_ unknownname zurückgibt, enthalten die zurückgegebenen DispIds DISPID \_ Unknown für jeden Eintrag, der einem unbekannten Namen entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasedispatch-Klasse**](cbasedispatch.md)
</dt> </dl>

 

 




