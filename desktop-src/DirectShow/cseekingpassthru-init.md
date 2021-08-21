---
description: Die Init-Methode initialisiert das -Objekt.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: CSeekingPassThru.Init-Methode (Seekpt.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91d20477f83ec79c6ae6095e81810c98454f9c26521eda995c919867b3e3ac12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953814"
---
# <a name="cseekingpassthruinit-method"></a>CSeekingPassThru.Init-Methode

Die `Init` -Methode initialisiert das -Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bSupportRendering* \[ In\]
</dt> <dd>

Boolescher Wert, der angibt, ob der Filter ein Renderer ist. Verwenden Sie den Wert **TRUE,** wenn der Filter ein Renderer ist, andernfalls **FALSE.**

</dd> <dt>

*pPin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) auf dem Eingabepin des Filters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                   | Beschreibung                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Das Objekt wurde bereits initialisiert.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher zum Erstellen des Objekts.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn der Wert von *bSupportRendering* **TRUE** ist, erstellt diese Methode eine Instanz der [**CRendererPosPassThru-Klasse.**](crendererpospassthru.md) Andernfalls wird eine Instanz der [**CPosPassThru-Klasse**](cpospassthru.md) erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Seekpt.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSeekingPassThru-Klasse**](cseekingpassthru.md)
</dt> </dl>

 

 




