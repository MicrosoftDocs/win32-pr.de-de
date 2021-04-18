---
description: 'Die QueryId-Methode ruft einen Bezeichner für die PIN ab. Diese Methode implementiert die IPin:: QueryId-Methode.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: Ctransformoutputpin. QueryId-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e8e5fbc4b4da7b38853df5b4dcf3580a8c198d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354697"
---
# <a name="ctransformoutputpinqueryid-method"></a>Ctransformoutputpin. QueryId-Methode

Die- `QueryId` Methode ruft einen Bezeichner für die PIN ab. Diese Methode implementiert die [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Id* 
</dt> <dd>

Empfängt eine Zeichenfolge mit dem PIN-Bezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                   | Beschreibung                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>                   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher<br/>       |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | **Null** -Zeigerargument<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der PIN-Bezeichner wird für die Diagramm Persistenz verwendet. Der PIN-Bezeichner für diese Klasse ist out. Diese Klasse überschreibt das Verhalten der [**cbasepin**](cbasepin.md) -Klasse. In der **cbasepin** -Klasse ist der PIN-Bezeichner mit dem PIN-Namen identisch, der im-Klassenkonstruktor angegeben ist. In der **ctransforminputpin** -Klasse sind der PIN-Bezeichner und der PIN-Name nicht identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




