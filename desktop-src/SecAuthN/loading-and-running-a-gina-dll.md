---
description: Windows lädt die Standardmäßige Microsoft GINA DLL (MSGina.dll) und führt sie aus. Um eine andere GINA zu laden, müssen Sie einen Registrierungsschlüsselwert ändern.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Laden und Ausführen einer GINA-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a4e8d68a1e1846a28e1db9402d730834768a132a7c502021fd101f20926f54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140953"
---
# <a name="loading-and-running-a-gina-dll"></a>Laden und Ausführen einer GINA-DLL

Windows lädt die Standardmäßige Microsoft GINA DLL (MSGina.dll) und führt sie aus. Um eine andere [*GINA*](../secgloss/g-gly.md)zu laden, müssen Sie den folgenden Registrierungsschlüsselwert ändern:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

Wenn der GinaDLL-Schlüsselwert vorhanden ist, muss er den Namen einer GINA-DLL enthalten, die [*von Winlogon*](../secgloss/w-gly.md) geladen und verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen und Testen einer GINA-DLL](building-and-testing-a-gina-dll.md)
</dt> <dt>

[GINA-Exportfunktionen](authentication-functions.md)
</dt> <dt>

[GINA-Strukturen](authentication-structures.md)
</dt> <dt>

[GINA-Funktionen für Terminaldienste](terminal-services-gina-functions.md)
</dt> </dl>

 

 
