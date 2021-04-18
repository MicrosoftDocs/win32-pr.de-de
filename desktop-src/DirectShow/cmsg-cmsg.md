---
description: Erstellt ein CMSG-Objekt.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: CMSG. CMSG-Konstruktor (msgthrd. h)
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
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358119"
---
# <a name="cmsgcmsg-constructor"></a>CMSG. CMSG-Konstruktor

Erstellt ein [**CMSG**](cmsg.md) -Objekt.

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

Anforderungs Code, der vom Client der Thread Klasse definiert und von der überschriebenen Arbeits Thread Funktion verstanden wird.

</dd> <dt>

*dw* 
</dt> <dd>

Markieren Sie den Parameter für den Anforderungs Code.

</dd> <dt>

*LP* 
</dt> <dd>

Zeiger auf Daten, die vom Arbeits Thread als Parameter oder Rückgabewerte benötigt werden. Diese Daten sollten nicht Stapel basiert sein, da nach Abschluss des Warteschlangen Vorgangs einige Zeit darauf verwiesen wird.

</dd> <dt>

*Peer Event* 
</dt> <dd>

Zeiger auf das Ereignis Objekt, das ein Arbeits Thread signalisieren kann, um den Abschluss des Vorgangs anzugeben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion enthält eine Anforderung für einen [**cmsgthread**](cmsgthread.md) -Arbeits Thread, der ausgeführt werden soll. Alle Parameter werden als Parameter an die Arbeits Thread Funktion als Parameter übermittelt, wenn diese Nachricht verarbeitet wird. Die Bedeutungen der Parameter werden von der Client Funktion definiert, die den Arbeits Thread aufruft, und von der abgeleiteten Klasse, die die Ausführungs Funktion des Arbeitsthreads bereitstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




