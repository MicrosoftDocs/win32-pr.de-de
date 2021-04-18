---
description: Die decidezuzuordcator-Methode aushandiert eine Zuweisung mit der Ausgabepin.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Cpullpin. decidezucator-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371682"
---
# <a name="cpullpindecideallocator-method"></a>Cpullpin. decidezucator-Methode

Die- `DecideAllocator` Methode aushandiert eine Zuweisung mit der Ausgabepin.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*palloc* 
</dt> <dd>

Ein Zeiger auf die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle der bevorzugten Zuweisung der Eingabe-PIN oder **null**.

</dd> <dt>

*p-Eigenschaften* 
</dt> <dd>

Zeiger auf eine optionale [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die Puffer Anforderungen der Eingabe-PIN enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder andernfalls einen Fehlercode zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die Methode [**iasynkreader:: requestzuweisung**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) auf, um eine Zuweisung auszuhandeln. Er übergibt den *palloc* -Parameter direkt an die **requestzuweisung** -Methode. Der Parameter " *prequiers* " wird an **requestzuweisung** übergeben, wenn " *prequiors* " nicht **null** ist. Andernfalls wird eine **zuordnereigenschaftenstruktur \_** mit einer Standard Anforderung von drei 64-KB-Puffern erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> <dt>

[**Cpullpin:: Connect**](cpullpin-connect.md)
</dt> </dl>

 

 




