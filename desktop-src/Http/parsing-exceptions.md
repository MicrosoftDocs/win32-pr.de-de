---
title: Auswerten von Ausnahmen
description: Die HTTP-Server-API stellt Registrierungsschlüssel zur Verfügung, um das Durchsuchen von Ausnahmen zur HTTP/1.1-Spezifikation aus Gründen der Abwärtskompatibilität
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Auswerten von Ausnahmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa071f141539a159d09f6a53f2e78a81bf75327b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947824"
---
# <a name="parsing-exceptions"></a>Auswerten von Ausnahmen

Die HTTP-Server-API stellt Registrierungsschlüssel zur Verfügung, um das Durchsuchen von Ausnahmen zur HTTP/1.1-Spezifikation aus Gründen der Abwärtskompatibilität Diese Ausnahmen sind nicht standardmäßig aktiviert und sollten nur für die Fall Weise aktiviert werden, wenn auf dem Server Kompatibilitätsprobleme mit HTTP-Clients auftreten. Diese Werte werden unter folgendem Registrierungs Speicherort erstellt:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

In der folgenden Tabelle sind die zur Unterstützung der aufgeführten Ausnahmen angegebenen Registrierungsschlüssel aufgeführt. Legen Sie zum Aktivieren einer Ausnahme den entsprechenden Schlüsselwert auf 1 fest, und starten Sie den HTTP-Dienst neu.



| Schlüsselname                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Allowweakheadernamesyntax (DWORD)     | Ermöglicht dem http-Parser das akzeptieren von Header Namen mit Trennzeichen wie z. b. "?".                                                                                                                                                                                                                                                                                            |
| Allowweakheadervaluesyntax (DWORD)    | Ermöglicht dem http-Parser das akzeptieren von Header Werten mit unformatierten (ohne Escapezeichen) Steuerzeichen.                                                                                                                                                                                                                                                                                   |
| Allowcaseinsensitiveverbs (DWORD)     | Ermöglicht es dem http-Parser, HTTP-Methoden/-Verben wie "Get" in Kleinbuchstaben zu akzeptieren.                                                                                                                                                                                                                                                                                                    |
| "Zugewunescapedrestrictedchars" (DWORD) | Ermöglicht es dem http-Parser, Steuerzeichen in abspath und Abfrage Zeichenfolgen der URL zu akzeptieren. Im Fall einer absolute URL werden Steuerzeichen im Hostnamen nicht zugelassen. Alle URLs von URLs, nämlich UTF8, DBCS und ANSI, lassen Steuerzeichen zu. Alle ASCII-Steuerzeichen mit Ausnahme von NUL (0x00), LF (0x0A), CR (0x0D) und horizontaler Registerkarte (0x09) sind zulässig. |



 

 

 




