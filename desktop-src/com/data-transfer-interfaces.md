---
title: Datenübertragungsschnittstellen
description: Datenübertragungsschnittstellen
ms.assetid: c42e65a4-7b77-4f39-8323-04fa60c5b140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63bffa72f2e6bd408cbb7f19121aeef991e74702ff1141b24aba779e6985585c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896340"
---
# <a name="data-transfer-interfaces"></a>Datenübertragungsschnittstellen

Die [**IDataObject-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) stellt Datenverbrauchern Methoden zum Abrufen und Festlegen der Daten eines Objekts bereit, bestimmt, welche Formate das Objekt unterstützt, und registriert sich für und empfängt Benachrichtigungen, wenn sich Daten im Objekt ändern. Beim Abrufen von Daten kann ein Aufrufer das Format angeben, in dem die Daten gerendert werden. Die Quelle der Daten bestimmt jedoch das Speichermedium, das in einem vom Aufrufer bereitgestellten out-Parameter zurückgegeben wird.

Allein stellt [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) alle Tools zur Verfügung, die Sie zum Implementieren Windows Übertragungen von Zwischenablage oder verbunddokumenten in Ihren Anwendungen benötigen. If you also want to support drag and drop transfers, you need to implement the [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interfaces along with **IDataObject**.

Die [**IDataObject-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) in Kombination mit OLE-Zwischenablage-APIs bietet alle Funktionen der Windows-APIs für die Zwischenablage. Es ist im Allgemeinen nicht erforderlich, beide Zwischenablage-APIs zu verwenden. Data suppliers that support either drag and drop transfers or OLE compound documents must implement the **IDataObject** interface. If your application supports only clipboard transfers now, but you intend to add drag and drop or compound documents in later releases, you may want to implement **IDataObject** and the OLE clipboard APIs now in order to minimize the amount of time spent recoding and debugging later. Möglicherweise möchten Sie auch **IDataObject** implementieren, um andere Übertragungsmedien als den globalen Arbeitsspeicher zu verwenden.

In der folgenden Tabelle sind die zu verwendenden Datenübertragungen zusammengefasst, je nachdem, welche Arten von Datenübertragungen Unterstützt werden sollen:



| So unterstützen Sie                                                                       | Zweck                                                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verbunddokumente<br/>                                                    | [**Idataobject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Drag & Drop-Übertragungen<br/>                                               | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource), [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget), [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (oder das Äquivalent)<br/> |
| Übertragungen der Zwischenablage ausschließlich mithilfe des globalen Arbeitsspeichers<br/>                   | [Zwischenablage-API](../dataxchg/clipboard.md)<br/>                                                                                                                            |
| Zwischenablageübertragungen mit anderen Exchange-Medien als dem globalen Arbeitsspeicher.<br/>  | [**Idataobject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Zwischenablageübertragungen jetzt, aber drag & drop oder zusammengesetzte Dokumente später<br/> | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and the interfaces and function listed above for "Drag and drop transfers"<br/>                                                    |



 

Wenn ein Benutzer einen Datenübertragungsvorgang initiiert, erstellt die Quellanwendung eine Instanz von [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) und stellt die Daten dadurch in mindestens einem Format zur Verfügung. In einer Zwischenablageübertragung ruft die Anwendung die [**OleSetClipboard-Funktion**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) auf, um einen Datenobjektzeiger an OLE zu übergeben. (**OleSetClipboard** also offers standard clipboard data formats for both OLE version 1 and non-OLE applications.) In a drag and drop transfer, the application calls the [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function instead.

On the receiving side of the transfer, the destination receives the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) pointer either as an argument to an invocation of [**IDropTarget::Drop**](/windows/desktop/api/OleIdl/nf-oleidl-idroptarget-drop) or by calling the [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) function, depending on whether the transfer is by means of drag and drop or the clipboard. Nach dem Abrufen dieses Zeigers ruft das Ziel [**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc) auf, um zu erfahren, welche Formate zum Abrufen verfügbar sind und welche Medientypen sie erhalten werden können. Mit diesen Informationen fordert die empfangende Anwendung die Daten mit einem Aufruf von [**IDataObject::GetData an.**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenübertragung](data-transfer.md)
</dt> </dl>

 

