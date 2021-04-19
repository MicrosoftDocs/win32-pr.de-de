---
title: Monikerclients
description: Monikerclients müssen zunächst einen Moniker erhalten, und es gibt mehrere Möglichkeiten, wie ein monikerclient einen Moniker erhalten kann.
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341422"
---
# <a name="moniker-clients"></a><span data-ttu-id="7ed29-103">Monikerclients</span><span class="sxs-lookup"><span data-stu-id="7ed29-103">Moniker Clients</span></span>

<span data-ttu-id="7ed29-104">Monikerclients müssen zunächst einen Moniker erhalten, und es gibt mehrere Möglichkeiten, wie ein monikerclient einen Moniker erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="7ed29-104">Moniker clients must start by getting a moniker, and there are several ways for a moniker client to get a moniker.</span></span> <span data-ttu-id="7ed29-105">Wenn z. b. der Endbenutzer in OLE-Verbund Dokumenten ein verknüpftes Element erstellt (entweder mithilfe des Dialog Felds " **Objekt einfügen** ", der Zwischenablage oder Drag & amp; Drop), wird ein Moniker als Teil des verknüpften Elements eingebettet.</span><span class="sxs-lookup"><span data-stu-id="7ed29-105">For example, in OLE compound documents, when the end user creates a linked item (either using **Insert Object** dialog, the clipboard, or drag-and drop), a moniker is embedded as part of the linked item.</span></span> <span data-ttu-id="7ed29-106">In diesem Fall hat der Programmierer minimalen Kontakt mit Monikern.</span><span class="sxs-lookup"><span data-stu-id="7ed29-106">In that case, the programmer has minimal contact with monikers.</span></span> <span data-ttu-id="7ed29-107">Wenn Sie über einen Schnittstellen Zeiger auf ein Objekt verfügen, das die [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) -Schnittstelle implementiert, können Sie dieses Programm gesteuert verwenden, um einen Moniker zu erhalten, und es gibt Methoden für andere Schnittstellen, die für die Rückgabe von Monikern definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7ed29-107">Programmatically, if you have an interface pointer to an object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface, you can use that to get a moniker, and there are methods on other interfaces that are defined to return monikers.</span></span>

<span data-ttu-id="7ed29-108">Es gibt verschiedene Arten von Monikern, die zur Identifizierung verschiedener Arten von Objekten verwendet werden, aber für einen monikerclient sehen alle Moniker identisch aus.</span><span class="sxs-lookup"><span data-stu-id="7ed29-108">There are different kinds of monikers, which are used to identify different kinds of objects, but to a moniker client, all monikers look the same.</span></span> <span data-ttu-id="7ed29-109">Ein monikerclient ruft einfach [**IMoniker:: bindjeobject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) für einen Moniker auf und Ruft einen Schnittstellen Zeiger auf das Objekt ab, das der Moniker identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7ed29-109">A moniker client simply calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on a moniker and gets an interface pointer to the object that the moniker identifies.</span></span> <span data-ttu-id="7ed29-110">Unabhängig davon, ob der Moniker ein Objekt so groß wie ein gesamtes Arbeitsblatt oder so klein wie eine einzelne Zelle in einer Kalkulations Tabelle identifiziert, gibt der Aufruf von **BindToObject** einen Zeiger auf dieses Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="7ed29-110">Whether the moniker identifies an object as large as an entire spreadsheet or as small as a single cell within a spreadsheet, calling **BindToObject** will return a pointer to that object.</span></span> <span data-ttu-id="7ed29-111">Wenn das Objekt bereits ausgeführt wird, wird es von **bindtoken** im Arbeitsspeicher gefunden.</span><span class="sxs-lookup"><span data-stu-id="7ed29-111">If the object is already running, **BindToObject** will find it in memory.</span></span> <span data-ttu-id="7ed29-112">Wenn das Objekt passiv auf dem Datenträger gespeichert wird, findet " **BindTo Object** " einen Server für dieses Objekt, führt den Server aus und versetzt den Server in den Status "wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="7ed29-112">If the object is stored passively on disk, **BindToObject** will locate a server for that object, run the server, and have the server bring the object into the running state.</span></span> <span data-ttu-id="7ed29-113">Alle Details des Bindungs Prozesses werden im monikerclient ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="7ed29-113">All the details of the binding process are hidden from the moniker client.</span></span> <span data-ttu-id="7ed29-114">Daher ist es für einen monikerclient sehr einfach, den Moniker zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ed29-114">Thus, for a moniker client, using the moniker is very simple.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ed29-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ed29-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed29-116">Monikeranbieter</span><span class="sxs-lookup"><span data-stu-id="7ed29-116">Moniker Providers</span></span>](moniker-providers.md)
</dt> <dt>

[<span data-ttu-id="7ed29-117">OLE-Monikerimplementierungen</span><span class="sxs-lookup"><span data-stu-id="7ed29-117">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




