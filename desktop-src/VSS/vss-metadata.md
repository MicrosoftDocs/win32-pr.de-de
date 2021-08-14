---
description: Sowohl Writer als auch Anfordernde verwalten informationen, die für einen Sicherungs- oder Wiederherstellungsvorgang erforderlich sind, in ihren eigenen Metadatendokumenten.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: VSS-Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e69d0a40bbbce2d231573d187843c14bd83fea419a7024940d0fd618838500b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986580"
---
# <a name="vss-metadata"></a>VSS-Metadaten

Sowohl Writer als auch Anfordernde verwalten informationen, die für einen Sicherungs- oder Wiederherstellungsvorgang erforderlich sind, in ihren eigenen Metadatendokumenten.

Diese Dokumente, das [*Writer-Metadatendokument*](vssgloss-w.md) bzw. das Sicherungskomponentendokument, werden als Grundlage für die Kommunikation und Koordination von Writern und Anfordernden während Sicherungs- und Wiederherstellungsaktivitäten verwendet. [](vssgloss-b.md)

Die Metadaten werden im XML-Format mithilfe eines proprietären Schemas dargestellt. Metadaten können auf Datenträger, Band oder ein anderes Massenspeichergerät kopiert werden. Sie sollte während eines Sicherungsvorganges immer auf dem Sicherungsmedium gespeichert werden und muss im Rahmen eines Wiederherstellungsvorgang von diesem Medium abgerufen werden.

**Vorsicht:** Die spezifischen Details des Formats und Schemas sind nur für die Systemnutzung. Entwickler sollten nicht versuchen, die XML-Darstellung der Metadaten zu ändern oder direkt zu verwenden.

Writer und Anfordernde erhalten eine Vielzahl von Abfrage- und Satzmethoden für den Zugriff auf und die Änderung der Dokumente sicherungskomponenten und Writermetadaten:

-   [Arbeiten mit dem Writer-Metadatendokument](working-with-the-writer-metadata-document.md)
-   [Arbeiten mit dem Dokument "Sicherungskomponenten"](working-with-the-backup-components-document.md)
-   [VSS-Metadatenkomponenten](vss-metadata-components.md)

 

 



