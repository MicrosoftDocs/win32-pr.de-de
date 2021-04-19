---
title: Datenübertragung Schnittstellen
description: Datenübertragung Schnittstellen
ms.assetid: c42e65a4-7b77-4f39-8323-04fa60c5b140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e1a580880c7202ec67d12965f6db7e0be99d0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341560"
---
# <a name="data-transfer-interfaces"></a>Datenübertragung Schnittstellen

Die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle stellt Consumer von Daten mit Methoden zum Abrufen und Festlegen der Daten eines Objekts, zum Bestimmen der vom Objekt unterstützten Formate und zum Registrieren und empfangen von Benachrichtigungen, wenn sich die Daten im Objekt ändern. Beim Abrufen von Daten kann ein Aufrufer das Format angeben, in dem die Daten dargestellt werden sollen. Die Quelle der Daten bestimmt jedoch das Speichermedium, das in einem vom Aufrufer bereitgestellten out-Parameter zurückgegeben wird.

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) bietet alle Tools, die Sie zum Implementieren von Windows-Zwischenablage Übertragungen oder Verbund Dokumenten Übertragungen in Ihren Anwendungen benötigen. Wenn Sie auch Drag & Drop-Übertragungen unterstützen möchten, müssen Sie die [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) -Schnittstelle und die [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) -Schnittstelle zusammen mit **IDataObject** implementieren.

Die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle, kombiniert mit OLE-Zwischenablage-APIs, bietet alle Funktionen der Windows-Zwischenablage-APIs. Es ist in der Regel nicht erforderlich, beide Zwischenablage-APIs zu verwenden. Datenlieferanten, die Drag & Drop-Übertragungen oder OLE-Verbund Dokumente unterstützen, müssen die **IDataObject** -Schnittstelle implementieren. Wenn Ihre Anwendung jetzt nur Zwischenablage Übertragungen unterstützt, Sie jedoch beabsichtigen, Drag & Drop-oder Verbund Dokumente in späteren Releases hinzuzufügen, sollten Sie **IDataObject** und die OLE-Zwischenablage-APIs jetzt implementieren, um die Zeitspanne zu verringern, die für das Wiederherstellen und Debuggen später aufgewendet wird. Möglicherweise möchten Sie auch **IDataObject** implementieren, um ein anderes Übertragungsmedium als den globalen Arbeitsspeicher zu verwenden.

In der folgenden Tabelle wird zusammengefasst, welche Typen von Datenübertragungen Sie verwenden möchten:



| Zur Unterstützung von                                                                       | Zweck                                                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verbund Dokumente<br/>                                                    | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Übertragungen per Drag & Drop<br/>                                               | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource), [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget), [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (oder das Äquivalent)<br/> |
| Zwischenablage Übertragungen ausschließlich mit globalem Speicher<br/>                   | [Zwischenablage-API](../dataxchg/clipboard.md)<br/>                                                                                                                            |
| Zwischenablage Übertragungen mit anderen Exchange-Medien als dem globalen Arbeitsspeicher.<br/>  | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Zwischenablage Übertragungen jetzt, jedoch später per Drag & Drop oder Verbund Dokumenten<br/> | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) und die oben aufgelisteten Schnittstellen und Funktionen für "Drag & Drop-Übertragungen"<br/>                                                    |



 

Wenn ein Benutzer einen Datenübertragungs Vorgang initiiert, erstellt die Quell Anwendung eine Instanz von [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) und macht die Daten in einem oder mehreren Formaten verfügbar. Bei einer Übertragung der Zwischenablage Ruft die Anwendung die [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) -Funktion auf, um einen Datenobjekt Zeiger an OLE zu übergeben. (**OleSetClipboard** bietet auch Standarddaten Formate der Zwischenablage sowohl für OLE-Version 1 als auch für nicht-OLE-Anwendungen.) Bei einer Drag & Drop-Übertragung Ruft die Anwendung stattdessen die [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) -Funktion auf.

Auf der Empfangsseite der Übertragung empfängt das Ziel den [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Zeiger entweder als Argument für einen Aufruf von [**IDropTarget::D ROP**](/windows/desktop/api/OleIdl/nf-oleidl-idroptarget-drop) oder durch Aufrufen der [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) -Funktion, je nachdem, ob die Übertragung per Drag & Drop oder der Zwischenablage erfolgt. Nachdem dieser Zeiger abgerufen wurde, ruft das Ziel [**IDataObject:: enumformatusw**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc) . auf, um zu erfahren, welche Formate für den Abruf verfügbar sind und welche Arten von Medien abgerufen werden können. Mit diesen Informationen, fordert die empfangende Anwendung die Daten mit einem [**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)-Aufrufen an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenübertragung](data-transfer.md)
</dt> </dl>

 

