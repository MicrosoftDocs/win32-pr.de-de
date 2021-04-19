---
description: Eine Anwendung, die Leistungsindikatoren unterstützt, muss unter dem Dienst Schlüssel über einen Leistungs Schlüssel verfügen. Das folgende Beispiel zeigt die Werte, die Sie für diesen Schlüssel einschließen müssen.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Erstellen des Anwendungs Leistungs Schlüssels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d39fb89f7f5feb4e34284b541775b5c093a6bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348015"
---
# <a name="creating-the-applications-performance-key"></a>Erstellen des Leistungs Schlüssels der Anwendung

Eine Anwendung, die Leistungsindikatoren unterstützt, muss unter dem **Dienst** Schlüssel über einen **Leistungs** Schlüssel verfügen. Das folgende Beispiel zeigt die Werte, die Sie für diesen Schlüssel einschließen müssen.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Library = Name of your performance DLL
                  Open = Name of your Open function in your DLL
                  Collect = Name of your Collect function in your DLL
                  Close = Name of your Close function in your DLL
```

Der **Bibliotheks** Wert gibt den Namen der Leistungs-DLL an, und die Werte " **Open**", " **Collect**" und " **Close** " stellen die Namen der Funktionen bereit, die von der Leistungs-DLL exportiert werden. Der Datentyp dieser Werte ist **reg \_ SZ**. Wenn ein Consumer Leistungsdaten anfordert, verwendet das System diese Werte, um zu bestimmen, welche Leistungs-DLLs geladen und welche DLL-Funktionen aufgerufen werden.

Der **Bibliotheks** Wert kann den DLL-Namen oder einen vollständigen Pfad zur dll enthalten. Wenn Sie den reg-Datentyp "reg" für die **Bibliothek** verwenden, können Sie Umgebungsvariablen in Ihrem Pfad angeben. **\_ \_**

Der Dienst Schlüssel der Anwendung muss vorhanden sein, bevor Sie **Lodctr** ausführen können, um ihre Namen und Hilfe Zeichenfolgen zu laden.

Weitere Registrierungs Werte, die Sie erstellen können, wie z. b. das Angeben von Timeout Werten für die [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -Funktion und die [**collectperformancedata**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) -Funktion, finden Sie unter [Erstellen anderer Registrierungseinträge](creating-other-registry-entries.md).

 

 
