---
description: Adressfenstererweiterungen (Address Windowing Extensions, AWE) sind eine Reihe von Erweiterungen, die es einer Anwendung ermöglichen, den physischen Speicher schnell zu bearbeiten, der größer als 4 GB ist.
ms.assetid: 48a29922-8130-4540-86b0-0faa120566a6
title: Adressfenstererweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5f0c68e9609834a9065a919d12c23c40521e99ede94feb96889050b6873654
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764410"
---
# <a name="address-windowing-extensions"></a>Adressfenstererweiterungen

Adressfenstererweiterungen (Address Windowing Extensions, AWE) sind eine Reihe von Erweiterungen, die es einer Anwendung ermöglichen, den physischen Speicher schnell zu bearbeiten, der größer als 4 GB ist. Bestimmte datenintensive Anwendungen, z. B. Datenbankverwaltungssysteme und wissenschaftliche und technische Software, benötigen Zugriff auf sehr große Caches von Daten. Bei sehr großen Datensätzen ist es eine schwerwiegende Einschränkung, den Cache so einzuschränken, dass er in den 2 GB des Benutzeradressraums einer Anwendung passt. In diesen Situationen ist der Cache zu klein, um die Anwendung ordnungsgemäß zu unterstützen.

AWE löst dieses Problem, indem Anwendungen große Mengen an Arbeitsspeicher direkt adressieren können, während weiterhin 32-Bit-Zeiger verwendet werden. AWE ermöglicht Anwendungen Datencaches, die größer als 4 GB sind (wenn ausreichend physischer Arbeitsspeicher vorhanden ist). AWE verwendet physischen nicht ausgelagerten Arbeitsspeicher und Fensteransichten verschiedener Teile dieses physischen Speichers innerhalb eines virtuellen 32-Bit-Adressraums.

AWE weist einige Einschränkungen auf, wie dieser Arbeitsspeicher verwendet werden kann. Dies liegt hauptsächlich daran, dass diese Einschränkungen eine extrem schnelle Zuordnung, Neuzuordnung und Freispeicherung ermöglichen. Eine schnelle Speicherverwaltung ist für diese potenziell enormen Adressräume wichtig.

-   Virtuelle Adressbereiche, die für die AWE zugeordnet sind, können nicht mit anderen Prozessen verknüpft (und daher nicht vererbt werden). Tatsächlich dürfen zwei verschiedene virtuelle AWE-Adressen innerhalb desselben Prozesses nicht die gleiche physische Seite zuordnen. Diese Einschränkungen ermöglichen eine schnelle Neuzuordnung und Bereinigung, wenn Arbeitsspeicher freigegeben wird.
-   Die physischen Seiten, die für eine AWE-Region zugeordnet werden können, sind durch die Anzahl der physischen Seiten beschränkt, die auf dem Computer vorhanden sind, da dieser Arbeitsspeicher nie ausgelagerungt wird. Er wird gesperrt, bis die Anwendung ihn explizit frei gibt oder beendet. Die physischen Seiten, die für einen bestimmten Prozess zugeordnet sind, können jeder virtuellen AWE-Region innerhalb desselben Prozesses zugeordnet werden. Anwendungen, die AWE verwenden, müssen darauf achten, dass sie nicht so viel physischen Speicher belegen, dass andere Anwendungen übermäßig seitenen oder die Erstellung neuer Prozesse oder Threads aufgrund fehlender Ressourcen verhindern. Verwenden Sie die [**GlobalMemoryStatusEx-Funktion,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) um die Nutzung des physischen Arbeitsspeichers zu überwachen.
-   Virtuelle AWE-Adressen sind immer lese-/schreibgeschützt und können nicht durch Aufrufe von [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) geschützt werden (d. h. kein schreibgeschützter Speicher, kein Zugriffsspeicher, Schutzseiten usw. können angegeben werden).
-   AWE-Adressbereiche können nicht zum Puffern von Daten für Grafiken oder Videoaufrufe verwendet werden.
-   Ein AWE-Speicherbereich kann weder geteilt noch gelöscht werden. Stattdessen muss der gesamte virtuelle Adressbereich als Einheit gelöscht werden, wenn ein Löschvorgang erforderlich ist. Dies bedeutet, dass Sie **MEM \_ RELEASE** angeben müssen, wenn [**Sie VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree)aufrufen.
-   Anwendungen können mehrere Regionen gleichzeitig zuordnen, sofern sie sich nicht überschneiden.
-   Anwendungen, die AWE verwenden, werden im Emulationsmodus nicht unterstützt. Das heißt, eine x86-Anwendung, die AWE-Funktionen verwendet, muss neu kompiliert werden, um auf einem anderen Prozessor ausgeführt zu werden, während die meisten Anwendungen ohne Neukompilierung unter einem Emulator auf anderen Plattformen ausgeführt werden können.

Diese Lösung behandelt die Probleme mit dem physischen Speicher auf sehr allgemeine und allgemein anwendbare Weise. Einige der Vorteile von AWE sind:

-   Eine kleine Gruppe neuer Funktionen wird definiert, um den AWE-Speicher zu bearbeiten.
-   AWE bietet eine sehr schnelle Neuzuordnungsfunktion. Die Neuzuordnung erfolgt durch Bearbeiten virtueller Speichertabellen, nicht durch Verschieben von Daten in den physischen Speicher.
-   AWE bietet eine für den Prozessor geeignete Granularität der Seitengröße (z. B. 4 KB bei x86), was für Anwendungen nützlicher ist als für große Seiten (z. B. 2 MB oder 4 MB auf x86).

Eine Anwendung muss über die Berechtigung Seiten im Arbeitsspeicher sperren verfügen, um AWE verwenden zu können. Um diese Berechtigung zu erhalten, muss ein Administrator den **Benutzerberechtigungszuweisungen** des Benutzers **Sperrenseiten im Arbeitsspeicher** hinzufügen. Weitere Informationen hierzu finden Sie unter "Benutzerrechte" in der Betriebssystemhilfe.

Die folgenden Funktionen bilden die AWE-API (Address Windowing Extensions).



| Funktion                                                                          | Beschreibung                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) und [ **VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Reservieren Sie einen Teil des virtuellen Adressraums für AWE mithilfe **von MEM \_ PHYSICAL**.                                                                                                                                                                       |
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)                    | Zuordnen von physischem Speicher für die Verwendung mit AWE.                                                                                                                                                                                                                |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)                              | Ordnen Sie virtuelle AWE-Adressen einer beliebigen Gruppe physischer Seiten zu, die mit [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)abgerufen werden, oder erklären Sie sie für ungültig.                                                                                                    |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter)                | Ordnen Sie virtuelle AWE-Adressen einer beliebigen Gruppe physischer Seiten zu, die mit [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)abgerufen wurden, aber mit einer feineren Steuerung als die von [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)bereitgestellte . |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages)                            | Freier physischer Arbeitsspeicher, der für AWE verwendet wurde.                                                                                                                                                                                                               |



 

 

 
