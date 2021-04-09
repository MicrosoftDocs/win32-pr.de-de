---
description: Bei Address windowingextensions (AWE) handelt es sich um einen Satz von Erweiterungen, mit denen eine Anwendung den physischen Speicher, der größer als 4 GB ist, schnell bearbeiten kann
ms.assetid: 48a29922-8130-4540-86b0-0faa120566a6
title: Address windowingextensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cb311bf9ecef2de334018ca3f9982a31f0b072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864867"
---
# <a name="address-windowing-extensions"></a>Address windowingextensions

Bei Address windowingextensions (AWE) handelt es sich um einen Satz von Erweiterungen, mit denen eine Anwendung den physischen Speicher, der größer als 4 GB ist, schnell bearbeiten kann Bestimmte datenintensive Anwendungen, wie z. b. Datenbankverwaltungssysteme und wissenschaftliche und technische Software, benötigen Zugriff auf sehr große Daten Caches. Im Fall von sehr großen Datasets ist das Einschränken des Caches auf den Zeitraum von 2 GB des Benutzer Adressraums einer Anwendung eine schwerwiegende Einschränkung. In diesen Fällen ist der Cache zu klein, um die Anwendung ordnungsgemäß zu unterstützen.

AWE löst dieses Problem, indem es Anwendungen ermöglicht, große Mengen an Arbeitsspeicher direkt zu adressieren und dabei weiterhin 32-Bit-Zeiger zu verwenden. AWE ermöglicht es Anwendungen, Daten Caches mit einer Größe von mehr als 4 GB zu haben (wobei ausreichend physischer Arbeitsspeicher vorhanden ist). AWE verwendet physische nicht auslagerbare Speicher-und Fenster Sichten verschiedener Teile dieses physischen Speichers innerhalb eines virtuellen 32-Bit-Adressraums.

AWE weist einige Einschränkungen hinsichtlich der Verwendung dieses Arbeitsspeichers auf, primär weil diese Einschränkungen eine extrem schnelle Zuordnung, Neuzuordnung und Freigabe ermöglichen. Die schnelle Speicherverwaltung ist für diese potenziell riesigen Adressräume von Bedeutung.

-   Virtuelle Adressbereiche, die für AWE reserviert sind, können nicht mit anderen Prozessen verwendet werden (und sind daher nicht vererbbar). Tatsächlich sind zwei verschiedene virtuelle AWE-Adressen innerhalb desselben Prozesses nicht berechtigt, dieselbe physische Seite zuzuordnen. Diese Einschränkungen ermöglichen eine schnelle Neuzuordnung und Bereinigung, wenn der Arbeitsspeicher freigegeben wird.
-   Die physischen Seiten, die für eine AWE-Region zugeordnet werden können, werden durch die Anzahl der auf dem Computer vorhandenen physischen Seiten beschränkt, da dieser Arbeitsspeicher nie ausgelagert wird – er wird gesperrt, bis die Anwendung ihn explizit freigibt oder beendet. Die physischen Seiten, die für einen bestimmten Prozess reserviert werden, können in einer beliebigen virtuellen AWE-Region innerhalb desselben Prozesses zugeordnet werden. Anwendungen, die AWE verwenden, müssen darauf achten, dass Sie nicht so viel physischen Arbeitsspeicher beanspruchen, weil Sie dazu führen, dass andere Anwendungen übermäßig viel oder weniger Ressourcen erstellt werden. Verwenden Sie die [**GlobalMemoryStatus usex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) -Funktion, um die Verwendung des physischen Speichers zu überwachen.
-   Virtuelle AWE-Adressen sind immer Lese-/Schreibzugriff und können nicht über Aufrufe von [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) geschützt werden (d. h. kein Schreib geschützter Speicher, NoAccess-Speicher, Wächter Seiten und die like-Angabe).
-   AWE-Adressbereiche können nicht verwendet werden, um Daten für Grafiken oder Videoaufrufe zu puffern.
-   Ein AWE-Speicherbereich kann nicht aufgeteilt werden und kann auch nicht gelöscht werden. Stattdessen muss der gesamte virtuelle Adressbereich als Einheit gelöscht werden, wenn ein Löschvorgang erforderlich ist. Dies bedeutet, dass Sie beim Aufrufen von [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree)eine Arbeitsspeicher **\_ Freigabe** angeben müssen.
-   Anwendungen können mehrere Regionen gleichzeitig zuordnen, sofern Sie sich nicht überlappen.
-   Anwendungen, die AWE verwenden, werden im Emulations Modus nicht unterstützt. Das heißt, eine x86-Anwendung, die AWE-Funktionen verwendet, muss neu kompiliert werden, damit Sie auf einem anderen Prozessor ausgeführt werden kann, während die meisten Anwendungen ohne erneute Kompilierung auf anderen Plattformen ausgeführt werden können.

Diese Lösung behandelt die Probleme mit dem physischen Speicher auf sehr allgemeine, weit verbreitete Weise. Zu den Vorteilen von AWE gehören:

-   Eine kleine Gruppe neuer Funktionen wird definiert, um AWE-Speicher zu bearbeiten.
-   AWE bietet eine sehr schnelle Neuzuordnung. Die Neuzuordnung erfolgt durch die Bearbeitung von virtuellen Arbeitsspeicher Tabellen, nicht durch das Verschieben von Daten im physischen Speicher.
-   AWE bietet eine für den Prozessor geeignete Granularität der Seitengröße (z. b. 4 KB auf x86), was für Anwendungen nützlicher ist als bei großen Seiten (z. b. 2 MB oder 4 MB auf x86).

Eine Anwendung muss über die Berechtigung Sperren von Seiten im Speicher verfügen, um AWE zu verwenden. Um diese Berechtigung zu erhalten, muss ein Administrator den **Benutzerrechten Zuweisungen** des Benutzers **Sperr Seiten im Arbeitsspeicher** hinzufügen. Weitere Informationen hierzu finden Sie unter "Benutzerrechte" in der Hilfe zum Betriebssystem.

Die folgenden Funktionen bilden die AWE-API (Address windowingextensions).



| Funktion                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Virtualzuweisung**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) und [ **virtualzuweisung**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Reservieren Sie einen Teil des virtuellen Adressraums, der für AWE verwendet werden soll, mithilfe von **\_ physischem** Arbeitsspeicher.                                                                                                                                                                       |
| [**"Zuordnung"**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)                    | Zuordnen von physischem Speicher für die Verwendung mit AWE.                                                                                                                                                                                                                |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)                              | Ordnen Sie virtuellen AWE-Adressen auf jedem Satz physischer Seiten zu, die mit "" [**zugeordnet**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)werden.                                                                                                    |
| [**Mapuserphysicalpagesscatcher**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter)                | Ordnen Sie virtuelle AWE-Adressen auf jedem Satz physischer Seiten zu, die mit "" [**zugeordnet**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)werden, und zwar mit einer feineren Kontrolle als die von [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)bereitgestellte. |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages)                            | Freier physischer Speicher, der für AWE verwendet wurde.                                                                                                                                                                                                               |



 

 

 
