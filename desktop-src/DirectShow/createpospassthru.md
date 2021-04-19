---
description: Die Funktion "anatepospassthru" erstellt ein cpospassthru-Objekt oder ein crendererpospassthru-Objekt.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Funktion "kreatepospassthru" (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361635"
---
# <a name="createpospassthru-function"></a>Funktion "kreatepospassthru"

Die- `CreatePosPassThru` Funktion erstellt ein [**cpospassthru**](cpospassthru.md) -Objekt oder ein [**crendererpospassthru**](crendererpospassthru.md) -Objekt.

## <a name="syntax"></a>Syntax


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pagg* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts. Andernfalls legen Sie diesen Parameter auf **null** fest.

</dd> <dt>

*brenderer* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Filter ein Renderer ist. Verwenden Sie den Wert **true** , wenn der Filter ein Renderer ist, und andernfalls **false** . Wenn der Wert **true** ist, erstellt diese Methode eine Instanz der [**crendererpospassthru**](crendererpospassthru.md) -Klasse. Wenn der Wert **false** ist, erstellt die Methode eine Instanz der **cpospassthru** -Klasse.

</dd> <dt>

*ppin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle für die Eingabe-PIN des Filters.

</dd> <dt>

*pppassthru* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die **IUnknown** -Schnittstelle des Objekts empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK zurück. Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode verwendet die [**iseekingpassthru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) -Schnittstelle zum Erstellen des-Objekts. Das Objekt wird dynamisch aus Quartz.dll geladen.

Wenn die Funktion erfolgreich ausgeführt wird, weist die zurückgegebene **IUnknown** -Schnittstelle einen ausstehenden Verweis Zähler auf. Der Aufrufer muss die-Schnittstelle freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




