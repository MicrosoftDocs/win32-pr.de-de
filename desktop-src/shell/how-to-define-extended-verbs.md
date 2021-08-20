---
description: Sie können die Registrierung verwenden, um ein oder mehrere erweiterte Verben zu definieren. Die zugeordneten Befehle werden nur angezeigt, wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, während er die UMSCHALTTASTE drückt.
ms.assetid: C6E51716-1D4F-454F-9AF4-8D0E486CB885
title: Definieren von erweiterten Verben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef73244a03101de02653625912701b81aa9e8e11d975f96dd417eaa137bfba07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859717"
---
# <a name="how-to-define-extended-verbs"></a>Definieren von erweiterten Verben

Sie können die Registrierung verwenden, um ein oder mehrere erweiterte Verben zu definieren. Die zugeordneten Befehle werden nur angezeigt, wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, während er die UMSCHALTTASTE drückt.

## <a name="instructions"></a>Anweisungen


Um ein Verb als erweitert zu definieren, fügen Sie einfach dem Unterschlüssel des Verbs einen "erweiterten" **REG \_ SZ-Wert** hinzu. Dem Wert dürfen keine Daten zugeordnet sein. Der folgende Beispielregistrierungseintrag zeigt das Beispiel aus dem vorherigen Abschnitt, wobei "doit" als erweitertes Verb definiert ist.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            extended
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



