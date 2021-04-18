---
description: Implementieren von Kontextmenü Erweiterungen
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementieren von Kontextmenü Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347600"
---
# <a name="implementing-context-menu-extensions"></a><span data-ttu-id="e4f49-103">Implementieren von Kontextmenü Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="e4f49-103">Implementing Context Menu Extensions</span></span>

<span data-ttu-id="e4f49-104">Die WPD-Namespace Erweiterung unterstützt erweiterbare Kontextmenüs (oder Verknüpfungs Menüs).</span><span class="sxs-lookup"><span data-stu-id="e4f49-104">The WPD Namespace Extension supports extensible context (or shortcut) menus.</span></span> <span data-ttu-id="e4f49-105">Dies sind die Menüs, die angezeigt werden, wenn ein Benutzer mit der rechten Maustaste auf ein Objekt, z. b. eine Datei oder einen Ordner, klickt.</span><span class="sxs-lookup"><span data-stu-id="e4f49-105">These are the menus that appear when a user right-clicks on an object such as a file or a folder.</span></span> <span data-ttu-id="e4f49-106">Einige WPD-Anwendungen profitieren von diesen erweiterbaren Menüs, um Vorgänge für Geräte seitigen Inhalt (oder Objekte, die sich auf dem Gerät befinden) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e4f49-106">Some WPD applications will take advantage of these extensible menus to support operations on device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="e4f49-107">Erweiterbare Kontextmenüs werden von den in der folgenden Tabelle beschriebenen Schnittstellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4f49-107">Extensible context menus are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="e4f49-108">Weitere Informationen zu diesen Schnittstellen finden Sie in der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e4f49-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="e4f49-109">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e4f49-109">Interface</span></span>           | <span data-ttu-id="e4f49-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4f49-110">Description</span></span>                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f49-111">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="e4f49-111">IContextMenu</span></span>        | <span data-ttu-id="e4f49-112">Die Windows Vista-Shell Ruft die Methoden in dieser Schnittstelle auf, um das neue Kontextmenü mit dem angegebenen Objekt zu erstellen oder zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="e4f49-112">The Windows Vista Shell calls the methods in this interface to create or merge the new context menu with the given object.</span></span> |
| <span data-ttu-id="e4f49-113">IDataObject</span><span class="sxs-lookup"><span data-stu-id="e4f49-113">IDataObject</span></span>         | <span data-ttu-id="e4f49-114">Wird verwendet, um das PIDL-Array des Kontextmenüs an den Kontextmenü Handler zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="e4f49-114">Used to pass the context menu's PIDL array to the context menu handler.</span></span>                                                    |
| <span data-ttu-id="e4f49-115">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="e4f49-115">IPropertySetStorage</span></span> | <span data-ttu-id="e4f49-116">Diese Schnittstelle wird verwendet, um WPD-Eigenschaften für das angegebene Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e4f49-116">This interface is used to retrieve WPD properties for the given object.</span></span>                                                    |
| <span data-ttu-id="e4f49-117">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="e4f49-117">IPropertyStorage</span></span>    | <span data-ttu-id="e4f49-118">Diese Schnittstelle wird auch zum Abrufen von WPD-Eigenschaften für das angegebene Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4f49-118">This interface is also used to retrieve WPD properties for the given object.</span></span>                                               |
| <span data-ttu-id="e4f49-119">Ishellextinit</span><span class="sxs-lookup"><span data-stu-id="e4f49-119">IShellExtInit</span></span>       | <span data-ttu-id="e4f49-120">Initialisiert die Windows Vista-Shellerweiterungen für das Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="e4f49-120">Initializes the Windows Vista Shell extensions for the context menu.</span></span>                                                       |
| <span data-ttu-id="e4f49-121">IStream</span><span class="sxs-lookup"><span data-stu-id="e4f49-121">IStream</span></span>             | <span data-ttu-id="e4f49-122">, Um bereitgestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="e4f49-122">To be supplied.</span></span>                                                                                                            |



 

<span data-ttu-id="e4f49-123">Kontextmenüs für WPD werden wie jedes andere Kontextmenü in Windows Vista implementiert.</span><span class="sxs-lookup"><span data-stu-id="e4f49-123">Context menus for WPD are implemented like any other context menu in Windows Vista.</span></span> <span data-ttu-id="e4f49-124">Wenn Sie bereits einen Kontextmenü Handler implementiert haben, können Sie den vorhandenen Code so ändern, dass er den Geräte seitigen Inhalt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4f49-124">If you've already implemented a context menu handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="e4f49-125">Wenn Sie noch nie einen Kontextmenü Handler erstellt haben, lesen Sie das Thema Erstellen von Kontextmenü Handlern in der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e4f49-125">If you have never created a context menu handler, see the Creating Context Menu Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="e4f49-126">Die zwei Punkte, an denen ein WPD-Kontextmenü Handler von einem anderen Handler abweicht, ist die Handlerregistrierung und die Unterstützung von Geräte seitigem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="e4f49-126">The two points at which a WPD context menu handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



