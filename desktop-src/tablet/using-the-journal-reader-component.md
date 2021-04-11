---
description: Die Microsoft Windows Journal Note Reader-Komponente ermöglicht programmgesteuerten Lesezugriff auf Dateien im Journal Format.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Verwenden der Journal Reader-Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958897"
---
# <a name="using-the-journal-reader-component"></a>Verwenden der Journal Reader-Komponente

Die Microsoft Windows Journal Note Reader-Komponente ermöglicht programmgesteuerten Lesezugriff auf Dateien im Journal Format.

## <a name="component-overview"></a>Übersicht über Komponenten

Journal Dateien haben die Dateierweiterung. jnt. Diese einfache Komponente übernimmt einen Stream, der eine JNT-Datei enthält, und gibt einen Stream zurück, der den Inhalt der Datei im XML-Format enthält. Der von der Komponente zurückgegebene XML-Code entspricht dem Journal Note Reader-Schema. Dieses Schema ist in der [Journal Reader-Schema Referenz](journal-reader-schema-reference.md)dokumentiert.

Die-Komponente bietet keine Möglichkeit, JNT-Dateien zu schreiben.

Die Komponente ist in nicht verwalteten und verwalteten Versionen verfügbar. Die nicht verwaltete Komponente ist in der journal.dll Dynamic Link Library (dll) verfügbar. Die verwaltete Version befindet sich entweder in der Microsoft.Ink.Journal.dll-Assembly (für die Weiterverteilung an Windows XP Tablet PC Edition oder Windows Vista) oder Microsoft.Ink.dll.

> [!IMPORTANT]
>
> Ab Windows 10, Version 1607, ist journal.dll nicht im Windows-Betriebssystem enthalten. Diese Bibliothek sollte als veraltet oder veraltet betrachtet werden und sollte nicht verwendet werden.

 

### <a name="assembly-changes-of-note"></a>Assemblyänderungen von Hinweis

Es ist wichtig, dass Sie einige Änderungen an der Assembly kennen, die die Journal Notiz Reader-Komponente enthält, die zwischen der Version, die in Verbindung mit Version 1,7 des Tablet Developers Kit veröffentlicht wurde, und der Version, die im Windows Vista-Betriebssystem enthalten ist, aufgetreten ist.

Die 1,7-Version der Reader-Komponente, die entweder an Windows XP oder Windows Vista weitergegeben werden kann, ist in einer Assembly mit dem Namen "Microsoft.Ink.Journal.dll" enthalten. Die Reader-Komponente ist in Windows Vista enthalten, wurde jedoch in die Core Microsoft.Ink.dll-Assembly integriert. Dies bedeutet, dass Anwendungen, die die 1,7-Assembly verwenden, diese Assembly mit Ihrem Setup neu verteilen müssen.

## <a name="using-the-component"></a>Verwenden der Komponente

Die Reader-Komponente für Journal Hinweise ist hilfreich zum Extrahieren der frei Hand Daten und anderer Informationen über die Datei aus einer Journal Datei.

### <a name="com"></a>COM

Die COM-Komponente "Journal Notiz Reader" befindet sich in der Datei Journal.dll, die beim Herunterladen und Ausführen der Installationsdatei für Journal Notiz Reader installiert und registriert wird.

Die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle wird von der COM-Komponente nicht unterstützt.

### <a name="managed"></a>Verwaltet

Die verwaltete Komponente "Journal Notiz Reader" befindet sich in der Microsoft.Ink.JournalReader.dll-Assembly. Diese Assembly wird im globalen Assemblycache installiert und registriert, wenn Sie die Installationsdatei des Journal Notiz Readers ausführen.

Fügen Sie einen Verweis auf die Assembly hinzu, um Sie in Ihrem verwalteten Projekt zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ijournalreader-Schnittstelle**](ijournalreader.md)
</dt> <dt>

[Schema Referenz für Journal Reader](journal-reader-schema-reference.md)
</dt> </dl>

 

 
