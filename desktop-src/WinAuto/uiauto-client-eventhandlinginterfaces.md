---
title: Ereignis Behandlungs Schnittstellen für Clients
description: In diesem Abschnitt werden die Schnittstellen zur Ereignis Behandlung für nicht verwaltete Benutzeroberflächenautomatisierungs-Client Anwendungen beschrieben.
ms.assetid: ce9c4044-f46b-42b7-af44-05aee728a0e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458be6fcf5ce47f285d46c0e61f80e0897f15613
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340236"
---
# <a name="event-handling-interfaces-for-clients"></a><span data-ttu-id="4bfe9-103">Ereignis Behandlungs Schnittstellen für Clients</span><span class="sxs-lookup"><span data-stu-id="4bfe9-103">Event Handling Interfaces for Clients</span></span>

<span data-ttu-id="4bfe9-104">In diesem Abschnitt werden die Schnittstellen zur Ereignis Behandlung für nicht verwaltete Benutzeroberflächenautomatisierungs-Client Anwendungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4bfe9-104">This section describes the event handling interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4bfe9-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4bfe9-105">In this section</span></span>



| <span data-ttu-id="4bfe9-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4bfe9-106">Interface</span></span>                                                                                                              | <span data-ttu-id="4bfe9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bfe9-107">Description</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bfe9-108">**Iuiautomationchangeseventhandler**</span><span class="sxs-lookup"><span data-stu-id="4bfe9-108">**IUIAutomationChangesEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationchangeseventhandler)<br/>                         | <span data-ttu-id="4bfe9-109">Macht eine Methode zur Behandlung von Ereignissen der Microsoft-Benutzeroberflächen Automatisierung verfügbar, die auftreten, wenn eine Eigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4bfe9-109">Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.</span></span><br/>                      |
| [<span data-ttu-id="4bfe9-110">**Iuiautomationeventhandler**</span><span class="sxs-lookup"><span data-stu-id="4bfe9-110">**IUIAutomationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)<br/>                                       | <span data-ttu-id="4bfe9-111">Macht eine Methode zum Behandeln von Benutzeroberflächenautomatisierungs-Ereignissen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4bfe9-111">Exposes a method to handle UI Automation events.</span></span><br/>                                                                      |
| [<span data-ttu-id="4bfe9-112">**Iuiautomationfocuschangedebug-thandler**</span><span class="sxs-lookup"><span data-stu-id="4bfe9-112">**IUIAutomationFocusChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)<br/>               | <span data-ttu-id="4bfe9-113">Macht eine Methode zum Behandeln von Ereignissen verfügbar, die ausgelöst werden, wenn der Tastaturfokus zu einem anderen Benutzeroberflächenautomatisierungs-Element wechselt.</span><span class="sxs-lookup"><span data-stu-id="4bfe9-113">Exposes a method to handle events that are raised when the keyboard focus moves to another UI Automation element.</span></span><br/>     |
| [<span data-ttu-id="4bfe9-114">**Iuiautomationnotificationeventhandler**</span><span class="sxs-lookup"><span data-stu-id="4bfe9-114">**IUIAutomationNotificationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)<br/>               | <span data-ttu-id="4bfe9-115">Macht eine Methode zum Behandeln von Benachrichtigungs Ereignissen für die Benutzeroberflächen Automatisierung verfügbar</span><span class="sxs-lookup"><span data-stu-id="4bfe9-115">Exposes a method to handle UI Automation notification events.</span></span><br/>                                                         |
| [<span data-ttu-id="4bfe9-116">**Iuiautomationpropertychangeabventhandler**</span><span class="sxs-lookup"><span data-stu-id="4bfe9-116">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)<br/>         | <span data-ttu-id="4bfe9-117">Macht eine Methode verfügbar, um Benutzeroberflächenautomatisierungs-Ereignisse zu behandeln, die beim Ändern einer Eigenschaft auftreten.</span><span class="sxs-lookup"><span data-stu-id="4bfe9-117">Exposes a method to handle UI Automation events that occur when a property is changed.</span></span><br/>                                |
| [<span data-ttu-id="4bfe9-118">**Iuiautomationstructurechangeabventhandler**</span><span class="sxs-lookup"><span data-stu-id="4bfe9-118">**IUIAutomationStructureChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler)<br/>       | <span data-ttu-id="4bfe9-119">Macht eine Methode verfügbar, um Ereignisse zu behandeln, die auftreten, wenn die Benutzeroberflächenautomatisierungs-Struktur geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4bfe9-119">Exposes a method to handle events that occur when the UI Automation tree structure is changed.</span></span><br/>                        |
| [<span data-ttu-id="4bfe9-120">**Iuiautomationtextedittextchangedebug**</span><span class="sxs-lookup"><span data-stu-id="4bfe9-120">**IUIAutomationTextEditTextChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextedittextchangedeventhandler)<br/> | <span data-ttu-id="4bfe9-121">Macht eine Methode verfügbar, um Ereignisse zu behandeln, die auftreten, wenn die Benutzeroberflächen Automatisierung ein Text Änderungs Ereignis aus Text Bearbeitungs Steuerelementen meldet.</span><span class="sxs-lookup"><span data-stu-id="4bfe9-121">Exposes a method to handle events that occur when UI Automation reports a text-changed event from text edit controls.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="4bfe9-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4bfe9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bfe9-123">UI-Automatisierungs Clients</span><span class="sxs-lookup"><span data-stu-id="4bfe9-123">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





