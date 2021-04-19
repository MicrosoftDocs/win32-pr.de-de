---
description: Die Init-Methode initialisiert das-Objekt.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: CSeekingPassThru.Init-Methode (seekpt. h)
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
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370543"
---
# <a name="cseekingpassthruinit-method"></a>CSeekingPassThru.Init-Methode

Die- `Init` Methode initialisiert das-Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bsupportrendering* \[ in\]
</dt> <dd>

Boolescher Wert, der angibt, ob der Filter ein Renderer ist. Verwenden Sie den Wert **true** , wenn der Filter ein Renderer ist, und andernfalls **false** .

</dd> <dt>

*ppin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle für die Eingabe-PIN des Filters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                   | Beschreibung                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Das Objekt wurde bereits initialisiert.<br/>         |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher zum Erstellen des Objekts.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Wert von *bsupportrendering* **true** ist, erstellt diese Methode eine Instanz der [**crendererpospassthru**](crendererpospassthru.md) -Klasse. Andernfalls wird eine Instanz der [**cpospassthru**](cpospassthru.md) -Klasse erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Seekpt. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cseekingpassthru-Klasse**](cseekingpassthru.md)
</dt> </dl>

 

 




