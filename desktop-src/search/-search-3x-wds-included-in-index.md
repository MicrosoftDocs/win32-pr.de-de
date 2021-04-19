---
description: In diesem Thema werden die Elemente beschrieben, die von Windows Search indiziert werden.
ms.assetid: vs|search|~\search\wds3x\overviews\misc_items_in_index.htm
title: Was ist im Index enthalten?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5560a14e3537c8e3ac8c7544aa7ffc9a0bc1bc64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346499"
---
# <a name="what-is-included-in-the-index"></a>Was ist im Index enthalten?

In diesem Thema werden die Elemente beschrieben, die von Windows Search indiziert werden.

Dieses Thema ist wie folgt organisiert:

-   [Standardmäßig indiziert](#indexed-by-default)
-   [Unterstützte Dateiformate](#file-formats-supported)
-   [Datei Ausschlüsse](#file-exclusions)
-   [Ordner Ausschlüsse](#folder-exclusions)
-   [Laufwerks Ausschlüsse](#drive-exclusions)
-   [Zugehörige Themen](#related-topics)

 

## <a name="indexed-by-default"></a>Standardmäßig indiziert

Protokollhandler und Filter sind in Windows Search enthalten, um die folgenden Inhaltstypen zu indizieren:

-   In Windows Vista und höher werden die Microsoft Outlook-und Microsoft Outlook Express-e-Mail-Elemente eines Benutzers indiziert, während die e-Mail-Anwendung ausgeführt wird.
-   Offline Dateien im Client seitigen Cache (Client-Side Cache, CSC) werden von Windows Search lokal indiziert.
-   Windows Search unterstützt das Sammeln von Datei Start Adressen auf NTFS-und FAT32-Volumes. NTFS unterstützt die Benachrichtigungs basierte Indizierung, und FAT32 unterstützt eine inkrementelle durch Forstung beim Start und antwortet dann auf Benachrichtigungen.
-   Windows Vista und höher macht weiterhin eine pro-Ordner/pro-Datei-Eigenschaft verfügbar, um die Indizierung zu ermöglichen: die Option "**für schnelles Suchen, die den Indizierungs Dienst zum Indizieren dieses Ordners ermöglicht**" im **Eigenschaften** Dialogfeld. Wenn Sie das Fanci-Bitflag festlegen, wird sichergestellt, dass grundlegende Eigenschaften aus dem Protokoll, z. b. URL, Dateiname und Größe, indiziert werden, aber weder Filter Handler noch Eigenschaften Handler ausgeführt werden.
-   Der Text Inhalt ist indiziert, die Satzzeichen sind jedoch nicht.

## <a name="file-formats-supported"></a>Unterstützte Dateiformate

Windows Search verfügt über Protokollhandler, Eigenschaften Handler und Filter Handler, um die folgenden Formate automatisch zu indizieren:

-   Mediendateien: alle Medien Dateitypen
-   **HTML** (nlhtml.dll):. ascx,. ASP,. aspx,. CSS,. hhc,. htm,. html,. htt,. htw,. HTX,. ODC,. stm
-   **MIME-HTML** (mimefilt.dll):. MHT,. MHTML
-   **Office** (offfilt.dll):. doc,. dot,. Pot,. PPS,. ppt,. xlb,. XLC,. xls,. xlt
-   **Text** (query.dll): ASM,. ASX,. bat,. c,. cmd,. cpp,. cxx,. def,. dic,. h,. HPP,. hxx,. idl,. idq,. inf,. ini,. INX,. js,. log,. m3u,. RC,. reg,. RTF,. txt,. URL,. vb,. WTX
-   **XML** (xmlfilt.dll):. XML,. Xsl
-   **OneNote**:. One
-   **Tablet Journal** (jntfiltr.dll):. jnt

Eigenschaften werden für alle Dateien mit Ausnahme von strukturiertem Speicher indiziert. Unter Windows Vista und höher werden viele Mediendatei Eigenschaften indiziert. der Inhalt wird jedoch nicht indiziert, wenn die Dateien durch Digital Rights Management (DRM) geschützt sind.

> [!Note]  
> Der HTML-Filter indiziert keine HTML-Kommentare.

 

## <a name="file-exclusions"></a>Datei Ausschlüsse

Wenn ein Dateityp nicht über einen zugeordneten Filter verfügt oder wenn eine Datei nicht über eine Erweiterung verfügt, werden die Systemeigenschaften für Dateien dieses Typs indiziert, aber der Inhalt der Datei ist nicht indiziert.

Außerdem indiziert Windows Search den Inhalt von Dateien unter Information Rights Management (unm) oder Digital Rights Management (DRM) nicht.

Unter Windows Vista (nur) werden die folgenden Dateien standardmäßig von der Indizierung ausgeschlossen:

-   Dateien, die als ausgeblendet oder als System markiert sind.
-   Dateien mit den folgenden Erweiterungen:

    .386,. APS,. AudioCD,. bin,. BK1,. BK2,. bkf,. BSC,. BTR,. chk,. CI,. crwl,. dbg,. DCT,. Desklink, ". dir", ". DL" \_ , ". dll", ". drv", ". DVD", ". evt", ". Ex", ". exe", " \_ . Exp", ". EYB", ". Ordner,. FON,. ghi,. gthr,. hqx,. ICM,. IDB,. idx,. ILK,. IMC,. in \_ ,. ini,. inv,. JBF,. Latex,. lib,. local,. M14,. Mac,. Manifest,. map,. MAPIMail,. mmf,. Movie,. MV,. MyDocs,. NCB,. obj,. OC \_ ,. ocx,. pch,. pdb,. PF,. PMA,. PMC,. PML,. "PMR", ". res", ". RMP", ". RPC", ". rsp", ". SBR", ". SC2", ". sit", ". SR", ".", ". sym", ". sys", ". \_ \_ TLB", ". trc", ".". ZF Send-Ziel.

## <a name="folder-exclusions"></a>Ordner Ausschlüsse

> [!TIP]
> Bei Ordnernamen wird die Groß-/Kleinschreibung nicht beachtet

 

Die folgenden Ordner werden standardmäßig von der Indizierung ausgeschlossen:



| Ordner Ausschluss Muster                                                              | Auswirkung in Windows 7 | Auswirkung in Windows Vista | BESCHREIBUNG                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *% System%* \\ ProgramData- \\ Microsoft- \\ \\ Suchdaten\\                                    | **Excluded**        | Keine Auswirkungen               | Indexer-Daten auf dem Systemlaufwerk.                                                                                                                                                                                          |
| *% System%* \\ Benutzer \\ *Benutzername* \\ AppData\\                                              | **Excluded**        | Keine Auswirkungen               | Die Anwendungsdaten des Benutzers (einschließlich Temp-Daten) auf dem Systemlaufwerk.<br/> Für jeden Benutzer, der sich auf dem System anmeldet, wird ein bestimmtes Ausschluss Muster hinzugefügt, das die Anwendungsdaten aus dem Index ausschließt.<br/> |
| *% System%* \\ Benutzer \\ \* \\ AppData \\ lokale \\ Microsoft \\ Windows- \\ Dateien für temporäre Internet Dateien\\ | **Excluded**        | Keine Auswirkungen               | Der Standard Speicherort für temporäre Internetdateien von Windows Internet Explorer auf dem Systemlaufwerk.<br/> Wenn der Speicherort der temporären Internetdateien von Internet Explorer geändert wird, können diese Dateien indiziert werden.<br/>    |
| *% System%* \\ Windows \\ csc\\                                                            | **Excluded**        | Keine Auswirkungen               | Wenn die Indizierung für das Windows-System Verzeichnis aktiviert ist, wird der CSC-Ordner (auf dem Systemlaufwerk) weiterhin von der Indizierung ausgeschlossen.                                                                                           |
| *% System%* \\ Windows- \\ \* \\ Temp\\                                                       | **Excluded**        | Keine Auswirkungen               | Temporäre Windows-Daten auf dem Systemlaufwerk.                                                                                                                                                                                     |
| *% System%* \\ Windows.\*\\                                                              | **Excluded**        | Keine Auswirkungen               | Alte Windows-Installationen auf dem Systemlaufwerk.                                                                                                                                                                             |
| *% System%* \\ ProgramData\\                                                             | **Excluded**        | **Excluded**            | Beachten Sie, dass der Unterordner für das freigegebene Startmenü indiziert ist.                                                                                                                                                                     |
| *% System%* \\ Benutzer \\ \* \\ AppData\\                                                      | **Excluded**        | **Excluded**            | Anwendungsdaten der Benutzer (einschließlich Temp-Daten).                                                                                                                                                                              |
| *% System%* \\ Benutzer \\ \* \\ lokale APPDATA- \\ \\ Temp\\                                         | **Excluded**        | **Excluded**            | Temporäre Daten der Benutzer. Wenn die Indizierung für Benutzer Anwendungsdaten aktiviert ist, werden die temporären Daten des Benutzers weiterhin standardmäßig von der Indizierung ausgeschlossen.                                                                                           |
| *% System%* \\ Windows\\                                                                 | **Excluded**        | **Excluded**            | Betriebssystemdateien auf dem Systemlaufwerk.                                                                                                                                                                                |
| *% System%* \\ $Recycle bin\\                                                            | **Excluded**        | **Excluded**            | Speicherort der Dateien im Papierkorb.                                                                                                                                                                                      |
| *% System%* \\ Erstellen\\                                                                   | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| *% System%* \\ Installiertes Repository\\                                                    | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| *% System%* \\ Programmdateien\\                                                           | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| *% System%* \\ Programmdateien (x86)\\                                                     | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| \*\\Temp\\\*                                                                          | Keine Auswirkungen           | **Excluded**            | Temporäre Windows-Daten und andere Ordner mit dem Namen "Temp".                                                                                                                                                                  |
| *% System%* \\ \\Standardbenutzer\\                                                          | Keine Auswirkungen           | **Excluded**            | Der Speicherort der Standardbenutzer Profildaten auf dem Systemlaufwerk.                                                                                                                                                             |
| \*\\Windows.\*\\                                                                      | Keine Auswirkungen           | **Excluded**            | Alte Windows-Installationen und andere Ordner mit Namen, die mit "Windows" beginnen.                                                                                                                                         |



 

## <a name="drive-exclusions"></a>Laufwerks Ausschlüsse

Unter Windows 7 und Windows Vista werden Wechsel Datenträger standardmäßig nicht indiziert.

> [!Note]  
> Wenn Wechsel Datenträger sich selbst als Festplattenlaufwerke melden, können Sie diese zur Indizierung hinzufügen, selbst wenn Sie tatsächlich entfernt werden. Die Informationen verbleiben im Index, und die Windows-Suche führt einen inkrementellen Crawl aus, um die Indizierungs Ergebnisse abzugleichen, wenn der Wechsel Datenträger Da sich USB-Speicherstick selbst als Wechselmedien melden, können Sie nicht indiziert werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Indizierung, Abfragen und Benachrichtigungen in Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Indizierungsprozess in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Abfrageprozess in Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Benachrichtigungs Prozess in Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[URL-Formatierungs Anforderungen](url-formatting-requirements.md)
</dt> </dl>

 

 




