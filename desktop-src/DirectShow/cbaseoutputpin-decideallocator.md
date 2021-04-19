---
description: Die decidezuordcator-Methode wählt eine Speicherzuweisung aus.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Cbaseoutputpin. decidezuordcator-Methode (amfilter. h)
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
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366754"
---
# <a name="cbaseoutputpindecideallocator-method"></a>Cbaseoutputpin. decidezuzuordcator-Methode

Die- `DecideAllocator` Methode wählt eine Speicherzuweisung aus.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppin* 
</dt> <dd>

Ein Zeiger auf die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle der Eingabe-PIN.

</dd> <dt>

*palloc* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird am Ende des PIN-Verbindungsprozesses aufgerufen. Sie führt die folgenden Schritte aus:

1.  Ruft die [**IMemInputPin:: getalloerrequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) -Methode auf, um die Puffer Anforderungen der Eingabe-PIN (sofern vorhanden) abzurufen.
2.  Ruft die [**IMemInputPin:: getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) -Methode auf, um eine Zuweisung von der eingabepin anzufordern. Wenn die eingabepin keine Zuweisung bereitstellt, erstellt die Ausgabe-PIN eine, indem Sie die [**cbaseoutputpin:: initaccesscator**](cbaseoutputpin-initallocator.md) -Klassenmethode aufrufen.
3.  Ruft die [**cbaseoutputpin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) -Klassenmethode auf, mit der die zuordnereigenschaften festgelegt werden. Dies ist eine reine virtuelle Methode. Diese Klasse muss von der abgeleiteten Klasse implementiert werden.
4.  Ruft die [**IMemInputPin:: notifyzucator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) -Methode auf, die die Eingabe-PIN der verwendeten Zuweisung benachrichtigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




