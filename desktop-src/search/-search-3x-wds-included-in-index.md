---
description: In diesem Thema werden die Elemente beschrieben, die Windows Indizes suchen.
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

In diesem Thema werden die Elemente beschrieben, die Windows Indizes suchen.

Dieses Thema ist wie folgt organisiert:

-   [Standardmäßig indiziert](#indexed-by-default)
-   [Unterstützte Dateiformate](#file-formats-supported)
-   [Dateiausschlüsse](#file-exclusions)
-   [Ordnerausschlüsse](#folder-exclusions)
-   [Laufwerkausschlüsse](#drive-exclusions)
-   [Zugehörige Themen](#related-topics)

 

## <a name="indexed-by-default"></a>Standardmäßig indiziert

Protokollhandler und Filter sind in Windows Search enthalten, um die folgenden Arten von Inhalten zu indizieren:

-   In Windows Vista und höher werden die Microsoft Outlook- und Microsoft Outlook Express-E-Mail-Elemente eines Benutzers indiziert, während die E-Mail-Anwendung ausgeführt wird.
-   Offlinedateien im clientseitigen Cache (Client-Side Cache, CSC) werden durch lokales Windows Suchen indiziert.
-   Windows Die Suche unterstützt das Sammeln von Dateistartadressen auf NTFS- und FAT32-Volumes. NTFS unterstützt die benachrichtigungsbasierte Indizierung, und FAT32 unterstützt eine inkrementelle Durchforstung beim Start und antwortet dann auf Benachrichtigungen.
-   Windows Vista und höher machen weiterhin eine Eigenschaft pro Ordner/pro Datei verfügbar, um die Indizierung zu aktivieren: die Option "**Für schnelle Suche, sodass der Indexierungsdienst diesen Ordner indizieren** kann " im Dialogfeld **Eigenschaft.** Durch Festlegen des FANCI-Bitflags wird sichergestellt, dass grundlegende Eigenschaften aus dem Protokoll, z. B. URL, Dateiname und Größe, indiziert werden, aber weder Filterhandler noch Eigenschaftenhandler ausgeführt werden.
-   Der Textinhalt wird indiziert, die Interpunktion jedoch nicht.

## <a name="file-formats-supported"></a>Unterstützte Dateiformate

Windows Die Suche verfügt über Protokollhandler, Eigenschaftenhandler und Filterhandler, um die folgenden Formate automatisch zu indiziert:

-   Mediendateien: alle Mediendateitypen
-   **HTML** (nlhtml.dll): .ascx, .asp, .aspx, .css, .hhc, .htm, .html, .htt, .htw, .htx, .odc, .stm
-   **MIME HTML** (mimefilt.dll): .mht, .mhtml
-   **Office** (offfilt.dll): .doc, .dot, .xl, .pps, .ppt, .xlb, .xlc, .xls, .xlt
-   **Text** (query.dll): .asm, .asx, .bat, .c, .cmd, .cpp, .cxx, .def, .dic, .h, .hpp, .hxx, .idl, .idq, .inf, .ini, .inx, .js, .log, .m3u, .rc, .reg, .rtf, .txt, .url, .vbs, .wtx
-   **XML** (xmlfilt.dll): .xml, .xsl
-   **OneNote:**.one
-   **Tablet Journal** (jntfiltr.dll): .jnt

Eigenschaften werden für alle Dateien mit Ausnahme des strukturierten Speichers indiziert. Auf Windows Vista und höher werden viele Mediendateieigenschaften indiziert. Der Inhalt wird jedoch nicht indiziert, wenn die Dateien durch drm (Digital Rights Management) geschützt sind.

> [!Note]  
> Der HTML-Filter indiziert keine HTML-Kommentare.

 

## <a name="file-exclusions"></a>Dateiausschlüsse

Wenn einem Dateityp kein Filter zugeordnet ist oder eine Datei keine Erweiterung aufweist, werden die Systemeigenschaften für Dateien dieses Typs indiziert, aber der Dateiinhalt wird nicht indiziert.

Darüber hinaus indiziert Windows Search den Inhalt von Dateien nicht unter Information Rights Management (IRM) oder Digital Rights Management (DRM).

Auf Windows Vista (nur) sind die folgenden Dateien standardmäßig von der Indizierung ausgeschlossen:

-   Dateien, die als Ausgeblendet oder System gekennzeichnet sind.
-   Dateien mit den folgenden Erweiterungen:

    .386, .aps, . AudioCD, .bin, .bk1, .bk2, .bkf, .bsc, .btr, .chk, .ci, .crwl, .dbg, .dct, . DeskLink, .dir, \_ .dl, .dll, .drv, .dvd, .evt, .ex \_ , .exe, .exp, .eyb, .fnd, .fnt, . Folder, .fon, .hui, .gthr, .hqx, .icm, .idb, .idx, .ilk, .imc, .in \_ , .ini, .inv, .jbf, .latex, .lib, .local, .m14, .mac, .manifest, .map, . MAPIMail, .mmf, .movie, .mv, .mydocs, .ncb, .obj, \_ .oc, .ocx, .pch, .pdb, .pf, .pma, .pmc, .pml, .pmr, .res, .rmp, .rpc, .rsp, .sbr, .sc2, .sit, .sr \_ , .sy, \_ .sym, .sys, .tlb, .trc, .ttc, .ttf, .vbx, .vxd, .wll, .wlt, .xix, .z96, . DLLSendToTarget.

## <a name="folder-exclusions"></a>Ordnerausschlüsse

> [!TIP]
> Bei Ordnernamen wird die Groß-/Kleinschreibung nicht beachtet.

 

Die folgenden Ordner sind standardmäßig von der Indizierung ausgeschlossen:



| Ordnerausschlussmuster                                                              | Auswirkung in Windows 7 | Auswirkung in Windows Vista | Beschreibung                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *%System%* \\ ProgramData \\ Microsoft \\ \\ Search-Daten\\                                    | **Excluded**        | Keine Auswirkungen               | Indexerdaten auf dem Systemlaufwerk.                                                                                                                                                                                          |
| *%System%* \\ \\*BenutzerBenutzername* \\ AppData\\                                              | **Excluded**        | Keine Auswirkungen               | Die Anwendungsdaten des Benutzers (einschließlich temporärer Daten) auf dem Systemlaufwerk.<br/> Für jeden Benutzer, der sich beim System anmeldet, wird ein bestimmtes Ausschlussmuster hinzugefügt, das seine Anwendungsdaten aus dem Index ausschließt.<br/> |
| *%System%* \\ Benutzer \\ \* \\ AppData \\ Local Microsoft Windows Temporäre \\ \\ \\ Internetdateien\\ | **Excluded**        | Keine Auswirkungen               | Standardspeicherort Windows Internet Explorer temporären Internetdateien auf dem Systemlaufwerk.<br/> Wenn der Speicherort Internet Explorer temporären Internetdateien geändert wird, können diese Dateien indiziert werden.<br/>    |
| *%System%* \\ \\Windows Csc\\                                                            | **Excluded**        | Keine Auswirkungen               | Wenn die Indizierung für das Windows Systemverzeichnis aktiviert ist, wird der CSC-Ordner (auf dem Systemlaufwerk) weiterhin von der Indizierung ausgeschlossen.                                                                                           |
| *%System%* \\ \\ \* Windows \\ Temp\\                                                       | **Excluded**        | Keine Auswirkungen               | Windows temporäre Daten auf dem Systemlaufwerk.                                                                                                                                                                                     |
| *%System%* \\ Windows.\*\\                                                              | **Excluded**        | Keine Auswirkungen               | Alte Windows Installationen auf dem Systemlaufwerk.                                                                                                                                                                             |
| *%System%* \\ ProgramData\\                                                             | **Excluded**        | **Excluded**            | Beachten Sie, dass der freigegebene Unterordner Startmenü indiziert ist.                                                                                                                                                                     |
| *%System%* \\ Benutzer \\ \* \\ AppData\\                                                      | **Excluded**        | **Excluded**            | Anwendungsdaten von Benutzern (einschließlich temporärer Daten).                                                                                                                                                                              |
| *%System%* \\ Benutzer \\ \* \\ AppData \\ Local \\ Temp\\                                         | **Excluded**        | **Excluded**            | Temporäre Daten von Benutzern. Wenn die Indizierung für Benutzeranwendungsdaten aktiviert ist, sind temporäre Benutzerdaten weiterhin standardmäßig von der Indizierung ausgeschlossen.                                                                                           |
| *%System%* \\ Windows\\                                                                 | **Excluded**        | **Excluded**            | Betriebssystemdateien auf dem Systemlaufwerk.                                                                                                                                                                                |
| *%System%* \\ $Papierkorb\\                                                            | **Excluded**        | **Excluded**            | Speicherort der Dateien im Papierkorb.                                                                                                                                                                                      |
| *%System%* \\ Bauen\\                                                                   | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| *%System%* \\ Installiertes Repository\\                                                    | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| *%System%* \\ Programmdateien\\                                                           | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| *%System%* \\ Programme (x86)\\                                                     | Keine Auswirkungen           | **Excluded**            | Auf dem Systemlaufwerk.                                                                                                                                                                                                       |
| \*\\Temp\\\*                                                                          | Keine Auswirkungen           | **Excluded**            | Windows temporäre Daten und andere Ordner mit dem Namen "temp".                                                                                                                                                                  |
| *%System%* \\ \\Standardbenutzer\\                                                          | Keine Auswirkungen           | **Excluded**            | Der Speicherort der Standardbenutzerprofildaten auf dem Systemlaufwerk.                                                                                                                                                             |
| \*\\Fenster.\*\\                                                                      | Keine Auswirkungen           | **Excluded**            | Alte Windows Installationen und andere Ordner mit Namen, die mit "windows. " beginnen.                                                                                                                                         |



 

## <a name="drive-exclusions"></a>Laufwerkausschlüsse

Auf Windows 7 und Windows Vista werden Wechseldatenträger standardmäßig nicht indiziert.

> [!Note]  
> Wenn Wechseldatenträger sich selbst als Festplattenlaufwerke melden, können Sie sie hinzufügen, um sie zu indizieren, auch wenn sie tatsächlich wechselbar sind. Informationen verbleiben im Index, und Windows Search führt eine inkrementelle Durchforstung durch, um die Indizierungsergebnisse abzustimmen, wenn der Wechseldatenträger wieder angeschlossen wird. Da USB-Speichersticks sich selbst als Wechseldatenträger melden, können sie nicht indiziert werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Indizieren, Abfragen und Benachrichtigungen in Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Indizierungsprozess in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Abfrageprozess in Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Benachrichtigungsprozess in Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Anforderungen an die URL-Formatierung](url-formatting-requirements.md)
</dt> </dl>

 

 




