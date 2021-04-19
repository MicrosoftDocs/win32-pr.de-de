---
description: Die ccritsec-Klasse stellt eine Thread Sperre bereit.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: Ccritsec-Klasse (wxutil. h)
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
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370641"
---
# <a name="ccritsec-class"></a>Ccritsec-Klasse

Die **ccritsec** -Klasse stellt eine Thread Sperre bereit.

Diese Klasse ist ein schlanker Wrapper für ein kritisches Windows- **\_ Abschnitts** Objekt. Sie können den Thread Sperren und entsperren, indem Sie die [**ccritsec:: Lock**](ccritsec-lock.md) -Methode und die [**ccritsec:: Unlock**](ccritsec-unlock.md) -Methode aufrufen. Es ist jedoch sicherer, diese Klasse in Verbindung mit der [**cautolock**](cautolock.md) -Klasse zu verwenden. Wenn die **cautolock** -Klasse den Gültigkeitsbereich verlässt, entsperrt Sie automatisch das **ccritsec** -Objekt. Außerdem wird es in effizienten Inline Code kompiliert.



| Öffentliche Element Variablen                            | BESCHREIBUNG                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [**m \_ currentowner**](ccritsec-m-currentowner.md) | Thread Bezeichner des besitzenden Threads.                  |
| [**m \_ Sperr Anzahl**](ccritsec-m-lockcount.md)       | Anzahl der ausstehenden Sperren für dieses Objekt.              |
| [**m-nach \_ Verfolgung**](ccritsec-m-ftrace.md)             | Boolescher Wert, der angibt, ob diese Sperre verfolgt werden soll. |
| Öffentliche Methoden                                     | BESCHREIBUNG                                              |
| [**Ccritsec**](ccritsec-ccritsec.md)              | Konstruktormethode.                                      |
| [**~ Ccritsec**](ccritsec--ccritsec.md)            | Dekonstruktormethode.                                       |
| [**Sperre**](ccritsec-lock.md)                      | Sperrt das kritische Abschnitts Objekt.                       |
| [**Entsperren**](ccritsec-unlock.md)                  | Entsperrt das Objekt des kritischen Abschnitts.                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kritische Abschnitts Objekte](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[Referenz zur DirectShow-Basisklasse](base-class-reference.md)
</dt> </dl>

 

