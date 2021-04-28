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
ms.openlocfilehash: 3f3b718c95d588ffdc7fa63902e6b26ffbf11fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099918"
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

Adresse eines Arrays von Breitzeichenzeichenfolgen, die die namen enthalten, die zugeordnet werden sollen.

</dd> <dt>

*cNames* 
</dt> <dd>

Die Größe des Arrays, das durch den *rgszNames-Parameter angegeben* wird.

</dd> <dt>

*lcid* 
</dt> <dd>

Der Kontext des Orts, in dem die Namen interpretiert werden. Kann NULL **sein.**

</dd> <dt>

*rgdispid* 
</dt> <dd>

Zeiger auf ein Array, das die DISPIDs empfängt. Jedes Element von empfängt einen Bezeichner, der einem der im *rgszNames-Parameter* übergebenen Namen entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                         | Beschreibung                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Erfolg.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Nicht genügend Arbeitsspeicher.<br/>                     |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl> | Mindestens einer der Namen war nicht bekannt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode verhält sich wie die **IDispatch::GetIDsOfNames-Methode,** aber der *riid-Parameter* gibt die Schnittstelle an, über die DISPIDs abgerufen werden sollen. (In der **IDispatch-Version** ist der *riid-Parameter* reserviert.)

Wenn die Methode DISP \_ E \_ UNKNOWNNAME zurückgibt, enthalten die zurückgegebenen DISPIDs DISPID UNKNOWN für jeden Eintrag, der \_ einem unbekannten Namen entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseDispatch-Klasse**](cbasedispatch.md)
</dt> </dl>

 

 




