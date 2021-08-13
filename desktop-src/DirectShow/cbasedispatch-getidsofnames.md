---
description: 'CBaseDispatch.GetIDsOfNames-Methode: Die GetIDsOfNames-Methode ordnet einen Satz von Namen einem entsprechenden Satz von DISPIDs zu.'
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: CBaseDispatch.GetIDsOfNames-Methode (Ctlutil.h)
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
ms.openlocfilehash: a9153dd2412018321374f558539690d5d146d8547d6247874bf5c1c79f1d4d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660027"
---
# <a name="cbasedispatchgetidsofnames-method"></a>CBaseDispatch.GetIDsOfNames-Methode

Die `GetIDsOfNames` -Methode ordnet einen Satz von Namen einem entsprechenden Satz von DISPIDs zu.

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

Verweis auf einen Schnittstellenbezeichner (IID), der die Schnittstelle angibt.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Adresse eines Arrays von Breitzeichenzeichenfolgen, die die zuzuordnenden Namen enthalten.

</dd> <dt>

*cNames* 
</dt> <dd>

Größe des Arrays, das vom *rgszNames-Parameter* angegeben wird.

</dd> <dt>

*lcid* 
</dt> <dd>

Gebietsschemakontext, in dem die Namen interpretiert werden sollen. Kann **NULL** sein.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Zeiger auf ein Array, das die DISPIDs empfängt. Jedes Element von empfängt einen Bezeichner, der einem der im *rgszNames-Parameter übergebenen* Namen entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                         | Beschreibung                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Erfolg.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Nicht genügend Arbeitsspeicher.<br/>                     |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl> | Mindestens ein Name war nicht bekannt.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode verhält sich wie die **IDispatch::GetIDsOfNames-Methode,** aber der *riid-Parameter* gibt die Schnittstelle an, für die DISPIDs abgerufen werden sollen. (In der **IDispatch-Version** ist der *riid-Parameter* reserviert.)

Wenn die Methode DISP \_ E \_ UNKNOWNNAME zurückgibt, enthalten die zurückgegebenen DISPIDs DISPID UNKNOWN für jeden Eintrag, der \_ einem unbekannten Namen entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseDispatch-Klasse**](cbasedispatch.md)
</dt> </dl>

 

 




