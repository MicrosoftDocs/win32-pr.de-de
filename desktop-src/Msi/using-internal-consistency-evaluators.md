---
description: Verwenden Sie zum Überprüfen einer Datenbank ein spezielles Validierungs Tool, um eine CUB-Datei mit den internen Konsistenz Auswertung (ICES) in der Datenbank zusammenzuführen, die ICES auszuführen und die Ergebnisse zu melden.
ms.assetid: bdf38673-ee3d-47d8-ad6e-562cd5626918
title: Verwenden interner Konsistenz Auswertungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e6dab453ae495dc6029b54eb039c8acc60f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345115"
---
# <a name="using-internal-consistency-evaluators"></a>Verwenden interner Konsistenz Auswertungen

Verwenden Sie zum Überprüfen einer Datenbank ein spezielles Validierungs Tool, um eine CUB-Datei mit den [internen Konsistenz Auswertung](internal-consistency-evaluators-ices.md) (ICES) in der Datenbank zusammenzuführen, die ICES auszuführen und die Ergebnisse zu melden. Im Microsoft Windows Software Development Kit (SDK) werden mehrere derartige Tools bereitgestellt. Erstellungs Umgebungen von Drittanbietern können auch das Ice-Validierungssystem in Ihre Erstellungs Umgebung integrieren. Es ist auch möglich, ein eigenes Tool zu schreiben, um die Ice-Validierung auszuführen. Die meisten Ice Validation Tools führen die CUB-Datei und Ihre Datenbank in einer dritten temporären Datenbank zusammen. In Windows Installer werden Warnungen, Fehler, Debuginformationen und API-Fehler angezeigt, während die einzelnen Ice in der CUB-Datei ausgeführt werden. Wenn das Installationsprogramm die Ausführung des ICES abgeschlossen hat, werden die MSI-Datei, die CUB-Datei und die temporäre Datenbank geschlossen, ohne dass Änderungen gespeichert werden. Die MSI-Datei und die CUB-Datei bleiben durch den Validierungstest unverändert.

Benutzerdefinierte Ice-Aktionen kommunizieren mit dem Benutzer, indem Sie [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) aufrufen und eine installmessage- \_ Benutzer Nachricht veröffentlichen. Eine Ice-Nachricht gibt im allgemeinen Informationen wie die folgenden zurück:

-   Der Name des ICE, bei dem ein Fehler gefunden wurde.
-   Datum, an dem das Eis erstellt wurde
-   Autor des ICE
-   Das Datum, an dem das Eis zuletzt geändert wurde.
-   Beschreibung des API-Fehlers, bei dem das Eis fehlschlägt
-   Beschreibung des Fehlers
-   Eine Warnung für den Benutzer.
-   Der Name der Datenbanktabelle, die den Fehler oder die Warnung enthält.
-   Der Name der Tabellenspalte, die den Fehler oder die Warnung enthält.
-   Primärschlüssel der Tabelle, in der der Fehler oder die Warnung enthalten ist
-   Eine URL zu einer HTML-Datei mit debuggingvorschlägen
-   Eine Zeichenfolge, die weitere Informationen enthalten kann.

Autoren von Installationspaketen können benutzerdefinierte Ice-Aktionen schreiben oder den Standardsatz von ICES verwenden, der in den Cub-Dateien enthalten ist, die mit dem SDK bereitgestellt werden. Weitere Informationen zum Schreiben eines ICE finden Sie unter Building a [Ice](building-an-ice.md).

Nachdem Sie die entsprechenden ICES zur Validierung geschrieben haben, muss ein Entwickler die benutzerdefinierten Aktionen zusammen in einer MSI-Datenbank (eine CUB-Datei) sammeln, die nur die ICES und die erforderlichen Tabellen enthält. Eine CUB-Datei kann nicht installiert werden und wird nur zum Speichern und Bereitstellen des Zugriffs auf benutzerdefinierte Ice-Aktionen verwendet. Weitere Informationen zum Erstellen von Cub-Dateien finden Sie unter [Building a Ice Database](building-an-ice-database.md). Alternativ können Entwickler das Installationspaket überprüfen, indem Sie die in [Ice Reference](ice-reference.md)beschriebenen vorhandenen ICES verwenden. Diese ICES können aus den standardmäßigen Cub-Dateien abgerufen werden, die mit dem SDK bereitgestellt werden.

Die Installation des Datenbanktabellen-Editors "Orca" oder "Validation Tool msival2" enthält die Dateien "Logo. Cub", "Darice. Cub" und "Mergemod. Cub". Der Satz von ICES in der Datei "Logo. Cub" ist eine Teilmenge der in der Datei "Darice. Cub". Wenn Ihr Paket die Überprüfung mithilfe von Darice. Cub übergibt, wird es mit "Logo. Cub" übergeben. Mergemod. Cub enthält einen Satz von ICES, die zum Überprüfen von Mergemodulen verwendet werden. Weitere Informationen finden Sie unter [Merge Module Ice Reference](merge-module-ice-reference.md).

**So überprüfen Sie ein Installationspaket**

1.  Abrufen oder Verfassen der entsprechenden benutzerdefinierten Ice-Aktionen. Möglicherweise können Sie einen oder mehrere der vorhandenen ICES verwenden, die in der [Ice-Referenz](ice-reference.md)beschrieben sind. Wenn Ihre Überprüfung noch nicht in dieser Liste enthalten ist, können Sie ein neues Eis erstellen, wie unter [Erstellen eines ICE](building-an-ice.md)beschrieben.
2.  Bereiten Sie eine Ice-Datenbank vor, die alle benutzerdefinierten Eis Aktionen enthält. Weitere Informationen zum Vorbereiten einer CUB-Datei finden Sie im Abschnitt [Erstellen einer Ice-Datenbank](building-an-ice-database.md) .
3.  Stellen Sie die CUB-Datei und die MSI-Datei für ein Paket Überprüfungs Tool wie [Orca.exe](orca-exe.md) oder [Msival2.exe](msival2-exe.md)bereit.

Beachten Sie, dass Mergemodule wie unter [Validieren von Mergemodulen](validating-merge-modules.md)beschrieben überprüft werden sollten.

 

 



