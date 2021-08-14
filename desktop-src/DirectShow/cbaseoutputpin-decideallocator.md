---
description: Die DecideAllocator-Methode wählt eine Speicherzuweisung aus.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: CBaseOutputPin.DecideAllocator-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 73d822450d635fe5f7620d59f39fcc7ed85fe1e2465f34af3ef561dfc2f3828f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814210"
---
# <a name="cbaseoutputpindecideallocator-method"></a>CBaseOutputPin.DecideAllocator-Methode

Die `DecideAllocator` -Methode wählt eine Speicherzuweisung aus.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPin* 
</dt> <dd>

Zeiger auf die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) des Eingabepins.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Zuweisung empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Diese Methode wird am Ende des Pinverbindungsprozesses aufgerufen. Sie führt die folgenden Schritte aus:

1.  Ruft die [**IMemInputPin::GetAllocatorRequirements-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) auf, um ggf. die Pufferanforderungen des Eingabepins abzurufen.
2.  Ruft die [**IMemInputPin::GetAllocator-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) auf, um eine Zuweisung vom Eingabepin anzufordern. Wenn der Eingabepin keine Zuweisung bereitstellt, erstellt der Ausgabepin einen durch Aufrufen der [**CBaseOutputPin::InitAllocator-Klassenmethode.**](cbaseoutputpin-initallocator.md)
3.  Ruft die [**CBaseOutputPin::D ecideBufferSize-Klassenmethode**](cbaseoutputpin-decidebuffersize.md) auf, die die Zuweisungseigenschaften festlegt. Dies ist eine reine virtuelle Methode. die abgeleitete Klasse muss sie implementieren.
4.  Ruft die [**IMemInputPin::NotifyAllocator-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) auf, die den Eingabepin über die verwendete Zuweisung benachrichtigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




