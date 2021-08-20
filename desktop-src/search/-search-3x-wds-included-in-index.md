---
description: In diesem Thema werden die Elemente beschrieben, die Windows Suchen von Indizes enthalten.
ms.assetid: vs|search|~\search\wds3x\overviews\misc_items_in_index.htm
title: Was ist im Index enthalten?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbffec8aba8a985faca112eac434b669d22eff82d94d6b4eaf5588585ced771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463323"
---
# <a name="what-is-included-in-the-index"></a>Was ist im Index enthalten?

In diesem Thema werden die Elemente beschrieben, die Windows Suchen von Indizes enthalten.

Dieses Thema ist wie folgt organisiert:

-   [Standardmäßig indiziert](#indexed-by-default)
-   [Unterstützte Dateiformate](#file-formats-supported)
-   [Dateiausschlüsse](#file-exclusions)
-   [Ordnerausschlüsse](#folder-exclusions)
-   [Laufwerkausschlüsse](#drive-exclusions)
-   [Zugehörige Themen](#related-topics)

 

## <a name="indexed-by-default"></a>Standardmäßig indiziert

Protokollhandler und Filter sind in Windows Search enthalten, um die folgenden Arten von Inhalt zu indizieren:

-   In Windows Vista und höher werden die E-Mail-Elemente Microsoft Outlook und Microsoft Outlook Express eines Benutzers indiziert, während die E-Mail-Anwendung ausgeführt wird.
-   Offlinedateien im clientseitigen Cache (CSC) werden von der lokalen Windows indiziert.
-   Windows Die Suche unterstützt das Sammeln von Dateistartadressen auf NTFS- und FAT32-Volumes. NTFS unterstützt die benachrichtigungsbasierte Indizierung, und FAT32 unterstützt eine inkrementelle Durchforstung beim Start und reagiert dann auf Benachrichtigungen.
-   Windows Vista und höher machen weiterhin eine Pro-Ordner-/Pro-Datei-Eigenschaft verfügbar, um die Indizierung zu aktivieren: die Option " For **fast searching, allowing Indexing Service to index this folder**" im Dialogfeld **Eigenschaft.** Durch festlegen des FANCI-Bitflags wird sichergestellt, dass grundlegende Eigenschaften des Protokolls wie URL, Dateiname und Größe indiziert werden, aber weder Filterhandler noch Eigenschaftenhandler ausgeführt werden.
-   Textinhalt wird indiziert, Interpunktion jedoch nicht.

## <a name="file-formats-supported"></a>Unterstützte Dateiformate

Windows Die Suche verfügt über Protokollhandler, Eigenschaftenhandler und Filterhandler, um die folgenden Formate automatisch zu indizieren:

-   Mediendateien: alle Mediendateitypen
-   **HTML** (nlhtml.dll): .ascx, .asp, .aspx, .css, .hhc, .htm, .html, .htt, .htw, .htx, .odc, .stm
-   **MIME HTML** (mimefilt.dll): .mht, .mhtml
-   **Office** (offfilt.dll): .doc, .dot, .pot, .pps, .ppt, .xlb, .xlc, .xls, .xlt
-   **Text** (query.dll): .asm, .asx, .bat, .c, .cmd, .cpp, .cxx, .def, .dic, .h, .hpp, .hxx, .idl, .idq , .inf, .ini, .inx, .js, .log, .m3u, .rc, .reg, .rtf, .txt, .url, .vbs, .wtx
-   **XML** (xmlfilt.dll): .xml, .xsl
-   **OneNote**: .one
-   **Tablet Journal** (jntfiltr.dll): .jnt

Eigenschaften werden für alle Dateien mit Ausnahme des strukturierten Speichers indiziert. Unter Windows Vista und höher werden viele Mediendateieigenschaften indiziert. Der Inhalt wird jedoch nicht indiziert, wenn die Dateien durch Digital Rights Management (DRM) geschützt sind.

> [!Note]  
> Der HTML-Filter indiziert keine HTML-Kommentare.

 

## <a name="file-exclusions"></a>Dateiausschlüsse

Wenn einem Dateityp kein Filter zugeordnet ist oder eine Datei keine Erweiterung aufweist, werden die Systemeigenschaften für Dateien dieses Typs indiziert, aber der Dateiinhalt wird nicht indiziert.

Darüber hinaus Windows Search den Inhalt von Dateien unter Information Rights Management (IRM) oder Digital Rights Management (DRM) nicht indiziert.

In Windows Vista (nur) werden die folgenden Dateien standardmäßig von der Indizierung ausgeschlossen:

-   Dateien, die als Ausgeblendet oder System markiert sind.
-   Dateien mit den folgenden Erweiterungen:

    .386, .aps, . AudioCD, .bin, .bk1, .bk2, .bkf, .bsc, .btr, .chk, .ci, .crwl, .dbg, .dct, . DeskLink, .dir, .dl \_ , .dll, .drv, .dvd, .evt, .ex \_ , .exe, .exp, .eyb, .fnd, .fnt, . Folder, .fon, .uld, .gthr, .hqx, .icm, .idb, .idx, .ilk, .imc, .in \_ , .ini, .inv, .jbf, .latex, .lib, .local, .m14, .mac, .manifest, .map, . MAPIMail, .mmf, .movie, .mv, .mydocs, .ncb, .obj, \_ .oc, .ocx, .pch, .pdb, .pf, .pma, .pmc, .pml, .pmr, .res, .rmp, .rpc, .rsp, .sbr, .sc2, .sit, .sr \_ , \_ .sy , .sym, .sys, .tlb, .trc, .ttc, .ttf, .vbx, .vxd, .wll, .wlt, .xix, .z96, . HEITSendToTarget.

## <a name="folder-exclusions"></a>Ordnerausschlüsse

> [!TIP]
> Bei Ordnernamen wird die Schreibung nicht beachtet.

 

Die folgenden Ordner sind standardmäßig von der Indizierung ausgeschlossen:



| Ordnerausschlussmuster                                                              | Auswirkung in Windows 7 | Auswirkung in Windows Vista | BESCHREIBUNG                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *%System%* \\ ProgramData \\ Microsoft \\ Search \\ Data\\                                    | **Excluded**        | Keine Auswirkungen               | Indexerdaten auf dem Systemlaufwerk.                                                                                                                                                                                          |
| *%System%* \\ UserName \\ *AppData für* \\ Benutzer\\                                              | **Excluded**        | Keine Auswirkungen               | Anwendungsdaten des Benutzers (einschließlich temporärer Daten) auf dem Systemlaufwerk.<br/> Für jeden Benutzer, der sich beim System anmeldet, wird ein bestimmtes Ausschlussmuster hinzugefügt, das seine Anwendungsdaten aus dem Index ausschließt.<br/> |
| *%System%* \\ Users \\ \* \\ AppData \\ Local Microsoft Windows Temporary Internet \\ \\ \\ Files\\ | **Excluded**        | Keine Auswirkungen               | Der Standardspeicherort Windows Internet Explorer temporären Internetdateien auf dem Systemlaufwerk.<br/> Wenn der Speicherort der Internet Explorer Internetdateien geändert wird, können diese Dateien indiziert werden.<br/>    |
| *%System%* \\ \\Windows Csc\\                                                            | **Excluded**        | Keine Auswirkungen               | Wenn die Indizierung für das Windows-Systemverzeichnis aktiviert ist, wird der CSC-Ordner (auf dem Systemlaufwerk) weiterhin von der Indizierung ausgeschlossen.                                                                                           |
| *%System%* \\ \\ \* Windows \\ Temp\\                                                       | **Excluded**        | Keine Auswirkungen               | Windows temporäre Daten auf dem Systemlaufwerk.                                                                                                                                                                                     |
| *%System%* \\ Windows.\*\\                                                              | **Excluded**        | Keine Auswirkungen               | Alte Windows auf dem Systemlaufwerk.                                                                                                                                                                             |
| *%System%* \\ ProgramData\\                                                             | **Excluded**        | **Excluded**            | Beachten Sie, dass der freigegebene Unterordner Startmenü indiziert ist.                                                                                                                                                                     |
| *%System%* \\ AppData \\ \* \\ für Benutzer\\                                                      | **Excluded**        | **Excluded**            | Anwendungsdaten von Benutzern (einschließlich temporärer Daten).                                                                                                                                                                              |
| *%System%* \\ AppData \\ \* \\ Local Temp \\ für \\ Benutzer\\                                         | **Excluded**        | **Excluded**            | Temporäre Daten von Benutzern. Wenn die Indizierung für Benutzeranwendungsdaten aktiviert ist, werden temporäre Benutzerdaten weiterhin standardmäßig von der Indizierung ausgeschlossen.                                                                                           |
| *%System%* \\ Windows\\                                                                 | **Excluded**        | **Excluded**            | Betriebssystemdateien auf dem Systemlaufwerk.                                                                                                                                                                                |
| *%System%* \\ $Papierkorb\\                                                            | **Excluded**        | **Excluded**            | Speicherort der Dateien im Papierkorb.                                                                                                                                                                                      |
| *%System%* \\ Bauen\\                                                                   | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| *%System%* \\ Installiertes Repository\\                                                    | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| *%System%* \\ Programmdateien\\                                                           | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| *%System%* \\ Programme (x86)\\                                                     | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| \*\\Temp\\\*                                                                          | Keine Auswirkungen           | **Excluded**            | Windows temporäre Daten und andere Ordner mit dem Namen "temp".                                                                                                                                                                  |
| *%System%* \\ Standardeinstellung für \\ Benutzer\\                                                          | Keine Auswirkungen           | **Excluded**            | Der Speicherort der Standardbenutzerprofildaten auf dem Systemlaufwerk.                                                                                                                                                             |
| \*\\Fenster.\*\\                                                                      | Keine Auswirkungen           | **Excluded**            | Alte Windows-Installationen und andere Ordner mit Namen, die mit "windows." beginnen.                                                                                                                                         |



 

## <a name="drive-exclusions"></a>Laufwerkausschlüsse

Auf Windows 7 und Windows Vista werden Wechseldatenträger standardmäßig nicht indiziert.

> [!Note]  
> Wenn Wechseldatenträger sich selbst als Festplattenlaufwerke melden, können Sie sie zur Indizierung hinzufügen, auch wenn sie tatsächlich wechselbar sind. Die Informationen verbleiben im Index, und Windows search führt eine inkrementelle Durchforstung durch, um die Indizierungsergebnisse abgleichen, wenn der Wechseldatenträger wieder angeschlossen wird. Da USB-Flashlaufwerke sich selbst als Wechseldatenträger melden, können sie nicht indiziert werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Indizierung, Abfrage und Benachrichtigungen in Windows Suchen](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Indizierungsprozess in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Abfrageprozess in Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Benachrichtigungsprozess in Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[URL-Formatierungsanforderungen](url-formatting-requirements.md)
</dt> </dl>

 

 




