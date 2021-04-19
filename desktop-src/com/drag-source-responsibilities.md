---
title: Quellen Zuständigkeiten ziehen
description: Quellen Zuständigkeiten ziehen
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339914"
---
# <a name="drag-source-responsibilities"></a>Quellen Zuständigkeiten ziehen

Die Zieh Quelle ist für die folgenden Aufgaben zuständig:

-   Bereitstellen eines Datenübertragungs Objekts für das Ablage Ziel, das die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle und die [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) -Schnittstelle verfügbar macht.
-   Zeiger-und Quell Feedback werden erzeugt.
-   Es wird ermittelt, wann der Zieh Vorgang abgebrochen wurde oder ein Ablage Vorgang aufgetreten ist.
-   Ausführen von Aktionen für die ursprünglichen Daten, die durch den Drop-Vorgang verursacht wurden, wie z. b. das Löschen der Daten oder das Erstellen einer Verknüpfung.

Die Hauptaufgabe ist das Erstellen eines Datenübertragungs Objekts, das die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle und die [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) -Schnittstelle verfügbar macht. Die Zieh Quelle enthält möglicherweise eine Kopie der ausgewählten Daten. Dies ist nicht zwingend erforderlich, aber dadurch wird der Schutz vor unbeabsichtigten Änderungen gewährleistet, und der Code der Zwischenablage kann mit dem Drag & Drop-Code identisch sein.

Während eines Zieh Vorgangs ist die Zieh Quelle für das Festlegen des Mauszeigers und ggf. für das Bereitstellen zusätzlicher Quell Feedback für den Benutzer verantwortlich. Die Zieh Quelle kann kein Feedback bereitstellen, das die Mausposition nachverfolgt, außer durch das tatsächliche Festlegen des echten Zeigers (siehe [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) -Funktion). Diese Regel muss erzwungen werden, um Konflikte mit dem vom Drop-Ziel bereitgestellten Feedback zu vermeiden. (Eine Zieh Quelle kann auch ein Ablage Ziel sein. Wenn Sie sich selbst ablegen, kann die Quelle/das Ziel natürlich das Ziel Feedback bereitstellen, um die Mausposition zu verfolgen. In diesem Fall ist es jedoch das Ablage Ziel, das die Maus nachverfolgt, nicht die Quelle.) Basierend auf dem Feedback, das das Ablage Ziel bietet, legt die Quelle einen entsprechenden Zeiger fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Drag &amp; Drop](drag-and-drop.md)
</dt> </dl>

 

 