---
description: 'CMediaPosition.GetIDsOfNames-Methode: Die GetIDsOfNames-Methode ordnet einen Satz von Namen einem entsprechenden Satz von DISPIDs zu.'
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: CMediaPosition.GetIDsOfNames-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eebd32638afdf957024f54f6a601e95bae274dc4ab9a8265e9a618d635a23530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634795"
---
# <a name="cmediapositiongetidsofnames-method"></a>CMediaPosition.GetIDsOfNames-Methode

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

Reserviert. Verwenden Sie IID \_ NULL.

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



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaPosition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




