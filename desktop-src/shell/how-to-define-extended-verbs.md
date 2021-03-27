---
description: Sie können die Registrierung verwenden, um ein oder mehrere erweiterte Verben zu definieren. Die zugehörigen Befehle werden nur angezeigt, wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, während er die UMSCHALTTASTE drückt.
ms.assetid: C6E51716-1D4F-454F-9AF4-8D0E486CB885
title: Definieren erweiterter Verben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4bd8cca04b40bb0b0b77bab5fd7546fd5bff45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979577"
---
# <a name="how-to-define-extended-verbs"></a>Definieren erweiterter Verben

Sie können die Registrierung verwenden, um ein oder mehrere erweiterte Verben zu definieren. Die zugehörigen Befehle werden nur angezeigt, wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, während er die UMSCHALTTASTE drückt.

## <a name="instructions"></a>Instructions


Wenn Sie ein Verb als erweitert definieren möchten, fügen Sie einfach einen "erweiterten" **reg \_ SZ** -Wert zum Unterschlüssel des Verbs hinzu. Dem Wert dürfen keine Daten zugeordnet werden. Der folgende Beispiel Registrierungs Eintrag zeigt das Beispiel aus dem vorherigen Abschnitt, wobei "doit" als erweitertes Verb definiert ist.

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

 

 



