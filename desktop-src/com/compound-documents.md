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
# <a name="compound-documents"></a><span data-ttu-id="292e7-103">Verbund Dokumente</span><span class="sxs-lookup"><span data-stu-id="292e7-103">Compound Documents</span></span>

<span data-ttu-id="292e7-104">Mit OLE-Verbund Dokumenten können Benutzer innerhalb einer einzelnen Anwendung Daten bearbeiten, die in verschiedenen Formaten geschrieben und aus mehreren Quellen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="292e7-104">OLE compound documents enable users working within a single application to manipulate data written in various formats and derived from multiple sources.</span></span> <span data-ttu-id="292e7-105">Beispielsweise kann ein Benutzer ein Dokument, das in einer zweiten Anwendung erstellt wurde, in ein Textverarbeitungsdokument einfügen und ein in einer dritten Anwendung erstelltes Sound Objekt.</span><span class="sxs-lookup"><span data-stu-id="292e7-105">For example, a user might insert into a word processing document a graph created in a second application and a sound object created in a third application.</span></span> <span data-ttu-id="292e7-106">Das Aktivieren des Diagramms bewirkt, dass die zweite Anwendung die Benutzeroberfläche lädt oder zumindest diesen Teil mit den Tools, die zum Bearbeiten des Objekts erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="292e7-106">Activating the graph causes the second application to load its user interface, or at least that part containing tools necessary to edit the object.</span></span> <span data-ttu-id="292e7-107">Das Aktivieren des Sound Objekts bewirkt, dass die dritte Anwendung Sie wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="292e7-107">Activating the sound object causes the third application to play it.</span></span> <span data-ttu-id="292e7-108">In beiden Fällen kann ein Benutzerdaten aus externen Quellen innerhalb des Kontexts eines einzelnen Dokuments bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="292e7-108">In both cases, a user is able to manipulate data from external sources from within the context of a single document.</span></span>

<span data-ttu-id="292e7-109">OLE-Verbund Dokument Technologien sind auf einer Grundlage von com, strukturierter Speicherung und einheitlicher Datenübertragung zu finden.</span><span class="sxs-lookup"><span data-stu-id="292e7-109">OLE compound document technology rests on a foundation consisting of COM, structured storage, and uniform data transfer.</span></span> <span data-ttu-id="292e7-110">Wie unten zusammengefasst, spielt jede dieser Kerntechnologien eine wichtige Rolle in OLE-Verbund Dokumenten:</span><span class="sxs-lookup"><span data-stu-id="292e7-110">As summarized below, each of these core technologies plays a critical role in OLE compound documents:</span></span>

<dl> <dt>

<span data-ttu-id="292e7-111"><span id="COM"></span><span id="com"></span>KOM</span><span class="sxs-lookup"><span data-stu-id="292e7-111"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="292e7-112">Bei einem Verbund Dokument Objekt handelt es sich im Wesentlichen um ein COM-Objekt, das in ein vorhandenes Dokument eingebettet oder damit verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="292e7-112">A compound document object is essentially a COM object that can be embedded in, or linked to, an existing document.</span></span> <span data-ttu-id="292e7-113">Als COM-Objekt stellt ein Verbund Dokument Objekt die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle zur Verfügung, über die Clients Zeiger auf Ihre anderen Schnittstellen abrufen können, wie z. b. [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**iolelink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)und [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), die besondere Features bereitstellen, die für Verbund Dokument Objekte eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="292e7-113">As a COM object, a compound document object exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces, including several, such as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink), and [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), that provide special features unique to compound document objects.</span></span>

</dd> <dt>

<span data-ttu-id="292e7-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Strukturierter Speicher</span><span class="sxs-lookup"><span data-stu-id="292e7-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Structured Storage</span></span>
</dt> <dd>

<span data-ttu-id="292e7-115">Ein Verbund Dokument Objekt muss die [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) -Schnittstelle oder die [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) -Schnittstelle implementieren, um den eigenen Speicher zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="292e7-115">A compound document object must implement the [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) or, optionally, [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) interfaces to manage its own storage.</span></span> <span data-ttu-id="292e7-116">Ein Container, der zum Erstellen von Verbund Dokumenten verwendet wird, muss die [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Schnittstelle bereitstellen, über die Objekte Daten speichern und abrufen.</span><span class="sxs-lookup"><span data-stu-id="292e7-116">A container used to create compound documents must supply the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface, through which objects store and retrieve data.</span></span> <span data-ttu-id="292e7-117">Container stellen fast immer Instanzen von **IStorage** bereit, die aus der Implementierung der Verbund Dateien von OLE abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="292e7-117">Containers almost always provide instances of **IStorage** obtained from OLE's Compound Files implementation.</span></span> <span data-ttu-id="292e7-118">Für Container müssen außerdem die **IPersistStorage** -und/oder **IPersistStream** -Schnittstellen eines Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="292e7-118">Containers must also use an object's **IPersistStorage** and/or **IPersistStream** interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="292e7-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer</span><span class="sxs-lookup"><span data-stu-id="292e7-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer</span></span>
</dt> <dd>

<span data-ttu-id="292e7-120">Anwendungen, die Verbund Dokumente unterstützen, müssen [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) implementieren, da eingebettete Objekte und verknüpfte Objekte als Daten beginnen, die mithilfe spezieller OLE-Zwischenablage Formate anstelle von standardmäßigen Microsoft Windows-Zwischenablage Formaten übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="292e7-120">Applications that support compound documents must implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) because embedded objects and linked objects begin as data that has been transferred using special OLE clipboard formats, rather than standard Microsoft Windows clipboard formats.</span></span> <span data-ttu-id="292e7-121">Anders ausgedrückt: das Formatieren von Daten als eingebettetes oder verknüpftes Objekt ist einfach eine weitere Option, die von dem einheitlichen Daten Übertragungs Modell von OLE bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="292e7-121">In other words, formatting data as an embedded or linked object is simply one more option provided by OLE's uniform data transfer model.</span></span>

</dd> </dl>

<span data-ttu-id="292e7-122">Die zusammengesetzte Dokumenten Technologie von OLE profitiert sowohl für Softwareentwickler als auch für Benutzer.</span><span class="sxs-lookup"><span data-stu-id="292e7-122">OLE's compound document technology benefits both software developers and users alike.</span></span> <span data-ttu-id="292e7-123">Anstatt sich für jede denkbare Funktion in einer einzigen Anwendung zu bemühen, sind Softwareentwickler nun kostenlos, wenn Sie möchten, kleinere Anwendungen zu entwickeln, die sich auf andere Anwendungen stützen, um zusätzliche Funktionen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="292e7-123">Instead of feeling obligated to cram every conceivable feature into a single application, software developers are now free, if they like, to develop smaller, more focused applications that rely on other applications to supply additional features.</span></span> <span data-ttu-id="292e7-124">In Fällen, in denen ein Softwareentwickler beschließt, eine Anwendung mit Funktionen zu versehen, die über die wichtigsten Features hinausgeht, kann der Entwickler diese zusätzlichen Dienste als separate DLLs implementieren, die nur dann in den Arbeitsspeicher geladen werden, wenn ihre Dienste erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="292e7-124">In cases where a software developer decides to provide an application with capabilities beyond its core features, the developer can implement these additional services as separate DLLs, which are loaded into memory only when their services are required.</span></span> <span data-ttu-id="292e7-125">Benutzer profitieren von einer kleineren, schnelleren und leistungsfähigeren Software, die Sie je nach Bedarf mischen und anpassen können, sodass Sie alle erforderlichen Komponenten innerhalb eines einzelnen Master Dokuments bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="292e7-125">Users benefit from smaller, faster, more capable software that they can mix and match as needed, manipulating all required components from within a single master document.</span></span>

<span data-ttu-id="292e7-126">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="292e7-126">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="292e7-127">Container und Server</span><span class="sxs-lookup"><span data-stu-id="292e7-127">Containers and Servers</span></span>](containers-and-servers.md)
-   [<span data-ttu-id="292e7-128">Verknüpfen und Einbetten</span><span class="sxs-lookup"><span data-stu-id="292e7-128">Linking and Embedding</span></span>](linking-and-embedding.md)
-   [<span data-ttu-id="292e7-129">Objekt Handler</span><span class="sxs-lookup"><span data-stu-id="292e7-129">Object Handlers</span></span>](object-handlers.md)
-   [<span data-ttu-id="292e7-130">Prozess interne Server</span><span class="sxs-lookup"><span data-stu-id="292e7-130">In-Process Servers</span></span>](in-process-servers.md)
-   [<span data-ttu-id="292e7-131">Verknüpfte Objekte und Moniker</span><span class="sxs-lookup"><span data-stu-id="292e7-131">Linked Objects and Monikers</span></span>](linked-objects-and-monikers.md)
-   [<span data-ttu-id="292e7-132">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="292e7-132">Notifications</span></span>](notifications.md)
-   [<span data-ttu-id="292e7-133">Verbund Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="292e7-133">Compound Document Interfaces</span></span>](compound-document-interfaces.md)
-   [<span data-ttu-id="292e7-134">Objektzustände</span><span class="sxs-lookup"><span data-stu-id="292e7-134">Object States</span></span>](object-states.md)
-   [<span data-ttu-id="292e7-135">Implementieren In-Place Aktivierung</span><span class="sxs-lookup"><span data-stu-id="292e7-135">Implementing In-Place Activation</span></span>](implementing-in-place-activation.md)
-   [<span data-ttu-id="292e7-136">Erstellen von verknüpften und eingebetteten Objekten aus vorhandenen Daten</span><span class="sxs-lookup"><span data-stu-id="292e7-136">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
-   [<span data-ttu-id="292e7-137">Zwischenspeichern anzeigen</span><span class="sxs-lookup"><span data-stu-id="292e7-137">View Caching</span></span>](view-caching.md)

## <a name="related-topics"></a><span data-ttu-id="292e7-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="292e7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="292e7-139">Datenübertragung</span><span class="sxs-lookup"><span data-stu-id="292e7-139">Data Transfer</span></span>](data-transfer.md)
</dt> <dt>

[<span data-ttu-id="292e7-140">Strukturierter Speicher</span><span class="sxs-lookup"><span data-stu-id="292e7-140">Structured Storage</span></span>](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 