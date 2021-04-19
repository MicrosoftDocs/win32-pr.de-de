---
description: Implementieren von Eigenschaften Blatt Erweiterungen
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementieren von Eigenschaften Blatt Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369080"
---
# <a name="implementing-property-sheet-extensions"></a><span data-ttu-id="05c3c-103">Implementieren von Eigenschaften Blatt Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="05c3c-103">Implementing Property Sheet Extensions</span></span>

<span data-ttu-id="05c3c-104">Die WPD-Namespace Erweiterung unterstützt erweiterbare Eigenschaften Blätter.</span><span class="sxs-lookup"><span data-stu-id="05c3c-104">The WPD Namespace Extension supports extensible property sheets.</span></span> <span data-ttu-id="05c3c-105">Dies sind die Eigenschaften Dialogfelder, die angezeigt werden, wenn ein Benutzer mit der rechten Maustaste auf ein Objekt, z. b. eine Datei oder einen Ordner, klickt und **Eigenschaften** auswählt.</span><span class="sxs-lookup"><span data-stu-id="05c3c-105">These are the property dialogs that appear when a user right-clicks on an object, such as a file or a folder, and selects **Properties**.</span></span> <span data-ttu-id="05c3c-106">Einige WPD-Anwendungen nutzen diese erweiterbaren Eigenschaften Blätter, um die Eigenschaften für Geräte seitigen Inhalt (oder Objekte, die sich auf dem Gerät befinden) anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="05c3c-106">Some WPD applications will take advantage of these extensible property sheets to display properties for device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="05c3c-107">Erweiterbare Eigenschaften Blätter werden von den in der folgenden Tabelle beschriebenen Schnittstellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05c3c-107">Extensible property sheets are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="05c3c-108">Weitere Informationen zu diesen Schnittstellen finden Sie in der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="05c3c-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="05c3c-109">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="05c3c-109">Interface</span></span>           | <span data-ttu-id="05c3c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05c3c-110">Description</span></span>                                                                  |
|---------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="05c3c-111">IDataObject</span><span class="sxs-lookup"><span data-stu-id="05c3c-111">IDataObject</span></span>         | <span data-ttu-id="05c3c-112">Wird verwendet, um das PIDL-Array des Kontextmenüs an den Kontextmenü Handler zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="05c3c-112">Used to pass the context menu's PIDL array to the context menu handler.</span></span>      |
| <span data-ttu-id="05c3c-113">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="05c3c-113">IPropertySetStorage</span></span> | <span data-ttu-id="05c3c-114">Diese Schnittstelle wird verwendet, um WPD-Eigenschaften für das angegebene Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="05c3c-114">This interface is used to retrieve WPD properties for the given object.</span></span>      |
| <span data-ttu-id="05c3c-115">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="05c3c-115">IPropertyStorage</span></span>    | <span data-ttu-id="05c3c-116">Diese Schnittstelle wird auch zum Abrufen von WPD-Eigenschaften für das angegebene Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="05c3c-116">This interface is also used to retrieve WPD properties for the given object.</span></span> |
| <span data-ttu-id="05c3c-117">Ishellextinit</span><span class="sxs-lookup"><span data-stu-id="05c3c-117">IShellExtInit</span></span>       | <span data-ttu-id="05c3c-118">Initialisiert die Windows Vista-Shellerweiterungen für das Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="05c3c-118">Initializes the Windows Vista Shell extensions for the context menu.</span></span>         |
| <span data-ttu-id="05c3c-119">Ishellpropsheetext</span><span class="sxs-lookup"><span data-stu-id="05c3c-119">IShellPropSheetExt</span></span>  | <span data-ttu-id="05c3c-120">Unterstützt das Hinzufügen von Eigenschaften Blatt Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="05c3c-120">Supports addition of property sheet extensions.</span></span>                              |



 

<span data-ttu-id="05c3c-121">Eigenschaften Blätter für WPD werden wie jedes andere Eigenschaften Blatt in Windows Vista implementiert.</span><span class="sxs-lookup"><span data-stu-id="05c3c-121">Property sheets for WPD are implemented like any other property sheet in Windows Vista.</span></span> <span data-ttu-id="05c3c-122">Wenn Sie bereits einen Eigenschaften Blatt Handler implementiert haben, können Sie den vorhandenen Code so ändern, dass er den Geräte seitigen Inhalt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05c3c-122">If you've already implemented a property sheet handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="05c3c-123">Wenn Sie noch nie einen Kontextmenü Handler erstellt haben, lesen Sie das Thema Erstellen von Eigenschaften Blatt Handlern in der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="05c3c-123">If you've never created a context menu handler, see the Creating Property Sheet Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="05c3c-124">Die zwei Punkte, an denen ein WPD-Eigenschaften Blatt Handler von einem anderen Handler abweicht, ist die Handlerregistrierung und die Unterstützung von Geräte seitigem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="05c3c-124">The two points at which a WPD property sheet handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



