---
title: Erstellen von verknüpften und eingebetteten Objekten aus vorhandenen Daten
description: Erstellen von verknüpften und eingebetteten Objekten aus vorhandenen Daten
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714267"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a><span data-ttu-id="941fb-103">Erstellen von verknüpften und eingebetteten Objekten aus vorhandenen Daten</span><span class="sxs-lookup"><span data-stu-id="941fb-103">Creating Linked and Embedded Objects from Existing Data</span></span>

<span data-ttu-id="941fb-104">Ein Benutzer assembliert in der Regel ein Verbund Dokument, indem es entweder die Zwischenablage oder Drag & Drop verwendet, um ein Datenobjekt aus seiner Serveranwendung in die Containeranwendung des Benutzers zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="941fb-104">A user typically assembles a compound document by using either the clipboard or drag and drop to copy a data object from its server application to the user's container application.</span></span> <span data-ttu-id="941fb-105">Bei Anwendungen, die OLE unterstützen, kann der Benutzer die Übertragung entweder vom Server oder vom Container initiieren.</span><span class="sxs-lookup"><span data-stu-id="941fb-105">With applications that support OLE, the user can initiate the transfer from either the server or the container.</span></span> <span data-ttu-id="941fb-106">Der Server kann z. b. Daten in die Zwischenablage in der Serveranwendung kopieren, dann zur Containeranwendung wechseln und ein spezielles/eingebettetes Objekt einfügen oder einen entsprechenden Menübefehl Einfügen, um ein neues eingebettetes Objekt aus den ausgewählten Daten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="941fb-106">For example, the server can copy data to the clipboard in the server application, then switch to the container application and choose Paste Special/Embedded Object or an equivalent menu command to create a new embedded object from the selected data.</span></span> <span data-ttu-id="941fb-107">Oder der Benutzer kann die Daten von einer Anwendung in die andere ziehen.</span><span class="sxs-lookup"><span data-stu-id="941fb-107">Or, the user can drag the data from one application to the other.</span></span> <span data-ttu-id="941fb-108">Der Prozess ähnelt dem Erstellen eines verknüpften Objekts.</span><span class="sxs-lookup"><span data-stu-id="941fb-108">The process is similar for creating a linked object.</span></span>

> [!Note]  
> <span data-ttu-id="941fb-109">Eine Anwendung, die sowohl als OLE-Server als auch als Container fungiert, kann eine Auswahl ihrer eigenen Daten verwenden, um ein eingebettetes oder verknüpftes Objekt an einem neuen Speicherort innerhalb desselben Dokuments zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="941fb-109">An application that functions as both OLE server and container can use a selection of its own data to create an embedded or linked object at a new location within the same document.</span></span>

 

<span data-ttu-id="941fb-110">Die Datenübertragung zwischen OLE-Server-und Container Anwendungen basiert auf einheitlicher Datenübertragung, wie in [Datenübertragung](data-transfer.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="941fb-110">Data transfer between OLE server and container applications is built on uniform data transfer, as described in [Data Transfer](data-transfer.md).</span></span> <span data-ttu-id="941fb-111">OLE-Server und Objekt Handler implementieren [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , um Ihre Daten für Übertragungen über die Zwischenablage oder Drag & Drop verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="941fb-111">OLE servers and object handlers implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) in order to make their data available for transfers using either the clipboard or drag and drop.</span></span> <span data-ttu-id="941fb-112">OLE-Objekte unterstützen alle üblichen Zwischenablage Formate.</span><span class="sxs-lookup"><span data-stu-id="941fb-112">OLE objects support all the usual clipboard formats.</span></span> <span data-ttu-id="941fb-113">Außerdem unterstützen Sie sechs Zwischenablage Formate, die die Erstellung von verknüpften und eingebetteten Objekten aus einem ausgewählten Datenobjekt unterstützen.</span><span class="sxs-lookup"><span data-stu-id="941fb-113">In addition, they support six clipboard formats that support the creation of linked and embedded objects from a selected data object.</span></span>

<span data-ttu-id="941fb-114">OLE-Zwischenablage Formate beschreiben Datenobjekte, die beim Ablegen oder Einfügen in OLE-Containern zu eingebetteten oder verknüpften Verbund Dokument Objekten werden.</span><span class="sxs-lookup"><span data-stu-id="941fb-114">OLE clipboard formats describe data objects that, upon being dropped or pasted in OLE containers, are to become embedded or linked compound-document objects.</span></span> <span data-ttu-id="941fb-115">Das Datenobjekt stellt den Container Anwendungen diese Formate in der Reihenfolge ihrer Genauigkeit als Beschreibungen der Daten zur Folge.</span><span class="sxs-lookup"><span data-stu-id="941fb-115">The data object presents these formats to container applications in order of their fidelity as descriptions of the data.</span></span> <span data-ttu-id="941fb-116">Anders ausgedrückt: das-Objekt stellt zuerst das Format dar, das es am besten darstellt, gefolgt vom nächst optimalen Format usw.</span><span class="sxs-lookup"><span data-stu-id="941fb-116">In other words, the object presents first the format that best represents it, followed by the next best format, and so on.</span></span> <span data-ttu-id="941fb-117">Diese absichtliche Reihenfolge fördert eine Containeranwendung, um das bestmögliche Format zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="941fb-117">This intentional ordering encourages a container application to use the best possible format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="941fb-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="941fb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="941fb-119">Verbund Dokumente</span><span class="sxs-lookup"><span data-stu-id="941fb-119">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="941fb-120">Datenübertragung</span><span class="sxs-lookup"><span data-stu-id="941fb-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




