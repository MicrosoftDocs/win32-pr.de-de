---
description: 'In diesem Thema werden die Funktionen zur Speicherverwaltung beschrieben:'
ms.assetid: 5a2a7a62-0bda-4a0d-93d2-25b4898871fd
title: Speicherverwaltungsfunktionen
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: a203583016a127a550f609068df8e86da384fa34
ms.sourcegitcommit: 43aef65e6563a56f35c019c5202827ab65772186
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2020
ms.locfileid: "103734776"
---
# <a name="memory-management-functions"></a>Speicherverwaltungsfunktionen

- [Allgemeine Speicherfunktionen](#general-memory-functions)
- [Funktionen zur Verhinderung von Datenausführung](#data-execution-prevention-functions)
- [Datei Mapping-Funktionen](#file-mapping-functions)
- [AWE-Funktionen](#awe-functions)
- [Heapfunktionen](#heap-functions)
- [Funktionen des virtuellen Arbeitsspeichers](#virtual-memory-functions)
- [Globale und lokale Funktionen](#global-and-local-functions)
- [Ungültige Speicherfunktionen](#bad-memory-functions)
- [Enclave-Funktionen](#enclave-functions)
- [ATL-Thunk-Funktionen](#atl-thunk-functions)
- [Veraltete Funktionen](#obsolete-functions)

## <a name="general-memory-functions"></a>Allgemeine Speicherfunktionen

| Funktion | BESCHREIBUNG |
|-|-|
| [**Addsecurememorycachecallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) | Registriert eine Rückruffunktion, die aufgerufen werden soll, wenn ein sicherer Speicherbereich freigegeben wird oder die zugehörigen Schutzmaßnahmen geändert werden. |
| [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) | Kopiert einen Speicherblock von einem Speicherort in einen anderen. |
| [**"Kreatememoryresourcenotifi"**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) | Erstellt ein Benachrichtigungs Objekt für Speicherressourcen. |
| [**FillMemory**](/previous-versions/windows/desktop/legacy/aa366561(v=vs.85)) | Füllt einen Speicherblock mit einem angegebenen Wert. |
| [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) | Ruft die Mindestgröße einer großen Seite ab. |
| [**Getphysicallyinstalledsystemmemory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getphysicallyinstalledsystemmemory) | Ruft die RAM-Größe ab, die physisch auf dem Computer installiert ist. |
| [**Getsystemflecachesize**](/windows/win32/api/memoryapi/nf-memoryapi-getsystemfilecachesize) | Ruft die aktuellen Größenbeschränkungen für das Workingset des System Caches ab. |
| [**Getschreitewatch**](/windows/win32/api/memoryapi/nf-memoryapi-getwritewatch) | Ruft die Adressen der Seiten ab, die in einen Bereich des virtuellen Arbeitsspeichers geschrieben wurden. |
| [**GlobalMemoryStatus usex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) | Ruft Informationen über die aktuelle Verwendung von physischem und virtuellem Arbeitsspeicher des Systems ab. |
| [**Arbeitsspeicher**](/previous-versions/windows/desktop/legacy/aa366788(v=vs.85)) | Verschiebt einen Speicherblock von einem Speicherort zu einem anderen. |
| [**QueryMemoryResourceNotification ermittelt**](/windows/win32/api/memoryapi/nf-memoryapi-querymemoryresourcenotification) | Ruft den Zustand des angegebenen Speicherressourcen Objekts ab. |
| [**Removesecurememorycachecallback**](/windows/desktop/api/WinBase/nf-winbase-removesecurememorycachecallback) | Hebt die Registrierung einer Rückruffunktion auf, die zuvor bei der [**addsecurememorycachecallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) -Funktion registriert wurde. |
| [**Resetschreitewatch**](/windows/win32/api/memoryapi/nf-memoryapi-resetwritewatch) | Setzt den Zustand der Schreib Nachverfolgung für einen Bereich des virtuellen Speichers zurück. |
| [**Securememorycachecallback**](/windows/desktop/api/WinNT/nc-winnt-psecure_memory_cache_callback) | Eine Anwendungs definierte Funktion, die aufgerufen wird, wenn ein gesicherter Speicherbereich freigegeben oder deren Schutzmaßnahmen geändert werden. |
| [**Securezeromemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) | Füllt einen Speicherblock mit Nullen auf. |
| [**Setsystemsplecachesize**](/windows/win32/api/memoryapi/nf-memoryapi-setsystemfilecachesize) | Begrenzt die Größe des Workingsets für den Dateisystem Cache. |
| [**Zeromemorisch**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) | Füllt einen Speicherblock mit Nullen auf. |

## <a name="data-execution-prevention-functions"></a>Funktionen zur Verhinderung von Datenausführung

Diese Funktionen werden mit der [Daten Ausführungs Verhinderung (Data Execution Prevention](data-execution-prevention.md) , DEP) verwendet.

| Funktion | BESCHREIBUNG |
|-|-|
| [**Getprocessdeppolicy**](/windows/desktop/api/WinBase/nf-winbase-getprocessdeppolicy) | Ruft die DEP-Einstellungen für einen Prozess ab. |
| [**Getsystemdeppolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) | Ruft die DEP-Einstellungen für das System ab. |
| [**Setprocessdeppolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) | Ändert die DEP-Einstellungen für einen Prozess. |

## <a name="file-mapping-functions"></a>Datei Mapping-Funktionen

Diese Funktionen werden bei der [Datei Zuordnung](file-mapping.md)verwendet.

| Funktion | BESCHREIBUNG |
|-|-|
| [**"Kreatefilemappinga"**](/windows/win32/api/winbase/nf-winbase-createfilemappinga) | Erstellt oder öffnet ein benanntes oder unbenanntes Datei Zuordnung-Objekt für eine angegebene Datei. |
| [**"Kreatefilemappingw"**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingw) | Erstellt oder öffnet ein benanntes oder unbenanntes Datei Zuordnung-Objekt für eine angegebene Datei. |
| [**CreateFileMapping2**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemapping2) | Erstellt oder öffnet ein benanntes oder unbenanntes Datei Zuordnung-Objekt für eine angegebene Datei. Sie können angeben, dass Sie einen bevorzugten NUMA-Knoten für den physischen Speicher als erweiterten Parameter angeben möchten. Siehe den *extendedparameters* -Parameter. |
| [**CreateFileMappingFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-createfilemappingfromapp) | Erstellt oder öffnet ein benanntes oder unbenanntes Datei Zuordnung-Objekt für eine angegebene Datei aus einer Windows Store-App. |
| [**"Kreatefilemappingnuma"**](/windows/desktop/api/WinBase/nf-winbase-createfilemappingnumaa) | Erstellt oder öffnet ein benanntes oder unbenanntes Datei Zuordnung-Objekt für eine angegebene Datei und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**Flushviewoffile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) | Schreibt einen Byte Bereich in eine zugeordnete Ansicht einer Datei in den Datenträger. |
| [**GetMappedFileName**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) | Überprüft, ob die angegebene Adresse in einer Speicher Abbild Datei im Adressraum des angegebenen Prozesses liegt. Wenn dies der Fall ist, gibt die Funktion den Namen der Speicher Abbild Datei zurück. |
| [**' MapViewOfFile '**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) | Ordnet eine Ansicht einer Datei Zuordnung dem Adressraum eines aufrufenden Prozesses zu. |
| [**MapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile2) | Ordnet eine Ansicht einer Datei oder eines Pagefile-gestützten Abschnitts dem Adressraum des angegebenen Prozesses zu. |
| [**MapViewOfFile3**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3) | Ordnet eine Ansicht einer Datei oder eines Pagefile-gestützten Abschnitts dem Adressraum des angegebenen Prozesses zu. |
| [**MapViewOfFile3FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3fromapp) | Ordnet eine Ansicht einer Datei Zuordnung dem Adressraum eines aufrufenden Prozesses aus einer Windows Store-App zu. |
| [**Fehler bei MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) | Ordnet eine Ansicht einer Datei Zuordnung dem Adressraum eines aufrufenden Prozesses zu. Ein Aufrufer kann optional eine vorgeschlagene Speicheradresse für die Ansicht angeben. |
| [**Mapviewoffileexnuma**](/windows/desktop/api/WinBase/nf-winbase-mapviewoffileexnuma) | Ordnet eine Ansicht einer Datei Zuordnung dem Adressraum eines aufrufenden Prozesses zu und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**MapViewOfFileFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffilefromapp) | Ordnet eine Ansicht einer Datei Zuordnung dem Adressraum eines aufrufenden Prozesses aus einer Windows Store-App zu. |
| [**MapViewOfFileNuma2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffilenuma2) | Ordnet eine Ansicht einer Datei oder eines Pagefile-gestützten Abschnitts dem Adressraum des angegebenen Prozesses zu. |
| [**Fehler bei OpenFileMapping**](/windows/win32/api/winbase/nf-winbase-openfilemappinga) | Öffnet ein benanntes Datei Zuordnung-Objekt. |
| [**OpenFileMappingFromApp**](/windows/win32/api/winbase/nf-winbase-openfilemappingafromapp) | Öffnet ein benanntes Datei Zuordnung-Objekt. |
| [**Fehler bei UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) | Entfernt eine zugeordnete Ansicht einer Datei aus dem Adressraum des aufrufenden Prozesses. |
| [**UnmapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile2) | Entordnet eine zuvor zugeordnete Ansicht einer Datei oder eines Abschnitts mit Pagefile-Unterstützung. |
| [**Unmapviewoffileex**](/windows/desktop/api/MemoryApi/nf-memoryapi-unmapviewoffileex) | Entordnet eine zuvor zugeordnete Ansicht einer Datei oder eines Abschnitts mit Pagefile-Unterstützung. |

## <a name="awe-functions"></a>AWE-Funktionen

Dies sind die [AWE-Funktionen](address-windowing-extensions.md).

| Funktion | BESCHREIBUNG |
|-|-|
| [**"Zuordnung"**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages) | Ordnet physische Speicherseiten zu, die in einem beliebigen AWE-Bereich des Prozesses zugeordnet und nicht zugeordnet werden. |
| [**Zuordnung von "Zuweisung"**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma) | Ordnet physische Speicherseiten zu, die in einem beliebigen AWE-Bereich des Prozesses zugeordnet und nicht zugeordnet werden, und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages) | Gibt physische Speicherseiten frei, die zuvor mit " [**zuordneter**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)" zugeordnet wurden. |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages) | Ordnet zuvor zugeordnete physische Speicherseiten an der angegebenen Adresse innerhalb einer AWE-Region zu. |
| [**Mapuserphysicalpagesscatcher**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter) | Ordnet zuvor zugeordnete physische Speicherseiten an der angegebenen Adresse innerhalb einer AWE-Region zu. |

## <a name="heap-functions"></a>Heapfunktionen

Dies sind die [Heap Funktionen](heap-functions.md).

| Funktion | BESCHREIBUNG |
|-|-|
| [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) | Ruft ein Handle für den Heap des aufrufenden Prozesses ab. |
| [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) | Ruft Handles für alle Heaps ab, die für den aufrufenden Prozess gültig sind. |
| [**Heapzuweisung**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) | Ordnet einen Speicherblock von einem Heap zu. |
| [**Heapcompact**](/windows/desktop/api/HeapApi/nf-heapapi-heapcompact) | Fügt angrenzende freie Speicherblöcke auf einem Heap zusammen. |
| [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) | Erstellt ein Heap Objekt. |
| [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) | Zerstört das angegebene Heap Objekt. |
| [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) | Gibt einen Speicherblock frei, der von einem Heap zugewiesen wurde. |
| [**Heaplock**](/windows/desktop/api/HeapApi/nf-heapapi-heaplock) | Versucht, die einem angegebenen Heap zugeordnete Sperre abzurufen. |
| [**Heapqueryinformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapqueryinformation) | Ruft Informationen zum angegebenen Heap ab. |
| [**Heaprezuweisung**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) | Ordnet einen Speicherblock von einem Heap neu zu. |
| [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) | Legt Heap Informationen für den angegebenen Heap fest. |
| [**HEAPSIZE**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) | Ruft die Größe eines Speicherblocks ab, der von einem Heap zugewiesen wurde. |
| [**Heapunlock**](/windows/desktop/api/HeapApi/nf-heapapi-heapunlock) | Gibt den Besitz der einem angegebenen Heap zugeordneten Sperre frei. |
| [**Heapvalidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) | Versucht, einen angegebenen Heap zu validieren. |
| [**Heapwalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) | Listet die Speicherblöcke in einem angegebenen Heap auf. |

## <a name="virtual-memory-functions"></a>Funktionen des virtuellen Arbeitsspeichers

Dabei handelt es sich um die [Funktionen des virtuellen Arbeitsspeichers](virtual-memory-functions.md).

| Funktion | BESCHREIBUNG |
|-|-|
| [**Verwerfen von virtualmemory**](/windows/win32/api/memoryapi/nf-memoryapi-discardvirtualmemory) | Verwirft den Speicherinhalt eines Bereichs von Speicherseiten, ohne den Arbeitsspeicher zu übernehmen. Der Inhalt des verworfenen Speichers ist nicht definiert und muss von der Anwendung umgeschrieben werden. |
| [**Offervirtualmemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory) | Gibt an, dass die Daten, die in einem Bereich von Speicherseiten enthalten sind, von der Anwendung nicht mehr benötigt werden und ggf. vom System verworfen werden können. |
| [**Prefetchvirtualmemory**](/windows/win32/api/memoryapi/nf-memoryapi-prefetchvirtualmemory) | Vorab Abruf virtueller Adressbereiche in den physischen Speicher. |
| [**Queryvirtualmemoryinformation**](/windows/desktop/api/MemoryApi/nf-memoryapi-queryvirtualmemoryinformation) | Gibt Informationen über eine Seite oder eine Gruppe von Seiten innerhalb des virtuellen Adressraums des angegebenen Prozesses zurück. |
| [**Reclaimvirtualmemory**](/windows/win32/api/memoryapi/nf-memoryapi-reclaimvirtualmemory) | Gibt einen Bereich von Speicherseiten frei, die dem System mit [**offervirtualmemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory)angeboten wurden. |
| [**Setprocessvalidcalltargets**](/windows/desktop/api/MemoryApi/nf-memoryapi-setprocessvalidcalltargets) | Stellt cfg mit einer Liste gültiger indirekter callziele bereit und gibt an, ob Sie als gültig gekennzeichnet werden sollen oder nicht. |
| [**VirtualAlloc**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc) | Reserviert oder übergibt einen Seitenbereich im virtuellen Adressraum des aufrufenden Prozesses. |
| [**VirtualAlloc2**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc2) | Reserviert oder ändert den Status eines Speicherbereichs innerhalb des virtuellen Adressraums eines angegebenen Prozesses. Die-Funktion initialisiert den Arbeitsspeicher, der für NULL zugewiesen wird. |
| [**VirtualAlloc2FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Reserviert oder ändert den Status eines Seitenbereichs im virtuellen Adressraum des aufrufenden Prozesses. Der von dieser Funktion zugewiesene Arbeitsspeicher wird automatisch mit 0 (null) initialisiert. |
| [**Virtualzuweisung**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Reserviert einen Seitenbereich im virtuellen Adressraum des angegebenen Prozesses oder führt einen Commit aus. |
| [**Virtualzuweisung-exnuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) | Reserviert einen Arbeitsspeicher Bereich innerhalb des virtuellen Adressraums des angegebenen Prozesses oder führt einen Commit aus und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**Virtualzuzuweisung**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Reserviert oder ändert den Status eines Seitenbereichs im virtuellen Adressraum des aufrufenden Prozesses. Der von dieser Funktion zugewiesene Arbeitsspeicher wird automatisch mit 0 (null) initialisiert. |
| [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) | Hiermit wird ein Seitenbereich innerhalb des virtuellen Adressraums des aufrufenden Prozesses freigegeben oder debugert. |
| [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) | Gibt einen Arbeitsspeicher Bereich innerhalb des virtuellen Adressraums eines angegebenen Prozesses frei oder debugert diesen. |
| [**Virtuzuweisung**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) | Sperrt den angegebenen Bereich des virtuellen Adressraums des Prozesses in den physischen Speicher. |
| [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) | Ändert den Zugriffsschutz für eine Region mit zugesicherte Seiten im virtuellen Adressraum des aufrufenden Prozesses. |
| [**Virtualprotectex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) | Ändert den Zugriffsschutz für eine Region mit zugesicherte Seiten im virtuellen Adressraum des aufrufenden Prozesses. |
| [**VirtualProtectFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualprotectfromapp) | Ändert den Schutz für eine Region mit zugesicherte Seiten im virtuellen Adressraum des aufrufenden Prozesses. |
| [**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) | Stellt Informationen zu einem Bereich von Seiten im virtuellen Adressraum des aufrufenden Prozesses bereit. |
| [**Virtualqueryex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) | Stellt Informationen zu einem Bereich von Seiten im virtuellen Adressraum des aufrufenden Prozesses bereit. |
| [**Virtualunlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) | Entsperrt einen angegebenen Seitenbereich im virtuellen Adressraum eines Prozesses. |

## <a name="global-and-local-functions"></a>Globale und lokale Funktionen

Siehe auch [globale und lokale Funktionen](global-and-local-functions.md). Diese Funktionen werden aus Kompatibilitätsgründen mit 16-Bit-Fenstern bereitgestellt und mit dynamischer Datenaustausch (DDE), den Zwischenablage Funktionen und OLE-Datenobjekten verwendet. Wenn in der Dokumentation nicht ausdrücklich angegeben ist, dass eine globale oder lokale Funktion verwendet werden soll, sollten neue Anwendungen die entsprechende [Heap-Funktion](heap-functions.md) mit dem von [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap)zurückgegebenen Handle verwenden. Legen Sie für die entsprechende Funktionalität der globalen oder lokalen Funktion den *dwFlags* -Parameter der Heap Funktion auf 0 fest.

| Funktion | BESCHREIBUNG | Entsprechende Heap-Funktion |
|-|-|-|
| [**Globalzuweisung**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [ **localzuweisung**](/windows/desktop/api/WinBase/nf-winbase-localalloc) | Ordnet die angegebene Anzahl von Bytes aus dem Heap zu. | [**Heapzuweisung**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) |
| [**Globalverwerfen**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard), [ **localdiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) | Verwirft den angegebenen globalen Speicherblock. | Nicht zutreffend |
| [**Globalflags**](/windows/desktop/api/WinBase/nf-winbase-globalflags), [ **localflags**](/windows/desktop/api/WinBase/nf-winbase-localflags) | Gibt Informationen zum angegebenen globalen Speicher Objekt zurück. | Nicht zutreffend Verwenden Sie [**heapvalidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) , um den Heap zu überprüfen. |
| [**Global Free**](/windows/desktop/api/WinBase/nf-winbase-globalfree), [ **LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) | Gibt das angegebene globale Speicher Objekt frei. | [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) |
| [**Globalhandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle), [ **localhandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) | Ruft das Handle ab, das dem angegebenen Zeiger auf einen globalen Speicherblock zugeordnet ist. Diese Funktion sollte nur mit OLE-und Clipboard-Funktionen verwendet werden, die dies erfordern. | Nicht zutreffend |
| [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock), [ **loczuweisung**](/windows/desktop/api/WinBase/nf-winbase-locallock) | Sperrt ein globales Speicher Objekt und gibt einen Zeiger auf das erste Byte des Speicherblocks des-Objekts zurück. | Nicht zutreffend |
| [**Globalrezuweisungen**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc), [ **localrezuweisung**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) | Ändert die Größe oder die Attribute eines angegebenen globalen Speicher Objekts. | [**Heaprezuweisung**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) |
| [**Globalsize**](/windows/desktop/api/WinBase/nf-winbase-globalsize), [ **localsize**](/windows/desktop/api/WinBase/nf-winbase-localsize) | Ruft die aktuelle Größe des angegebenen globalen Speicher Objekts ab. | [**HEAPSIZE**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) |
| [**Globalunlock**](/windows/desktop/api/WinBase/nf-winbase-globalunlock), [ **localunlock**](/windows/desktop/api/WinBase/nf-winbase-localunlock) | Dekremente die einem Speicher Objekt zugeordnete Sperr Anzahl. Diese Funktion sollte nur mit OLE-und Clipboard-Funktionen verwendet werden, die dies erfordern. | Nicht zutreffend |

## <a name="bad-memory-functions"></a>Ungültige Speicherfunktionen

| Funktion | BESCHREIBUNG |
|-|-|
| [**Badmemorycallbackroutine**](/previous-versions/windows/desktop/legacy/hh691011(v=vs.85)) | Eine Anwendungs definierte Funktion, die bei der [**registerbadmemorynotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) -Funktion registriert wird, die aufgerufen wird, wenn eine oder mehrere fehlerhafte Speicherseiten erkannt werden. |
| [**Getmemoryerrorhandling-Funktionen**](/windows/win32/api/memoryapi/nf-memoryapi-getmemoryerrorhandlingcapabilities) | Ruft die Speicherfehler Behandlungs Funktionen des Systems ab. |
| [**Registerbadmemorynotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) | Registriert eine fehlerhafte Speicher Benachrichtigung, die aufgerufen wird, wenn eine oder mehrere fehlerhafte Speicherseiten erkannt werden. |
| [**Unregisterbadmemorynotification**](/windows/win32/api/memoryapi/nf-memoryapi-unregisterbadmemorynotification) | Schließt das angegebene Benachrichtigungs Handle für ungültige Arbeitsspeicher. |

## <a name="enclave-functions"></a>Enclave-Funktionen

| Funktion | BESCHREIBUNG |
|-|-|
| [**"Kreateenclave"**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave) | Erstellt eine neue nicht initialisierte Enclave. Eine Enclave ist ein isolierter Code Bereich und Daten innerhalb des Adressraums für eine Anwendung. Nur Code, der innerhalb der Enclave ausgeführt wird, kann auf Daten innerhalb desselben Enclave zugreifen. |
| [**Initializeenclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave) | Initialisiert eine Enclave, die Sie erstellt und mit Daten geladen haben. |
| [**Isenvetypesupportiert**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported) | Ruft ab, ob der angegebene Typ von Enclave unterstützt wird. |
| [**Loadenclavedata**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) | Lädt Daten in eine nicht initialisierte Enclave, die Sie durch Aufrufen von [**createenclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)erstellt haben. |

## <a name="atl-thunk-functions"></a>ATL-Thunk-Funktionen

| Funktion | BESCHREIBUNG |
|-|-|
| [**AtlThunk_AllocateData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_allocatedata) | Weist Speicherplatz im Arbeitsspeicher für einen ATL-Thunk zu. |
| [**AtlThunk_DataToCode**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_datatocode) | Gibt eine ausführbare Funktion zurück, die dem AtlThunkData_t-Parameter entspricht. |
| [**AtlThunk_FreeData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_freedata) | Gibt den einem ATL-Thunk zugeordneten Arbeitsspeicher frei. |
| [**AtlThunk_InitData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_initdata) | Initialisiert einen ATL-Thunk. |

## <a name="obsolete-functions"></a>Veraltete Funktionen

Diese Funktionen werden nur für die Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt:

- [**Isbadcodeptr**](/windows/desktop/api/WinBase/nf-winbase-isbadcodeptr)
- [**Isbadumptr**](/windows/desktop/api/WinBase/nf-winbase-isbadreadptr)
- [**Isbadstringptr**](/windows/desktop/api/WinBase/nf-winbase-isbadstringptra)
- [**Isbadschreiteptr**](/windows/desktop/api/WinBase/nf-winbase-isbadwriteptr)

Die folgende Funktion kann falsche Informationen zurückgeben und sollte nicht verwendet werden. Verwenden Sie stattdessen die [**GlobalMemoryStatus usex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) -Funktion.

- [**GlobalMemoryStatus**](/windows/desktop/api/WinBase/nf-winbase-globalmemorystatus)