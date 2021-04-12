---
description: Nachdem Sie eine Ereignisklasse im com+-Katalog registriert haben, können Sie der-Ereignisklasse Abonnenten und Abonnements für die Abonnenten hinzufügen.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Registrieren eines Abonnements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393174"
---
# <a name="registering-a-subscription"></a><span data-ttu-id="dac3d-103">Registrieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="dac3d-103">Registering a Subscription</span></span>

<span data-ttu-id="dac3d-104">Nachdem Sie eine Ereignisklasse im com+-Katalog registriert haben, können Sie der-Ereignisklasse Abonnenten und Abonnements für die Abonnenten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dac3d-104">After you have registered an event class in the COM+ catalog, you can add subscribers to the event class and subscriptions to the subscribers.</span></span> <span data-ttu-id="dac3d-105">Abonnements können eine einzelne Methode oder alle Methoden einer Schnittstelle abonnieren.</span><span class="sxs-lookup"><span data-stu-id="dac3d-105">Subscriptions can subscribe to a single method or to all the methods of an interface.</span></span> <span data-ttu-id="dac3d-106">Zum Empfangen von Aufrufen für mehr als eine Methode – aber nicht für jede Methode – einer Schnittstelle müssen Sie für jede Methode, an die Sie einen Aufruf erhalten möchten, ein Abonnement hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dac3d-106">To receive calls on more than one method—but not to every method—of an interface, you must add a subscription for each method to which you want to receive a call.</span></span> <span data-ttu-id="dac3d-107">Mit dem Verwaltungs Tool Komponenten Dienste können Sie den com+-Katalog nach registrierten Ereignis Klassen durchsuchen, die die vom Abonnenten implementierten Schnittstellen unterstützen. Sie können auch abonnieren.</span><span class="sxs-lookup"><span data-stu-id="dac3d-107">The Component Services administration tool can search the COM+ catalog for registered event classes that support the interfaces implemented by the subscriber and offers you the choice to subscribe.</span></span> <span data-ttu-id="dac3d-108">Wählen Sie den Herausgeber aus, der Ihnen die gewünschten Ereignisse anbietet.</span><span class="sxs-lookup"><span data-stu-id="dac3d-108">Choose the publisher that offers you the desired events.</span></span>

<span data-ttu-id="dac3d-109">Führen Sie die folgenden Schritte aus, um der Abonnenten Komponente Abonnenten hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="dac3d-109">To add subscribers to the subscriber component, use the following steps:</span></span>

1.  <span data-ttu-id="dac3d-110">Nachdem Sie eine neue COM+-Anwendung erstellt und die Abonnenten Komponente installiert haben, klicken Sie mit der rechten Maustaste auf den Ordner **Abonnements** , um den com+-Assistenten für neue Abonnements zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="dac3d-110">After creating a new COM+ application and installing the subscriber component, right-click the **Subscriptions** folder to enable the COM+ New Subscription Wizard.</span></span>

2.  <span data-ttu-id="dac3d-111">Wählen Sie die Ereignisklasse aus, von der Sie Ereignisse empfangen möchten.</span><span class="sxs-lookup"><span data-stu-id="dac3d-111">Choose the event class from which you want to receive events.</span></span>

3.  <span data-ttu-id="dac3d-112">Geben Sie einen Namen für das Abonnement ein.</span><span class="sxs-lookup"><span data-stu-id="dac3d-112">Enter a name for the subscription.</span></span>

4.  <span data-ttu-id="dac3d-113">Aktivieren Sie das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dac3d-113">Enable the subscription.</span></span>

5.  <span data-ttu-id="dac3d-114">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="dac3d-114">Click **OK**.</span></span>

<span data-ttu-id="dac3d-115">Wenn eine Verleger Anwendung ein Ereignis auslösen möchte, instanziiert der Verleger das Ereignis Klassenobjekt und ruft eine Methode dafür auf.</span><span class="sxs-lookup"><span data-stu-id="dac3d-115">When a publisher application wants to fire an event, the publisher instantiates the event class object and calls a method on it.</span></span> <span data-ttu-id="dac3d-116">Com+ durchsucht den com+-Katalog, um alle Abonnenten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="dac3d-116">COM+ searches the COM+ catalog to find all the subscribers.</span></span> <span data-ttu-id="dac3d-117">Er erstellt das Abonnenten Objekt (direkt, in der Warteschlange oder mit einem Moniker) und übergibt den Methodenaufruf, der ursprünglich vom Verleger erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="dac3d-117">It creates the subscriber object (directly, queued, or with a moniker) and passes on the method call originally made by the publisher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dac3d-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dac3d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dac3d-119">Registrieren einer Ereignisklasse</span><span class="sxs-lookup"><span data-stu-id="dac3d-119">Registering an Event Class</span></span>](registering-an-event-class.md)
</dt> </dl>

 

 



