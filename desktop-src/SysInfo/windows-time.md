---
description: Windows Zeit ist die Anzahl von Millisekunden, die seit dem letzten Start des Systems verstrichen sind.
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Windows-Zeitdienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363f455842a144decc9db7f4d15fa3353b16e74290252b911a814eb62832a790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884046"
---
# <a name="windows-time"></a>Windows-Zeitdienst

*Windows Zeit* ist die Anzahl von Millisekunden, die seit dem letzten Start des Systems verstrichen sind. Dieses Format ist hauptsächlich aus Gründen der Abwärtskompatibilität mit 16-Bit-Windows vorhanden. Um sicherzustellen, dass Anwendungen, die für 16-Bit-Windows entwickelt wurden, weiterhin erfolgreich ausgeführt werden, gibt die [**GetTickCount-Funktion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) die aktuelle Windows Zeit zurück.

In der Regel verwenden Sie die [**GetTickCount-**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) oder [**GetTickCount64-Funktion,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) um die aktuelle Windows Zeit mit der von der [**GetMessageTime-Funktion zurückgegebenen**](/windows/win32/api/winuser/nf-winuser-getmessagetime) Zeit zu vergleichen. **GetMessageTime** gibt den Windows Zeitpunkt zurück, zu dem die angegebene Nachricht erstellt wurde. **GetTickCount** und **GetTickCount64** sind auf die Auflösung des Systemtimers beschränkt, die ungefähr 10 Millisekunden bis 16 Millisekunden beträgt. Die von **GetTickCount** oder **GetTickCount64** abgerufene verstrichene Zeit umfasst die Zeit, die das System im Standbymodus oder Ruhezustand aufwendet.

Wenn Sie einen Zeitgeber mit höherer Auflösung benötigen, verwenden Sie die [**QueryUnbiasedInterruptTime-Funktion,**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) einen [Multimediatimer](/windows/desktop/Multimedia/multimedia-timers)oder einen [Zeitgeber mit hoher Auflösung.](../winmsg/about-timers.md) Die von der **QueryUnbiasedInterruptTime-Funktion** abgerufene verstrichene Zeit umfasst nur die Zeit, die das System im Arbeitszustand aufwendet.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP/2000:** Die [**QueryUnbiasedInterruptTime-Funktion**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) ist ab Windows 7 und Windows Server 2008 R2 verfügbar.

Sie können den System up Time-Leistungsindikator verwenden, um die Anzahl von Sekunden abzurufen, die seit dem Starten des Computers verstrichen sind. Dieser Leistungsindikator kann aus den Leistungsdaten im Registrierungsschlüssel **HKEY \_ PERFORMANCE \_ DATA** abgerufen werden. Der zurückgegebene Wert ist ein 8-Byte-Wert. Weitere Informationen finden Sie unter [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

 

 
