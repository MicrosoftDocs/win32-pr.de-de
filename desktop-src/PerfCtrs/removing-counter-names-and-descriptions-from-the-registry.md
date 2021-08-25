---
description: Das Unlodctr-Tool entfernt die von lodctr erstellten Registrierungseinträge.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Entfernen von Indikatornamen und Beschreibungen aus der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c086520f1fb261a0b9850c03f2aee28065a03ee514df277fbf1cae602deed6a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962350"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a>Entfernen von Indikatornamen und Beschreibungen aus der Registrierung

Das **Unlodctr-Tool** entfernt die von lodctr erstellten **Registrierungseinträge.** Der Anwendungsname, den Sie an **unlodctr** übergeben, muss mit dem Namen des Anwendungsschlüssels übereinstimmen, den Sie unter dem Schlüssel **Dienste erstellt** haben. [](creating-the-applications-performance-key.md) Weitere Informationen zum Ausführen **von unlodctr finden** Sie unter Hilfe- und Supportcenter.

## <a name="using-unlodctr"></a>Verwenden von unlodctr

Das **unlodctr-Tool** sucht den ersten und letzten Leistungsindikator und hilft bei der Indizierung von Werten mithilfe der benannten Registrierungswerte wie unter dem **Leistungsschlüssel Ihrer** Anwendung. Das **unlodctr-Tool** verwendet den Indexwertbereich, um  den Text für jeden Sprachbezeichner aus **Den Leistungsindikatoren** und Hilfewerten zu entfernen.

Mithilfe der Indexwerte **werden von unlodctr** die folgenden Änderungen an der Registrierung vorgenommen.

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

Das **unlodctr-Tool** entfernt auch die Werte für First **Counter,** Last **Counter,** First  **Help,** **Last Help** und **Object List** aus dem Leistungsschlüssel der Anwendung unter **HKEY LOCAL \_ \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ *application-name* \\ **Performance**.

> [!Note]  
> Die Entladefunktion **von unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), wird in Loadperf.h deklariert und aus Loadperf.dll. Dadurch können Sie diese Funktion direkt aus Ihrem Deinstallationsprogramm aufrufen.

 

 

 



