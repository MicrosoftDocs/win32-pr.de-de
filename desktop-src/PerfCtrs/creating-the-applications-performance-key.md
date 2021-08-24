---
description: Eine Anwendung, die Leistungsindikatoren unterstützt, muss unter dem Dienstschlüssel über einen Leistungsschlüssel verfügen. Das folgende Beispiel zeigt die Werte, die Sie für diesen Schlüssel einschließen müssen.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Erstellen des Anwendungsleistungsschlüssels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149e8142b892edeb43f5459fe68bc6ad4b7453118c64cb2e288bb334c054fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144033"
---
# <a name="creating-the-applications-performance-key"></a>Erstellen des Leistungsschlüssels der Anwendung

Eine Anwendung, die Leistungsindikatoren unterstützt, muss unter dem **Dienstschlüssel** über einen **Leistungsschlüssel** verfügen. Das folgende Beispiel zeigt die Werte, die Sie für diesen Schlüssel einschließen müssen.

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

Der **Wert Library** stellt den Namen der Leistungs-DLL bereit, und die Werte **Open**, **Collect** und **Close** stellen die Namen der Funktionen bereit, die aus der Leistungs-DLL exportiert werden. Der Datentyp dieser Werte ist **REG \_ SZ.** Wenn ein Consumer Leistungsdaten anfordert, verwendet das System diese Werte, um zu bestimmen, welche Leistungs-DLLs geladen und welche DLL-Funktionen aufgerufen werden sollen.

Der **Library-Wert** kann den DLL-Namen oder einen vollständigen Pfad zur DLL enthalten. Wenn Sie den **REG \_ EXPAND \_ SZ-Datentyp** für **Library** verwenden, können Sie Umgebungsvariablen in Ihrem Pfad angeben.

Der Dienstschlüssel der Anwendung muss vorhanden sein, bevor Sie **lodctr** ausführen können, um Ihre Indikatornamen und Hilfezeichenfolgen zu laden.

Weitere Registrierungswerte, die Sie erstellen können, z. B. das Angeben von Time out-Werten für die Funktionen [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) und [**CollectPerformanceData,**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) finden Sie unter [Creating Other Registry Entries](creating-other-registry-entries.md).

 

 
