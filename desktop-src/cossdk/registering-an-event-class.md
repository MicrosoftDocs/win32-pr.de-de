---
description: Damit Abonnenten eine Ereignisklasse finden und Sie abonnieren können, müssen Ereignis Klassen im com+-Katalog registriert werden.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Registrieren einer Ereignisklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748289"
---
# <a name="registering-an-event-class"></a><span data-ttu-id="78ac6-103">Registrieren einer Ereignisklasse</span><span class="sxs-lookup"><span data-stu-id="78ac6-103">Registering an Event Class</span></span>

<span data-ttu-id="78ac6-104">Damit Abonnenten eine Ereignisklasse finden und Sie abonnieren können, müssen Ereignis Klassen im com+-Katalog registriert werden.</span><span class="sxs-lookup"><span data-stu-id="78ac6-104">So that subscribers can find an event class and subscribe to it, event classes must be registered in the COM+ catalog.</span></span> <span data-ttu-id="78ac6-105">Com+ erfordert eine Typbibliothek, die die Ereignis Schnittstellen und Methoden beschreibt, damit Sie Abonnenten und Verleger ordnungsgemäß abgleichen und verbinden können.</span><span class="sxs-lookup"><span data-stu-id="78ac6-105">COM+ requires a type library that describes the event interfaces and methods so that it can properly match and connect subscribers and publishers.</span></span> <span data-ttu-id="78ac6-106">Die Typbibliothek muss sich in einer selbst Registrierungs-DLL befinden oder von ihr begleitet werden.</span><span class="sxs-lookup"><span data-stu-id="78ac6-106">The type library must reside in or be accompanied by a self-registering DLL.</span></span>

<span data-ttu-id="78ac6-107">Sie können das Verwaltungs Programmkomponenten Dienste oder die administrativen com+-Funktionen verwenden, um eine Ereignisklasse im com+-Katalog zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="78ac6-107">You can use the Component Services administrative tool or the COM+ Administrative functions to register an event class in the COM+ catalog.</span></span>

<span data-ttu-id="78ac6-108">**So registrieren Sie eine Ereignisklasse beim Verwaltungs Programm "Komponenten Dienste"**</span><span class="sxs-lookup"><span data-stu-id="78ac6-108">**To register an event class with the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="78ac6-109">Erstellen Sie eine neue COM+-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="78ac6-109">Create a new COM+ application.</span></span>

2.  <span data-ttu-id="78ac6-110">Öffnen Sie den Anwendungsordner, und wählen Sie **Komponenten** aus.</span><span class="sxs-lookup"><span data-stu-id="78ac6-110">Open the application folder and select **Components**.</span></span>

3.  <span data-ttu-id="78ac6-111">Klicken Sie im Menü **Aktion** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="78ac6-111">On the **Action** menu, click **New**.</span></span> <span data-ttu-id="78ac6-112">(Sie können auch den Ordner **Komponenten** auswählen, mit der rechten Maustaste klicken, auf **neu** zeigen und dann auf **Komponente** klicken.)</span><span class="sxs-lookup"><span data-stu-id="78ac6-112">(You can also select the **Components** folder, right-click, point to **New**, and then click **Component**.)</span></span>

4.  <span data-ttu-id="78ac6-113">Klicken Sie auf **neue Ereignisklasse installieren**.</span><span class="sxs-lookup"><span data-stu-id="78ac6-113">Click **Install new event class(es)**.</span></span>

5.  <span data-ttu-id="78ac6-114">Geben Sie den Pfad zur Komponenten-DLL der Ereignisklasse ein.</span><span class="sxs-lookup"><span data-stu-id="78ac6-114">Enter the path to the event class component DLL.</span></span>

6.  <span data-ttu-id="78ac6-115">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="78ac6-115">Click **OK**.</span></span>

<span data-ttu-id="78ac6-116">Die Ereignisklasse wird im com+-Katalog registriert und kann von Abonnenten gefunden werden, die an der Beschaffung der von der Ereignisklasse bereitgestellten Informationen interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="78ac6-116">The event class is registered in the COM+ catalog and can be located by subscribers interested in obtaining the information provided by the event class.</span></span> <span data-ttu-id="78ac6-117">Informationen zum Registrieren der Ereignisklasse mithilfe der com+-Verwaltungs Schnittstellen finden Sie unter [**icomadmincatalog:: installeventclass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span><span class="sxs-lookup"><span data-stu-id="78ac6-117">For information about how to register the event class by using the COM+ administrative interfaces, see [**ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="78ac6-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78ac6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ac6-119">Registrieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="78ac6-119">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 



