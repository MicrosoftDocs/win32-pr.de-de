---
title: Übersicht über die Entwicklung von Benutzeroberflächen
description: In diesem Abschnitt werden die drei Phasen des Entwurfs von Benutzeroberflächen beschrieben und die Aufgaben eingeführt, die in der Regel mit den einzelnen Phasen verknüpft sind.
ms.assetid: ab544cb9-eed3-4575-a8dd-2f5d7b5c575f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b531fb07a1805c14441c81777bbdddad0739e7cb
ms.sourcegitcommit: e5c43274e96cb8fd1b60fc187ef16723e9258367
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2020
ms.locfileid: "104038471"
---
# <a name="overview-of-the-user-interface-development-process"></a><span data-ttu-id="de145-103">Übersicht über den Entwicklungsprozess der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="de145-103">Overview of the User Interface Development Process</span></span>

<span data-ttu-id="de145-104">In diesem Abschnitt werden die drei Phasen des Entwurfs von Benutzeroberflächen beschrieben und die Aufgaben eingeführt, die in der Regel mit den einzelnen Phasen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="de145-104">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span>

## <a name="the-application-user-interface-and-the-user-experience"></a><span data-ttu-id="de145-105">Die Benutzeroberfläche der Anwendung und die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="de145-105">The Application User Interface and the User Experience</span></span>

<span data-ttu-id="de145-106">Zunächst müssen die Begriffe "Benutzeroberfläche" und "Benutzeroberfläche" erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="de145-106">To begin, the terms "user interface" and "user experience" must be clarified.</span></span>

<span data-ttu-id="de145-107">Die Benutzeroberfläche einer Anwendung umfasst in der Regel die Objekte, die einem Benutzer direkt auf dem Bildschirm angezeigt werden und mit denen er interagiert.</span><span class="sxs-lookup"><span data-stu-id="de145-107">The user interface of an application typically involves those objects that a user sees and interacts with directly on their screen.</span></span> <span data-ttu-id="de145-108">Zu diesen Objekten gehören z. b. der Dokument Raum, Menüs, Dialogfelder, Symbole, Bilder und Animationen.</span><span class="sxs-lookup"><span data-stu-id="de145-108">For example, such objects include the document space, menus, dialog boxes, icons, images, and animations.</span></span>

<span data-ttu-id="de145-109">Die Benutzeroberfläche einer Anwendung ist jedoch nur ein Aspekt der gesamten Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="de145-109">However, the user interface of an application is only one aspect of the overall user experience.</span></span> <span data-ttu-id="de145-110">Weitere Aspekte der Benutzerfreundlichkeit, die für den Benutzer nicht sichtbar sind, aber für eine Anwendung von entscheidender Bedeutung sind, und für die Benutzerfreundlichkeit wichtig sind, sind Start Zeit, Latenz, Fehlerbehandlung und automatisierte Aufgaben, die ohne direkte Benutzerinteraktion abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="de145-110">Other aspects of the user experience that are not visible to the user, but are integral to an application and critical to its usability, include start up time, latency, error handling, and automated tasks that are completed without direct user interaction.</span></span>

<span data-ttu-id="de145-111">Im Allgemeinen erfordert eine Benutzeroberfläche eine Aktion durch einen Benutzer, um eine Aufgabe auszuführen, während eine großartige Benutzeroberfläche ohne Benutzeroberfläche erreicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="de145-111">In general, a user interface requires action by a user to accomplish a task, while a great user experience can be achieved with no user interface at all.</span></span>

## <a name="user-interface-development"></a><span data-ttu-id="de145-112">Benutzeroberflächen Entwicklung</span><span class="sxs-lookup"><span data-stu-id="de145-112">User Interface Development</span></span>

<span data-ttu-id="de145-113">Die Bereitstellung eines erfolgreichen Benutzer Erlebnisses erfordert während des gesamten Entwicklungs Lebenszyklus einen ausgeglichenen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="de145-113">Providing a successful user experience requires a balanced approach throughout the development life cycle.</span></span> <span data-ttu-id="de145-114">Um diesen Saldo sicherzustellen, dürfen Sie sich nicht nur auf die Implementierung der Funktionen konzentrieren, die zum Ausführen einer Aufgabe erforderlich sind, sondern auch darauf, wie die Aufgabe über die Benutzeroberfläche verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="de145-114">To ensure this balance, you must not only focus on implementing the functionality required to complete a task but also on how the task is exposed through the user interface.</span></span> <span data-ttu-id="de145-115">Beachten Sie, dass die Benutzeroberfläche nicht nur funktionsfähig sein muss, sondern auch verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="de145-115">Remember, the user interface must not only be functional, it must also be usable.</span></span>

<span data-ttu-id="de145-116">Im folgenden werden die typischen Phasen des dvelopment-Prozesses der Benutzeroberfläche erläutert:</span><span class="sxs-lookup"><span data-stu-id="de145-116">The following outlines the typical phases of the user interface dvelopment process:</span></span>

### <a name="designing"></a><span data-ttu-id="de145-117">Entwerfen</span><span class="sxs-lookup"><span data-stu-id="de145-117">Designing</span></span>

-   <span data-ttu-id="de145-118">Funktionale Anforderungen – bestimmen Sie die anfänglichen Anforderungen und Ziele für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="de145-118">Functional requirements – Determine the initial requirements and goals for the application.</span></span>
-   <span data-ttu-id="de145-119">Benutzer Analyse – identifizieren Sie die Benutzer Szenarios, und verstehen Sie die Anforderungen und Erwartungen der Benutzer für jedes Szenario.</span><span class="sxs-lookup"><span data-stu-id="de145-119">User analysis – Identify the user scenarios and understand the needs and expectations of users for each scenario.</span></span>
-   <span data-ttu-id="de145-120">Konzeptioneller Entwurf – modellieren Sie das zugrunde liegende Unternehmen, das die Anwendung unterstützen muss.</span><span class="sxs-lookup"><span data-stu-id="de145-120">Conceptual design – Model the underlying business that the application must support.</span></span>
-   <span data-ttu-id="de145-121">Logischer Entwurf – entwerfen Sie den Prozess und den Informationsfluss der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="de145-121">Logical design – Design the process and information flow of the application.</span></span>
-   <span data-ttu-id="de145-122">Physischer Entwurf – legen Sie fest, wie der logische Entwurf auf bestimmten physischen Plattformen implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="de145-122">Physical design – Decide how the logical design will be implemented on specific physical platforms.</span></span>

### <a name="implementing"></a><span data-ttu-id="de145-123">Um</span><span class="sxs-lookup"><span data-stu-id="de145-123">Implementing</span></span>

-   <span data-ttu-id="de145-124">Prototype – entwickeln Sie Papier-oder interaktive Bildschirm Entwürfe, die sich auf die Schnittstelle konzentrieren und keine ablenkend visuellen Entwurfs Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="de145-124">Prototype – Develop paper or interactive screen mockups that focus on the interface and don't include distracting visual design elements.</span></span>
-   <span data-ttu-id="de145-125">Construct – erstellen Sie die Anwendung, und bereiten Sie sich auf Entwurfs Änderungsanforderungen vor.</span><span class="sxs-lookup"><span data-stu-id="de145-125">Construct – Build the application and prepare for design change requests.</span></span>

### <a name="testing"></a><span data-ttu-id="de145-126">Test</span><span class="sxs-lookup"><span data-stu-id="de145-126">Testing</span></span>

-   <span data-ttu-id="de145-127">Benutzerbarkeits Tests – testen Sie die Anwendung mit verschiedenen Benutzern und Szenarios.</span><span class="sxs-lookup"><span data-stu-id="de145-127">Usability testing – Test the application with various users and scenarios.</span></span>
-   <span data-ttu-id="de145-128">Barrierefreiheits Tests – testen Sie die Anwendung mit zugänglichen Technologien und automatisierten TestTools.</span><span class="sxs-lookup"><span data-stu-id="de145-128">Accessibility testing – Test the application with accessible technologies and automated test tools.</span></span>

 

 




