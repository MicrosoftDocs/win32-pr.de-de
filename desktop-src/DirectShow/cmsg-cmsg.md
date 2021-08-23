---
description: Erstellt ein CMsg-Objekt.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: CMsg.CMsg-Konstruktor (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f921c96ae185d8993002c84a09b4efb8bc5977104c274de3a2ffc964a093f1a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831900"
---
# <a name="cmsgcmsg-constructor"></a>CMsg.CMsg-Konstruktor

Erstellt ein [**CMsg-Objekt.**](cmsg.md)

## <a name="syntax"></a>Syntax


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Anforderungscode, der vom Client der Threadklasse definiert und von der überschriebenen Arbeitsthreadfunktion verstanden wird.

</dd> <dt>

*dw* 
</dt> <dd>

Flagparameter für den Anforderungscode.

</dd> <dt>

*Lp* 
</dt> <dd>

Zeiger auf Daten, die vom Arbeitsthread als Parameter oder Rückgabewerte benötigt werden. Diese Daten sollten nicht stapelbasierte Daten sein, da nach Abschluss des Warteschlangenvorgang einige Zeit darauf verwiesen wird.

</dd> <dt>

*pEvent* 
</dt> <dd>

Zeiger auf das Ereignisobjekt, das ein Arbeitsthread signalisieren kann, um den Abschluss des Vorgangs anzugeben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Memberfunktion enthält eine Anforderung für einen [**CMsgThread-Arbeitsthread,**](cmsgthread.md) der ausgeführt werden soll. Alle Parameter werden an die Arbeitsthreadfunktion als Parameter übergeben, wenn diese Meldung verarbeitet wird. Die Bedeutungen der Parameter werden von der Clientfunktion definiert, die den Arbeitsthread aufruft, und der abgeleiteten Klasse, die die Ausführungsfunktion des Arbeitsthreads liefert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




