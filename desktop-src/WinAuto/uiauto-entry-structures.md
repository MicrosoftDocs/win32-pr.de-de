---
title: UI-Automatisierungs Strukturen
description: In diesem Abschnitt werden die von Benutzeroberflächenautomatisierungs-Client Anwendungen und Benutzeroberflächenautomatisierungs-Anbietern für Microsoft Win32 verwendeten Strukturen beschrieben.
ms.assetid: 37d6a7c0-6925-443b-aa21-da2a14a9ddad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55ddf9086f0714665c944a5a80e53e63eb3a91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471029"
---
# <a name="ui-automation-structures"></a><span data-ttu-id="9fa2d-103">UI-Automatisierungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="9fa2d-103">UI Automation Structures</span></span>

<span data-ttu-id="9fa2d-104">In diesem Abschnitt werden die von Benutzeroberflächenautomatisierungs-Client Anwendungen und Benutzeroberflächenautomatisierungs-Anbietern für Microsoft Win32 verwendeten Strukturen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9fa2d-104">This section describes the structures used by UI Automation client applications and UI Automation provider for Microsoft Win32.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9fa2d-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9fa2d-105">In this section</span></span>



| <span data-ttu-id="9fa2d-106">Struktur</span><span class="sxs-lookup"><span data-stu-id="9fa2d-106">Structure</span></span>                                                                            | <span data-ttu-id="9fa2d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9fa2d-107">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fa2d-108">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="9fa2d-108">**ExtendedProperty**</span></span>](/windows/desktop/api/UIAutomationClient/ns-uiautomationclient-extendedproperty)<br/>                       | <span data-ttu-id="9fa2d-109">Enthält Informationen über eine erweiterte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9fa2d-109">Contains information about an extended property.</span></span> <br/>                                  |
| [<span data-ttu-id="9fa2d-110">**Uiautomationeventinfo**</span><span class="sxs-lookup"><span data-stu-id="9fa2d-110">**UIAutomationEventInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo)<br/>       | <span data-ttu-id="9fa2d-111">Enthält Informationen über ein benutzerdefiniertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9fa2d-111">Contains information about a custom event.</span></span><br/>                                         |
| [<span data-ttu-id="9fa2d-112">**Uiautomationmethodinfo**</span><span class="sxs-lookup"><span data-stu-id="9fa2d-112">**UIAutomationMethodInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo)<br/>     | <span data-ttu-id="9fa2d-113">Enthält Informationen über eine Methode, die von einem benutzerdefinierten Steuerelement Muster unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9fa2d-113">Contains information about a method that is supported by a custom control pattern.</span></span><br/> |
| [<span data-ttu-id="9fa2d-114">**Uiautomationparameter**</span><span class="sxs-lookup"><span data-stu-id="9fa2d-114">**UIAutomationParameter**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter)<br/>       | <span data-ttu-id="9fa2d-115">Enthält Informationen zu einem Parameter eines benutzerdefinierten Steuerelement Musters.</span><span class="sxs-lookup"><span data-stu-id="9fa2d-115">Contains information about a parameter of a custom control pattern.</span></span><br/>                |
| [<span data-ttu-id="9fa2d-116">**Uiautomationpatterninfo**</span><span class="sxs-lookup"><span data-stu-id="9fa2d-116">**UIAutomationPatternInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo)<br/>   | <span data-ttu-id="9fa2d-117">Enthält Informationen über ein benutzerdefiniertes Steuerelement Muster.</span><span class="sxs-lookup"><span data-stu-id="9fa2d-117">Contains information about a custom control pattern.</span></span><br/>                               |
| [<span data-ttu-id="9fa2d-118">**Uiautomationpropertyinfo**</span><span class="sxs-lookup"><span data-stu-id="9fa2d-118">**UIAutomationPropertyInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo)<br/> | <span data-ttu-id="9fa2d-119">Enthält Informationen zu einer benutzerdefinierten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9fa2d-119">Contains information about a custom property.</span></span><br/>                                      |
| [<span data-ttu-id="9fa2d-120">**Uiachangeingefo**</span><span class="sxs-lookup"><span data-stu-id="9fa2d-120">**UiaChangeInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiachangeinfo)<br/>                                    | <span data-ttu-id="9fa2d-121">Enthält Daten zu einer Änderung der Benutzeroberflächenautomatisierungs-Änderung.</span><span class="sxs-lookup"><span data-stu-id="9fa2d-121">Contains data about a UI Automation change that occurred.</span></span><br/>                          |
| [<span data-ttu-id="9fa2d-122">**Uiapoint**</span><span class="sxs-lookup"><span data-stu-id="9fa2d-122">**UiaPoint**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiapoint)<br/>                                 | <span data-ttu-id="9fa2d-123">Enthält die Koordinaten eines Punkts.</span><span class="sxs-lookup"><span data-stu-id="9fa2d-123">Contains the coordinates of a point.</span></span> <br/>                                              |
| [<span data-ttu-id="9fa2d-124">**Uiarect**</span><span class="sxs-lookup"><span data-stu-id="9fa2d-124">**UiaRect**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect)<br/>                                   | <span data-ttu-id="9fa2d-125">Enthält die Position und Größe eines Rechtecks in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="9fa2d-125">Contains the position and size of a rectangle, in screen coordinates.</span></span><br/>              |



 

 

 





