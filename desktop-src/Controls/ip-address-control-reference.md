---
title: IP-Adressensteuerelement
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit IP-Adress Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471069"
---
# <a name="ip-address-control"></a><span data-ttu-id="5eb19-103">IP-Adressensteuerelement</span><span class="sxs-lookup"><span data-stu-id="5eb19-103">IP Address Control</span></span>

<span data-ttu-id="5eb19-104">Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit IP-Adress Steuerelementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5eb19-104">This section contains information about the programming elements used with IP address controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="5eb19-105">Übersichten</span><span class="sxs-lookup"><span data-stu-id="5eb19-105">Overviews</span></span>



| <span data-ttu-id="5eb19-106">Thema</span><span class="sxs-lookup"><span data-stu-id="5eb19-106">Topic</span></span>                                          | <span data-ttu-id="5eb19-107">Inhalte</span><span class="sxs-lookup"><span data-stu-id="5eb19-107">Contents</span></span>                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eb19-108">IP-Adress Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="5eb19-108">IP Address Controls</span></span>](ip-address-controls.md) | <span data-ttu-id="5eb19-109">Ein IP-Adress Steuerelement (Internet Protocol) ermöglicht es dem Benutzer, eine IP-Adresse in einem leicht verständlichen Format einzugeben.</span><span class="sxs-lookup"><span data-stu-id="5eb19-109">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span><br/> |



 

### <a name="macros"></a><span data-ttu-id="5eb19-110">Makros</span><span class="sxs-lookup"><span data-stu-id="5eb19-110">Macros</span></span>



| <span data-ttu-id="5eb19-111">Thema</span><span class="sxs-lookup"><span data-stu-id="5eb19-111">Topic</span></span>                                         | <span data-ttu-id="5eb19-112">Inhalte</span><span class="sxs-lookup"><span data-stu-id="5eb19-112">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eb19-113">**erste \_ IP-Adresse**</span><span class="sxs-lookup"><span data-stu-id="5eb19-113">**FIRST\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | <span data-ttu-id="5eb19-114">Extrahiert den Wert von Feld 0 aus einer gepackten IP-Adresse, die mit der [**IPM \_ GetAddress**](ipm-getaddress.md) -Nachricht abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5eb19-114">Extracts the field 0 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="5eb19-115">**vierte \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="5eb19-115">**FOURTH\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | <span data-ttu-id="5eb19-116">Extrahiert den Wert von Feld 3 aus einer gepackten IP-Adresse, die mit der [**IPM \_ GetAddress**](ipm-getaddress.md) -Nachricht abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5eb19-116">Extracts the field 3 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="5eb19-117">**MakeIPAddress**</span><span class="sxs-lookup"><span data-stu-id="5eb19-117">**MAKEIPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | <span data-ttu-id="5eb19-118">Packt vier Byte-Werte in einem einzelnen lParam-Element, das für die Verwendung mit der [**IPM- \_ setAddress**](ipm-setaddress.md) -Nachricht geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="5eb19-118">Packs four byte-values into a single LPARAM suitable for use with the [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span> <br/>  |
| [<span data-ttu-id="5eb19-119">**Makeiprange**</span><span class="sxs-lookup"><span data-stu-id="5eb19-119">**MAKEIPRANGE**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | <span data-ttu-id="5eb19-120">Packt zwei Bytewerte in einem einzelnen lParam-Element, das für die Verwendung mit der [**IPM \_**](ipm-setrange.md) -Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5eb19-120">Packs two byte-values into a single LPARAM suitable for use with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span> <br/>       |
| [<span data-ttu-id="5eb19-121">**zweite \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="5eb19-121">**SECOND\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | <span data-ttu-id="5eb19-122">Extrahiert den Wert für Feld 1 aus einer gepackten IP-Adresse, die mit der [**IPM \_ GetAddress**](ipm-getaddress.md) -Nachricht abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5eb19-122">Extracts the field 1 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="5eb19-123">**Dritte \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="5eb19-123">**THIRD\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | <span data-ttu-id="5eb19-124">Extrahiert den Wert von Feld 2 aus einer gepackten IP-Adresse, die mit der [**IPM \_ GetAddress**](ipm-getaddress.md) -Nachricht abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5eb19-124">Extracts the field 2 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |



 

### <a name="messages"></a><span data-ttu-id="5eb19-125">Meldungen</span><span class="sxs-lookup"><span data-stu-id="5eb19-125">Messages</span></span>



| <span data-ttu-id="5eb19-126">Thema</span><span class="sxs-lookup"><span data-stu-id="5eb19-126">Topic</span></span>                                         | <span data-ttu-id="5eb19-127">Inhalte</span><span class="sxs-lookup"><span data-stu-id="5eb19-127">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eb19-128">**IPM- \_ clearaddress**</span><span class="sxs-lookup"><span data-stu-id="5eb19-128">**IPM\_CLEARADDRESS**</span></span>](ipm-clearaddress.md) | <span data-ttu-id="5eb19-129">Löscht den Inhalt des Steuer Elements für die IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5eb19-129">Clears the contents of the IP address control.</span></span> <br/>                                                                            |
| [<span data-ttu-id="5eb19-130">**IPM- \_ GetAddress**</span><span class="sxs-lookup"><span data-stu-id="5eb19-130">**IPM\_GETADDRESS**</span></span>](ipm-getaddress.md)     | <span data-ttu-id="5eb19-131">Ruft die Adress Werte für alle vier Felder im IP-Adress Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="5eb19-131">Gets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="5eb19-132">**IPM \_ isblank**</span><span class="sxs-lookup"><span data-stu-id="5eb19-132">**IPM\_ISBLANK**</span></span>](ipm-isblank.md)           | <span data-ttu-id="5eb19-133">Bestimmt, ob alle Felder im IP-Adress Steuerelement leer sind.</span><span class="sxs-lookup"><span data-stu-id="5eb19-133">Determines if all fields in the IP address control are blank.</span></span> <br/>                                                             |
| [<span data-ttu-id="5eb19-134">**IPM- \_ setAddress**</span><span class="sxs-lookup"><span data-stu-id="5eb19-134">**IPM\_SETADDRESS**</span></span>](ipm-setaddress.md)     | <span data-ttu-id="5eb19-135">Legt die Adress Werte für alle vier Felder im IP-Adress Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="5eb19-135">Sets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="5eb19-136">**IPM- \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="5eb19-136">**IPM\_SETFOCUS**</span></span>](ipm-setfocus.md)         | <span data-ttu-id="5eb19-137">Legt den Tastaturfokus auf das angegebene Feld im IP-Adress Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="5eb19-137">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="5eb19-138">Der gesamte Text in diesem Feld wird ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="5eb19-138">All of the text in that field will be selected.</span></span> <br/> |
| [<span data-ttu-id="5eb19-139">**IPM-über \_ Tragung**</span><span class="sxs-lookup"><span data-stu-id="5eb19-139">**IPM\_SETRANGE**</span></span>](ipm-setrange.md)         | <span data-ttu-id="5eb19-140">Legt den gültigen Bereich für das angegebene Feld im IP-Adress Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="5eb19-140">Sets the valid range for the specified field in the IP address control.</span></span> <br/>                                                   |



 

### <a name="notifications"></a><span data-ttu-id="5eb19-141">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="5eb19-141">Notifications</span></span>



| <span data-ttu-id="5eb19-142">Thema</span><span class="sxs-lookup"><span data-stu-id="5eb19-142">Topic</span></span>                                     | <span data-ttu-id="5eb19-143">Inhalte</span><span class="sxs-lookup"><span data-stu-id="5eb19-143">Contents</span></span>                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eb19-144">IPN- \_ FieldChanged</span><span class="sxs-lookup"><span data-stu-id="5eb19-144">IPN\_FIELDCHANGED</span></span>](ipn-fieldchanged.md) | <span data-ttu-id="5eb19-145">Wird gesendet, wenn der Benutzer ein Feld im Steuerelement ändert oder von einem Feld zu einem anderen verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="5eb19-145">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="5eb19-146">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="5eb19-146">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="5eb19-147">Strukturen</span><span class="sxs-lookup"><span data-stu-id="5eb19-147">Structures</span></span>



| <span data-ttu-id="5eb19-148">Thema</span><span class="sxs-lookup"><span data-stu-id="5eb19-148">Topic</span></span>                              | <span data-ttu-id="5eb19-149">Inhalte</span><span class="sxs-lookup"><span data-stu-id="5eb19-149">Contents</span></span>                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eb19-150">**Nmipaddress**</span><span class="sxs-lookup"><span data-stu-id="5eb19-150">**NMIPADDRESS**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | <span data-ttu-id="5eb19-151">Enthält Informationen für den [IPN \_ FieldChanged](ipn-fieldchanged.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="5eb19-151">Contains information for the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification code.</span></span> <br/> |



 

 

 





