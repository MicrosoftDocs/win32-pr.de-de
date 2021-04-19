---
description: 'Weitere Informationen finden Sie unter: Versions-, automatische Inkrement-und hinterlegte Spalten.'
title: Versions-, automatische Inkrement-und hinterlegte Spalten
TOCTitle: Version, Auto-Increment and Escrow Columns
ms:assetid: b12724a4-6846-49a7-9223-43895f91427e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294059(v=EXCHG.10)
ms:contentKeyID: 32765674
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e5966990a51e87b90946416161e20d677116f8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345760"
---
# <a name="version-auto-increment-and-escrow-columns"></a>Versions-, automatische Inkrement-und hinterlegte Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="version-auto-increment-and-escrow-columns"></a>Versions-, automatische Inkrement-und hinterlegte Spalten

ESE bietet Versions Typen für Versions-, automatische Inkrement-und hinterlegter-Updates, die besondere Fähigkeiten aufweisen. Die Spalten Optionen, die im **grbit** -Member der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur festgelegt sind, die im Befehl [jetaddcolumn](./jetaddcolumn-function.md) verwendet wird, geben an, ob die Spalte einer der spezialisierten Typen ist, die hier angegeben sind.

### <a name="version-jet_bitcolumnversion"></a>Version (JET_bitColumnVersion)

Die Version Column-Option, die nur auf JET_coltypLong Spalten angewendet wird, gibt an, dass die Spalte Versionsinformationen zum Datensatz enthält, mit denen bestimmt werden kann, ob eine Kopie eines bestimmten Datensatzes im Arbeitsspeicher aktualisiert werden muss. Versions Spalten werden automatisch von ESE inkrementiert, wenn die Spalte über [jetupdate](./jetupdate-function.md)von der Anwendung geändert wird.

### <a name="auto-increment-jet_bitcolumnautoincrement"></a>Automatische Inkrement (JET_bitColumnAutoincrement)

Automatische inkrementelle Spalten werden automatisch von ESE inkrementiert, wenn ein neuer Datensatz in die Tabelle eingefügt wird. Der in der Spalte für die automatische Inkrement enthaltene Wert ist für jeden Datensatz in der Tabelle eindeutig und nicht unbedingt kontinuierlich. Diese Werte werden nicht wieder verwendet, können aber in bestimmten Fällen wieder verwendet werden. Nur Spalten vom Typ JET_coltypLong und JET_coltypLongLong können automatische Inkrement-Spalten sein.

### <a name="escrow-jet_bitcolumnescrowupdate"></a>Hinterlegung (JET_bitColumnEscrowUpdate)

Hinterlegte Spalten können im Befehl [jetescrowupdate](./jetescrowupdate-function.md)geändert werden. Bei den Hinterlegungs Vorgängen handelt es sich um numerische Delta Vorgänge, die nicht durch Schreib Konflikte beeinträchtigt werden. Dies bedeutet, dass eine beliebige Anzahl von Sitzungen eine hinterlegte Spalte in einem Datensatz über [jetescrowupdate](./jetescrowupdate-function.md) ohne Konflikte gleichzeitig aktualisieren kann. Beachten Sie, dass ein anderer Aktualisierungs Vorgang möglicherweise immer noch zu einem Schreib Konflikt mit einem hinterlegungsaktualisierungs Vorgang führt. Hinterlegte Aktualisierungen können nur an Spalten vom Typ JET_coltypLong vorgenommen werden, die einen Standardwert aufweisen. Diese Spalten müssen auch einer Tabelle hinzugefügt werden, bevor Sie mit Zeilen geladen werden. Schließlich können Zeilen, die eine Spalte für das hinterlegter-Update enthalten, so konfiguriert werden, dass ein Zeilen Abschluss Rückruf (JET_bitColumnFinalize) unterstützt oder automatisch gelöscht wird, wenn der Verweis Zähler Null (JET_bitColumnDeleteOnZero) erreicht. Weitere Informationen finden Sie in der [JET_COLUMNDEF](./jet-columndef-structure.md) -Struktur.
