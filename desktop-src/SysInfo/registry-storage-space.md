---
description: Es gibt zwar nur wenige technische Einschränkungen hinsichtlich des Typs und der Größe der Daten, die eine Anwendung in der Registrierung speichern kann, aber es gibt bestimmte praktische Richtlinien, die die Systemeffizienz herauf Stufen.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Registrierungs Speicherplatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b776498528d6c7deaacd92f9e010758b5d57c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357810"
---
# <a name="registry-storage-space"></a>Registrierungs Speicherplatz

Es gibt zwar nur wenige technische Einschränkungen hinsichtlich des Typs und der Größe der Daten, die eine Anwendung in der Registrierung speichern kann, aber es gibt bestimmte praktische Richtlinien, die die Systemeffizienz herauf Stufen. Eine Anwendung sollte Konfigurations-und Initialisierungs Daten in der Registrierung speichern und andere Arten von Daten an einem anderen Ort speichern.

Im Allgemeinen sollten Daten, die aus mehr als einem oder zwei Kilobyte (K) bestehen, als Datei gespeichert werden, und es wird auf einen Schlüssel in der Registrierung verwiesen, anstatt als Wert gespeichert zu werden. Anstatt große Datenelemente in der Registrierung zu duplizieren, sollte eine Anwendung die Daten als Datei speichern und auf die Datei verweisen. Der binäre Code der ausführbaren Datei sollte nie in der Registrierung gespeichert werden.

Ein Wert Eintrag verwendet viel weniger Registrierungs Raum als ein Schlüssel. Um Speicherplatz zu sparen, sollte eine Anwendung ähnliche Daten als Struktur gruppieren und die Struktur als Wert speichern, anstatt jedes der Strukturmember als separaten Schlüssel zu speichern. (Das Speichern der Daten in Binär Form ermöglicht einer Anwendung das Speichern von Daten in einem Wert, der andernfalls aus mehreren inkompatiblen Typen besteht.)

Sichten der Registrierungsdateien werden im Auslagerungsseiten-Speicher zugeordnet.

**Windows Server 2008 für 32 Bit, Windows Vista mit SP1 für 32-Bit, Windows Vista, Windows Server 2003, Windows XP:** Sichten der Registrierungsdateien werden im Cache Adressraum des Computers zugeordnet. Daher wird unabhängig von der Größe der Registrierungsdaten nicht mehr als 4 Megabyte (MB) abgerechnet.

Die maximale Größe einer Registrierungs Struktur beträgt 2 GB, mit Ausnahme der Systemstruktur.

**Windows Server 2003 mit SP1, Windows Server 2003 und Windows XP:** Es gibt keine expliziten Grenzwerte für die Gesamtmenge des Speicherplatzes, der von Strukturen in auslagertem Pool Speicher und Speicherplatz beansprucht werden kann, obwohl sich System Kontingente möglicherweise auf die tatsächliche maximale Größe auswirken. Die maximale Größe einer Registrierungs Struktur ist ab Windows Server 2003 mit Service Pack 2 (SP2) auf 2 GB beschränkt.

Die maximale Größe der Systemstruktur wird durch den physischen Speicher eingeschränkt, wie in der folgenden Tabelle gezeigt. 

| System                      | Maximale Größe der Systemstruktur                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| x86-basierte Systeme           | 50% des physischen Arbeitsspeichers, bis zu 400 MB. **Windows Server 2003 mit SP2, Windows Server 2003 mit SP1, Windows Server 2003 und Windows XP:** 25% des physischen Arbeitsspeichers, bis zu 200 MB.<br/>                                    |
| x64-basierte Systeme           | 50% des physischen Arbeitsspeichers, bis zu 1,5 GB. **Windows Server 2003 mit SP2:** 25% des System Arbeitsspeichers, bis zu 200 MB.<br/> **Windows Server 2003 mit SP1, Windows Server 2003 und Windows XP 64-Bit Edition:** 32 MB.<br/> |
| Intel Itanium-basierte Systeme | 50% des physischen Arbeitsspeichers, bis zu 1 GB. **Windows Server 2008, Windows Vista, Windows Server 2003 mit SP2, Windows Server 2003 mit SP1, Windows Server 2003 und Windows XP 64-Bit Edition:** 32 MB.<br/>                         |



 

## <a name="windows-2000"></a>Windows 2000

Registrierungsdaten werden im ausgelagerten Pool gespeichert, einem Bereich von physischem Arbeitsspeicher, der für Systemdaten verwendet wird, die auf den Datenträger geschrieben werden können, wenn Sie nicht verwendet werden. Mit dem Wert **RegistrySizeLimit** wird die maximale Größe des Auslagerungs Pools festgelegt, der von Registrierungsdaten von allen Anwendungen genutzt werden kann. Dieser Wert befindet sich im folgenden Registrierungsschlüssel:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

Standardmäßig beträgt das Registrierungs Größenlimit 25 Prozent des Auslagerungs Pools. (Die Standardgröße des Auslagerungs Pools beträgt 32 MB, also 8 MB.) Das System stellt sicher, dass der Mindestwert von " **RegistrySizeLimit** " 4 MB und der Höchstwert ungefähr 80 Prozent des Werts "Wert von" **paarweise** "ist. Wenn der Wert dieses Eintrags größer als 80 Prozent der Größe des Auslagerungs Pools ist, legt das System die maximale Größe der Registrierung auf 80 Prozent der Größe des Auslagerungs Pools fest. Dies verhindert, dass die Registrierung Speicherplatz beansprucht, der von Prozessen benötigt wird. Beachten Sie, dass durch Festlegen dieses Werts weder Speicherplatz im Auslagerungs Pool belegt wird noch sichergestellt wird, dass der Speicherplatz bei Bedarf verfügbar ist.

Die Größe des ausgelagerten Pools wird durch den Wert für den Wert von " **pgedpoolsize** " im folgenden Registrierungsschlüssel bestimmt:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

Ein Beispiel für die Bestimmung der aktuellen und der maximalen Größe der Registrierung finden Sie unter [bestimmen der Registrierungs Größe](determining-the-registry-size.md).

Der maximale Auslagerungs Pool beträgt ungefähr 300.470 MB, sodass die Registrierungs Größenbeschränkung 240-376 MB beträgt. Wenn jedoch der/3GB-Schalter verwendet wird, beträgt die maximale Größe des Auslagerungs Pools 192 MB, sodass die Registrierung maximal 153,6 MB betragen kann.

 

 




