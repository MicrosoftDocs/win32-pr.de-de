---
description: Die System Zeit ist das aktuelle Datum und die aktuelle Uhrzeit.
ms.assetid: 1a1e251e-2375-4134-bbd8-1e4670b9f9d2
title: Systemzeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c727e8898fc2bc973d963c3a3c90524ca50958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869204"
---
# <a name="system-time"></a>Systemzeit

Die *System Zeit* ist das aktuelle Datum und die aktuelle Uhrzeit. Das System behält Zeit, sodass Ihre Anwendungen über den richtigen Zugriff auf die genaue Zeit verfügen. Das System basiert auf der *koordinierten Weltzeit* (UTC). Die UTC-basierte Zeit ist lose definiert als das aktuelle Datum und die aktuelle Uhrzeit in Greenwich, England.

Wenn das System zum ersten Mal gestartet wird, wird die Systemzeit auf einen Wert festgelegt, der auf der Echtzeit des Computers basiert, und die Uhrzeit regelmäßig aktualisiert. Verwenden Sie die [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime) -Funktion, um die Systemzeit abzurufen. **GetSystemTime** kopiert die Uhrzeit in eine [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die einzelne Elemente für Monat, Tag, Jahr, Wochentag, Stunde, Minute, Sekunde und Millisekunden enthält. Es ist einfach, dieses Format für einen Benutzer anzuzeigen.

Mit der [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) -Funktion können Sie auch die Systemzeit im Datei Zeitformat abrufen. **GetSystemTimeAsFileTime** kopiert die Uhrzeit in eine [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur.

Verwenden Sie die [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime) -Funktion, um die Systemzeit festzulegen. **SetSystemTime** geht davon aus, dass Sie einen UTC-basierten Zeitpunkt angegeben haben.

Die Funktionen " [**getsystemtimesettings**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment) " und " [**setsystemtimeadjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment) " synchronisieren die Tageszeit mit einer anderen Zeit Quelle, wobei eine periodische Zeitanpassung bei jedem Takt Interrupt angewendet wird.

Beachten Sie, dass das System die Zeit regelmäßig durch Synchronisierung mit einer Zeit Quelle aktualisieren kann. Da die Systemzeit entweder vorwärts oder rückwärts angepasst werden kann, vergleichen Sie die systemzeitmesswerte nicht, um die verstrichene Zeit zu bestimmen. Verwenden Sie stattdessen eine der in [Windows-Zeit](windows-time.md)beschriebenen Methoden.

 

 
