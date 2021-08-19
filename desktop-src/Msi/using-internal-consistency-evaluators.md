---
description: Um eine Datenbank zu überprüfen, verwenden Sie ein spezielles Validierungstool, um eine CUB-Datei, die die internen Konsistenzauswertungen (Internal Consistency Evaluators, ICEs) enthält, mit Ihrer Datenbank zusammenzuführen, die ICEs auszuführen und die Ergebnisse zu melden.
ms.assetid: bdf38673-ee3d-47d8-ad6e-562cd5626918
title: Verwenden interner Konsistenzauswertungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd0964b43bdf237c01b2645ca9556ed5560cefd2b047cc108a8919060d1fad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012748"
---
# <a name="using-internal-consistency-evaluators"></a>Verwenden interner Konsistenzauswertungen

Um eine Datenbank zu überprüfen, verwenden Sie ein spezielles Validierungstool, um eine CUB-Datei, die die [internen Konsistenzauswertungen (Internal Consistency Evaluators,](internal-consistency-evaluators-ices.md) ICEs) enthält, mit Ihrer Datenbank zusammenzuführen, die ICEs auszuführen und die Ergebnisse zu melden. Mehrere dieser Tools werden im Microsoft Windows Software Development Kit (SDK) bereitgestellt. Erstellungsumgebungen von Drittanbietern können auch das ICE-Überprüfungssystem in ihre Erstellungsumgebung integrieren. Es ist auch möglich, ein eigenes Tool zum Durchführen der ICE-Überprüfung zu schreiben. Die meisten ICE-Validierungstools führen die CUB-Datei und Ihre Datenbank in einer dritten temporären Datenbank zusammen. Windows Das Installationsprogramm zeigt Warnungen, Fehler, Debuginformationen und API-Fehler an, während jedes ICE in der CUB-Datei ausgeführt wird. Wenn das Installationsprogramm die Ausführung der ICEs abgeschlossen hat, schließt es die .msi Datei, CUB-Datei und temporäre Datenbank, ohne Änderungen zu speichern. Die .msi-Datei und die CUB-Datei bleiben beim Validierungstest unverändert.

Benutzerdefinierte ICE-Aktionen kommunizieren mit dem Benutzer, indem [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) aufgerufen und eine INSTALLMESSAGE \_ USER-Nachricht gepostet wird. Eine ICE-Nachricht gibt häufig Informationen wie die folgenden zurück:

-   Name des ICE, der einen Fehler gefunden hat
-   Erstellungsdatum des ICE
-   Autor des ICE
-   Datum, an dem der ICE zuletzt geändert wurde.
-   Beschreibung des API-Fehlers, der zu einem Fehler des ICE führt
-   Beschreibung des Fehlers
-   Eine Warnung für den Benutzer
-   Name der Datenbanktabelle, die den Fehler oder die Warnung enthält
-   Name der Tabellenspalte, die den Fehler oder die Warnung enthält
-   Primärschlüssel der Tabelle, die den Fehler oder die Warnung enthält
-   Eine URL zu einer HTML-Datei, die Debugvorschläge enthält
-   Eine Zeichenfolge, die andere Informationen enthalten kann

Autoren von Installationspaketen können benutzerdefinierte ICE-Aktionen schreiben oder den Standardsatz von ICEs verwenden, die in den CUB-Dateien enthalten sind, die mit dem SDK bereitgestellt werden. Weitere Informationen zum Schreiben eines ICE finden Sie unter [Building an ICE](building-an-ice.md).

Nach dem Schreiben der entsprechenden ICEs für die Überprüfung muss ein Entwickler die benutzerdefinierten Aktionen zusammen in einer .msi Datenbank sammeln, die als CUB-Datei bezeichnet wird und nur die ICEs und die erforderlichen Tabellen enthält. Eine CUB-Datei kann nicht installiert werden und wird nur zum Speichern und Bereitstellen des Zugriffs auf benutzerdefinierte ICE-Aktionen verwendet. Weitere Informationen zum Erstellen von CUB-Dateien finden Sie unter [Erstellen einer ICE-Datenbank.](building-an-ice-database.md) Alternativ können Entwickler ihr Installationspaket mithilfe der vorhandenen ICEs überprüfen, die unter [ICE-Referenz](ice-reference.md)beschrieben sind. Diese ICEs können aus CUB-Standarddateien abgerufen werden, die mit dem SDK bereitgestellt werden.

Die Installation des Datenbanktabellen-Editors Orca oder des Überprüfungstools msival2 stellt die Dateien Logo.cub, Darice.cub und Mergemod.cub bereit. Der Satz von ICEs in der Datei Logo.cub ist eine Teilmenge der ICEs in der Datei Darice.cub. Wenn Ihr Paket die Überprüfung mit Darice.cub besteht, wird es mit Logo.cub übergeben. Mergemod.cub enthält eine Reihe von ICEs, die zum Überprüfen von Mergemodulen verwendet werden. Weitere Informationen finden Sie unter [Merge Module ICE Reference (ICE-Referenz zum Mergemodul).](merge-module-ice-reference.md)

**So überprüfen Sie ein Installationspaket**

1.  Rufen Sie die entsprechenden benutzerdefinierten ICE-Aktionen ab, oder erstellen Sie sie. Möglicherweise können Sie eine oder mehrere der vorhandenen ICEs verwenden, die in der [ICE-Referenz](ice-reference.md)beschrieben sind. Wenn ihre Überprüfung einen ICE erfordert, der noch nicht in dieser Liste enthalten ist, können Sie einen neuen ICE erstellen, wie unter [Erstellen eines ICE](building-an-ice.md)beschrieben.
2.  Bereiten Sie eine ICE-Datenbank mit allen benutzerdefinierten ICE-Aktionen vor. Informationen zum Vorbereiten einer CUB-Datei finden Sie im Abschnitt Erstellen einer [ICE-Datenbank.](building-an-ice-database.md)
3.  Geben Sie die CUB-Datei und die .msi-Datei einem Paketvalidierungstool wie [Orca.exe](orca-exe.md) oder [Msival2.exe](msival2-exe.md)an.

Beachten Sie, dass Mergemodule wie unter [Überprüfen von Mergemodulen](validating-merge-modules.md)beschrieben überprüft werden sollten.

 

 



