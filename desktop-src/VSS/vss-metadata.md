---
description: Sowohl Writer als auch Anforderer behalten die für einen Sicherungs-oder Wiederherstellungs Vorgang erforderlichen Informationen in ihren eigenen Metadatendokumenten.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: VSS-Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e718d3fb0290f8610944180c079e4d615124eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350443"
---
# <a name="vss-metadata"></a>VSS-Metadaten

Sowohl Writer als auch Anforderer behalten die für einen Sicherungs-oder Wiederherstellungs Vorgang erforderlichen Informationen in ihren eigenen Metadatendokumenten.

Diese Dokumente, das [*Writer-Metadatendokument*](vssgloss-w.md) und das [*Sicherungs Komponenten Dokument*](vssgloss-b.md), werden als Grundlage für die Kommunikation und Koordination von Writer und Anforderer während der Sicherungs-und Wiederherstellungs Aktivitäten verwendet.

Die Metadaten werden im XML-Format mithilfe eines proprietären Schemas dargestellt. Metadaten können auf einen Datenträger, ein Band oder ein beliebiges anderes Massen Speichergerät kopiert werden. Er sollte bei einem Sicherungs Vorgang immer auf dem Sicherungsmedium gespeichert werden und muss im Verlauf eines Wiederherstellungs Vorgangs von diesem Medium abgerufen werden.

**Vorsicht:** Die spezifischen Details des Formats und des Schemas sind nur für die Verwendung durch das System vorgesehen. Entwickler sollten nicht versuchen, die XML-Darstellung der Metadaten zu ändern oder direkt zu verwenden.

Writer und Anforderer verfügen über eine Vielzahl von Abfrage-und Set-Methoden für den Zugriff auf und die Änderung der Sicherungs Komponenten und Writer-Metadatendokumente:

-   [Arbeiten mit dem Writer-Metadatendokument](working-with-the-writer-metadata-document.md)
-   [Arbeiten mit dem Dokument mit den Sicherungs Komponenten](working-with-the-backup-components-document.md)
-   [VSS-Metadatenkomponenten](vss-metadata-components.md)

 

 



