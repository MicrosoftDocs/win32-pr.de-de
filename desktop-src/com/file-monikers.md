---
title: Dateimoniker
description: Dateimoniker
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309635"
---
# <a name="file-monikers"></a><span data-ttu-id="e4077-103">Dateimoniker</span><span class="sxs-lookup"><span data-stu-id="e4077-103">File Monikers</span></span>

<span data-ttu-id="e4077-104">*Dateimoniker* sind die einfachste Monikerklasse.</span><span class="sxs-lookup"><span data-stu-id="e4077-104">*File monikers* are the simplest moniker class.</span></span> <span data-ttu-id="e4077-105">Dateimoniker können verwendet werden, um alle Objekte zu identifizieren, die in einer eigenen Datei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e4077-105">File monikers can be used to identify any object that is stored in its own file.</span></span> <span data-ttu-id="e4077-106">Ein dateimoniker fungiert als Wrapper für den Pfadnamen, den das systemeigene Dateisystem der Datei zuweist.</span><span class="sxs-lookup"><span data-stu-id="e4077-106">A file moniker acts as a wrapper for the path name the native file system assigns to the file.</span></span> <span data-ttu-id="e4077-107">Das Aufrufen von [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) für diesen Moniker würde dazu führen, dass dieses Objekt aktiviert wird und dann einen Schnittstellen Zeiger auf das-Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e4077-107">Calling [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) for this moniker would cause this object to be activated and then would return an interface pointer to the object.</span></span> <span data-ttu-id="e4077-108">Die Quelle des Objekts, das vom Moniker benannt wird, muss eine Implementierung der [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) -Schnittstelle bereitstellen, um die Bindung eines dateimonikers zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e4077-108">The source of the object named by the moniker must provide an implementation of the [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) interface to support binding a file moniker.</span></span> <span data-ttu-id="e4077-109">Dateimoniker können entweder einen kompletten oder einen relativen Pfad darstellen.</span><span class="sxs-lookup"><span data-stu-id="e4077-109">File monikers can represent either a complete or a relative path.</span></span>

<span data-ttu-id="e4077-110">Beispielsweise würde der dateimoniker für ein Tabellenobjekt, das als Datei C: WorkMySheet.xls gespeichert ist, Informationen enthalten, die dem \\ \\ Pfadnamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e4077-110">For example, the file moniker for a spreadsheet object stored as the file C:\\Work\\MySheet.xls would contain information equivalent to that path name.</span></span> <span data-ttu-id="e4077-111">Der Moniker würde jedoch nicht notwendigerweise aus derselben Zeichenfolge bestehen.</span><span class="sxs-lookup"><span data-stu-id="e4077-111">The moniker would not necessarily consist of the same string, however.</span></span> <span data-ttu-id="e4077-112">Die Zeichenfolge ist nur Ihr *Display Name*, eine Darstellung der Inhalte des Monikers, die für einen Endbenutzer von Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="e4077-112">The string is just its *displayÂ name*, a representation of the moniker's contents that is meaningful to an end user.</span></span> <span data-ttu-id="e4077-113">Der Anzeige Name, der über die [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) -Methode verfügbar ist, wird nur verwendet, wenn ein Moniker für einen Endbenutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e4077-113">The display name, which is available through the [**IMoniker::GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) method, is used only when displaying a moniker to an end user.</span></span> <span data-ttu-id="e4077-114">Diese Methode ruft den anzeigen Amen für jede der Monikerklassen ab.</span><span class="sxs-lookup"><span data-stu-id="e4077-114">This method gets the display name for any of the moniker classes.</span></span> <span data-ttu-id="e4077-115">Intern kann der Moniker die gleichen Informationen in einem Format speichern, das für die Ausführung von monikervorgängen effizienter ist, aber für Benutzer nicht sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="e4077-115">Internally, the moniker may store the same information in a format that is more efficient for performing moniker operations but isn't meaningful to users.</span></span> <span data-ttu-id="e4077-116">Wenn das gleiche Objekt dann durch einen Aufrufen der [**BindTo Object**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) -Methode gebunden wird, wird das Objekt aktiviert, wahrscheinlich durch Laden der Datei in das Arbeitsblatt.</span><span class="sxs-lookup"><span data-stu-id="e4077-116">Then, when this same object is bound through a call to the [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) method, the object would be activated, probably by loading the file into the spreadsheet.</span></span>

<span data-ttu-id="e4077-117">OLE bietet monikeranbietern die Hilfsfunktion " [**kreatefilemoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) ", die ein dateimonikerobjekt erstellt und seinen Zeiger auf den Anbieter zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e4077-117">OLE offers moniker providers the helper function [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) that creates a file moniker object and returns its pointer to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4077-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4077-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4077-119">Anti-Moniker</span><span class="sxs-lookup"><span data-stu-id="e4077-119">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="e4077-120">Klassenmoniker</span><span class="sxs-lookup"><span data-stu-id="e4077-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="e4077-121">Zusammengesetzte Moniker</span><span class="sxs-lookup"><span data-stu-id="e4077-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="e4077-122">Elementmoniker</span><span class="sxs-lookup"><span data-stu-id="e4077-122">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="e4077-123">Zeigermoniker</span><span class="sxs-lookup"><span data-stu-id="e4077-123">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




