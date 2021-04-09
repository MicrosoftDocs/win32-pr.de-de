---
description: Vorübergehende Abonnements können nicht mithilfe des Verwaltungs Tools für Komponenten Dienste festgelegt werden. Sie müssen die com+-Verwaltungs Schnittstellen verwenden, um ein vorübergehendes Abonnement zu erstellen oder zu aktualisieren.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Registrieren eines vorübergehenden Abonnements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fc85f189d14fbe6220d6f3760509e1ba0248a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126704"
---
# <a name="registering-a-transient-subscription"></a><span data-ttu-id="5c8b8-104">Registrieren eines vorübergehenden Abonnements</span><span class="sxs-lookup"><span data-stu-id="5c8b8-104">Registering a Transient Subscription</span></span>

<span data-ttu-id="5c8b8-105">Vorübergehende Abonnements fordern ein Ereignis für ein bestimmtes Abonnenten Objekt an, das bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-105">Transient subscriptions request an event for a specific subscriber object that already exists.</span></span> <span data-ttu-id="5c8b8-106">Vorübergehende Abonnements werden im com+-Katalog gespeichert, aber das Abonnement wird gelöscht, wenn das Ereignis System oder das Betriebssystem beendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-106">Transient subscriptions are stored in the COM+ catalog, but the subscription is deleted if the event system or operating system is stopped.</span></span> <span data-ttu-id="5c8b8-107">Im Gegensatz zu permanenten Abonnements sind vorübergehende Abonnements an ein bestimmtes Objekt gebunden und nur im-Ereignis System gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-107">Unlike persistent subscriptions, transient subscriptions are tied to a particular object and are stored only in the event system.</span></span> <span data-ttu-id="5c8b8-108">Wenn ein Problem mit dem Ereignis System oder dem Betriebssystem vorliegt, verschwindet das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-108">If there is a problem with the event system or operating system, the subscription disappears.</span></span> <span data-ttu-id="5c8b8-109">Vorübergehende Abonnements können effizienter als persistente Abonnements sein, aber Sie müssen deren Objekt Lebenszyklen verwalten.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-109">Transient subscriptions can be more efficient than persistent subscriptions, but you must manage their object life cycles.</span></span>

<span data-ttu-id="5c8b8-110">Vorübergehende Abonnements können nicht mithilfe des Verwaltungs Tools für Komponenten Dienste festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-110">Transient subscriptions cannot be set by using the Component Services administration tool.</span></span> <span data-ttu-id="5c8b8-111">Sie müssen die com+-Verwaltungs Schnittstellen verwenden, um ein vorübergehendes Abonnement zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-111">You must use the COM+ administrative interfaces to create or update a transient subscription.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="5c8b8-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5c8b8-112">Visual Basic</span></span>

<span data-ttu-id="5c8b8-113">Im folgenden Verfahren wird das Erstellen eines vorübergehenden Abonnements mit Microsoft Visual Basic beschrieben:</span><span class="sxs-lookup"><span data-stu-id="5c8b8-113">The following procedure describes how to create a transient subscription using Microsoft Visual Basic:</span></span>

1.  <span data-ttu-id="5c8b8-114">Geben Sie ein Abonnement als flüchtig an, indem Sie einen neuen Eintrag zur [**transientabonnements**](transientsubscriptions.md) -Auflistung hinzufügen und die Eigenschaft "Abonnement Schnittstelle" auf die [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Abonnenten Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-114">Specify a subscription as transient by adding a new entry to the [**TransientSubscriptions**](transientsubscriptions.md) collection and setting the SubscriberInterface property to the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface of the subscriber object.</span></span> <span data-ttu-id="5c8b8-115">Com+-Ereignisse erstellt keine neue Instanz des Abonnenten Objekts, wenn ein Ereignis ausgelöst wird, sondern verwendet stattdessen die von Ihnen angegebene Instanz.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-115">COM+ Events does not create a new instance of the subscriber object when firing an event but instead uses the instance you specify.</span></span> <span data-ttu-id="5c8b8-116">Com+-Ereignisse enthalten einen Verweis Zähler für das Abonnenten Objekt, bis das Abonnement aus dem System entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-116">COM+ Events holds a reference count for the subscriber object until the subscription is removed from the system.</span></span>
2.  <span data-ttu-id="5c8b8-117">Erstellen Sie eine COM+-Serveranwendung (eine exe-, dll-oder OCX-Datei) mit einem Objekt, das die Schnittstellen oder Methoden implementiert, die Sie abonnieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-117">Create a COM+ server application (an .exe, a .dll, or an .ocx file) with an object that implements the interfaces or methods you want to subscribe to.</span></span>
3.  <span data-ttu-id="5c8b8-118">Erstellen Sie mit dem folgenden Code ein vorübergehendes Abonnement, indem Sie die CLSID des [Ereignis Klassen](the-com--event-class-object.md) Objekts und die Instanz des Abonnenten Objekts übergeben.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-118">Create your transient subscription using the following code, by passing in the CLSID of the [event class](the-com--event-class-object.md) object and the instance of the subscriber object.</span></span> <span data-ttu-id="5c8b8-119">Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie die eventclsid-Eigenschaft erhalten, indem Sie mit der rechten Maustaste auf die COM+-Komponente klicken, **Eigenschaften** auswählen und die Registerkarte **Allgemein** auswählen.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-119">Using the Component Services administrative tool, you can get the EventCLSID property by right-clicking the COM+ component, selecting **Properties**, and selecting the **General** tab.</span></span>

    ``` syntax
    Public Function CreateTransientSubscription( _
      ByVal clsid As String, ByVal objref As Object) As String 
        Dim oCOMAdminCatalog As COMAdmin.COMAdminCatalog
        Dim oTSCol As COMAdminCatalogCollection
        Dim oSubscription As ICatalogObject
        Dim objvar As Variant
        On Error GoTo CreateTransientSubscriptionError
        Set oCOMAdminCatalog = CreateObject("COMAdmin.COMAdminCatalog")
        'Gets the TransientSubscriptions collection
        Set oTSCol = oCOMAdminCatalog.GetCollection( _
          "TransientSubscriptions")
        Set oSubscription = oTSCol.Add
        Set objvar = objref
        oSubscription.Value("SubscriberInterface") = objref
        oSubscription.Value("EventCLSID") = clsid
        oSubscription.Value("Name") = "TransientSubscription"
        oTSCol.SaveChanges
        CreateTransientSubscription = oSubscription.Value("ID")
        Set oSubscription = Nothing
        Set oTSCol = Nothing
        Set oCOMAdminCatalog = Nothing
        Set objvar = Nothing
        Exit Function
    CreateTransientSubscriptionError:
        CreateTransientSubscription = ""
        Err.Raise Err.Number, "[CreateTransientSubscription]" & _
          Err.Source, Err.Description
    End Function
    ```

<span data-ttu-id="5c8b8-120">Das folgende Beispiel veranschaulicht, wie die Funktion "foratetransientabonnement" aufgerufen wird, um eine Schnittstelle mit dem Namen "istockticker" zu abonnieren, die eine Methode namens "updatestock" aufweist.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-120">The following example illustrates how to call the CreateTransientSubscription function to subscribe to an interface called IStockTicker, which has a method called UpdateStock.</span></span>

1.  <span data-ttu-id="5c8b8-121">Erstellen Sie eine Ereignisklasse, die die istockticker-Schnittstelle unterstützt, die über eine Methode, updatestock verfügt.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-121">Create an event class that supports the interface IStockTicker, which has one method, UpdateStock.</span></span>
2.  <span data-ttu-id="5c8b8-122">Fügen Sie in Ihrem Abonnenten Projekt eine Klasse hinzu, die die istockticker-Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-122">In your subscriber project, add a class that implements the IStockTicker interface.</span></span>
3.  <span data-ttu-id="5c8b8-123">Wenn Sie abonnieren möchten, führen Sie den folgenden Code aus:</span><span class="sxs-lookup"><span data-stu-id="5c8b8-123">When you want to subscribe execute the following code:</span></span>

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

<span data-ttu-id="5c8b8-124">Die Funktion "kreatetransientabonnementabonnement" gibt eine Zeichenfolge zurück, die eine GUID ist, die als handle oder Cookie verwendet werden kann, um das Abonnement später aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-124">The CreateTransientSubscription function returns a string, which is a GUID that can be used as a handle or a cookie to revoke the subscription later.</span></span> <span data-ttu-id="5c8b8-125">Um das Abonnement zu entfernen, rufen Sie die [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methode von [**comadmincatalogcollection**](comadmincatalogcollection.md) für die [**transientabonnements**](transientsubscriptions.md) -Auflistung auf, und übergeben Sie den Index, der dem Abonnement mit der zuvor empfangenen GUID entspricht.</span><span class="sxs-lookup"><span data-stu-id="5c8b8-125">To remove the subscription, call the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of [**COMAdminCatalogCollection**](comadmincatalogcollection.md) on the [**TransientSubscriptions**](transientsubscriptions.md) collection, passing in the index corresponding to the subscription with the GUID previously received.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c8b8-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c8b8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c8b8-127">Registrieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="5c8b8-127">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 
