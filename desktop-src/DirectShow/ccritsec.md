---
description: Die CCritSec-Klasse bietet eine Threadsperre.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: CCritSec-Klasse (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eb57004935a85392057120c0ec369d19217148780079ab4be83088dd3de3ea8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872190"
---
# <a name="ccritsec-class"></a>CCritSec-Klasse

Die **CCritSec-Klasse** bietet eine Threadsperre.

Diese Klasse ist ein schlanker Wrapper für ein Windows **CRITICAL \_ SECTION-Objekt.** Sie können den Thread sperren und entsperren, indem Sie die [**Methoden CCritSec::Lock**](ccritsec-lock.md) und [**CCritSec::Unlock**](ccritsec-unlock.md) aufrufen. Es ist jedoch sicherer, diese Klasse in Verbindung mit der [**CAutoLock-Klasse zu**](cautolock.md) verwenden. Wenn die **CAutoLock-Klasse** den Gültigkeitsbereich übergeht, entsperrt sie automatisch das **CCritSec-Objekt.** Darüber hinaus wird er zu effizientem Inlinecode kompiliert.



| Öffentliche Membervariablen                            | BESCHREIBUNG                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [**m \_ currentOwner**](ccritsec-m-currentowner.md) | Threadbezeichner des besitzenden Threads.                  |
| [**m \_ lockCount**](ccritsec-m-lockcount.md)       | Anzahl ausstehender Sperren für dieses Objekt.              |
| [**m \_ fTrace**](ccritsec-m-ftrace.md)             | Boolescher Wert, der angibt, ob diese Sperre verfolgt werden soll. |
| Öffentliche Methoden                                     | BESCHREIBUNG                                              |
| [**CCritSec**](ccritsec-ccritsec.md)              | Konstruktormethode.                                      |
| [**~CCritSec**](ccritsec--ccritsec.md)            | Destruktormethode.                                       |
| [**Sperre**](ccritsec-lock.md)                      | Sperrt das kritische Abschnittsobjekt.                       |
| [**Entsperren**](ccritsec-unlock.md)                  | Entsperrt das kritische Abschnittsobjekt.                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kritische Abschnittsobjekte](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[DirectShow-Basisklassenreferenz](base-class-reference.md)
</dt> </dl>

 

