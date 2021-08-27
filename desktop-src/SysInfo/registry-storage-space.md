---
description: Obwohl es einige technische Grenzwerte für den Typ und die Größe der Daten gibt, die eine Anwendung in der Registrierung speichern kann, gibt es bestimmte praktische Richtlinien, um die Systemeffizienz zu steigern.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Registrierungsspeicherplatz Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00414edbd34452fd6943a4d73a2ebe85af5d38884ddd0ca77f1d8fb41ae6e0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885078"
---
# <a name="registry-storage-space"></a>Registrierungsspeicherplatz Storage

Obwohl es einige technische Grenzwerte für den Typ und die Größe der Daten gibt, die eine Anwendung in der Registrierung speichern kann, gibt es bestimmte praktische Richtlinien, um die Systemeffizienz zu steigern. Eine Anwendung sollte Konfigurations- und Initialisierungsdaten in der Registrierung speichern und andere Arten von Daten an anderer Stelle speichern.

Im Allgemeinen sollten Daten, die aus mehr als einem oder zwei Kilobytes (K) bestehen, als Datei gespeichert und mithilfe eines Schlüssels in der Registrierung als Wert bezeichnet werden. Anstatt große Daten in der Registrierung zu duplizieren, sollte eine Anwendung die Daten als Datei speichern und auf die Datei verweisen. Ausführbarer Binärcode sollte nie in der Registrierung gespeichert werden.

Ein Werteintrag verwendet viel weniger Registrierungsspeicherplatz als ein Schlüssel. Um Speicherplatz zu sparen, sollte eine Anwendung ähnliche Daten als Struktur gruppieren und die Struktur als Wert speichern, anstatt jeden der Strukturmitglieder als separaten Schlüssel zu speichern. (Das Speichern der Daten in binärer Form ermöglicht einer Anwendung, Daten in einem Wert zu speichern, der andernfalls aus mehreren inkompatiblen Typen besteht.)

Ansichten der Registrierungsdateien werden im Ausseitenpoolspeicher zugeordnet.

**Windows Server 2008 für 32-Bit, Windows Vista mit SP1 für 32-Bit, Windows Vista, Windows Server 2003, Windows XP:** Ansichten der Registrierungsdateien werden im Adressraum des Computercaches zugeordnet. Daher werden unabhängig von der Größe der Registrierungsdaten nicht mehr als 4 Megabyte (MB) berechnet.

Die maximale Größe einer Registrierungsstruktur beträgt 2 GB, mit Ausnahme der Systemstruktur.

**Windows Server 2003 mit SP1, Windows Server 2003 und Windows XP:** Es gibt keine expliziten Grenzwerte für die Gesamtmenge des Speicherplatzes, der von Hives im Ausseitenpoolspeicher und im Speicherplatz auf dem Datenträger verbraucht werden kann, obwohl sich Systemkontingente möglicherweise auf die tatsächliche maximale Größe auswirken. Die maximale Größe einer Registrierungsstruktur war ab Windows Server 2003 mit Service Pack 2 (SP2) auf 2 GB beschränkt.

Die maximale Größe der Systemstruktur wird durch den physischen Speicher beschränkt, wie in der folgenden Tabelle gezeigt. 

| System                      | Maximale Größe der Systemstruktur                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| x86-basierte Systeme           | 50 Prozent des physischen Speichers, bis zu 400 MB. **Windows Server 2003 mit SP2, Windows Server 2003 mit SP1, Windows Server 2003** und Windows XP: 25 Prozent des physischen Arbeitsspeichers, bis zu 200 MB.<br/>                                    |
| x64-basierte Systeme           | 50 Prozent des physischen Speichers, bis zu 1,5 GB. **Windows Server 2003 mit SP2:** 25 Prozent des Systemspeichers, bis zu 200 MB.<br/> **Windows Server 2003 mit SP1, Windows Server 2003 und Windows XP 64-Bit Edition:** 32 MB.<br/> |
| Intel Itanium-basierte Systeme | 50 Prozent des physischen Speichers, bis zu 1 GB. **Windows Server 2008, Windows Vista, Windows Server 2003 mit SP2, Windows Server 2003 mit SP1, Windows Server 2003 und Windows XP 64-Bit Edition:** 32 MB.<br/>                         |



 

## <a name="windows-2000"></a>Windows 2000

Registrierungsdaten werden im ausgelagerten Pool gespeichert, einem Bereich des physischen Speichers, der für Systemdaten verwendet wird, die auf den Datenträger geschrieben werden können, wenn sie nicht verwendet werden. Der **RegistrySizeLimit-Wert** legt die maximale Menge an auspageten Pools fest, die von Registrierungsdaten aller Anwendungen verwendet werden können. Dieser Wert befindet sich im folgenden Registrierungsschlüssel:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

Standardmäßig beträgt das Limit für die Registrierungsgröße 25 Prozent des auspageten Pools. (Die Standardgröße des ausseitigen Pools beträgt 32 MB, also 8 MB.) Das System stellt sicher, dass der Mindestwert von **RegistrySizeLimit** 4 MB beträgt und der Höchstwert ungefähr 80 Prozent des **PagedPoolSize-Werts** beträgt. Wenn der Wert dieses Eintrags größer als 80 Prozent der Größe des ausseitigen Pools ist, legt das System die maximale Größe der Registrierung auf 80 Prozent der Größe des auspageten Pools fest. Dadurch wird verhindert, dass die Registrierung Speicherplatz verbraucht, der von Prozessen benötigt wird. Beachten Sie, dass durch festlegen dieses Werts weder Speicherplatz im ausseitigen Pool reserviert wird noch sichergestellt wird, dass der Speicherplatz bei Bedarf verfügbar ist.

Die Größe des aus paged-Pools wird durch den **PagedPoolSize-Wert** im folgenden Registrierungsschlüssel bestimmt:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

Ein Beispiel zum Bestimmen der aktuellen und maximalen Größe der Registrierung finden Sie unter [Bestimmen der Registrierungsgröße.](determining-the-registry-size.md)

Der maximale Auspagepool beträgt ca. 300.470 MB, sodass das Limit für die Registrierungsgröße 240 bis 376 MB beträgt. Wenn jedoch der Schalter /3GB verwendet wird, beträgt die maximale Größe des aus paged-Pools 192 MB, sodass die Registrierung maximal 153,6 MB betragen kann.

 

 




