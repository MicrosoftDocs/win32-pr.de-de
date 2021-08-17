---
description: 'Weitere Informationen finden Sie unter: Versions-, Auto-Increment- und Escrow-Spalten'
title: Versions-, Auto-Increment- und Escrow-Spalten
TOCTitle: Version, Auto-Increment and Escrow Columns
ms:assetid: b12724a4-6846-49a7-9223-43895f91427e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294059(v=EXCHG.10)
ms:contentKeyID: 32765674
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: b86b37663f7968ad77874ebcc7b2d0f8fd569cc265424bc36feeecccb6d7e148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471280"
---
# <a name="version-auto-increment-and-escrow-columns"></a>Versions-, Auto-Increment- und Escrow-Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="version-auto-increment-and-escrow-columns"></a>Versions-, Auto-Increment- und Escrow-Spalten

ESE bietet Spaltentypen für Version, automatisches Inkrementen und Stirnrunzeln, die besondere Fähigkeiten haben. Die Spaltenoptionen, die im **Grbit-Member** der [JET_COLUMNDEF-Struktur](./jet-columndef-structure.md) festgelegt sind, die im Aufruf von [JetAddColumn](./jetaddcolumn-function.md) verwendet werden, geben an, ob die Spalte einer der hier notierten spezialisierten Typen ist.

### <a name="version-jet_bitcolumnversion"></a>Version (JET_bitColumnVersion)

Die Versionsspaltenoption, die nur auf JET_coltypLong-Spalten angewendet wird, gibt an, dass die Spalte Versionsinformationen zum Datensatz enthält, mit denen bestimmt werden kann, ob eine In-Memory-Kopie eines bestimmten Datensatzes aktualisiert werden muss. Versionsspalten werden automatisch von ESE erhöht, wenn die Spalte von der Anwendung über [JetUpdate geändert wird.](./jetupdate-function.md)

### <a name="auto-increment-jet_bitcolumnautoincrement"></a>Automatisches Inkrement (JET_bitColumnAutoincrement)

Automatisch inkrementierte Spalten werden automatisch von ESE erhöht, wenn ein neuer Datensatz in die Tabelle eingefügt wird. Der Inkrementwert in der Spalte mit automatischer Inkrement ist für jeden Datensatz in der Tabelle eindeutig und garantiert nicht kontinuierlich. Diese Werte werden nicht wiederverwendet, können aber in bestimmten Fällen wiederverwendet werden. Nur Spalten vom Typ JET_coltypLong und JET_coltypLongLong können automatisch inkrementiert werden.

### <a name="escrow-jet_bitcolumnescrowupdate"></a>Escrow (JET_bitColumnEscrowUpdate)

Escrow-Spalten können im Aufruf von [JetEscrowUpdate geändert werden.](./jetescrowupdate-function.md) Updates in escrow sind numerische Deltavorgänge, die nicht unter Schreibkonflikten stehen. Dies bedeutet, dass eine beliebige Anzahl von Sitzungen gleichzeitig eine Escrow-Spalte in einem Datensatz über [JetEscrowUpdate ohne](./jetescrowupdate-function.md) Konflikte aktualisieren kann. Beachten Sie, dass jeder andere Aktualisierungsvorgang weiterhin zu einem Schreibkonflikt mit einem Escrow-Updatevorgang führen kann. Escrow-Aktualisierungen können nur für Spalten vom Typ JET_coltypLong, die einen Standardwert haben. Diese Spalten müssen auch einer Tabelle hinzugefügt werden, bevor sie mit Zeilen geladen wird. Schließlich können Zeilen, die eine Spalte zum Aktualisieren der Hinterlegung enthalten, so konfiguriert werden, dass sie einen Zeilen finalisierungsrückruf (JET_bitColumnFinalize) unterstützen oder automatisch gelöscht werden, wenn die Ref-Anzahl 0 (null) erreicht (JET_bitColumnDeleteOnZero). Weitere Informationen finden Sie unter [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur.
