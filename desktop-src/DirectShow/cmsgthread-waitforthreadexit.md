---
description: Blockiert, bis der Thread beendet wird.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Cmsgthread. waitforthreadexit-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361586"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a>Cmsgthread. waitforthreadexit-Methode

Blockiert, bis der Thread beendet wird.

## <a name="syntax"></a>Syntax


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpdwexitcode* 
</dt> <dd>

Zeiger auf den Exitcode, der vom Thread zurückgegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt entweder " **true** " oder " **false**" zurück. die Bedeutung von wird von der Klasse bestimmt, die die überschriebene [**cmsgthread:: threadmessageproc**](cmsgthread-threadmessageproc.md) -Member-Funktion und die aufrufende Member-Funktion bereitstellt.

## <a name="remarks"></a>Bemerkungen

Stellen Sie sicher, dass der Arbeitsthread vollständig beendet wurde, bevor Sie die Zerstörung ihrer abgeleiteten Klasse abschließen. Andernfalls kann der Thread nach dem Entladen der Dynamic Link Library (dll) aus dem Adressraum des Prozesses weiter ausgeführt werden. Auch wenn die einzige Anweisung, die zum Beenden übrig ist, eine-Anweisung ist, würde dies zu einer Ausnahme führen. Die einzige zuverlässige Möglichkeit, um sicherzustellen, dass der Thread beendet wurde, besteht darin, den Thread zu beenden (mithilfe eines privat ausgehandelten [**CMSG**](cmsg.md) -Objekts, das an die Member-Funktion [**cmsgthread::P utthreadmsg**](cmsgthread-putthreadmsg.md) gesendet wurde), und dann diese Member-Funktion aufzurufen. Dies sollte im Dekonstruktor für Ihre abgeleitete Klasse durchzuführen sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmsgthread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




