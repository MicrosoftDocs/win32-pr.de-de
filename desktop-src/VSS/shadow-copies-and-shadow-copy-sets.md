---
description: Eine Schattenkopie ist eine Momentaufnahme eines Volumes, die alle Daten dupliziert, die zu einem genau definierten Zeitpunkt auf diesem Volume gespeichert sind. VSS identifiziert jede Schattenkopie durch eine persistente GUID.
ms.assetid: 8ef2478a-c8bc-4517-9a14-e1d9226ec4cd
title: Schattenkopien und Schattenkopiesätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764478c371cf4a622612865ef7a529955780d82847125874253533d331c195f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998154"
---
# <a name="shadow-copies-and-shadow-copy-sets"></a>Schattenkopien und Schattenkopiesätze

Eine [*Schattenkopie*](vssgloss-s.md) ist eine Momentaufnahme eines Volumes, die alle Daten dupliziert, die zu einem genau definierten Zeitpunkt auf diesem Volume gespeichert sind. VSS identifiziert jede Schattenkopie durch eine persistente GUID.

Ein [*Schattenkopiesatz ist*](vssgloss-s.md) eine Sammlung von Schattenkopien verschiedener Volumes, die alle gleichzeitig aufgenommen werden. VSS identifiziert jeden Schattenkopiesatz durch eine persistente GUID.

Wie sich ein bestimmter Hardware- oder Softwareanbieter für die Implementierung von Schattenkopien entscheidet, liegt vollständig in seinem Ermessen. Sobald eine Schattenkopie erstellt wurde, stehen dem System zwei Bilder des kopierten Schattenvolumens zur Verfügung: das ursprüngliche Volume, auf das herkömmlicher Weise zugegriffen werden kann. und die kopierten Daten, auf die über die VSS-API zugegriffen werden kann.

Dadurch können zwei Sätze von Aktivitäten gleichzeitig stattfinden:

-   Normale Anwendungen im System können schnell mit der Verwendung des ursprünglichen Volumes fortfahren oder fortsetzen und daten auf dem Datenträger aktualisieren.
-   Anwendungen, die die VSS-Anforderungs-API für den Zugriff auf das Schattenkopie-Volume verwenden, können Sicherungen oder ähnliche Vorgänge ausführen.

Schattenkopien müssen nicht für jede Datei, jedes Verzeichnis oder Volume auf die gleiche Weise implementiert werden. Verschiedene Implementierungen des Schattenkopiemechanismus [*(Anbieter*](vssgloss-p.md)) können verschiedene Ansätze zum Erstellen einer Schattenkopie verwenden. Für alle Anwendungen, die die VSS-API verwenden, sollten jedoch alle Schattenkopien identisch sein.

Informationen zur Standardimplementierung Windows-Anbieters finden Sie unter [Systemanbieter](providers.md).

## <a name="default-shadow-copy-state"></a>Standardstatus der Schattenkopie

Obwohl das Dateisystem alle E/A-Puffer leert, bevor eine Schattenkopie erstellt wird, wird dadurch nicht sichergestellt, dass unvollständige E/A ordnungsgemäß verarbeitet werden.

Wenn das System über keine VSS-fähigen Anwendungen verfügt, werden die Daten in einer Schattenkopie daher als absturz konsistent [*bezeichnet.*](vssgloss-c.md) Eine Schattenkopie in einem absturzeinheitlichen Zustand enthält ein Image des Datenträgers, das mit dem Image identisch ist, das nach einem schwerwiegenden Herunterfahren des Systems vorhanden wäre. Alle geöffneten Dateien sind weiterhin auf dem Volume vorhanden, aber es ist nicht garantiert, dass sie frei von unvollständigen E/A-Vorgängen oder Datenbeschädigungen sind.

Obwohl der absturz konsistente Zustand nicht alle Probleme im Zusammenhang mit der [](common-volume-backup-issues.md)Definition eines stabilen Sicherungssets vollständig behandelt (siehe Allgemeine Probleme bei der Volumesicherung), hat er gegenüber dem Sicherungssatz mehrere Vorteile, die herkömmliche Sicherungsvorgänge verwenden müssten:

-   Ein Volume, das in einer Schattenkopie enthalten ist, enthält auch in einem absturz konsistenten Zustand weiterhin alle Dateien. Ein Sicherungssatz, der ohne Schattenkopie erstellt wurde, würde nicht alle Dateien enthalten, die zum Zeitpunkt der Sicherung geöffnet waren. Dateien, die zum Zeitpunkt des Sicherungsvorgang geöffnet bleiben, werden von der Sicherung ausgeschlossen.
-   Die Schattenkopie des Volumes wird zu einem Zeitpunkt erstellt und nicht durch das Durchlaufen eines aktiven Dateisystems, was in der Regel viel mehr Zeit erfordert.

Anwendungen auf einem System, die VSS-ler sind – Wortprozessoren, Editoren und so weiter – haben ihre Dateien wahrscheinlich in einem absturzeinheitlichen Zustand. VSS-orientierte Anwendungen (Writer) können ihre Aktionen jedoch so koordinieren, dass der Status ihrer Dateien in der Schattenkopie klar definiert und konsistent ist.

## <a name="shadow-copy-freeze-and-thaw"></a>Einfrieren und Auftauen von Schattenkopien

Die Erstellung jedes VSS-Schattenkopie-Vorgangs wird durch Freeze- und [*Thaw-Ereignisse*](vssgloss-t.md) in Klammern gesetzt, die Writer verwenden, um ihre Dateien vor der Schattenkopie in einen stabilen Zustand zu bringen. [](vssgloss-f.md)

Das Einfrieren und Auftauen von Ereignissen als Teil des VSS-Modells bedeutet:

-   Die Behandlung des Freeze-Ereignisses bedeutet, dass diejenigen, die Writer entwickeln, einen klar definierten Punkt im Sicherungszyklus haben müssen, an dem sie sicherstellen, dass alle Schreibvorgänge auf dem Datenträger beendet werden und dass dateien sich in einem klar definierten Zustand für die Sicherung befinden.
-   Die Behandlung des Thaw-Ereignisses bietet den Mechanismus, mit dem Writer Schreibvorgänge auf dem Datenträger fortsetzen und alle temporären Dateien oder anderen temporären Zustandsinformationen bereinigt, die in Verbindung mit der Schattenkopie erstellt wurden.
-   Das Standardfenster zwischen den Ereignissen Freeze und Thaw ist kurz (in der Regel 60 Sekunden). Daher kann die tatsächliche Unterbrechung eines Diensts, der von einem Writer zur Verfügung steht, minimiert werden.
-   Die Behandlung anderer Ereignisse (z. B. PrepareForSnapshot) vor bzw. nach den Freeze- bzw. Thaw-Ereignissen bietet die erforderliche Flexibilität, damit Writer komplizierte Vorgänge abschließen können, um Schattenkopien zu unterstützen.

 

 



