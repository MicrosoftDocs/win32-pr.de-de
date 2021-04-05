---
title: Dragpattern/dragdroppattern-Elemente erfordern gültiges dropffect
description: Dragpattern/dragdroppattern-Elemente erfordern gültiges dropffect
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33acda19732e2ebd96182023fce9641012b50d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707164"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a><span data-ttu-id="7c8ff-103">Dragpattern/dragdroppattern-Elemente erfordern gültiges dropffect</span><span class="sxs-lookup"><span data-stu-id="7c8ff-103">DragPattern/DragDropPattern elements requires valid DropEffect</span></span>

## <a name="text"></a><span data-ttu-id="7c8ff-104">Text</span><span class="sxs-lookup"><span data-stu-id="7c8ff-104">Text</span></span>

<span data-ttu-id="7c8ff-105">Für Elemente, die Drag & Drop unterstützen, sollte ein gültiger "dropeer"-Satz festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="7c8ff-105">Elements that support Drag/Drop should have a valid 'DropEffect' set</span></span>

## <a name="type"></a><span data-ttu-id="7c8ff-106">type</span><span class="sxs-lookup"><span data-stu-id="7c8ff-106">Type</span></span>

<span data-ttu-id="7c8ff-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="7c8ff-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="7c8ff-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c8ff-108">Description</span></span>

<span data-ttu-id="7c8ff-109">Das-Element unterstützt entweder [**iuiautomationdragpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) oder [**iuiautomationdroptargetpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), aber es ist keine gültige [**dropeer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c8ff-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property set.</span></span>

<span data-ttu-id="7c8ff-110">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm verlassen, Probleme haben.</span><span class="sxs-lookup"><span data-stu-id="7c8ff-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="7c8ff-111">Der Benutzer kann nicht erkennen, welche Auswirkung dieses Objekt beim ziehen hat.</span><span class="sxs-lookup"><span data-stu-id="7c8ff-111">The user will not be able to tell what effect this object has when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="7c8ff-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="7c8ff-112">Possible causes</span></span>

-   <span data-ttu-id="7c8ff-113">Das-Element oder das übergeordnete Element hat den [**dropffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) -oder den [**dropeer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) -Typ nicht zu einem fälschlicherweise zugewiesenen Namen oder einer Bezeichnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="7c8ff-113">The element, or its parent, has not created the [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) or [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="7c8ff-114">Ein Entwickler weiß nicht, dass die Bildschirm Sprachausgaben dropeer ffect (s) lesen.</span><span class="sxs-lookup"><span data-stu-id="7c8ff-114">A developer is not aware that screen readers read DropEffect(s).</span></span>

 

 




