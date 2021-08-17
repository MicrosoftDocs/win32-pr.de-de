---
description: Die Komponente Microsoft Windows Journal Note Reader bietet programmgesteuerten Lesezugriff auf Dateien im Journalformat.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Verwenden der Journalreaderkomponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41559ac31ff081ecb810b0fe6e82ce1107ed87dae897cc7e6b8be4569e9b78f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449190"
---
# <a name="using-the-journal-reader-component"></a>Verwenden der Journalreaderkomponente

Die Komponente Microsoft Windows Journal Note Reader bietet programmgesteuerten Lesezugriff auf Dateien im Journalformat.

## <a name="component-overview"></a>Komponentenübersicht

Journaldateien haben die Dateierweiterung .jnt. Diese einfache Komponente verwendet einen Stream mit einer JNT-Datei und gibt einen Stream zurück, der den Inhalt der Datei im XML-Format enthält. Der von der Komponente zurückgegebene XML-Code entspricht dem Journal Note Reader-Schema. Dieses Schema ist in [journal reader schema reference](journal-reader-schema-reference.md)dokumentiert.

Die Komponente bietet nicht die Möglichkeit, JNT-Dateien auszuschreiben.

Die Komponente ist in nicht verwalteten und verwalteten Versionen verfügbar. Die nicht verwaltete Komponente ist in der journal.dll DLL (Dynamic Link Library) verfügbar. Die verwaltete Version befindet sich entweder in der Microsoft.Ink.Journal.dll Assembly (für die Weiterverteilung an Windows XP Tablet PC Edition oder Windows Vista) oder Microsoft.Ink.dll.

> [!IMPORTANT]
>
> Ab Windows 10 Version 1607 ist journal.dll nicht im Windows Betriebssystem enthalten. Diese Bibliothek sollte als veraltet oder veraltet betrachtet und nicht verwendet werden.

 

### <a name="assembly-changes-of-note"></a>Assembly Changes of Note

Es ist wichtig, einige Änderungen an der Assembly zu beachten, die die Komponente Journal Note Reader enthält, die zwischen der Version, die in Verbindung mit Version 1.7 des Tablet Developers Kit veröffentlicht wurde, und der Version aufgetreten sind, die im Betriebssystem Windows Vista enthalten ist.

Die Version 1.7 der Readerkomponente, die entweder an Windows XP oder Windows Vista verteilt werden kann, ist in einer Assembly namens Microsoft.Ink.Journal.dll enthalten. Die Readerkomponente ist in Windows Vista enthalten, wurde jedoch in die Kernassembly Microsoft.Ink.dll integriert. Dies bedeutet, dass Anwendungen, die die 1.7-Assembly verwenden, diese Assembly mit ihrem Setup neu verteilen müssen.

## <a name="using-the-component"></a>Verwenden der Komponente

Die Komponente Journal Note Reader ist nützlich, um die Ink-Daten und andere Informationen zur Datei aus einer Journaldatei zu extrahieren.

### <a name="com"></a>COM

Die COM-Komponente journal note reader befindet sich in der Datei Journal.dll, die beim Herunterladen und Ausführen der Installationsdatei journal note reader installiert und registriert wird.

Die COM-Komponente unterstützt die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) nicht.

### <a name="managed"></a>Verwaltet

Die vom Journalnotizleser verwaltete Komponente befindet sich in der Microsoft.Ink.JournalReader.dll Assembly. Diese Assembly wird installiert und im globalen Assemblycache registriert, wenn Sie die Installationsdatei journal note reader ausführen.

Fügen Sie einen Verweis auf die Assembly hinzu, um sie in Ihrem verwalteten Projekt zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IJournalReader-Schnittstelle**](ijournalreader.md)
</dt> <dt>

[Schemareferenz für Journalleser](journal-reader-schema-reference.md)
</dt> </dl>

 

 
