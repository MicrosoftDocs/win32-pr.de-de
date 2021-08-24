---
title: Windows Glossar des projizierten Dateisystems
description: Spezielle Begriffe, die in ProjFS verwendet werden.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 12b6e90d98fce3882aa5dc8d552f88e9cd9f389d24673fdc5caf175e180082f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030982"
---
# <a name="windows-projected-file-system-glossary"></a>Windows Glossar des projizierten Dateisystems

Spezielle Begriffe, die in ProjFS verwendet werden.

<dl>
<dt>

<span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**Backing Store**
</dt>
<dd>

Vom Anbieter beibehaltene hierarchische Daten, die als Dateien und Verzeichnisse in das Dateisystem projiziert werden.
</dd>

<dt>

<span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**Dirty-Platzhalter**
</dt>
<dd>

Eine Datei oder ein Verzeichnis, die lokal geändert wurde und nicht mehr ein Cache des Zustands im Speicher des Anbieters ist.  Weitere Informationen [finden Sie unter Cachezustand im Virtualisierungsstamm.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**Vollständige Datei/vollständiges Verzeichnis**
</dt>
<dd>

Eine Datei oder ein Verzeichnis, die im lokalen Dateisystem erstellt wurde, oder eine Datei, die geändert wurde, wodurch sie nicht mehr als Cache ihres Zustands im Hintergrundspeicher verwendet wird.  Weitere Informationen [finden Sie unter Cachezustand im Virtualisierungsstamm.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**Hydrated-Platzhalter**
</dt>
<dd>

Eine Datei, deren Inhalt und Metadaten auf dem Datenträger zwischengespeichert wurden.  Weitere Informationen [finden Sie unter Cachezustand im Virtualisierungsstamm.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**Platzhalter**
</dt>
<dd>

Eine Datei oder ein Verzeichnis, die bzw. das nicht vollständig auf dem Datenträger vorhanden ist.  Weitere Informationen [finden Sie unter Cachezustand im Virtualisierungsstamm.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**Tombstone**
</dt>
<dd>

Ein spezieller ausgeblendeter Platzhalter, der ein Element darstellt, das aus dem lokalen Dateisystem gelöscht wurde.  Weitere Informationen [finden Sie unter Cachezustand im Virtualisierungsstamm.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**Virtuelle Datei/Verzeichnis**
</dt>
<dd>

Eine Datei oder ein Verzeichnis, die physisch nicht auf dem Datenträger vorhanden ist, aber in Enumerationsergebnisse projiziert wird.  Weitere Informationen [finden Sie unter Cachezustand im Virtualisierungsstamm.](cache-state.md)
</dd>

<dt>

<span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**Virtualisierungsinstanz**
</dt>
<dd>

Ein In-Memory-Objekt, das die Kommunikation zwischen dem Anbieter und ProjFS für den Satz von Dateien und Verzeichnissen verwaltet, die sich unter einem bestimmten Virtualisierungsstamm befinden.
</dd>

<dt>

<span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**Virtualisierungsstamm**
</dt>
<dd>

Ein Verzeichnis im Dateisystem, unter dem die Daten des Anbieters projiziert werden.
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