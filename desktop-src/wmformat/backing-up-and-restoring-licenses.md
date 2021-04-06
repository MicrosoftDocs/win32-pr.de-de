---
title: Sichern und Wiederherstellen von Lizenzen
description: Sichern und Wiederherstellen von Lizenzen
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- Windows Media-Format-SDK, Sichern von Lizenzen
- Windows Media-Format-SDK, Wiederherstellen von Lizenzen
- Windows Media-Format-SDK, Lizenz Sicherung und-Wiederherstellung
- Advanced Systems Format (ASF), Sichern von Lizenzen
- ASF (Advanced Systems Format), Sichern von Lizenzen
- Advanced Systems Format (ASF), Wiederherstellen von Lizenzen
- ASF (Advanced Systems Format), Wiederherstellen von Lizenzen
- Advanced Systems Format (ASF), Lizenz Sicherung und-Wiederherstellung
- ASF (Advanced Systems Format), Lizenz Sicherung und-Wiederherstellung
- Digital Rights Management (DRM), Sichern von Lizenzen
- DRM (Digital Rights Management), Sichern von Lizenzen
- Digital Rights Management (DRM), Wiederherstellen von Lizenzen
- DRM (Digital Rights Management), Wiederherstellen von Lizenzen
- Digital Rights Management (DRM), Lizenz Sicherung und-Wiederherstellung
- DRM (Digital Rights Management), Lizenz Sicherung und-Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10d8e76c191225288a1021e08e4c77e7e14f3c6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723528"
---
# <a name="backing-up-and-restoring-licenses"></a>Sichern und Wiederherstellen von Lizenzen

Die Sicherungs-und Wiederherstellungs Prozesse sind asynchron. Sie werden ausgelöst, wenn der Benutzer einen Menübefehl oder eine Option in der Anwendung auswählt, um Lizenzen zu sichern oder wiederherzustellen. Sie sollten zulassen, dass der Benutzer die Orte angeben kann, an denen Lizenzen gesichert und wieder hergestellt werden müssen.

So sichern Sie Lizenzen:

1.  Verwenden Sie die [**wmkreatebackuprestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) -Funktion, um das Backup Restorer-Objekt zu erstellen.
2.  Rufen Sie die [**iwmbackuprestoreprop:: setprop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) -Methode auf, um den Sicherungs Pfad (den Speicherort, an den Sie die Dateien schreiben, z \\ . b. A: oder D: \\ Licenses) festzulegen.
3.  Nennen Sie die [**iwmlicenlbackup:: backuplicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) -Methode, um die Lizenzen im angegebenen Pfad zu sichern.

Die folgenden Ereignisse werden an die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode gesendet:

-   **WMT \_ Backuprestore \_ Begin** gibt an, dass der Sicherungs Vorgang gestartet wurde.
-   **WMT \_ Backuprestore- \_ Ende** gibt an, dass der Sicherungs Vorgang abgeschlossen wurde.
-   **WMT \_ Eingeschränkte \_** Lizenzen gibt an, dass eine oder mehrere Lizenzen nicht gesichert werden können, da das Recht vom Besitzer des Inhalts nicht zugelassen wurde.

Die Schlüssel-ID ist auch in dieser Nachricht enthalten. Wenn Sie eine Datenbank für geschützte Dateien implementiert haben, die die Schlüssel-ID und die Metadaten enthält, können Sie dem Benutzer eine Meldung mit dem jeweiligen Titel (z. b. einem Buchtitel) anzeigen, für die die Lizenz nicht gesichert werden kann. Andernfalls muss die Nachricht generisch sein und den Benutzer darüber informieren, dass einige Lizenzen nicht gesichert werden können.

So stellen Sie Lizenzen wieder her:

1.  Verwenden Sie die **wmkreatebackuprestorer** -Funktion, um das Backup Restorer-Objekt zu erstellen.
2.  Rufen Sie die **iwmbackuprestoreprop:: setprop** -Methode auf, um den Wiederherstellungs Pfad auf den Speicherort festzulegen, an dem Lizenzen gesichert werden.
3.  Rufen Sie die [**iwmlicenserestore:: restorelicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) -Methode auf, um Lizenzen von diesem Speicherort wiederherzustellen.

Die folgenden Ereignisse werden an die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode gesendet:

-   **WMT \_ Backuprestore- \_ Verbindung** gibt an, dass die Anwendung eine Verbindung mit dem Lizenz Verwaltungsdienst herstellt.
-   **WMT \_ Durch die \_ Trennung von backuprestore** wird angegeben, dass die Verbindung mit dem Lizenz Verwaltungsdienst getrennt wird.
-   **WMT \_ Backuprestore \_ Begin** gibt an, dass der Wiederherstellungs Vorgang gestartet wurde.
-   **WMT \_ Backuprestore- \_ Ende** gibt an, dass der Wiederherstellungs Vorgang abgeschlossen wurde.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features digitaler Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**Iwmbackuprestoredie-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[**Iwmlicenabbackup-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[**Iwmlicenserestore-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




