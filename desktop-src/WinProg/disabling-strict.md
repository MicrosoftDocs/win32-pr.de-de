---
title: Deaktivieren von Strict
description: Wenn Sie die strikte Typüberprüfung deaktivieren möchten, definieren Sie den Symbolnamen "No \_ Strict". In Visual C/C++ können Sie diese Definition auch in der Befehlszeile oder in einem Makefile-Element angeben, indem Sie/DNO \_ Strict als Compileroption angeben.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711976"
---
# <a name="disabling-strict"></a>Deaktivieren von Strict

Wenn Sie die **strikte** Typüberprüfung deaktivieren möchten, definieren Sie den Symbolnamen " **No \_ Strict**". In Visual C/C++ können Sie diese Definition auch in der Befehlszeile oder in einem Makefile-Element angeben, indem Sie **/DNO \_ Strict** als Compileroption angeben.

Fügen Sie vor dem einschließen von Windows. h eine **\# define** -Anweisung ein, um **keine \_ strikte** Datei zu definieren:


```C++
#define NO_STRICT
#include <windows.h>
```



Um optimale Ergebnisse zu erzielen, sollten Sie auch die Warnstufe für Fehlermeldungen auf mindestens **/w3** festlegen. Dies ist bei Anwendungen für Windows immer empfehlenswert, da eine Codierungs Praxis, die eine Warnung auslöst (z. b. das übergeben der falschen Anzahl von Parametern), in der Regel zur Laufzeit einen schwerwiegenden Fehler verursacht, wenn Sie nicht korrigiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von Strict](enabling-strict.md)
</dt> <dt>

[Strikte Konformität](strict-compliance.md)
</dt> </dl>

 

 




