---
title: Deaktivieren von STRICT
description: Um die STRICT-Typüberprüfung zu deaktivieren, definieren Sie den Symbolnamen NO \_ STRICT. In Visual C/C++ können Sie diese Definition auch in der Befehlszeile oder in einem Makefile angeben, indem Sie /DNO \_ STRICT als Compileroption angeben.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078361b5cc3fd4916ac2ab4f7207752e869568b8781c9ef3dd8e38427d252592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743656"
---
# <a name="disabling-strict"></a>Deaktivieren von STRICT

Um die **STRICT-Typüberprüfung** zu deaktivieren, definieren Sie den Symbolnamen **NO \_ STRICT**. In Visual C/C++ können Sie diese Definition auch in der Befehlszeile oder in einem Makefile angeben, indem Sie **/DNO \_ STRICT** als Compileroption angeben.

Um **NO \_ STRICT dateispezifische** Definitionen zu definieren, fügen Sie eine **\# define-Anweisung** ein, bevor Sie Windows.h einfügen:


```C++
#define NO_STRICT
#include <windows.h>
```



Um optimale Ergebnisse zu erzielen, sollten Sie auch die Warnstufe für Fehlermeldungen auf **mindestens /W3 festlegen.** Dies ist bei Anwendungen für Windows immer ratsam, da eine Codierungsübung, die eine Warnung verursacht (z. B. die falsche Anzahl von Parametern), in der Regel zur Laufzeit einen schwerwiegenden Fehler verursacht, wenn er nicht korrigiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von STRICT](enabling-strict.md)
</dt> <dt>

[STRICT-Konformität](strict-compliance.md)
</dt> </dl>

 

 




