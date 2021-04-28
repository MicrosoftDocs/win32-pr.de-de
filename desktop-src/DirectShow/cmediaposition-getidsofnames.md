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
ms.openlocfilehash: 26a348e58fa84aa4134ce9f2ea756874b9ce2724
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095528"
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



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaPosition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




