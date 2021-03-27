---
description: Dieses Thema enthält eine Schritt-für-Schritt-Untersuchung der Anforderungen zum Erstellen einer DLL-Datei, die einen Handler implementiert, der mit dem Synchronisierungs Center verwendet werden soll. Diese Informationen gelten ab Windows Vista.
title: Entwickeln eines Windows Sync Center-Handlers
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 66b40f81-9515-4190-8ced-44f20bb9df86
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11185aa5976c27b7af95787b081e1eaacd99c8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979800"
---
# <a name="developing-a-windows-sync-center-handler"></a>Entwickeln eines Windows Sync Center-Handlers

Dieses Thema enthält eine Schritt-für-Schritt-Untersuchung der Anforderungen zum Erstellen einer DLL-Datei, die einen Handler implementiert, der mit dem Synchronisierungs Center verwendet werden soll. Diese Informationen gelten ab Windows Vista.

-   [Windows-Synchronisierungs Darstellung vor Vista](#the-windows-synchronization-experience-before-vista)
-   [Sync Center-APIs](#sync-center-apis)
    -   [Wichtige Schnittstellen](#essential-interfaces)

## <a name="the-windows-synchronization-experience-before-vista"></a>Windows-Synchronisierungs Darstellung vor Vista

In Windows XP wurde ein [Synchronisierungs-Manager](syncmgr-start-page.md) (mobsync.exe) bereitgestellt. Viele Geräte, wie z. b. MP3-Player, Mobiltelefone und Kameras, haben auch Ihre eigenen Synchronisierungs Schnittstellen und nicht den Synchronisierungs-Manager bereitgestellt. Dies führte zu einer inkonsistenten und nicht zentralisierten Benutzer Darstellung.

Das neue Feature Sync Center in Windows Vista hat gegenüber dem älteren Synchronisierungs-Manager mehrere Vorteile.

-   Bessere Auffindbarkeit
-   Weniger Anforderungen an direkte Benutzeraktionen
-   Andere Vorgänge werden von nicht blockiert.
-   Bessere Visualisierung des Synchronisierungs Status
-   Besseres Verständnis des Entwicklungsmodells

## <a name="sync-center-apis"></a>Sync Center-APIs

Das Synchronisierungs Center kommuniziert mit Handlern über eine Reihe von Component Object Model (com)-Schnittstellen. Nicht alle diese Schnittstellen sind erforderlich, um einen Synchronisierungs Center-Handler zu implementieren. Dieses Thema wurde in zwei Abschnitte unterteilt. Im ersten Abschnitt werden die wesentlichen com-Schnittstellen erläutert, die von jedem Handler unterstützt werden müssen. im zweiten Abschnitt werden die optionalen com-Schnittstellen untersucht und die Gründe für die Unterstützung durch einen Handler erläutert.

-   [Wichtige Schnittstellen](#essential-interfaces)

### <a name="essential-interfaces"></a>Wichtige Schnittstellen

Alle Synchronisierungs Center-Handler müssen die folgenden Schnittstellen unterstützen:

-   [**Isyncmgrhandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler)
-   [**Isyncmgrhandlerinfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo)
-   [**Isyncmgrsyncitemcontainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer)
-   [**Ienumsyncmgrsyncitems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems)
-   [**Isyncmgrsyncitem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem)
-   [**Isyncmgrsynciteminfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo)

[**Isyncmgrsyncitem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) und [**isyncmgrsynciteminfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) werden verwendet, um ein einzelnes Synchronisierungs Element zu beschreiben, das bei der Synchronisierung mit dem Synchronisierungs Center beteiligt ist. Ein Synchronisierungs Element stellt in der Regel entweder einen bestimmten Datentyp (z. b. Bilder) oder eine bestimmte Position der Daten dar.

Synchronisierungs Elemente, die unterschiedliche Datenspeicher Orte darstellen, ermöglichen sehr spezifische Synchronisierung. Die Granularität der Position liegt beim Autor des Handlers, aber es sollte darauf geachtet werden, dass der Entwurf berücksichtigt wird. Wenn zu wenig Synchronisierungs Elemente (Speicherorte) vorhanden sind, ist der Benutzer nicht in der Lage, nur bestimmte Daten zu synchronisieren. Im anderen Extremfall kann eine zu hohe Granularität nicht mehr verwaltet werden.

Wenn ein Handler mehr als einen Datentyp oder mehrere Datenspeicher Orte unterstützt, muss er mehr als ein Synchronisierungs Element Objekt unterstützen. Ein Beispiel hierfür ist ein persönlicher Daten Assistant (PDA), der es dem Benutzer ermöglicht, Kontakte, Kalender Elemente und Dokumente zu synchronisieren. Diese drei Datentypen müssen von drei eindeutigen Objekten dargestellt werden, die jeweils die Schnittstellen [**isyncmgrsyncitem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) und [**isyncmgrsynciteminfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) verfügbar machen.

Die [**ienumsyncmgrsyncitems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems) -Schnittstelle bietet einen Mechanismus zum Auflisten der Synchronisierungs Elemente eines Handlers. Um diesen Enumerator abzurufen, ruft das [**Synchronisierungs Center die isyncmgrsyncitemcontainer:: getsyncitemenumerator**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator) -Methode auf, die vom Handler verfügbar gemacht wird. [**Isyncmgrsyncitemcontainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer) enthält auch zwei weitere Methoden, die das Synchronisierungs Center zum Abrufen von Informationen zu den Synchronisierungs Elementen des Handlers verwenden kann:

-   [**Getsyncitem**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem) gibt ein bestimmtes Synchronisierungs Element zurück.
-   " [**Getsyncitemcount**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount) " gibt die Anzahl von Synchronisierungs Elementen zurück, die vom Handler unterstützt werden.

[**Isyncmgrhandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler) und [**isyncmgrhandlerinfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo) werden verwendet, um die Eigenschaften des handers zu beschreiben und die eigentliche Synchronisierung zu starten. [**Isyncmgrhandler::**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandler-synchronize) Sync führt den Handlercode aus, der die Synchronisierung ausführt und Feedback zum Fortschritt und alle auftretenden Probleme bereitstellt.

Viele der Schnittstellen Methoden müssen nicht vollständig implementiert werden. Das Synchronisierungs Center bietet eine bestimmte Menge an Standardinformationen. Mithilfe der Schnittstellen kann ein Handler diese Informationen überschreiben und ggf. benutzerdefinierte Informationen zur Anzeige bereitstellen.

 

 



