---
description: Die FASTOEM-Eigenschaft ist so konzipiert, dass OEMs die Zeit reduzieren können, die zum Installieren Windows Installer-Anwendungen für ein bestimmtes Szenario benötigt wird.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: FASTOEM-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c882ee78645a7f3a0fd8cd2677ca7ddfabade9b4395202cbbf0ab547b12a19eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129580"
---
# <a name="fastoem-property"></a>FASTOEM-Eigenschaft

Die **FASTOEM-Eigenschaft** ist so konzipiert, dass OEMs die Zeit reduzieren können, die zum Installieren von Windows Installer-Anwendungen für ein bestimmtes Szenario benötigt wird. Erstellen Sie die **FASTOEM-Eigenschaft** nicht in der [Eigenschaftentabelle](property-table.md).

Die **FASTOEM-Eigenschaft** ist nur anwendbar, wenn alle diese Bedingungen erfüllt sind:

-   Die Anwendung wird auf demselben Volume wie der Ordner installiert, der die Quelldateien enthält.
-   Die Quelldateien werden nach der Installation gelöscht.
-   Während der Installation wird keine Benutzeroberfläche angezeigt. Die [Benutzeroberflächenebene](user-interface-levels.md) ist "none".
-   Die Installation wird im Installationskontext pro [Computer ausgeführt.](installation-context.md)
-   Auf dem Computer ist genügend Speicherplatz für eine erfolgreiche Installation vorhanden.
-   Dies ist die erste Installation. Die Installation wird nicht anknativ, neu installiert, entfernt oder eine Administratorinstallation.
-   Es werden keine Features installiert, um von der Quelle aus ausgeführt zu werden.
-   Das Installationspaket enthält keine [isolierten Komponenten.](isolated-components.md) Da isolierte Komponenten erfordern, dass Quelldateien an der Quelle gespeichert bleiben, kann die **FASTOEM-Eigenschaft** derzeit nicht mit isolierten Komponenten verwendet werden.

Wenn alle vorherigen Bedingungen erfüllt sind, ermöglicht das Festlegen der **FASTOEM-Eigenschaft,** Windows Installer die Leistung wie folgt zu verbessern:

-   Verschieben Sie Dateien auf demselben Volume, anstatt sie zu kopieren. Dies garantiert nicht, dass alle Dateien verschoben und nicht kopiert werden. Beachten Sie, dass Sie die [**ROOTDRIVE-Eigenschaft**](rootdrive.md) in der Befehlszeile auf demselben Laufwerk initialisieren müssen, das die Installationsquelle enthält, wenn der Computer über mehrere Festplatten verfügt.
-   Diese Quelle aus der Quellliste der Anwendung weglassen, sodass nachfolgende Neuinstallations- oder Wartungsinstallationen standardmäßig auf die CD-ROM-Quellen festgelegt sind, die in der [Medientabelle angegeben sind.](media-table.md)
-   Optimieren [Sie die Dateikosten.](file-costing.md)
-   Unterdrücken Sie Statusmeldungen, die vom Windows Installer an den Client gesendet werden.

## <a name="remarks"></a>Hinweise

Da beim Festlegen von **FASTOEM** keine Statusmeldungen gesendet werden, wird empfohlen, dass Autoren den Wert 1800 für Timeout manuell in den Schlüssel schreiben.

**HKLM** \\ **SoftWare** \\ **Richtlinien** \\ **Microsoft** \\ **Windows** \\ **Installer** \\ **Timeout**

Timeout ist ein **REG \_ DWORD-Typ.**

Um die Größe der Anwendung unter Programme hinzufügen oder entfernen im Windows 2000 Systemsteuerung anzuzeigen, müssen Sie den Wert von EstimatedSize manuell in den Schlüssel schreiben.

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Deinstallieren** \\ **<  Produktcode >**

Dies ist **ein \_ REG-DWORD-Typ,** der der Größe der Anwendung in KB entspricht. Das Installationsprogramm schreibt diesen Wert nicht automatisch.

Verwenden Sie die folgende Beispielbefehlszeile, wenn die cd-ROM, die an Endbenutzer geliefert wird, das Installationspaket der Anwendung im Stammverzeichnis der CD-ROM speichert. Beachten Sie, dass die Volumebezeichnung in der [Medientabelle](media-table.md) der .msi der Volumebezeichnung der CD-ROM übereinstimmen muss.

**Msiexec /I C: \\ TempImage \\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 ROOTDRIVE=C:\\**

Verwenden Sie die folgende Beispielbefehlszeile, wenn sich das Installationspaket nicht im Stammverzeichnis der CD-ROM befindet, die an Endbenutzer geliefert wird. Sie müssen die [**MEDIAPACKAGEPATH-Eigenschaft**](mediapackagepath.md) in diesem Fall auf den Pfad zum Installationspaket festlegen. Die Volumebezeichnung in der [Medientabelle](media-table.md) der .msi muss mit der Volumebezeichnung der CD-ROM übereinstimmen. Befolgen Sie in diesem Fall dieses Beispiel.

**Msiexec /I C: \\ TempImage \\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 MEDIAPACKAGEPATH=C: \\ TempImage \\package.msi ROOTDRIVE=C:\\**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




