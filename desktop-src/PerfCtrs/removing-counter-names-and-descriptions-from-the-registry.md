---
description: Das unlodctr-Tool entfernt die von lodctr erstellten Registrierungseinträge.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Entfernen von Counter-Namen und Beschreibungen aus der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ea8c0a8efbe9a798f980a061c6cfc65745b89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363469"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a>Entfernen von Counter-Namen und Beschreibungen aus der Registrierung

Das **unlodctr** -Tool entfernt die von **Lodctr** erstellten Registrierungseinträge. Der Name der Anwendung, die Sie an **unlodctr** übergeben, muss mit dem [Namen des Anwendungs Schlüssels](creating-the-applications-performance-key.md) , den Sie unter dem **Dienst** Schlüssel erstellt haben, identisch sein. Ausführliche Informationen zum Ausführen von **unlodctr** finden Sie unter Hilfe und Support Center.

## <a name="using-unlodctr"></a>Verwenden von unlodctr

Das **unlodctr** -Tool sucht den ersten und den letzten Indikator und unterstützt die Indexwerte mithilfe der benannten Registrierungs Werte unter dem **Leistungs** Schlüssel Ihrer Anwendung. Das **unlodctr** **-Tool** verwendet den Bereich der Indexwerte, um den Text aus den Indikatoren und den **Hilfe** Werten für die einzelnen Sprachen Bezeichner zu entfernen.

Durch die Verwendung der Indexwerte nimmt **unlodctr** die folgenden Änderungen an der Registrierung vor.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = updated if changed
                  Last Help = updated if changed
                  \009
                     Counters = application text removed
                     Help = application text removed
                  \supported language, other than English
                     Counters = application text removed
                     Help = application text removed
```

Das **unlodctr** -Tool entfernt auch die Werte für " **Counter**", " **Last Counter**", " **First Help**", " **Last Help**" und " **Object List** " aus dem **Leistungs** Schlüssel der Anwendung unter **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ *Application-Name* \\ **Performance**.

> [!Note]  
> Die Entlade Funktion von **unlodctr**, [**unloadperfcountertextstrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), wird in "LoadPerf. h" deklariert und aus Loadperf.dll exportiert. Dies ermöglicht es Ihnen, diese Funktion direkt über das Deinstallationsprogramm aufzurufen.

 

 

 



