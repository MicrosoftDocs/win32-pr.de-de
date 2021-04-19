---
description: Die FASTOEM-Eigenschaft ist so konzipiert, dass OEMs den Zeitaufwand für die Installation Windows Installer Anwendungen für ein bestimmtes Szenario verkürzen können.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: FASTOEM-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362133"
---
# <a name="fastoem-property"></a>FASTOEM-Eigenschaft

Die **FASTOEM** -Eigenschaft ist so konzipiert, dass OEMs den Zeitaufwand für die Installation Windows Installer Anwendungen für ein bestimmtes Szenario verkürzen können. Erstellen Sie die **FASTOEM** -Eigenschaft nicht in der [Eigenschaften Tabelle](property-table.md).

Die **FASTOEM** -Eigenschaft ist nur anwendbar, wenn alle folgenden Bedingungen zutreffen:

-   Die Anwendung wird auf demselben Volume wie der Ordner installiert, der die Quelldateien enthält.
-   Die Quelldateien werden nach der Installation gelöscht.
-   Während der Installation wird keine Benutzeroberfläche angezeigt. Die [Benutzeroberflächen Ebene](user-interface-levels.md) ist "None".
-   Die Installation wird im [Installations Kontext](installation-context.md)pro Computer durchgeführt.
-   Auf dem Computer ist ausreichend Speicherplatz für eine erfolgreiche Installation vorhanden.
-   Dies ist die erstmalige Installation. Die Installation ist nicht Werbung, Neuinstallation, Entfernung oder Durchführung einer administrativen Installation.
-   Es sind keine Features zum Ausführen von der Quelle installiert.
-   Das Installationspaket enthält keine [isolierten Komponenten](isolated-components.md). Da für isolierte Komponenten das verbleiben der Quelldateien an der Quelle erforderlich ist, kann die **FASTOEM** -Eigenschaft derzeit nicht mit isolierten Komponenten verwendet werden.

Wenn alle vorherigen Bedingungen zutreffen, ermöglicht das Festlegen der **FASTOEM** -Eigenschaft Windows Installer, die Leistung zu verbessern, indem die folgenden Schritte ausgeführt werden:

-   Verschieben Sie Dateien auf demselben Volume, anstatt Sie zu kopieren. Dies garantiert nicht, dass alle Dateien verschoben und nicht kopiert werden. Beachten Sie Folgendes: Wenn der Computer über mehrere Festplatten verfügt, müssen Sie die Eigenschaft [**ROOTDRIVE**](rootdrive.md) in der Befehlszeile mit dem Laufwerk initialisieren, das die Installationsquelle enthält.
-   Lassen Sie diese Quelle aus der Quell Liste der Anwendung Weg, damit nachfolgende Neuinstallations-oder Wartungs Installationen standardmäßig die in der [Medien Tabelle](media-table.md)angegebenen CD-ROM-Quellen enthalten.
-   Optimieren Sie die [Datei Kosten](file-costing.md).
-   Unterdrücken von Windows Installer an den Client gesendete Fortschrittsmeldungen.

## <a name="remarks"></a>Bemerkungen

Da bei der Festlegung von **FASTOEM** keine Statusmeldungen gesendet werden, wird empfohlen, dass Autoren den Wert 1800 manuell für das Timeout in den Schlüssel schreiben.

**HKLM** \\ **Software** \\ **Richtlinien** \\ **Microsoft** \\ **Windows** \\ **Installer** \\ **Timeout**

Timeout ist ein **reg \_ DWORD** -Typ.

Um die Größe der Anwendung in der Windows 2000-Systemsteuerung unter Software anzuzeigen, müssen Sie den Wert von EstimatedSize manuell in den Schlüssel schreiben.

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Deinstallieren** \\ **< *Produkt* Code >**

Dies ist ein **reg \_ DWORD** -Typ, der der Größe der Anwendung in kBytes entspricht. Dieser Wert wird vom Installationsprogramm nicht automatisch geschrieben.

Verwenden Sie die folgende Beispiel Befehlszeile, wenn die CD-ROM, die an Endbenutzer ausgeliefert wird, das Installationspaket der Anwendung im Stammverzeichnis der CD-ROM speichert. Beachten Sie, dass die Volumebezeichnung in der [Medien Tabelle](media-table.md) der MSI-Datei der Volumebezeichnung der CD-ROM entsprechen muss.

**Msiexec/I C: \\ tempimage \\package.msi/Qn/Le logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 ROOTDRIVE = C:\\**

Verwenden Sie die folgende Beispiel Befehlszeile, wenn sich das Installationspaket nicht im Stammverzeichnis der CD-ROM befindet, die an Endbenutzer gesendet wurde. Sie müssen die [**mediapackagepath**](mediapackagepath.md) -Eigenschaft in diesem Fall auf den Pfad zum Installationspaket festlegen. Die Volumebezeichnung in der [Medien Tabelle](media-table.md) der MSI-Datei muss mit der Volumebezeichnung der CD-ROM identisch sein. Beachten Sie in diesem Fall dieses Beispiel.

**Msiexec/I C: \\ tempimage \\package.msi/Qn/Le logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 mediapackagepath = C: \\ tempimage \\package.msi ROOTDRIVE = c:\\**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




