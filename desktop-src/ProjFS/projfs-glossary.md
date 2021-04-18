---
title: Windows projiziertes Datei System Glossar
description: Besondere Begriffe, die in projfs verwendet werden.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2020
ms.locfileid: "106338649"
---
# <a name="windows-projected-file-system-glossary"></a>Windows projiziertes Datei System Glossar

Besondere Begriffe, die in projfs verwendet werden.

<dl>
<dt>

<span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**Sicherungs Speicher**
</dt>
<dd>

Vom Anbieter erhaltene hierarchische Daten, die als Dateien und Verzeichnisse in das Dateisystem projiziert werden.
</dd>

<dt>

<span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**Platzhalter für Dirty**
</dt>
<dd>

Eine Datei oder ein Verzeichnis, das lokal geändert wurde und kein Cache seines Zustands im Speicher des Anbieters mehr ist.  Siehe [Cache Status im virtualisierungsstamm](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**vollständige Datei/Verzeichnis**
</dt>
<dd>

Eine Datei oder ein Verzeichnis, die im lokalen Dateisystem erstellt wurde, oder eine Datei, die geändert wurde, sodass Sie nicht mehr in den Sicherungs Speicher versetzt wird.  Siehe [Cache Status im virtualisierungsstamm](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**Platzhalter**
</dt>
<dd>

Eine Datei, deren Inhalt und Metadaten auf dem Datenträger zwischengespeichert wurden.  Siehe [Cache Status im virtualisierungsstamm](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**Platzhalter**
</dt>
<dd>

Eine Datei oder ein Verzeichnis, die auf dem Datenträger nicht vollständig vorhanden ist.  Siehe [Cache Status im virtualisierungsstamm](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**Tombstone**
</dt>
<dd>

Ein spezieller ausgeblendeter Platzhalter, der ein Element darstellt, das aus dem lokalen Dateisystem gelöscht wurde.  Siehe [Cache Status im virtualisierungsstamm](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**virtuelle Datei/Verzeichnis**
</dt>
<dd>

Eine Datei oder ein Verzeichnis, die physisch nicht auf dem Datenträger vorhanden ist, jedoch in enumerationsergebnisse projiziert wird.  Siehe [Cache Status im virtualisierungsstamm](cache-state.md).
</dd>

<dt>

<span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**virtualisierungsinstanz**
</dt>
<dd>

Ein in-Memory-Objekt, das die Kommunikation zwischen dem Anbieter und projfs für den Satz von Dateien und Verzeichnissen verwaltet, die sich unter einem bestimmten virtualisierungsstamm befinden.
</dd>

<dt>

<span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**virtualisierungsstamm**
</dt>
<dd>

Ein Verzeichnis im Dateisystem, in dem die Daten des Anbieters projiziert werden.
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->