---
title: Sichern und Wiederherstellen von Lizenzen
description: Sichern und Wiederherstellen von Lizenzen
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- Windows Medienformat-SDK, Sichern von Lizenzen
- Windows Medienformat-SDK, Wiederherstellen von Lizenzen
- Windows Medienformat-SDK, Lizenzsicherung und -wiederherstellung
- Advanced Systems Format (ASF), Sichern von Lizenzen
- ASF (Advanced Systems Format), Sichern von Lizenzen
- Advanced Systems Format (ASF), Wiederherstellen von Lizenzen
- ASF (Advanced Systems Format), Wiederherstellen von Lizenzen
- Advanced Systems Format (ASF), Lizenzsicherung und -wiederherstellung
- ASF (Advanced Systems Format), Lizenzsicherung und -wiederherstellung
- Digital Rights Management (DRM), Sichern von Lizenzen
- DRM (Digital Rights Management), Sichern von Lizenzen
- Verwaltung digitaler Rechte (Digital Rights Management, DRM), Wiederherstellen von Lizenzen
- DRM (Digital Rights Management), Wiederherstellen von Lizenzen
- Digital Rights Management (DRM), Lizenzsicherung und -wiederherstellung
- DRM (Digital Rights Management), Lizenzsicherung und -wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378a41d975e8f19d38c637d585759d0038f5b86550769ae49d6a6490844f223e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028138"
---
# <a name="backing-up-and-restoring-licenses"></a>Sichern und Wiederherstellen von Lizenzen

Die Sicherungs- und Wiederherstellungsprozesse sind asynchron. Sie werden ausgelöst, wenn der Benutzer einen Menübefehl oder eine Option in der Anwendung zum Sichern oder Wiederherstellen von Lizenzen auswählt. Sie sollten dem Benutzer erlauben, die Speicherorte anzugeben, an denen Lizenzen sicherungs- und wiederhergestellt werden müssen.

So sichern Sie Lizenzen:

1.  Verwenden Sie [**die WMCreateBackupRestorer-Funktion,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) um das Sicherungswiederherstellungsobjekt zu erstellen.
2.  Rufen Sie [**die IWMBackupRestoreProps::SetProp-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) auf, um den Sicherungspfad (den Speicherort, an dem Sie die Dateien schreiben, z. B. A: oder \\ D: \\ Lizenzen) zu festlegen.
3.  Rufen Sie [**die IWMLicenseBackup::BackupLicenses-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) auf, um die Lizenzen im angegebenen Pfad zu sichern.

Die folgenden Ereignisse werden an die [**IWMStatusCallback::OnStatus-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) gesendet:

-   **WMT \_ BACKUPRESTORE \_ BEGIN gibt** an, dass der Sicherungsprozess gestartet wurde.
-   **WMT \_ BACKUPRESTORE \_ END gibt** an, dass der Sicherungsvorgang abgeschlossen wurde.
-   **WMT \_ RESTRICTED \_ LICENSE** gibt an, dass eine oder mehrere Lizenzen nicht sichern werden können, da das Recht vom Inhaltsbesitzer nicht zugelassen wurde.

Die Schlüssel-ID ist ebenfalls in dieser Meldung enthalten. Wenn Sie eine Datenbank für geschützte Dateien implementiert haben, die die Schlüssel-ID und metadaten enthält, können Sie dem Benutzer eine Meldung mit dem spezifischen Titel (z. B. einem Titel) anzeigen, für den die Lizenz nicht gesichert werden kann. Andernfalls muss die Meldung generisch sein und den Benutzer darüber informieren, dass einige Lizenzen nicht sichern werden können.

Wiederherstellen von Lizenzen:

1.  Verwenden Sie **die WMCreateBackupRestorer-Funktion,** um das Sicherungswiederherstellungsobjekt zu erstellen.
2.  Rufen Sie **die IWMBackupRestoreProps::SetProp-Methode** auf, um den Wiederherstellungspfad auf den Speicherort zu setzen, an dem Lizenzen sichern werden.
3.  Rufen Sie [**die IWMLicenseRestore::RestoreLicenses-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) auf, um Lizenzen von diesem Speicherort wiederherzustellen.

Die folgenden Ereignisse werden an die [**IWMStatusCallback::OnStatus-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) gesendet:

-   **WMT \_ BACKUPRESTORE \_ CONNECTING gibt** an, dass die Anwendung eine Verbindung mit dem Lizenzverwaltungsdienst herstellen soll.
-   **WMT \_ BACKUPRESTORE \_ DISCONNECTING gibt** an, dass die Anwendung die Verbindung mit dem Lizenzverwaltungsdienst trennt.
-   **WMT \_ BACKUPRESTORE \_ BEGIN gibt** an, dass der Wiederherstellungsprozess gestartet wurde.
-   **WMT \_ BACKUPRESTORE \_ END gibt** an, dass der Wiederherstellungsvorgang abgeschlossen wurde.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Digital Rights Management Features**](digital-rights-management-features.md)
</dt> <dt>

[**IWMBackupRestoreProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[**IWMLicenseBackup-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[**IWMLicenseRestore-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




