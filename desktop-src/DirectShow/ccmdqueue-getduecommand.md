---
description: Die getduecommand-Methode ruft einen Zeiger auf den nächsten Befehl ab, der fällig ist.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Ccmdqueue. getduecommand-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360278"
---
# <a name="ccmdqueuegetduecommand-method"></a>Ccmdqueue. getduecommand-Methode

Die- `GetDueCommand` Methode ruft einen Zeiger auf den nächsten Befehl ab, der fällig ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppCmd* 
</dt> <dd>

Adresse eines Zeigers auf den verzögerten Befehl.

</dd> <dt>

*mstimeout* 
</dt> <dd>

Zeitspanne, die gewartet werden soll, bevor das Timeout durchgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den \_ Abbruch bei einem Timeout zurück. Gibt \_ bei Erfolg S OK zurück; andernfalls wird ein Fehler zurückgegeben. Gibt ein Objekt zurück, das mit **IUnknown:: adressf** inkrementiert wurde.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion wird blockiert, bis ein ausstehender Befehl fällig ist. Die Element Funktionsblöcke für die Zeitspanne (in Millisekunden), die im *mstimeout* -Parameter angegeben ist. Stream-Zeit-Befehle werden nur durch die Member-Funktionen [**ccmdqueue:: Run**](ccmdqueue-run.md) und [**ccmdqueue:: EndRun**](ccmdqueue-endrun.md) verursacht. Der Befehl wird bis zum Ausführen oder Abbrechen in die Warteschlange eingereiht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccmdqueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




