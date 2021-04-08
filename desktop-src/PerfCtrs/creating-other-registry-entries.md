---
description: Die openperformancedata-Funktion der Leistungs-DLLs nimmt ein Zeichen folgen Argument als Eingabe an.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Erstellen anderer Registrierungseinträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dfc3b46ce642069210df5112eb41cac9a038797
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959767"
---
# <a name="creating-other-registry-entries"></a>Erstellen anderer Registrierungseinträge

Die [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -Funktion der Leistungs-DLL nimmt als Eingabe ein Zeichen folgen Argument an. Um eine Eingabe Zeichenfolge für die Open-Funktion bereitzustellen, fügen Sie einen **Verknüpfungs** Schlüssel unter Ihrem **Dienst** Schlüssel ein. Der **Verknüpfungs** Schlüssel enthält einen **Export** Wert. Legen Sie die Wertdaten für **Export** in die Eingabe Zeichenfolge fest, die Sie an die Open-Funktion übergeben möchten. Der Datentyp des **Exports** lautet **" \_ reg \_ MultiSZ**".

Wenn **Export** nicht definiert ist (der **Export** ist optional), übergibt das System **null** an die [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -Funktion.

Wenn mehr als eine Anwendung dieselbe Leistungs-DLL gemeinsam nutzt, enthält jede Anwendung in der Regel einen **Verknüpfungs** Schlüssel und einen **Export** Wert, um Kontext anzugeben, welche Anwendung die DLL aufrufen soll.

Im folgenden werden die Registrierungseinträge angezeigt:

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

Standardmäßig müssen die [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -und [**collectperformancedata**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) -Funktionen der Leistungs-DLL innerhalb von 10.000 Millisekunden zurückgeben. Wenn dies nicht der Wert ist, verwendet das System nicht die von der DLL zurückgegebenen Daten. Die Anwendung kann den Timeout Wert erhöhen oder verringern, indem Sie unter Ihrem **Leistungs** Schlüssel einen Registrierungs Wert für das **Öffnen von Timeout** oder einen **Timeout** Wert für den Registrierungs Wert angibt, wie im folgenden Beispiel gezeigt.

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

Zum Abrufen der Leistungsdaten für einige Anwendungen (solche, die Leistungsindikatoren mithilfe der [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion zurückgeben) ist es erforderlich [**, die Funktion "-Funktion"**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zu verwenden, um das Gerät zu öffnen, das der Anwendung zugeordnet ist. In diesem Fall muss der in " **kreatefile** " angegebene Name auch im Knoten "DOS-Geräte" der Registrierung installiert werden, wie hier gezeigt:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
