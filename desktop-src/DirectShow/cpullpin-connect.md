---
description: Die Connect-Methode schließt eine Verbindung mit der Ausgabepin ab.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: Cpullpin. Connect-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369188"
---
# <a name="cpullpinconnect-method"></a>Cpullpin. Connect-Methode

Die- `Connect` Methode schließt eine Verbindung mit der Ausgabepin ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kro* 
</dt> <dd>

Ein Zeiger auf die **IUnknown** -Schnittstelle der Ausgabe-PIN.

</dd> <dt>

*palloc* 
</dt> <dd>

Ein Zeiger auf die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle der bevorzugten Zuweisung der Eingabe-PIN oder **null**.

</dd> <dt>

*bsync* 
</dt> <dd>

Boolescher Wert, der angibt, ob synchrone Lesevorgänge verwendet werden sollen. Wenn der Wert **true** ist, führt die PIN synchrone Lesevorgänge für die Ausgabe-PIN aus. **False** gibt an, dass die PIN asynchrone Lese Anforderungen ausführt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **HRESULT** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                               | Beschreibung                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Erfolg.<br/>                                                             |
| <dl> <dt>**VFW \_ E \_ bereits \_ verbunden**</dt> </dl> | Die eingabepin ist bereits verbunden.<br/>                                  |
| <dl> <dt>**E \_ nointerface**</dt> </dl>             | Der Ausgabepin macht [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)nicht verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ruft diese Methode während des Verbindungs Vorgangs der Eingabe-PIN auf. Wenn die Methode fehlschlägt, sollte die PIN die Verbindung nicht herstellen.

Diese Methode fragt die Ausgabe-PIN für die **iasynkreader** -Schnittstelle ab. Bei erfolgreicher Ausführung wird [**cpullpin::D-ecidezuordcator**](cpullpin-decideallocator.md) aufgerufen, um die Zuweisung für die Verbindung auszuhandeln. Wenn Ihre Eingabe-PIN über einen bevorzugten Zuweiser verfügt, geben Sie Sie im *palloc* -Parameter an. die **decidezuzuordcator** -Methode übergibt diesen Zeiger an die [**iasynkreader:: Request-**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) Methode der Ausgabe-PIN. Andernfalls legen Sie *palloc* auf **null** fest.

Wenn der Wert von *bsync* **true** ist, führt das **cpullpin** -Objekt synchrone Lese Anforderungen durch Aufrufen des [**iasyncreader:: syncreadausgerichteten**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)-Objekts der Ausgabe-PIN aus. Andernfalls wird die [**iasynkreader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) -Methode aufgerufen, um überlappende Lese Anforderungen zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




