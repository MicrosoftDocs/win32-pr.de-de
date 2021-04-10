---
title: Fenster Stationen
description: Eine Fenster Station enthält eine Zwischenablage, eine Atom-Tabelle und ein oder mehrere Desktop Objekte. Jedes Fenster Station-Objekt ist ein Sicherungs fähiges Objekt. Wenn eine Fenster Station erstellt wird, wird Sie mit dem aufrufenden Prozess verknüpft und der aktuellen Sitzung zugewiesen.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- Fenster Station-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039162"
---
# <a name="window-stations"></a><span data-ttu-id="462ac-106">Fenster Stationen</span><span class="sxs-lookup"><span data-stu-id="462ac-106">Window Stations</span></span>

<span data-ttu-id="462ac-107">Eine *Fenster Station* enthält eine Zwischenablage, eine Atom-Tabelle und ein oder mehrere [Desktop](desktops.md) Objekte.</span><span class="sxs-lookup"><span data-stu-id="462ac-107">A *window station* contains a clipboard, an atom table, and one or more [desktop](desktops.md) objects.</span></span> <span data-ttu-id="462ac-108">Jedes Fenster Station-Objekt ist ein Sicherungs fähiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="462ac-108">Each window station object is a securable object.</span></span> <span data-ttu-id="462ac-109">Wenn eine Fenster Station erstellt wird, wird Sie mit dem aufrufenden Prozess verknüpft und der aktuellen Sitzung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="462ac-109">When a window station is created, it is associated with the calling process and assigned to the current session.</span></span>

<span data-ttu-id="462ac-110">Die *interaktive Fenster Station* ist die einzige Fenster Station, auf der eine Benutzeroberfläche angezeigt oder Benutzereingaben empfangen werden können.</span><span class="sxs-lookup"><span data-stu-id="462ac-110">The *interactive window station* is the only window station that can display a user interface or receive user input.</span></span> <span data-ttu-id="462ac-111">Sie wird der Anmelde Sitzung des interaktiven Benutzers zugewiesen und enthält das Tastatur-, Maus-und Anzeigegerät.</span><span class="sxs-lookup"><span data-stu-id="462ac-111">It is assigned to the logon session of the interactive user, and contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="462ac-112">Der Name lautet immer "WinSta0".</span><span class="sxs-lookup"><span data-stu-id="462ac-112">It is always named "WinSta0".</span></span> <span data-ttu-id="462ac-113">Alle anderen Fenster Stationen sind nicht interaktiv, was bedeutet, dass Sie keine Benutzeroberfläche anzeigen oder Benutzereingaben empfangen können.</span><span class="sxs-lookup"><span data-stu-id="462ac-113">All other window stations are noninteractive, which means they cannot display a user interface or receive user input.</span></span>

<span data-ttu-id="462ac-114">Wenn sich ein Benutzer über Remotedesktopdienste an einem Computer anmeldet, wird eine Sitzung für den Benutzer gestartet.</span><span class="sxs-lookup"><span data-stu-id="462ac-114">When a user logs on to a computer using Remote Desktop Services, a session is started for the user.</span></span> <span data-ttu-id="462ac-115">Jede Sitzung ist mit der eigenen interaktiven Fenster Station namens "WinSta0" verknüpft.</span><span class="sxs-lookup"><span data-stu-id="462ac-115">Each session is associated with its own interactive window station named "WinSta0".</span></span> <span data-ttu-id="462ac-116">Weitere Informationen finden Sie unter [Remotedesktop-Sitzungen](/windows/desktop/TermServ/terminal-services-sessions).</span><span class="sxs-lookup"><span data-stu-id="462ac-116">For more information, see [Remote Desktop Sessions](/windows/desktop/TermServ/terminal-services-sessions).</span></span>

<span data-ttu-id="462ac-117">Weitere Informationen zu Fenster Stationen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="462ac-117">For more information on window stations, see the following topics:</span></span>

-   [<span data-ttu-id="462ac-118">Fenster Station und Desktop Erstellung</span><span class="sxs-lookup"><span data-stu-id="462ac-118">Window Station and Desktop Creation</span></span>](window-station-and-desktop-creation.md)
-   [<span data-ttu-id="462ac-119">Verarbeiten der Verbindung mit einer Fenster Station</span><span class="sxs-lookup"><span data-stu-id="462ac-119">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
-   [<span data-ttu-id="462ac-120">Sicherheit und Zugriffsrechte für die Fenster Station</span><span class="sxs-lookup"><span data-stu-id="462ac-120">Window Station Security and Access Rights</span></span>](window-station-security-and-access-rights.md)

 

 