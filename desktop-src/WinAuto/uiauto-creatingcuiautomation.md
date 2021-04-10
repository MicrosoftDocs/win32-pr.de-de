---
title: Erstellen des cuiautomation-Objekts
description: In diesem Abschnitt wird beschrieben, wie Sie mit dem Schreiben einer Microsoft UI Automation-Client Anwendung beginnen, indem Sie ein Objekt instanziieren, das iuiautomation implementiert.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- Clients, Erstellen eines cuiautomation-Objekts
- Clients, cuiautomation-Objekt
- Benutzeroberflächenautomatisierungs-, cuiautomation-Objekt
- UI-Automatisierung, Erstellen eines cuiautomation-Objekts
- cuiautomation-Objekt wird erstellt
- Cuiautomation-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948799"
---
# <a name="creating-the-cuiautomation-object"></a><span data-ttu-id="1f329-109">Erstellen des cuiautomation-Objekts</span><span class="sxs-lookup"><span data-stu-id="1f329-109">Creating the CUIAutomation Object</span></span>

<span data-ttu-id="1f329-110">In diesem Abschnitt wird beschrieben, wie Sie mit dem Schreiben einer Microsoft UI Automation-Client Anwendung beginnen, indem Sie ein Objekt instanziieren, das [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)implementiert.</span><span class="sxs-lookup"><span data-stu-id="1f329-110">This section describes how to get started writing a Microsoft UI Automation client application by instantiating an object that implements [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>

<span data-ttu-id="1f329-111">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="1f329-111">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1f329-112">Das cuiautomation-Objekt</span><span class="sxs-lookup"><span data-stu-id="1f329-112">The CUIAutomation Object</span></span>](#the-cuiautomation-object)
-   [<span data-ttu-id="1f329-113">Erstellen des Objekts</span><span class="sxs-lookup"><span data-stu-id="1f329-113">Creating the Object</span></span>](#creating-the-object)
-   [<span data-ttu-id="1f329-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1f329-114">Related topics</span></span>](#related-topics)

## <a name="the-cuiautomation-object"></a><span data-ttu-id="1f329-115">Das cuiautomation-Objekt</span><span class="sxs-lookup"><span data-stu-id="1f329-115">The CUIAutomation Object</span></span>

<span data-ttu-id="1f329-116">Der erste Schritt bei der Verwendung der Benutzeroberflächen Automatisierung besteht darin, ein Objekt der Klasse " [**cuiautomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) " zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1f329-116">The first step in using UI Automation is to create an object of the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) class.</span></span> <span data-ttu-id="1f329-117">Dieses Objekt macht die [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstelle verfügbar, die das Gateway für alle anderen Objekte und Schnittstellen ist, die von Client Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f329-117">This object exposes the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface, which is the gateway to all the other objects and interfaces that are used by client applications.</span></span> <span data-ttu-id="1f329-118">Unter anderem wird **iuiautomation** für die folgenden Aufgaben verwendet:</span><span class="sxs-lookup"><span data-stu-id="1f329-118">Among other things, **IUIAutomation** is used for the following tasks:</span></span>

-   <span data-ttu-id="1f329-119">Ereignisse werden abonniert.</span><span class="sxs-lookup"><span data-stu-id="1f329-119">Subscribing to events.</span></span>
-   <span data-ttu-id="1f329-120">Erstellen von Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="1f329-120">Creating conditions.</span></span> <span data-ttu-id="1f329-121">Bedingungen sind Objekte, die verwendet werden, um den Suchbereich für Benutzeroberflächenautomatisierungs-Elemente einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="1f329-121">Conditions are objects used to narrow the scope of searches for UI Automation elements.</span></span>
-   <span data-ttu-id="1f329-122">Abrufen von Benutzeroberflächenautomatisierungs-Elementen direkt vom Desktop (dem Stamm Element) oder von Bildschirm Koordinaten oder Fenster Handles.</span><span class="sxs-lookup"><span data-stu-id="1f329-122">Obtaining UI Automation elements directly from the desktop (the root element), or from screen coordinates or window handles.</span></span>
-   <span data-ttu-id="1f329-123">Erstellen von Tree Walker-Objekten, die zum Navigieren in der Hierarchie der Benutzeroberflächenautomatisierungs-Elemente verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="1f329-123">Creating tree walker objects that can be used to navigate the hierarchy of UI Automation elements.</span></span>
-   <span data-ttu-id="1f329-124">Datentypen werden umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="1f329-124">Converting data types.</span></span>

## <a name="creating-the-object"></a><span data-ttu-id="1f329-125">Erstellen des Objekts</span><span class="sxs-lookup"><span data-stu-id="1f329-125">Creating the Object</span></span>

<span data-ttu-id="1f329-126">Führen Sie die folgenden Schritte aus, um die Verwendung der Benutzeroberflächen Automatisierung in Ihrer Anwendung zu starten:</span><span class="sxs-lookup"><span data-stu-id="1f329-126">To get started using UI Automation in your application, take the following steps:</span></span>

-   <span data-ttu-id="1f329-127">Fügen Sie "uiautomation. h" in Ihre Projekt Header ein.</span><span class="sxs-lookup"><span data-stu-id="1f329-127">Include UIAutomation.h in your project headers.</span></span> <span data-ttu-id="1f329-128">Uiautomation. h führt die anderen Header ein, die die API definieren.</span><span class="sxs-lookup"><span data-stu-id="1f329-128">UIAutomation.h brings in the other headers that define the API.</span></span>
-   <span data-ttu-id="1f329-129">Deklarieren Sie einen Zeiger auf [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span><span class="sxs-lookup"><span data-stu-id="1f329-129">Declare a pointer to [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>
-   <span data-ttu-id="1f329-130">Initialisieren Sie die Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="1f329-130">Initialize the Component Object Model (COM).</span></span>
-   <span data-ttu-id="1f329-131">Erstellen Sie eine Instanz von [**cuiautomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , und rufen Sie die [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstelle in Ihrem Zeiger ab.</span><span class="sxs-lookup"><span data-stu-id="1f329-131">Create an instance of [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) and retrieve the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in your pointer.</span></span>

<span data-ttu-id="1f329-132">Die folgende Beispiel Funktion initialisiert com und erstellt dann das [**cuiautomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) -Objekt, das die [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstelle im *ppautomation* -Zeiger abruft.</span><span class="sxs-lookup"><span data-stu-id="1f329-132">The following example function initializes COM, and then creates the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) object, retrieving the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in the *ppAutomation* pointer.</span></span>


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a><span data-ttu-id="1f329-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1f329-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1f329-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="1f329-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1f329-135">Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="1f329-135">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="1f329-136">Abrufen von Benutzeroberflächenautomatisierungs-Elementen</span><span class="sxs-lookup"><span data-stu-id="1f329-136">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> </dl>

 

 