---
description: Windows lädt die standardmäßige Microsoft Gina-DLL (MSGina.dll) und führt Sie aus. Sie müssen einen Registrierungsschlüssel Wert ändern, um eine andere Gina zu laden.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Laden und Ausführen einer Gina-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356208"
---
# <a name="loading-and-running-a-gina-dll"></a>Laden und Ausführen einer Gina-dll

Windows lädt die standardmäßige Microsoft Gina-DLL (MSGina.dll) und führt Sie aus. Zum Laden einer anderen [*Gina*](../secgloss/g-gly.md)müssen Sie den folgenden Registrierungsschlüssel Wert ändern:

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

Wenn der GinaDLL-Schlüsselwert vorhanden ist, muss er den Namen einer Gina-DLL enthalten, die von [*Winlogon*](../secgloss/w-gly.md) geladen und verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln und Testen einer Gina-dll](building-and-testing-a-gina-dll.md)
</dt> <dt>

[Gina-Export Funktionen](authentication-functions.md)
</dt> <dt>

[Gina-Strukturen](authentication-structures.md)
</dt> <dt>

[Terminal Dienste-Gina-Funktionen](terminal-services-gina-functions.md)
</dt> </dl>

 

 
