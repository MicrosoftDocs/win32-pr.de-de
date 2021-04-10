---
title: Schnittstellen für Eigenschafts Bedingungen für Clients
description: In diesem Abschnitt werden Eigenschaften Bedingungs Schnittstellen für Benutzeroberflächenautomatisierungs-Clients für Microsoft Win32-Anwendungen beschrieben.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039079"
---
# <a name="property-condition-interfaces-for-clients"></a><span data-ttu-id="ba602-103">Schnittstellen für Eigenschafts Bedingungen für Clients</span><span class="sxs-lookup"><span data-stu-id="ba602-103">Property Condition Interfaces for Clients</span></span>

<span data-ttu-id="ba602-104">In diesem Abschnitt werden Eigenschaften Bedingungs Schnittstellen für Benutzeroberflächenautomatisierungs-Clients für Microsoft Win32-Anwendungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ba602-104">This section describes property condition interfaces for UI Automation clients for Microsoft Win32 applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ba602-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ba602-105">In this section</span></span>



| <span data-ttu-id="ba602-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ba602-106">Interface</span></span>                                                                                  | <span data-ttu-id="ba602-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba602-107">Description</span></span>                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba602-108">**Iuiautomationandcondition**</span><span class="sxs-lookup"><span data-stu-id="ba602-108">**IUIAutomationAndCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | <span data-ttu-id="ba602-109">Macht Eigenschaften und Methoden verfügbar, die Microsoft UI Automation-Client Anwendungen verwenden können, um Informationen über eine und eine-basierte Eigenschafts Bedingung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ba602-109">Exposes properties and methods that Microsoft UI Automation client applications can use to retrieve information about an AND-based property condition.</span></span> <br/> |
| [<span data-ttu-id="ba602-110">**Iuiautomationboolcondition**</span><span class="sxs-lookup"><span data-stu-id="ba602-110">**IUIAutomationBoolCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | <span data-ttu-id="ba602-111">Stellt eine Bedingung dar, die entweder **true** (alle Elemente auswählt) oder **false** (wählt keine Elemente) sein kann.</span><span class="sxs-lookup"><span data-stu-id="ba602-111">Represents a condition that can be either **TRUE** (selects all elements) or **FALSE** (selects no elements).</span></span><br/>                                           |
| [<span data-ttu-id="ba602-112">**Iuiautomationcondition**</span><span class="sxs-lookup"><span data-stu-id="ba602-112">**IUIAutomationCondition**</span></span>](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | <span data-ttu-id="ba602-113">Dies ist die primäre Schnittstelle für Bedingungen, die beim Suchen nach Elementen in der Benutzeroberflächenautomatisierungs-Struktur beim Filtern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba602-113">This is the primary interface for conditions used in filtering when searching for elements in the UI Automation tree.</span></span><br/>                                   |
| [<span data-ttu-id="ba602-114">**Iuiautomationnotcondition**</span><span class="sxs-lookup"><span data-stu-id="ba602-114">**IUIAutomationNotCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | <span data-ttu-id="ba602-115">Stellt eine Bedingung dar, die das negative einer anderen Bedingung ist.</span><span class="sxs-lookup"><span data-stu-id="ba602-115">Represents a condition that is the negative of another condition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="ba602-116">**Iuiautomationorcondition**</span><span class="sxs-lookup"><span data-stu-id="ba602-116">**IUIAutomationOrCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | <span data-ttu-id="ba602-117">Stellt eine Bedingung dar, die aus mehreren Bedingungen besteht, von denen mindestens ein true sein muss.</span><span class="sxs-lookup"><span data-stu-id="ba602-117">Represents a condition made up of multiple conditions, at least one of which must be true.</span></span><br/>                                                              |
| [<span data-ttu-id="ba602-118">**Iuiautomationpropertycondition**</span><span class="sxs-lookup"><span data-stu-id="ba602-118">**IUIAutomationPropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | <span data-ttu-id="ba602-119">Stellt eine Bedingung dar, die auf einem Eigenschafts Wert basiert, mit dem Benutzeroberflächenautomatisierungs-Elemente gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="ba602-119">Represents a condition based on a property value that is used to find UI Automation elements.</span></span><br/>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="ba602-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ba602-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba602-121">UI-Automatisierungs Clients</span><span class="sxs-lookup"><span data-stu-id="ba602-121">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

