---
title: Verbunddokumente
description: OLE-Verbunddokumente ermöglichen Es Benutzern, die in einer einzelnen Anwendung arbeiten, Daten zu bearbeiten, die in verschiedenen Formaten geschrieben und aus mehreren Quellen abgeleitet wurden.
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8add155f60a9cbbce96f6d5bc0434ec2759d3e33c42aac2a5b47c8dc1bb4a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410480"
---
# <a name="compound-documents"></a>Verbunddokumente

OLE-Verbunddokumente ermöglichen Es Benutzern, die in einer einzelnen Anwendung arbeiten, Daten zu bearbeiten, die in verschiedenen Formaten geschrieben und aus mehreren Quellen abgeleitet wurden. Beispielsweise kann ein Benutzer in ein Textverarbeitungsdokument einen Graphen einfügen, der in einer zweiten Anwendung erstellt wurde, und ein Soundobjekt, das in einer dritten Anwendung erstellt wurde. Das Aktivieren des Graphen bewirkt, dass die zweite Anwendung ihre Benutzeroberfläche oder mindestens den Teil mit den Tools, die zum Bearbeiten des Objekts erforderlich sind, geladen. Wenn Sie das Soundobjekt aktivieren, wird es von der dritten Anwendung wieder verwendet. In beiden Fällen kann ein Benutzer Daten aus externen Quellen innerhalb des Kontexts eines einzelnen Dokuments bearbeiten.

Die OLE-Verbunddokumenttechnologie beruht auf einer Grundlage, die aus COM, strukturiertem Speicher und einheitlicher Datenübertragung besteht. Wie unten zusammengefasst, spielt jede dieser Kerntechnologien eine wichtige Rolle in OLE-Verbunddokumenten:

<dl> <dt>

<span id="COM"></span><span id="com"></span>Com
</dt> <dd>

Ein zusammengesetztes Dokumentobjekt ist im Wesentlichen ein COM-Objekt, das in ein vorhandenes Dokument eingebettet oder mit diesem verknüpft werden kann. Als COM-Objekt macht ein zusammengesetztes Dokumentobjekt die [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) verfügbar, über die Clients Zeiger auf ihre anderen Schnittstellen abrufen können, darunter mehrere, z. B. [**IOleObject,**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)und [**IViewObject2,**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)die spezielle Features bereitstellen, die für zusammengesetzte Dokumentobjekte eindeutig sind.

</dd> <dt>

<span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Strukturierte Storage
</dt> <dd>

Ein zusammengesetztes Dokumentobjekt muss die [**IPersistStorage-**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) oder optional [**IPersistStream-Schnittstellen**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) implementieren, um seinen eigenen Speicher zu verwalten. Ein Container, der zum Erstellen zusammengesetzter Dokumente verwendet wird, muss die [**IStorage-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istorage) zur Verfügung stellen, über die Objekte Daten speichern und abrufen. Container stellen fast immer Instanzen von **IStorage** zur Verfügung, die aus der Ole-Implementierung von Verbunddateien ermittelt wurden. Container müssen auch die **IPersistStorage-** und/oder **IPersistStream-Schnittstellen eines Objekts** verwenden.

</dd> <dt>

<span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer
</dt> <dd>

Anwendungen, die verbundgebundene Dokumente unterstützen, müssen [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) implementieren, da eingebettete objekte und verknüpfte Objekte als Daten beginnen, die mithilfe spezieller OLE-Zwischenablageformate übertragen wurden, und nicht als standarde Microsoft Windows-Zwischenablageformate. Anders ausgedrückt: Das Formatieren von Daten als eingebettetes oder verknüpftes Objekt ist einfach eine weitere Option, die vom einheitlichen Datenübertragungsmodell von OLE bereitgestellt wird.

</dd> </dl>

Die Verbunddokumenttechnologie von OLE profitiert sowohl von Softwareentwicklern als auch von Benutzern. Anstatt sich zu fühlen, jedes mögliche Feature in eine einzelne Anwendung zu gieren, können Softwareentwickler nun, wenn sie möchten, kleinere, fokussiertere Anwendungen entwickeln, die sich auf andere Anwendungen verlassen, um zusätzliche Features zur Verfügung zu stellen. In Fällen, in denen ein Softwareentwickler entscheidet, einer Anwendung Funktionen zur Verfügung zu stellen, die über die Kernfunktionen hinausgehen, kann der Entwickler diese zusätzlichen Dienste als separate DLLs implementieren, die nur dann in den Arbeitsspeicher geladen werden, wenn ihre Dienste erforderlich sind. Benutzer profitieren von kleinerer, schnellerer, fähiger Software, die sie nach Bedarf mischen und abordnen können, und bearbeiten alle erforderlichen Komponenten innerhalb eines einzelnen Masterdokuments.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Container und Server](containers-and-servers.md)
-   [Verknüpfen und Einbetten](linking-and-embedding.md)
-   [Objekthandler](object-handlers.md)
-   [In-Process-Server](in-process-servers.md)
-   [Verknüpfte Objekte und Moniker](linked-objects-and-monikers.md)
-   [Benachrichtigungen](notifications.md)
-   [Verbunddokumentschnittstellen](compound-document-interfaces.md)
-   [Objektzustände](object-states.md)
-   [Implementieren In-Place Aktivierung](implementing-in-place-activation.md)
-   [Erstellen verknüpfter und eingebetteter Objekte aus vorhandenen Daten](creating-linked-and-embedded-objects-from-existing-data.md)
-   [Anzeigen der Zwischenspeicherung](view-caching.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenübertragung](data-transfer.md)
</dt> <dt>

[Strukturierte Storage](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 