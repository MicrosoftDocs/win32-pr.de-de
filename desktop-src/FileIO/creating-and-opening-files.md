---
description: Überlegungen zum Erstellen oder Öffnen einer Datei mithilfe der CreateFile-Funktion.
ms.assetid: 094cac29-c66d-409e-8928-878dc693d393
title: Erstellen und Öffnen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e80449942fbceb39c37604bf6d8b5410d171d195
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469927"
---
# <a name="creating-and-opening-files"></a>Erstellen und Öffnen von Dateien

Die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) kann eine neue Datei erstellen oder eine vorhandene Datei öffnen. Sie müssen den Dateinamen, Erstellungsanweisungen und andere Attribute angeben. Wenn eine Anwendung eine neue Datei erstellt, fügt das Betriebssystem sie dem angegebenen Verzeichnis hinzu.

Das Betriebssystem weist jeder Datei, die mit CreateFile geöffnet oder erstellt wird, einen eindeutigen Bezeichner zu, der als [**Handle bezeichnet wird.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Eine Anwendung kann dieses Handle mit Funktionen verwenden, die die Datei lesen, in diese schreiben und beschreiben. Sie ist gültig, bis alle Verweise auf dieses Handle geschlossen sind. Wenn eine Anwendung gestartet wird, erbt sie alle geöffneten Handles vom Prozess, der sie gestartet hat, wenn die Handles als vererbbar erstellt wurden.

Eine Anwendung sollte den Wert des von [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) zurückgegebenen Handles überprüfen, bevor versucht wird, das Handle für den Zugriff auf die Datei zu verwenden. Wenn ein Fehler auftritt, ist der Handlewert **INVALID \_ HANDLE \_ VALUE,** und die Anwendung kann die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) für erweiterte Fehlerinformationen verwenden.

Wenn eine Anwendung [**CreateFile verwendet,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)muss sie den *dwDesiredAccess-Parameter* verwenden, um anzugeben, ob sie aus der Datei lesen, in die Datei schreiben möchte, sowohl Lese- als auch Schreibzugriff oder keines von beiden. Dies wird als Anfordern eines *Zugriffsmodus bezeichnet.* Die Anwendung muss auch den *dwCreationDisposition-Parameter* verwenden, um anzugeben, welche Aktion zu ergreifen ist, wenn die Datei bereits vorhanden ist. Dies wird als *Erstellungsdisposition bezeichnet.* Beispielsweise kann eine Anwendung **CreateFile** aufrufen, bei der *dwCreationDisposition* auf **CREATE \_ ALWAYS** festgelegt ist, um immer eine neue Datei zu erstellen, auch wenn bereits eine Datei mit demselben Namen vorhanden ist (wodurch die vorhandene Datei überschreiben wird). Ob dies erfolgreich ist, hängt von Faktoren wie den Attributen und Sicherheitseinstellungen der vorherigen Datei ab (weitere Informationen finden Sie in den folgenden Abschnitten).

Eine Anwendung verwendet auch [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) um anzugeben, ob die Datei zum Lesen, Schreiben, beides oder keines von beiden gemeinsam verwendet werden soll. Dies wird als *Freigabemodus bezeichnet.* Eine nicht freigegebene geöffnete Datei *(dwShareMode* auf 0 festgelegt) kann nicht erneut geöffnet werden, weder von der Anwendung, die sie geöffnet hat, noch von einer anderen Anwendung, bis ihr Handle geschlossen wurde. Dies wird auch als exklusiver Zugriff bezeichnet.

Wenn ein Prozess [**createFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) verwendet, um zu versuchen, eine Datei zu öffnen, die bereits im Freigabemodus geöffnet wurde *(dwShareMode* ist auf einen gültigen Wert ungleich 0 festgelegt), vergleicht das System die angeforderten Zugriffs- und Freigabemodi mit denen, die beim Öffnen der Datei angegeben wurden. Wenn Sie einen Zugriffs- oder Freigabemodus angeben, der mit den im vorherigen Aufruf angegebenen Modi in Konflikt steht, schlägt **CreateFile** fehl.

Die folgende Tabelle veranschaulicht die gültigen Kombinationen von zwei Aufrufen von [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) mit verschiedenen Zugriffsmodi und Freigabemodi (*dwDesiredAccess* bzw. *dwShareMode).* Es spielt keine Rolle, in welcher Reihenfolge **die CreateFile-Aufrufe** vorgenommen werden. Alle nachfolgenden Datei-E/A-Vorgänge für jedes Dateihand handle werden jedoch weiterhin durch die aktuellen Zugriffs- und Freigabemodi eingeschränkt, die diesem bestimmten Dateihand handle zugeordnet sind.




| Erster Aufruf von <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a> | Gültige zweite Aufrufe von <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a> | 
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 




 

Zusätzlich zu den Standarddateiattributen können Sie auch Sicherheitsattribute angeben, indem Sie einen Zeiger auf eine [**SECURITY \_ ATTRIBUTES-Struktur**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) als vierten Parameter von [**CreateFile angeben.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Das zugrunde liegende Dateisystem muss jedoch die Sicherheit unterstützen, damit dies auswirkungen hat (z. B. unterstützt das NTFS-Dateisystem dies, die verschiedenen FAT-Dateisysteme jedoch nicht). Weitere Informationen zu Sicherheitsattributen finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).

Eine Anwendung, die eine neue Datei erstellt, kann ein optionales Handle für eine Vorlagendatei angeben, aus der [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Dateiattribute und erweiterte Attribute für die Erstellung der neuen Datei verwendet.

## <a name="createfile-scenarios"></a>CreateFile-Szenarien

Es gibt mehrere grundlegende Szenarien für das Initiieren des Zugriffs auf eine Datei mithilfe der [**CreateFile-Funktion.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Diese werden wie folgt zusammengefasst:

-   Erstellen einer neuen Datei, wenn eine Datei mit diesem Namen noch nicht vorhanden ist.
-   Erstellen einer neuen Datei, auch wenn bereits eine Datei mit demselben Namen vorhanden ist, löschen Sie ihre Daten, und beginnen Sie leer.
-   Öffnen einer vorhandenen Datei nur, wenn sie vorhanden und nur intakt ist.
-   Öffnen Sie eine vorhandene Datei nur, wenn sie vorhanden ist, und schneiden Sie sie so ab, dass sie leer ist.
-   Öffnen einer Datei immer: wie vorhanden, wenn sie vorhanden ist, erstellen Sie eine neue Datei, wenn sie nicht vorhanden ist.

Diese Szenarien werden durch die ordnungsgemäße Verwendung des *dwCreationDisposition-Parameters* gesteuert. Im Folgenden finden Sie eine Aufschlüsselung der Zuordnung dieser Szenarien zu Werten für diesen Parameter und deren Verwendung.

Beim Erstellen oder Öffnen einer neuen Datei, wenn noch keine Datei mit diesem Namen vorhanden ist *(dwCreationDisposition* auf **CREATE \_ NEW,** CREATE ALWAYS oder **OPEN \_** **\_ ALWAYS** festgelegt), führt die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) die folgenden Aktionen aus:

-   Kombiniert die von *dwFlagsAndAttributes* angegebenen Dateiattribute und Flags mit **FILE ATTRIBUTE \_ \_ ARCHIVE.**
-   Legt die Dateilänge auf 0 (null) fest.
-   Kopiert die erweiterten Attribute, die von der Vorlagendatei bereitgestellt werden, in die neue Datei, wenn der *Parameter hTemplateFile* angegeben ist (dadurch werden alle zuvor angegebenen **FILE \_ \_ \* ATTRIBUTE-Flags** überschrieben).
-   Legt das vom **bInheritHandle-Member** angegebene Erbenflag und den Sicherheitsdeskriptor fest, der vom **lpSecurityDescriptor-Member** des *lpSecurityAttributes-Parameters* ([**SECURITY \_ ATTRIBUTES-Struktur)**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) angegeben wird, sofern angegeben.

Wenn Sie eine neue Datei erstellen, auch wenn bereits eine Datei mit demselben Namen vorhanden ist *(dwCreationDisposition* auf **CREATE \_ ALWAYS** festgelegt), führt die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) die folgenden Aktionen aus:

-   Überprüft die aktuellen Dateiattribute und Sicherheitseinstellungen auf Schreibzugriff und führt zu einem Fehler, wenn der Zugriff verweigert wird.
-   Kombiniert die von *dwFlagsAndAttributes* angegebenen Dateiattribute und Flags mit **FILE ATTRIBUTE \_ \_ ARCHIVE** und den vorhandenen Dateiattributen.
-   Legt die Dateilänge auf 0 (null) fest (d. h., alle Daten in der Datei sind nicht mehr verfügbar, und die Datei ist leer).
-   Kopiert die erweiterten Attribute, die von der Vorlagendatei bereitgestellt werden, in die neue Datei, wenn der *Parameter hTemplateFile* angegeben ist (dadurch werden alle zuvor angegebenen **FILE \_ \_ \* ATTRIBUTE-Flags** überschrieben).
-   Legt das erben-Flag fest, das vom **bInheritHandle-Member** des *lpSecurityAttributes-Parameters* [**(SECURITY \_ ATTRIBUTES-Struktur)**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) angegeben wird, sofern angegeben, ignoriert jedoch den **lpSecurityDescriptor-Member** der **SECURITY \_ ATTRIBUTES-Struktur.**
-   Wenn dies andernfalls erfolgreich ist [**(d.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) h., CreateFile gibt ein gültiges Handle zurück), gibt der Aufruf von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) den Code **ERROR ALREADY \_ \_ EXISTS** zurück, obwohl es sich für diesen speziellen Verwendungsfall eigentlich nicht um einen Fehler als solchen handelt (wenn Sie eine "neue" (leere) Datei statt der vorhandenen erstellen möchten).

Beim Öffnen einer vorhandenen Datei *(dwCreationDisposition* entweder auf **OPEN \_ EXISTING,** **OPEN \_ ALWAYS** oder **TRUNCATE \_ EXISTING** festgelegt), führt die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) die folgenden Aktionen aus:

-   Überprüft die aktuellen Dateiattribute und Sicherheitseinstellungen auf den angeforderten Zugriff und führt zu einem Fehler, wenn der Zugriff verweigert wird.
-   Kombiniert die von _dwFlagsAndAttributes* angegebenen Dateiflags (**FILE \_ FLAG \_ \** _) mit vorhandenen Dateiattributen \_ \_ \** und ignoriert alle Dateiattribute (**FILE ATTRIBUTE _), die von _dwFlagsAndAttributes* angegeben werden.
-   Legt die Dateilänge nur dann auf 0 (null) fest, wenn *dwCreationDisposition* auf **TRUNCATE \_ EXISTING** festgelegt ist. Andernfalls wird die aktuelle Dateilänge beibehalten, und die Datei wird im vorliegenden Zustand geöffnet.
-   Ignoriert den *hTemplateFile-Parameter.*
-   Legt das erben-Flag fest, das vom **bInheritHandle-Member** des *lpSecurityAttributes-Parameters* [**(SECURITY \_ ATTRIBUTES-Struktur)**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) angegeben wird, sofern angegeben, ignoriert jedoch den **lpSecurityDescriptor-Member** der **SECURITY \_ ATTRIBUTES-Struktur.**

## <a name="file-attributes-and-directories"></a>Dateiattribute und Verzeichnisse

Dateiattribute sind Teil der Metadaten, die einer Datei oder einem Verzeichnis zugeordnet sind, die jeweils einen eigenen Zweck haben und regeln, wie sie festgelegt und geändert werden können. Einige dieser Attribute gelten nur für Dateien und andere nur für Verzeichnisse. Das FILE **\_ ATTRIBUTE \_ DIRECTORY-Attribut** gilt beispielsweise nur für Verzeichnisse: Es wird vom Dateisystem verwendet, um zu bestimmen, ob ein Objekt auf dem Datenträger ein Verzeichnis ist, es kann jedoch nicht für ein vorhandenes Dateisystemobjekt geändert werden.

Einige Dateiattribute können für ein Verzeichnis festgelegt werden, haben jedoch nur für Dateien, die in diesem Verzeichnis erstellt wurden und als Standardattribute verwendet werden. Beispielsweise kann **FILE \_ ATTRIBUTE \_ COMPRESSED** für ein Verzeichnisobjekt festgelegt werden, aber da das Verzeichnisobjekt selbst keine tatsächlichen Daten enthält, wird es nicht wirklich komprimiert. Verzeichnisse, die mit diesem Attribut gekennzeichnet sind, teilen dem Dateisystem jedoch mit, alle neuen Dateien zu komprimieren, die diesem Verzeichnis hinzugefügt wurden. Jedes Dateiattribut, das für ein Verzeichnis festgelegt werden kann und auch für neue Dateien festgelegt wird, die diesem Verzeichnis hinzugefügt werden, wird als *geerbtes Attribut bezeichnet.*

Die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) bietet einen Parameter zum Festlegen bestimmter Dateiattribute, wenn eine Datei erstellt wird. Im Allgemeinen werden diese Attribute am häufigsten von einer Anwendung zum Zeitpunkt der Dateierstellung verwendet, aber nicht alle möglichen Dateiattribute sind für **CreateFile verfügbar.** Einige Dateiattribute erfordern die Verwendung anderer Funktionen, z. B. [**SetFileAttributes,**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)oder [**DecryptFile,**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) nachdem die Datei bereits vorhanden ist. Im Fall von **FILE \_ ATTRIBUTE \_ DIRECTORY** ist die [**CreateDirectory-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) zum Zeitpunkt der Erstellung erforderlich, da **CreateFile** keine Verzeichnisse erstellen kann. Die anderen Dateiattribute, die eine besondere Behandlung erfordern, sind **FILE \_ ATTRIBUTE \_ REPARSE \_ POINT** und **FILE ATTRIBUTE \_ \_ SPARSE \_ FILE,** für die **DeviceIoControl erforderlich ist.** Weitere Informationen finden Sie unter [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa).

Wie bereits erwähnt, tritt die Vererbung von Dateiattributen auf, wenn eine Datei mit Dateiattributen erstellt wird, die aus den Verzeichnisattributen gelesen werden, in denen sich die Datei befindet. In der folgenden Tabelle werden diese geerbten Attribute und ihre Beziehung zu [**CreateFile-Funktionen**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) zusammengefasst.



| Verzeichnisattributstatus                                      | [](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) CreateFile-Vererbungsüberschreibungsfunktion für neue Dateien      |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **FILE \_ ATTRIBUTE \_ COMPRESSED set.**<br/>                | Kein Steuerelement. Verwenden [**Sie DeviceIoControl zum**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) Löschen.<br/>    |
| **FILE \_ ATTRIBUTE \_ COMPRESSED** nicht festgelegt.<br/>            | Kein Steuerelement. Verwenden [**Sie DeviceIoControl zum**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) Festlegen.<br/>      |
| **FILE \_ ATTRIBUTE \_ ENCRYPTED festgelegt.**<br/>                 | Kein Steuerelement. Verwenden Sie [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea).<br/>                      |
| **FILE \_ ATTRIBUTE \_ ENCRYPTED** ist nicht festgelegt.<br/>             | Kann mit [**CreateFile festgelegt werden.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)<br/>                       |
| **FILE \_ ATTRIBUTE \_ NOT \_ CONTENT \_ INDEXED** set.<br/>     | Kein Steuerelement. Verwenden [**Sie SetFileAttributes zum**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) Löschen.<br/> |
| **FILE \_ ATTRIBUTE \_ NOT \_ CONTENT \_ INDEXED** nicht festgelegt.<br/> | Kein Steuerelement. Legen [**Sie setFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) fest.<br/>   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugriffssteuerung](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**Dateiattributkonst constants**](file-attribute-constants.md)
</dt> <dt>

[Dateikomprimierung und Dekomprimierung](file-compression-and-decompression.md)
</dt> <dt>

[Dateiverschlüsselung](file-encryption.md)
</dt> <dt>

[Dateiverwaltungsfunktionen](file-management-functions.md)
</dt> <dt>

[Handles und Objekte](/windows/desktop/SysInfo/handles-and-objects)
</dt> <dt>

[Behandeln der Vererbung](/windows/desktop/SysInfo/handle-inheritance)
</dt> <dt>

[Öffnen einer Datei zum Lesen oder Schreiben](opening-a-file-for-reading-or-writing.md)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> </dl>

 

