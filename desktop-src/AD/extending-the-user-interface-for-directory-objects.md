---
title: Erweitern der Benutzeroberfläche für Verzeichnisobjekte
description: Mit Microsoft Windows 2000 und höher sind Microsoft Management Console (MMC)-Snap-Ins (z. b. das Active Directory-Benutzer und-Computer-Snap-in für die Verwaltung von Active Directory Domain Services verfügbar.
ms.assetid: 758ec25d-42ab-46ba-aa58-416d7ac8fd68
ms.tgt_platform: multiple
keywords:
- Active Directory, verwenden, Erweitern der Benutzeroberfläche
- Objekte AD, Erweitern der Benutzeroberfläche für Verzeichnisobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d635132a26e80a63fddb35f779211308779f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707620"
---
# <a name="extending-the-user-interface-for-directory-objects"></a><span data-ttu-id="8e342-105">Erweitern der Benutzeroberfläche für Verzeichnisobjekte</span><span class="sxs-lookup"><span data-stu-id="8e342-105">Extending the User Interface for Directory Objects</span></span>

<span data-ttu-id="8e342-106">Mit Microsoft Windows 2000 und höher sind Microsoft Management Console (MMC)-Snap-Ins (z. b. das Active Directory-Benutzer und-Computer-Snap-in für die Verwaltung von Active Directory Domain Services verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e342-106">With Microsoft Windows 2000 and later, Microsoft Management Console (MMC) snap-ins, such as the Active Directory Users and Computers snap-in, for administration of Active Directory Domain Services, are available.</span></span> <span data-ttu-id="8e342-107">Außerdem enthält die Windows 2000 Shell Benutzeroberflächen (User Interfaces, UIs) zum Suchen nach Objekten, die sich im Verzeichnis befinden, sowie zum Lesen und Schreiben von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8e342-107">In addition, the Windows 2000 shell includes user interfaces (UIs) for finding objects that reside in the directory and reading and writing properties.</span></span> <span data-ttu-id="8e342-108">In diesem Abschnitt wird erläutert, wie Sie die Benutzeroberfläche zum Anzeigen und Verwalten von Active Directory Domain Services Objekten in der Windows-Shell und Active Directory Verwaltungs-Snap-Ins erweitern. In diesem Abschnitt wird auch erläutert, was erforderlich ist, um die UI-Erweiterungen auf den Desktops des Benutzers bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8e342-108">This section explains how to extend the UI for viewing and managing Active Directory Domain Services objects in the Windows shell and Active Directory administrative snap-ins. This section also covers what is required to deploy the UI extensions to the user's desktops.</span></span>

<span data-ttu-id="8e342-109">In diesem Abschnitt wird insbesondere Folgendes erläutert:</span><span class="sxs-lookup"><span data-stu-id="8e342-109">Specifically, this section discusses the following:</span></span>

-   [<span data-ttu-id="8e342-110">Informationen zu Active Directory Benutzeroberflächen</span><span class="sxs-lookup"><span data-stu-id="8e342-110">About Active Directory User Interfaces</span></span>](about-the-user-interfaces-of-active-directory-domain-services.md)
-   [<span data-ttu-id="8e342-111">Anzeige spezifiker</span><span class="sxs-lookup"><span data-stu-id="8e342-111">Display Specifiers</span></span>](display-specifiers.md)
-   [<span data-ttu-id="8e342-112">Klassen-und Attribut anzeigen Amen</span><span class="sxs-lookup"><span data-stu-id="8e342-112">Class and Attribute Display Names</span></span>](class-and-attribute-display-names.md)
-   [<span data-ttu-id="8e342-113">Klassen Symbole</span><span class="sxs-lookup"><span data-stu-id="8e342-113">Class Icons</span></span>](class-icons.md)
-   [<span data-ttu-id="8e342-114">Anzeigen von Containern als Blattknoten</span><span class="sxs-lookup"><span data-stu-id="8e342-114">Viewing Containers as Leaf Nodes</span></span>](viewing-containers-as-leaf-nodes.md)
-   [<span data-ttu-id="8e342-115">Ändern vorhandener Benutzeroberflächen</span><span class="sxs-lookup"><span data-stu-id="8e342-115">Modifying Existing User Interfaces</span></span>](modifying-existing-user-interfaces.md)
-   [<span data-ttu-id="8e342-116">Benutzeroberflächen Erweiterung für neue Objektklassen</span><span class="sxs-lookup"><span data-stu-id="8e342-116">User Interface Extension for New Object Classes</span></span>](user-interface-extension-for-new-object-classes.md)
-   [<span data-ttu-id="8e342-117">Eigenschaften Seiten für die Verwendung mit Anzeige spezifiken</span><span class="sxs-lookup"><span data-stu-id="8e342-117">Property Pages for Use with Display Specifiers</span></span>](property-pages-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="8e342-118">Kontextmenüs für die Verwendung mit Anzeige spezifiken</span><span class="sxs-lookup"><span data-stu-id="8e342-118">Context Menus for Use with Display Specifiers</span></span>](context-menus-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="8e342-119">Assistenten zum Erstellen von Objekten</span><span class="sxs-lookup"><span data-stu-id="8e342-119">Object Creation Wizards</span></span>](object-creation-wizards.md)
-   [<span data-ttu-id="8e342-120">Verwenden von Standard Dialogfeldern zum Behandeln von Objekten in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="8e342-120">Using Standard Dialog Boxes for Handling Objects in Active Directory Domain Services</span></span>](using-standard-dialog-boxes-to-handle-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="8e342-121">Verwaltung von Benachrichtigungs Handlern</span><span class="sxs-lookup"><span data-stu-id="8e342-121">Administrative Notification Handlers</span></span>](administrative-notification-handlers.md)
-   [<span data-ttu-id="8e342-122">Verteilen von Benutzeroberflächen Komponenten</span><span class="sxs-lookup"><span data-stu-id="8e342-122">Distributing User Interface Components</span></span>](distributing-user-interface-components.md)
-   [<span data-ttu-id="8e342-123">Verwendung von Anzeige Spezifikations Anwendungen durch Anwendungen</span><span class="sxs-lookup"><span data-stu-id="8e342-123">How Applications Should Use Display Specifiers</span></span>](how-applications-should-use-display-specifiers.md)
-   [<span data-ttu-id="8e342-124">Debuggen einer Active Directory-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="8e342-124">Debugging an Active Directory Extension</span></span>](debugging-an-active-directory-extension.md)

 

 




