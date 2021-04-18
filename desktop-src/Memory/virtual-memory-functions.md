---
description: Mit den Funktionen des virtuellen Arbeitsspeichers kann ein Prozess den Status von Seiten im virtuellen Adressraum bearbeiten oder ermitteln.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Funktionen des virtuellen Arbeitsspeichers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76866fd10dac01315622e8a4faef7bea436a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347231"
---
# <a name="virtual-memory-functions"></a>Funktionen des virtuellen Arbeitsspeichers

Mit den Funktionen des virtuellen Arbeitsspeichers kann ein Prozess den Status von Seiten im virtuellen Adressraum bearbeiten oder ermitteln. Sie können die folgenden Vorgänge ausführen:

-   Reservieren Sie einen Bereich des virtuellen Adressraums eines Prozesses. Durch das Reservieren des Adressraums wird kein physischer Speicher zugeordnet, aber es wird verhindert, dass andere Zuordnungs Vorgänge den angegebenen Bereich verwenden. Dies hat keine Auswirkung auf die virtuellen Adressräume anderer Prozesse. Das Reservieren von Seiten verhindert den unnötigen Verbrauch von physischem Speicher, während ein Prozess einen Bereich des Adressraums reservieren kann, in den eine dynamische Datenstruktur vergrößert werden kann. Der Prozess kann bei Bedarf physischen Speicher für diesen Speicherplatz zuweisen.
-   Commit für einen Bereich von reservierten Seiten im virtuellen Adressraum eines Prozesses, sodass physischer Speicher (entweder im RAM oder auf dem Datenträger) nur für den Zuweisungs Prozess zugänglich ist.
-   Geben Sie Lese-/Schreibzugriff, schreibgeschützt oder keinen Zugriff für einen Bereich von zugegebenen Seiten an. Dies unterscheidet sich von den Standard Zuordnungs Funktionen, die immer Seiten mit Lese-/Schreibzugriff zuordnen.
-   Freigeben eines Bereichs von reservierten Seiten, sodass der Bereich der virtuellen Adressen für nachfolgende Zuordnungs Vorgänge durch den aufrufenden Prozess verfügbar ist.
-   Debuggen Sie einen Bereich von ausgeführtem Commit, um den physischen Speicher freizugeben und ihn für die nachfolgende Zuordnung durch jeden Prozess verfügbar zu gestalten.
-   Sperren Sie eine oder mehrere Seiten mit zugesteuertem Speicher in den physischen Speicher (RAM), damit das System die Seiten nicht in die Auslagerungs Datei austauschen kann.
-   Abrufen von Informationen zu einem Bereich von Seiten im virtuellen Adressraum des aufrufenden Prozesses oder eines angegebenen Prozesses.
-   Ändern des Zugriffs Schutzes für einen angegebenen Bereich von zugegebenen Seiten im virtuellen Adressraum des aufrufenden Prozesses oder eines angegebenen Prozesses.

Weitere Informationen finden Sie in den nachfolgenden Themen.

-   [Zuordnen des virtuellen Speichers](allocating-virtual-memory.md)
-   [Vergleichen von Speicher Belegungs Methoden](comparing-memory-allocation-methods.md)
-   [Freigeben von virtuellem Speicher](freeing-virtual-memory.md)
-   [Arbeiten mit Seiten](working-with-pages.md)
-   [Speicherverwaltungsfunktionen](memory-management-functions.md)

 

 



