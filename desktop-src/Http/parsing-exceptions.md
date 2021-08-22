---
title: Analysieren von Ausnahmen
description: Die HTTP-Server-API bietet Registrierungsschlüssel zur Unterstützung der Analyse von Ausnahmen der HTTP/1.1-Spezifikation aus Gründen der Abwärtskompatibilität.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Analysieren von Ausnahmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b546c5473641bbd5d719908903c2d9e19db25ade2ff6677a5ce5ec7ea472d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950729"
---
# <a name="parsing-exceptions"></a>Analysieren von Ausnahmen

Die HTTP-Server-API bietet Registrierungsschlüssel zur Unterstützung der Analyse von Ausnahmen der HTTP/1.1-Spezifikation aus Gründen der Abwärtskompatibilität. Diese Ausnahmen sind standardmäßig nicht aktiviert und sollten nur von Fall zu Fall aktiviert werden, wenn beim Server Kompatibilitätsprobleme mit HTTP-Clients auftreten. Diese Werte werden unter dem folgenden Registrierungsspeicherort erstellt:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

In der folgenden Tabelle sind registrierungsschlüssel aufgeführt, die zur Unterstützung der aufgeführten Ausnahmen bereitgestellt werden. Legen Sie zum Aktivieren einer Ausnahme den entsprechenden Schlüsselwert auf 1 fest, und starten Sie den HTTP-Dienst neu.



| Schlüsselname                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowWeakHeaderNameSyntax (DWORD)     | Ermöglicht dem HTTP-Parser das Akzeptieren von Headernamen mit Trennzeichen wie "?".                                                                                                                                                                                                                                                                                            |
| AllowWeakHeaderValueSyntax (DWORD)    | Ermöglicht es dem HTTP-Parser, Headerwerte mit unformatierten Steuerzeichen (ohne Leerzeichen) zu akzeptieren.                                                                                                                                                                                                                                                                                   |
| AllowCaseInsensitiveVerbs (DWORD)     | Ermöglicht es dem HTTP-Parser, HTTP-Methoden/-Verben in Kleinbuchstaben wie "get" zu akzeptieren.                                                                                                                                                                                                                                                                                                    |
| AllowUnEscapedRestrictedChars (DWORD) | Ermöglicht es dem HTTP-Parser, Steuerzeichen in Abspath- und Abfragezeichenfolgen der URL zu akzeptieren. Bei einem absolute URL sind Steuerzeichen im Hostnamen nicht zulässig. Alle Arten von URLs, nämlich UTF8, DBCS und ANSI, lassen Steuerzeichen zu. Alle ASCII-Steuerzeichen außer NUL (0x00), LF (0x0a), CR (0x0d) und Horizontal Tab(0x09) sind zulässig. |



 

 

 




