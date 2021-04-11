---
description: Windows-Zeit gibt die Anzahl der Millisekunden an, die seit dem letzten Start des Systems verstrichen sind.
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Windows-Zeitdienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af776e2cc5a36993f6be0e0776d5b73fab6622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131284"
---
# <a name="windows-time"></a>Windows-Zeitdienst

*Windows-Zeit* gibt die Anzahl der Millisekunden an, die seit dem letzten Start des Systems verstrichen sind. Dieses Format ist hauptsächlich aus Gründen der Abwärtskompatibilität mit 16-Bit-Fenstern vorhanden. Um sicherzustellen, dass die für 16-Bit-Windows entwickelten Anwendungen weiterhin erfolgreich ausgeführt werden, gibt die [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) -Funktion die aktuelle Windows-Zeit zurück.

Normalerweise verwenden Sie die [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) -Funktion oder die [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) -Funktion, um die aktuelle Windows-Zeit mit der von der [**getmessagetime**](/windows/win32/api/winuser/nf-winuser-getmessagetime) -Funktion zurückgegebenen Zeit zu vergleichen. **Getmessagetime** gibt die Windows-Zeit zurück, zu der die angegebene Meldung erstellt wurde. **GetTickCount** und **GetTickCount64** sind auf die Auflösung des Systemzeit Gebers beschränkt, was ungefähr 10 Millisekunden bis 16 Millisekunden beträgt. Die verstrichene Zeit, die von **GetTickCount** oder **GetTickCount64** abgerufen wird, umfasst die Zeit, die das System in den Standbymodus oder

Wenn Sie einen Zeitgeber höherer Auflösung benötigen, verwenden Sie die [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) -Funktion, einen [Multimedia-Timer](/windows/desktop/Multimedia/multimedia-timers)oder einen Zeit Geber mit [hoher Auflösung](../winmsg/about-timers.md). Die verstrichene Zeit, die von der **queryunbiasedinterrupttime** -Funktion abgerufen wird, umfasst nur die Zeit, die das System im Arbeitszustand verbringt.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP/2000:** Die [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) -Funktion ist ab Windows 7 und Windows Server 2008 R2 verfügbar.

Mithilfe des Leistungs Zählers System Zeit können Sie die Anzahl der Sekunden abrufen, die seit dem Start des Computers verstrichen sind. Dieser Leistungswert kann aus den Leistungsdaten in den **HKEY- \_ Leistungs \_ Daten** des Registrierungsschlüssels abgerufen werden. Der zurückgegebene Wert ist ein 8-Byte-Wert. Weitere Informationen finden Sie unter [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

 

 
