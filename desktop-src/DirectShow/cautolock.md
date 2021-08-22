---
description: Die CAutoLock-Klasse enthält einen kritischen Abschnitt für den Bereich eines Codeblocks.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: CAutoLock-Klasse (Wxutil.h)
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
ms.openlocfilehash: 4b046111e3a7e22fcf9e380fae09bb2d2007a583e49c0507b8e214142505fe02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661702"
---
# <a name="cautolock-class"></a>CAutoLock-Klasse

Die `CAutoLock` -Klasse enthält einen kritischen Abschnitt für den Bereich eines Codeblocks.

Diese Klasse funktioniert in Verbindung mit der [**CCritSec-Klasse,**](ccritsec.md) die ein Wrapper für kritische Abschnittsobjekte ist. Der `CAutoLock` Konstruktor sperrt den kritischen Abschnitt, und der Destruktor entsperrt ihn. Wenn Sie ein -Objekt als lokale Variable verwenden, können Sie einen kritischen Abschnitt mit der Garantie sperren, dass alle Codepfade den `CAutoLock` kritischen Abschnitt entsperren.

Im folgenden Codebeispiel wird die Verwendung dieser Klasse veranschaulicht:


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



Die Methoden in dieser Klasse sind nicht für das Überschreiben konzipiert.



| Geschützte Membervariablen                 | BESCHREIBUNG                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [**m \_ pLock**](cautolock-m-plock.md)      | Kritischer Abschnitt für diese Sperre.                                  |
| Öffentliche Methoden                             | BESCHREIBUNG                                                      |
| [**CAutoLock**](cautolock-cautolock.md)   | Konstruktormethode. Sperrt das angegebene kritische Abschnittsobjekt. |
| [**~CAutoLock**](cautolock--cautolock.md) | Destruktormethode. Entsperrt das kritische Abschnittsobjekt.          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




