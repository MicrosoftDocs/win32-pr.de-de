---
title: Verbund Dokumente
description: Mit OLE-Verbund Dokumenten können Benutzer innerhalb einer einzelnen Anwendung Daten bearbeiten, die in verschiedenen Formaten geschrieben und aus mehreren Quellen abgeleitet werden.
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f12e0228b7c8c1d74e4ec33d8069490351f77f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102447"
---
# <a name="compound-documents"></a>Verbund Dokumente

Mit OLE-Verbund Dokumenten können Benutzer innerhalb einer einzelnen Anwendung Daten bearbeiten, die in verschiedenen Formaten geschrieben und aus mehreren Quellen abgeleitet werden. Beispielsweise kann ein Benutzer ein Dokument, das in einer zweiten Anwendung erstellt wurde, in ein Textverarbeitungsdokument einfügen und ein in einer dritten Anwendung erstelltes Sound Objekt. Das Aktivieren des Diagramms bewirkt, dass die zweite Anwendung die Benutzeroberfläche lädt oder zumindest diesen Teil mit den Tools, die zum Bearbeiten des Objekts erforderlich sind. Das Aktivieren des Sound Objekts bewirkt, dass die dritte Anwendung Sie wieder gibt. In beiden Fällen kann ein Benutzerdaten aus externen Quellen innerhalb des Kontexts eines einzelnen Dokuments bearbeiten.

OLE-Verbund Dokument Technologien sind auf einer Grundlage von com, strukturierter Speicherung und einheitlicher Datenübertragung zu finden. Wie unten zusammengefasst, spielt jede dieser Kerntechnologien eine wichtige Rolle in OLE-Verbund Dokumenten:

<dl> <dt>

<span id="COM"></span><span id="com"></span>KOM
</dt> <dd>

Bei einem Verbund Dokument Objekt handelt es sich im Wesentlichen um ein COM-Objekt, das in ein vorhandenes Dokument eingebettet oder damit verknüpft werden kann. Als COM-Objekt stellt ein Verbund Dokument Objekt die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle zur Verfügung, über die Clients Zeiger auf Ihre anderen Schnittstellen abrufen können, wie z. b. [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**iolelink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)und [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), die besondere Features bereitstellen, die für Verbund Dokument Objekte eindeutig sind.

</dd> <dt>

<span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Strukturierter Speicher
</dt> <dd>

Ein Verbund Dokument Objekt muss die [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) -Schnittstelle oder die [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) -Schnittstelle implementieren, um den eigenen Speicher zu verwalten. Ein Container, der zum Erstellen von Verbund Dokumenten verwendet wird, muss die [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Schnittstelle bereitstellen, über die Objekte Daten speichern und abrufen. Container stellen fast immer Instanzen von **IStorage** bereit, die aus der Implementierung der Verbund Dateien von OLE abgerufen wurden. Für Container müssen außerdem die **IPersistStorage** -und/oder **IPersistStream** -Schnittstellen eines Objekts verwendet werden.

</dd> <dt>

<span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer
</dt> <dd>

Anwendungen, die Verbund Dokumente unterstützen, müssen [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) implementieren, da eingebettete Objekte und verknüpfte Objekte als Daten beginnen, die mithilfe spezieller OLE-Zwischenablage Formate anstelle von standardmäßigen Microsoft Windows-Zwischenablage Formaten übertragen wurden. Anders ausgedrückt: das Formatieren von Daten als eingebettetes oder verknüpftes Objekt ist einfach eine weitere Option, die von dem einheitlichen Daten Übertragungs Modell von OLE bereitgestellt wird.

</dd> </dl>

Die zusammengesetzte Dokumenten Technologie von OLE profitiert sowohl für Softwareentwickler als auch für Benutzer. Anstatt sich für jede denkbare Funktion in einer einzigen Anwendung zu bemühen, sind Softwareentwickler nun kostenlos, wenn Sie möchten, kleinere Anwendungen zu entwickeln, die sich auf andere Anwendungen stützen, um zusätzliche Funktionen bereitzustellen. In Fällen, in denen ein Softwareentwickler beschließt, eine Anwendung mit Funktionen zu versehen, die über die wichtigsten Features hinausgeht, kann der Entwickler diese zusätzlichen Dienste als separate DLLs implementieren, die nur dann in den Arbeitsspeicher geladen werden, wenn ihre Dienste erforderlich sind. Benutzer profitieren von einer kleineren, schnelleren und leistungsfähigeren Software, die Sie je nach Bedarf mischen und anpassen können, sodass Sie alle erforderlichen Komponenten innerhalb eines einzelnen Master Dokuments bearbeiten können.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Container und Server](containers-and-servers.md)
-   [Verknüpfen und Einbetten](linking-and-embedding.md)
-   [Objekt Handler](object-handlers.md)
-   [Prozess interne Server](in-process-servers.md)
-   [Verknüpfte Objekte und Moniker](linked-objects-and-monikers.md)
-   [Benachrichtigungen](notifications.md)
-   [Verbund Dokument Schnittstellen](compound-document-interfaces.md)
-   [Objektzustände](object-states.md)
-   [Implementieren In-Place Aktivierung](implementing-in-place-activation.md)
-   [Erstellen von verknüpften und eingebetteten Objekten aus vorhandenen Daten](creating-linked-and-embedded-objects-from-existing-data.md)
-   [Zwischenspeichern anzeigen](view-caching.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenübertragung](data-transfer.md)
</dt> <dt>

[Strukturierter Speicher](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 