---
title: MDI-Client Fenster (MSAA UI-Element Referenz)
description: Die Multiple Document Interface (MDI) ist eine Spezifikation, die die Standardbenutzer Oberfläche für für Windows geschriebene Anwendungen definiert. Mithilfe einer MDI-Anwendung kann ein Benutzer mehrere Dokumente gleichzeitig bearbeiten.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947672"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a><span data-ttu-id="8c397-104">MDI-Client Fenster (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="8c397-104">MDI Client Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="8c397-105">Die Multiple Document Interface (MDI) ist eine Spezifikation, die die Standardbenutzer Oberfläche für für Windows geschriebene Anwendungen definiert.</span><span class="sxs-lookup"><span data-stu-id="8c397-105">The multiple document interface (MDI) is a specification that defines the standard user interface for applications written for Windows.</span></span> <span data-ttu-id="8c397-106">Mithilfe einer MDI-Anwendung kann ein Benutzer mehrere Dokumente gleichzeitig bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8c397-106">An MDI application enables a user to work with more than one document at a time.</span></span>

<span data-ttu-id="8c397-107">Eine MDI-Anwendung verfügt über drei Arten von Fenstern: ein Rahmen Fenster, ein Client Fenster und eine Reihe von untergeordneten Fenstern.</span><span class="sxs-lookup"><span data-stu-id="8c397-107">An MDI application has three kinds of windows: a frame window, a client window, and a number of child windows.</span></span> <span data-ttu-id="8c397-108">Das Rahmen Fenster ist wie das Hauptfenster einer Anwendung und umgibt das Client Fenster.</span><span class="sxs-lookup"><span data-stu-id="8c397-108">The frame window is like the main window of an application, and it surrounds the client window.</span></span> <span data-ttu-id="8c397-109">Das Client Fenster ist ein untergeordnetes Element des Rahmen Fensters und dient als Hintergrund für die untergeordneten Fenster.</span><span class="sxs-lookup"><span data-stu-id="8c397-109">The client window is a child of the frame window and serves as the background for the child windows.</span></span> <span data-ttu-id="8c397-110">Das Client Fenster bietet auch Unterstützung für das Erstellen und Bearbeiten der untergeordneten Fenster, in denen Dokumente angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8c397-110">The client window also provides support for creating and manipulating the child windows in which documents are displayed.</span></span>

<span data-ttu-id="8c397-111">Der Fenster Klassenname für ein MDI-Client Fenster lautet "MdiClient".</span><span class="sxs-lookup"><span data-stu-id="8c397-111">The window class name for an MDI client window is "MDIClient".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="8c397-112">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="8c397-112">IAccessible Methods</span></span>

<span data-ttu-id="8c397-113">Ein MDI-Client Fenster unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="8c397-113">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="8c397-114">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="8c397-114">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="8c397-115">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="8c397-115">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="8c397-116">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="8c397-116">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="8c397-117">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="8c397-117">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="8c397-118">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c397-118">IAccessible Properties</span></span>

<span data-ttu-id="8c397-119">Ein MDI-Client Fenster unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8c397-119">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="8c397-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c397-120">Property</span></span>                                                                 | <span data-ttu-id="8c397-121">Kommentare</span><span class="sxs-lookup"><span data-stu-id="8c397-121">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c397-122">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="8c397-122">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="8c397-123">Die **childCount** -Eigenschaft ist die Anzahl der untergeordneten Fenster, in denen Dokumente angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8c397-123">The **ChildCount** property is the number of child windows in which documents are displayed.</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="8c397-124">**\_Zugriffs Fokus erhalten**</span><span class="sxs-lookup"><span data-stu-id="8c397-124">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="8c397-125">**\_accName erhalten**</span><span class="sxs-lookup"><span data-stu-id="8c397-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="8c397-126">Die **Name** -Eigenschaft ist "Workspace".</span><span class="sxs-lookup"><span data-stu-id="8c397-126">The **Name** property is "Workspace".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="8c397-127">**\_accParent erhalten**</span><span class="sxs-lookup"><span data-stu-id="8c397-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="8c397-128">Die über **geordnete** Eigenschaft ist das MDI-Rahmen Fenster.</span><span class="sxs-lookup"><span data-stu-id="8c397-128">The **Parent** property is the MDI frame window.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="8c397-129">**get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="8c397-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="8c397-130">Die **Role** -Eigenschaft ist [**Rollen \_ System \_ Client**](object-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="8c397-130">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md)</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="8c397-131">**\_Zugriffs Auswahl**</span><span class="sxs-lookup"><span data-stu-id="8c397-131">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="8c397-132">**\_accState erhalten**</span><span class="sxs-lookup"><span data-stu-id="8c397-132">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="8c397-133">Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="8c397-133">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="8c397-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8c397-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c397-135">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8c397-135">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





