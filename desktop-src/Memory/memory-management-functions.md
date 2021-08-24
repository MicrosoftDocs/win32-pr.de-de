---
description: 'In diesem Thema werden die Speicherverwaltungsfunktionen beschrieben:'
ms.assetid: 5a2a7a62-0bda-4a0d-93d2-25b4898871fd
title: Speicherverwaltungsfunktionen
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: 635fa59b6a5b6a549438d8bfed71781d6d9e6fa6a9d2c12524684ded28a0f3df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822190"
---
# <a name="memory-management-functions"></a>Speicherverwaltungsfunktionen

- [Allgemeine Arbeitsspeicherfunktionen](#general-memory-functions)
- [Funktionen zur Verhinderung der Datenausführung](#data-execution-prevention-functions)
- [Dateizuordnungsfunktionen](#file-mapping-functions)
- [AWE-Funktionen](#awe-functions)
- [Heapfunktionen](#heap-functions)
- [Funktionen des virtuellen Arbeitsspeichers](#virtual-memory-functions)
- [Globale und lokale Funktionen](#global-and-local-functions)
- [Funktionen für ungültigen Arbeitsspeicher](#bad-memory-functions)
- [Enclave-Funktionen](#enclave-functions)
- [ATL-Thunkfunktionen](#atl-thunk-functions)
- [Veraltete Funktionen](#obsolete-functions)

## <a name="general-memory-functions"></a>Allgemeine Arbeitsspeicherfunktionen

| Funktion | BESCHREIBUNG |
|-|-|
| [**AddSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) | Registriert eine Rückruffunktion, die aufgerufen wird, wenn ein geschützter Speicherbereich freigegeben oder dessen Schutz geändert wird. |
| [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) | Kopiert einen Speicherblock von einem Speicherort an einen anderen. |
| [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) | Erstellt ein Speicherressourcen-Benachrichtigungsobjekt. |
| [**FillMemory**](/previous-versions/windows/desktop/legacy/aa366561(v=vs.85)) | Füllt einen Speicherblock mit einem angegebenen Wert aus. |
| [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) | Ruft die Mindestgröße einer großen Seite ab. |
| [**GetPhysicallyInstalledSystemMemory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getphysicallyinstalledsystemmemory) | Ruft den Arbeitsspeicher ab, der physisch auf dem Computer installiert ist. |
| [**GetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-getsystemfilecachesize) | Ruft die aktuellen Größenbeschränkungen für den Arbeitssatz des Systemcaches ab. |
| [**GetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-getwritewatch) | Ruft die Adressen der Seiten ab, in die in einem Bereich des virtuellen Arbeitsspeichers geschrieben wurde. |
| [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) | Ruft Informationen zur aktuellen Nutzung des physischen und virtuellen Speichers durch das System ab. |
| [**MoveMemory**](/previous-versions/windows/desktop/legacy/aa366788(v=vs.85)) | Verschiebt einen Speicherblock von einem Speicherort an einen anderen. |
| [**QueryMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-querymemoryresourcenotification) | Ruft den Zustand des angegebenen Speicherressourcenobjekts ab. |
| [**RemoveSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-removesecurememorycachecallback) | Aufheben der Registrierung einer Rückruffunktion, die zuvor mit der [**AddSecureMemoryCacheCallback-Funktion**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) registriert wurde. |
| [**ResetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-resetwritewatch) | Setzt den Zustand der Schreibnachverfolgung für einen Bereich des virtuellen Arbeitsspeichers zurück. |
| [**SecureMemoryCacheCallback**](/windows/desktop/api/WinNT/nc-winnt-psecure_memory_cache_callback) | Eine anwendungsdefinierte Funktion, die aufgerufen wird, wenn ein geschützter Speicherbereich freigegeben oder deren Schutz geändert wird. |
| [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) | Füllt einen Speicherblock mit Nullen aus. |
| [**SetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-setsystemfilecachesize) | Schränkt die Größe des Arbeitssatzes für den Dateisystemcache ein. |
| [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) | Füllt einen Speicherblock mit Nullen aus. |

## <a name="data-execution-prevention-functions"></a>Funktionen zur Verhinderung der Datenausführung

Diese Funktionen werden mit [datenausführungsverhinderung (Data Execution Prevention,](data-execution-prevention.md) DEP) verwendet.

| Funktion | BESCHREIBUNG |
|-|-|
| [**GetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getprocessdeppolicy) | Ruft DEP-Einstellungen für einen Prozess ab. |
| [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) | Ruft DIE DEP-Einstellungen für das System ab. |
| [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) | Ändert die DEP-Einstellungen für einen Prozess. |

## <a name="file-mapping-functions"></a>Dateizuordnungsfunktionen

Diese Funktionen werden in der [Dateizuordnung](file-mapping.md)verwendet.

| Funktion | BESCHREIBUNG |
|-|-|
| [**CreateFileMappingA**](/windows/win32/api/winbase/nf-winbase-createfilemappinga) | Erstellt oder öffnet ein benanntes oder unbenanntes Dateizuordnungsobjekt für eine angegebene Datei. |
| [**CreateFileMappingW**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingw) | Erstellt oder öffnet ein benanntes oder unbenanntes Dateizuordnungsobjekt für eine angegebene Datei. |
| [**CreateFileMapping2**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemapping2) | Erstellt oder öffnet ein benanntes oder unbenanntes Dateizuordnungsobjekt für eine angegebene Datei. Sie können einen bevorzugten NUMA-Knoten für den physischen Speicher als erweiterten Parameter angeben. weitere Informationen finden Sie unter dem *Parameter ExtendedParameters.* |
| [**CreateFileMappingFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-createfilemappingfromapp) | Erstellt oder öffnet ein benanntes oder unbenanntes Dateizuordnungsobjekt für eine angegebene Datei aus einer Windows Store-App. |
| [**CreateFileMappingNuma**](/windows/desktop/api/WinBase/nf-winbase-createfilemappingnumaa) | Erstellt oder öffnet ein benanntes oder unbenanntes Dateizuordnungsobjekt für eine angegebene Datei und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) | Schreibt einen Bytebereich innerhalb einer zugeordneten Ansicht einer Datei auf den Datenträger. |
| [**GetMappedFileName**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) | Überprüft, ob sich die angegebene Adresse innerhalb einer Speicherzuordnungsdatei im Adressraum des angegebenen Prozesses befindet. Wenn ja, gibt die Funktion den Namen der speicherzuordnungsbasierten Datei zurück. |
| [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) | Karten eine Ansicht einer Dateizuordnung in den Adressraum eines aufrufenden Prozesses. |
| [**MapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile2) | Karten eine Ansicht einer Datei oder eines seitendateibasierten Abschnitts in den Adressraum des angegebenen Prozesses ein. |
| [**MapViewOfFile3**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3) | Karten eine Ansicht einer Datei oder eines seitendateibasierten Abschnitts in den Adressraum des angegebenen Prozesses ein. |
| [**MapViewOfFile3FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3fromapp) | Karten eine Ansicht einer Dateizuordnung im Adressraum eines aufrufenden Prozesses aus einer Windows Store-App. |
| [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) | Karten eine Ansicht einer Dateizuordnung in den Adressraum eines aufrufenden Prozesses. Ein Aufrufer kann optional eine vorgeschlagene Speicheradresse für die Ansicht angeben. |
| [**MapViewOfFileExNuma**](/windows/desktop/api/WinBase/nf-winbase-mapviewoffileexnuma) | Karten eine Ansicht einer Dateizuordnung im Adressraum eines aufrufenden Prozesses und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**MapViewOfFileFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffilefromapp) | Karten eine Ansicht einer Dateizuordnung im Adressraum eines aufrufenden Prozesses aus einer Windows Store-App. |
| [**MapViewOfFileNuma2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffilenuma2) | Karten eine Ansicht einer Datei oder eines seitendateibasierten Abschnitts in den Adressraum des angegebenen Prozesses ein. |
| [**OpenFileMapping**](/windows/win32/api/winbase/nf-winbase-openfilemappinga) | Öffnet ein benanntes Dateizuordnungsobjekt. |
| [**OpenFileMappingFromApp**](/windows/win32/api/winbase/nf-winbase-openfilemappingafromapp) | Öffnet ein benanntes Dateizuordnungsobjekt. |
| [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) | Entfernt die Zuordnung einer zugeordneten Ansicht einer Datei zum Adressraum des aufrufenden Prozesses. |
| [**UnmapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile2) | Entzuordnung einer zuvor zugeordneten Ansicht einer Datei oder eines aus einer Auslagerungsdatei unterstützten Abschnitts. |
| [**UnmapViewOfFileEx**](/windows/desktop/api/MemoryApi/nf-memoryapi-unmapviewoffileex) | Entzuordnung einer zuvor zugeordneten Ansicht einer Datei oder eines aus einer Auslagerungsdatei unterstützten Abschnitts. |

## <a name="awe-functions"></a>AWE-Funktionen

Dies sind die [AWE-Funktionen.](address-windowing-extensions.md)

| Funktion | BESCHREIBUNG |
|-|-|
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages) | Ordnet physische Speicherseiten zu, die innerhalb einer beliebigen AWE-Region des Prozesses zugeordnet und nicht zugeordnet werden sollen. |
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma) | Ordnet physische Speicherseiten zu, die innerhalb eines beliebigen AWE-Prozesses zugeordnet und nicht zugeordnet werden sollen, und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages) | Gibt physische Speicherseiten frei, die zuvor mit [**AllocateUserPhysicalPages zugeordnet wurden.**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages) |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages) | Karten zuvor physische Speicherseiten an der angegebenen Adresse innerhalb einer AWE-Region zugeordnet haben. |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter) | Karten zuvor physische Speicherseiten an der angegebenen Adresse innerhalb einer AWE-Region zugeordnet haben. |

## <a name="heap-functions"></a>Heapfunktionen

Dies sind [die Heapfunktionen](heap-functions.md).

| Funktion | BESCHREIBUNG |
|-|-|
| [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) | Ruft ein Handle für den Heap des aufrufenden Prozesses ab. |
| [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) | Ruft Handles für alle Heaps ab, die für den aufrufenden Prozess gültig sind. |
| [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) | Ordnet einen Speicherblock aus einem Heap zu. |
| [**HeapCompact**](/windows/desktop/api/HeapApi/nf-heapapi-heapcompact) | Verknappt angrenzende freie Speicherblöcke auf einem Heap. |
| [**HeapErzeugen**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) | Erstellt ein Heapobjekt. |
| [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) | Zerstört das angegebene Heapobjekt. |
| [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) | Gibt einen Speicherblock frei, der einem Heap zugeordnet ist. |
| [**HeapLock**](/windows/desktop/api/HeapApi/nf-heapapi-heaplock) | Versucht, die einem angegebenen Heap zugeordnete Sperre zu erhalten. |
| [**HeapQueryInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapqueryinformation) | Ruft Informationen zum angegebenen Heap ab. |
| [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) | Neuverlegung eines Speicherblocks aus einem Heap. |
| [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) | Legt Heapinformationen für den angegebenen Heap fest. |
| [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) | Ruft die Größe eines Speicherblocks ab, der aus einem Heap zugeordnet ist. |
| [**HeapUnlock**](/windows/desktop/api/HeapApi/nf-heapapi-heapunlock) | Gibt den Besitz der Sperre frei, die einem angegebenen Heap zugeordnet ist. |
| [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) | Versucht, einen angegebenen Heap zu überprüfen. |
| [**HeapWalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) | Enumeriert die Speicherblöcke in einem angegebenen Heap. |

## <a name="virtual-memory-functions"></a>Funktionen des virtuellen Arbeitsspeichers

Dies sind die [virtuellen Speicherfunktionen](virtual-memory-functions.md).

| Funktion | BESCHREIBUNG |
|-|-|
| [**DiscardVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-discardvirtualmemory) | Verwirft den Arbeitsspeicherinhalt eines Bereichs von Speicherseiten, ohne den Arbeitsspeicher zu dekomprimieren. Der Inhalt des verworfenen Arbeitsspeichers ist nicht definiert und muss von der Anwendung neu geschrieben werden. |
| [**OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory) | Gibt an, dass die in einem Bereich von Speicherseiten enthaltenen Daten von der Anwendung nicht mehr benötigt werden und bei Bedarf vom System verworfen werden können. |
| [**PrefetchVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-prefetchvirtualmemory) | Vorabruft virtuelle Adressbereiche in physischen Speicher. |
| [**QueryVirtualMemoryInformation**](/windows/desktop/api/MemoryApi/nf-memoryapi-queryvirtualmemoryinformation) | Gibt Informationen zu einer Seite oder einer Gruppe von Seiten innerhalb des virtuellen Adressraums des angegebenen Prozesses zurück. |
| [**ReclaimVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-reclaimvirtualmemory) | Gibt einen Bereich von Speicherseiten zurück, die dem System mit [**OfferVirtualMemory angeboten wurden.**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory) |
| [**SetProcessValidCallTargets**](/windows/desktop/api/MemoryApi/nf-memoryapi-setprocessvalidcalltargets) | Stellt CFG eine Liste gültiger indirekter Aufrufziele zur Folge und gibt an, ob sie als gültig markiert werden sollen. |
| [**Virtualalloc**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc) | Reserviert oder committ einen Bereich von Seiten im virtuellen Adressraum des aufrufenden Prozesses. |
| [**VirtualAlloc2**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc2) | Reserviert, committ oder ändert den Zustand eines Speicherbereichs innerhalb des virtuellen Adressraums eines angegebenen Prozesses. Die Funktion initialisiert den Arbeitsspeicher, den sie 0 (null) zuteilen. |
| [**VirtualAlloc2FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Reserviert, committ oder ändert den Zustand eines Seitenbereichs im virtuellen Adressraum des aufrufenden Prozesses. Der von dieser Funktion zugeordnete Arbeitsspeicher wird automatisch mit 0 initialisiert. |
| [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Reserviert einen Bereich von Seiten im virtuellen Adressraum des angegebenen Prozesses oder committ diesen. |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) | Reserviert einen Speicherbereich innerhalb des virtuellen Adressraums des angegebenen Prozesses oder führt einen Commit aus und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**VirtualAllocFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Reserviert, committ oder ändert den Zustand eines Seitenbereichs im virtuellen Adressraum des aufrufenden Prozesses. Der von dieser Funktion zugeordnete Arbeitsspeicher wird automatisch mit 0 initialisiert. |
| [**Virtualfree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) | Gibt einen Bereich von Seiten innerhalb des virtuellen Adressraums des aufrufenden Prozesses frei oder dekomprimiert diesen. |
| [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) | Gibt einen Speicherbereich innerhalb des virtuellen Adressraums eines angegebenen Prozesses frei oder dekomprimiert diesen. |
| [**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) | Sperrt den angegebenen Bereich des virtuellen Adressraums des Prozesses im physischen Speicher. |
| [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) | Ändert den Zugriffsschutz für einen Bereich von Seiten, für die ein Committed ausgeführt wurde, im virtuellen Adressraum des aufrufenden Prozesses. |
| [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) | Ändert den Zugriffsschutz für einen Bereich von Seiten, für die ein Committed ausgeführt wurde, im virtuellen Adressraum des aufrufenden Prozesses. |
| [**VirtualProtectFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualprotectfromapp) | Ändert den Schutz für einen Bereich von Seiten, für die ein Committed ausgeführt wurde, im virtuellen Adressraum des aufrufenden Prozesses. |
| [**Virtualquery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) | Stellt Informationen zu einem Seitenbereich im virtuellen Adressraum des aufrufenden Prozesses bereit. |
| [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) | Stellt Informationen zu einem Seitenbereich im virtuellen Adressraum des aufrufenden Prozesses bereit. |
| [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) | Entsperrt einen angegebenen Seitenbereich im virtuellen Adressraum eines Prozesses. |

## <a name="global-and-local-functions"></a>Globale und lokale Funktionen

Siehe auch [globale und lokale Funktionen.](global-and-local-functions.md) Diese Funktionen werden aus Gründen der Kompatibilität mit 16-Bit-Windows bereitgestellt und mit dynamische Daten Exchange (DDE), den Zwischenablagefunktionen und OLE-Datenobjekten verwendet. Sofern in der Dokumentation nicht ausdrücklich angegeben ist, dass eine globale oder lokale Funktion verwendet werden soll, sollten neue Anwendungen die entsprechende [Heapfunktion](heap-functions.md) mit dem von [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap)zurückgegebenen Handle verwenden. Legen Sie für die entsprechende Funktionalität der globalen oder lokalen Funktion den *dwFlags-Parameter* der Heapfunktion auf 0 fest.

| Funktion | BESCHREIBUNG | Entsprechende Heapfunktion |
|-|-|-|
| [**GlobalAlloc,**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) [ **LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) | Ordnet die angegebene Anzahl von Bytes aus dem Heap zu. | [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) |
| [**GlobalDiscard,**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) [ **LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) | Verwirft den angegebenen globalen Speicherblock. | Nicht zutreffend |
| [**GlobalFlags,**](/windows/desktop/api/WinBase/nf-winbase-globalflags) [ **LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) | Gibt Informationen zum angegebenen globalen Speicherobjekt zurück. | Nicht zutreffend Verwenden Sie [**HeapValidate,**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) um den Heap zu überprüfen. |
| [**GlobalFree,**](/windows/desktop/api/WinBase/nf-winbase-globalfree) [ **LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) | Gibt das angegebene globale Speicherobjekt frei. | [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) |
| [**GlobalHandle,**](/windows/desktop/api/WinBase/nf-winbase-globalhandle) [ **LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) | Ruft das Handle ab, das dem angegebenen Zeiger auf einen globalen Speicherblock zugeordnet ist. Diese Funktion sollte nur mit OLE- und Zwischenablagefunktionen verwendet werden, die sie benötigen. | Nicht zutreffend |
| [**GlobalLock,**](/windows/desktop/api/WinBase/nf-winbase-globallock) [ **LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) | Sperrt ein globales Speicherobjekt und gibt einen Zeiger auf das erste Byte des Speicherblocks des Objekts zurück. | Nicht zutreffend |
| [**GlobalReAlloc,**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc) [ **LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) | Ändert die Größe oder die Attribute eines angegebenen globalen Speicherobjekts. | [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) |
| [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize), [ **LocalSize**](/windows/desktop/api/WinBase/nf-winbase-localsize) | Ruft die aktuelle Größe des angegebenen globalen Speicherobjekts ab. | [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) |
| [**GlobalUnlock,**](/windows/desktop/api/WinBase/nf-winbase-globalunlock) [ **LocalUnlock**](/windows/desktop/api/WinBase/nf-winbase-localunlock) | Dekrementierung der einem Speicherobjekt zugeordneten Sperrenanzahl. Diese Funktion sollte nur mit OLE- und Zwischenablagefunktionen verwendet werden, die sie benötigen. | Nicht zutreffend |

## <a name="bad-memory-functions"></a>Funktionen für ungültigen Arbeitsspeicher

| Funktion | BESCHREIBUNG |
|-|-|
| [**BadMemoryCallbackRoutine**](/previous-versions/windows/desktop/legacy/hh691011(v=vs.85)) | Eine anwendungsdefinierte Funktion, die bei der [**RegisterBadMemoryNotification-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) registriert ist und aufgerufen wird, wenn eine oder mehrere Fehlerhafte Speicherseiten erkannt werden. |
| [**GetMemoryErrorHandlingCapabilities**](/windows/win32/api/memoryapi/nf-memoryapi-getmemoryerrorhandlingcapabilities) | Ruft die Speicherfehlerbehandlungsfunktionen des Systems ab. |
| [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) | Registriert eine Benachrichtigung über fehlerhaften Arbeitsspeicher, die aufgerufen wird, wenn eine oder mehrere Seiten mit fehlerhaftem Speicher erkannt werden. |
| [**UnregisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-unregisterbadmemorynotification) | Schließt das angegebene Benachrichtigungshandle für ungültigen Arbeitsspeicher. |

## <a name="enclave-functions"></a>Enclave-Funktionen

| Funktion | BESCHREIBUNG |
|-|-|
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave) | Erstellt eine neue nicht initialisierte Enclave. Eine Enclave ist eine isolierte Code- und Datenregion innerhalb des Adressraums für eine Anwendung. Nur Code, der innerhalb der Enclave ausgeführt wird, kann auf Daten innerhalb derselben Enclave zugreifen. |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave) | Initialisiert eine Enclave, die Sie erstellt und mit Daten geladen haben. |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported) | Ruft ab, ob der angegebene Enclave-Typ unterstützt wird. |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) | Lädt Daten in eine nicht initialisierte Enclave, die Sie durch Aufrufen von [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)erstellt haben. |

## <a name="atl-thunk-functions"></a>ATL-Thunkfunktionen

| Funktion | BESCHREIBUNG |
|-|-|
| [**AtlThunk_AllocateData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_allocatedata) | Belegt Speicherplatz im Arbeitsspeicher für einen ATL-Thunk. |
| [**AtlThunk_DataToCode**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_datatocode) | Gibt eine ausführbare Funktion zurück, die dem AtlThunkData_t Parameter entspricht. |
| [**AtlThunk_FreeData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_freedata) | Gibt Arbeitsspeicher frei, der einem ATL-Thunk zugeordnet ist. |
| [**AtlThunk_InitData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_initdata) | Initialisiert einen ATL-Thunk. |

## <a name="obsolete-functions"></a>Veraltete Funktionen

Diese Funktionen werden nur für die Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt:

- [**IsBadCodePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadcodeptr)
- [**IsBadReadPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadreadptr)
- [**IsBadStringPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadstringptra)
- [**IsBadWritePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadwriteptr)

Die folgende Funktion kann falsche Informationen zurückgeben und sollte nicht verwendet werden. Verwenden Sie stattdessen die [**GlobalMemoryStatusEx-Funktion.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex)

- [**GlobalMemoryStatus**](/windows/desktop/api/WinBase/nf-winbase-globalmemorystatus)