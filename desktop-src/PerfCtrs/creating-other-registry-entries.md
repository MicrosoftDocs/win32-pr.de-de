---
description: Die OpenPerformanceData-Funktion der Leistungs-DLLs verwendet ein Zeichenfolgenargument als Eingabe.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Erstellen anderer Registrierungseinträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ad9fe960713a481ba5a9b8f4b73e11bdbdd4d9fe9474b04b994e373ce8e1bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683970"
---
# <a name="creating-other-registry-entries"></a>Erstellen anderer Registrierungseinträge

Die [**OpenPerformanceData-Funktion**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) der Leistungs-DLL nimmt ein Zeichenfolgenargument als Eingabe an. Um ihrer geöffneten Funktion eine Eingabezeichenfolge bereitzustellen, fügen Sie einen **Verknüpfungsschlüssel** unter Ihren **Dienstschlüssel** ein. Der **Verknüpfungsschlüssel** enthält einen **Exportwert.** Legen Sie die Wertdaten für **Export** auf die Eingabezeichenfolge fest, die Sie an Ihre geöffnete Funktion übergeben möchten. Der Datentyp von **Export** ist **REG MULTI \_ \_ SZ**.

Wenn **Export** nicht definiert ist **(Export** ist optional), übergibt das System **NULL** an Ihre [**OpenPerformanceData-Funktion.**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))

Wenn mehrere Anwendungen dieselbe Leistungs-DLL gemeinsam nutzen, enthält jede Anwendung in der Regel einen **Verknüpfungsschlüssel** und einen **Exportwert,** um Kontext für die Anwendung bereitzustellen, die die DLL aufruft.

Im Folgenden werden die Registrierungseinträge angezeigt:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name-1
               \Linkage
                  Export = app-1 context strings
               \Performance
                  Library = perfctrs.dll
            \application-name-2
               \Linkage
                  Export = app-2 context strings
               \Performance
                  Library = perfctrs.dll
```

Standardmäßig müssen die Funktionen [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) und [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) der Leistungs-DLL innerhalb von 10.000 Millisekunden zurückgeben. Wenn nicht, verwendet das System nicht die Daten, die von der DLL zurückgegeben werden. Die Anwendung kann den Timeoutwert erhöhen oder verringern, indem sie einen **Open Timeout-** oder **Collect Timeout-Registrierungswert** unter ihrem **Leistungsschlüssel** angibt, wie im folgenden Beispiel gezeigt.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Open Timeout = Timeout value for your open function, in milliseconds
                  Collect Timeout = Timeout value for your collect function, in milliseconds
```

Zum Abrufen der Leistungsdaten für einige Anwendungen (die Leistungsindikatoren mithilfe der [**DeviceIoControl-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) zurückgeben), müssen Sie die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) verwenden, um das gerät zu öffnen, das der Anwendung zugeordnet ist. In diesem Fall muss der in **CreateFile** angegebene Name auch im Knoten DOS-Geräte der Registrierung installiert werden, wie hier gezeigt:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
