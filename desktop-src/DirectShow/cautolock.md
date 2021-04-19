---
description: Die cautolock-Klasse enthält einen kritischen Abschnitt für den Bereich eines Codeblocks.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: Cautolock-Klasse (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356477"
---
# <a name="cautolock-class"></a>Cautolock-Klasse

Die- `CAutoLock` Klasse enthält einen kritischen Abschnitt für den Bereich eines Codeblocks.

Diese Klasse funktioniert in Verbindung mit der [**ccritsec**](ccritsec.md) -Klasse, bei der es sich um einen Wrapper für kritische Abschnitts Objekte handelt. Der `CAutoLock` -Konstruktor sperrt den kritischen Abschnitt, und der Dekonstruktor entsperrt ihn. Indem Sie ein- `CAutoLock` Objekt als lokale Variable verwenden, können Sie einen kritischen Abschnitt mit der Garantie sperren, dass alle Codepfade den kritischen Abschnitt entsperren werden.

Im folgenden Codebeispiel wird gezeigt, wie diese Klasse verwendet wird:


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



Die Methoden in dieser Klasse können nicht überschrieben werden.



| Geschützte Member-Variablen                 | BESCHREIBUNG                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [**m \_ Plock**](cautolock-m-plock.md)      | Kritischer Abschnitt für diese Sperre.                                  |
| Öffentliche Methoden                             | BESCHREIBUNG                                                      |
| [**Cautolock**](cautolock-cautolock.md)   | Konstruktormethode. Sperrt das angegebene kritische Abschnitts Objekt. |
| [**~ Cautolock**](cautolock--cautolock.md) | Dekonstruktormethode. Entsperrt das Objekt des kritischen Abschnitts.          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




