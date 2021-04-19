---
description: Das RealTimeStylus-Objekt dient zum Bereitstellen von Echtzeitzugriff auf den Datenstrom vom Tablettstift.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Plug-ins und die RealTimeStylus-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08177c5f4110897fa1887857788766f67ae38167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352750"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a><span data-ttu-id="03113-103">Plug-ins und die RealTimeStylus-Klasse</span><span class="sxs-lookup"><span data-stu-id="03113-103">Plug-ins and the RealTimeStylus Class</span></span>

<span data-ttu-id="03113-104">Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt dient zum Bereitstellen von Echtzeitzugriff auf den Datenstrom vom Tablettstift.</span><span class="sxs-lookup"><span data-stu-id="03113-104">The [**RealTimeStylus**](realtimestylus-class.md) object is designed to provide real-time access to the data stream from the tablet pen.</span></span> <span data-ttu-id="03113-105">Plug-ins, Objekte, die die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -oder [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle implementieren, können einem **RealTimeStylus** -Objekt hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="03113-105">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface, can be added to a **RealTimeStylus** object.</span></span> <span data-ttu-id="03113-106">Synchrone Plug-ins werden im allgemeinen direkt durch das **RealTimeStylus** -Objekt in einem Thread mit hoher Priorität aufgerufen, während asynchrone Plug-ins im Allgemeinen für den Benutzeroberflächen Thread der Anwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="03113-106">Synchronous plug-ins are generally called directly by the **RealTimeStylus** object on a high-priority thread, while asynchronous plug-ins are generally called on the application's user interface (UI) thread.</span></span> <span data-ttu-id="03113-107">Erstellen oder verwenden Sie synchrone Plug-Ins für Aufgaben, die Echtzeitzugriff auf den Datenstrom benötigen und Rechen mäßig nicht anspruchsvoll sind (z. b. Paketfilterung).</span><span class="sxs-lookup"><span data-stu-id="03113-107">Create or use synchronous plug-ins for tasks that require real-time access to the data stream and are computationally undemanding, such as packet filtering.</span></span> <span data-ttu-id="03113-108">Erstellen oder verwenden Sie asynchrone Plug-Ins für Aufgaben, die keinen Echtzeitzugriff auf den Datenstrom benötigen, z. b. eine frei Hand Auflistung.</span><span class="sxs-lookup"><span data-stu-id="03113-108">Create or use asynchronous plug-ins for tasks that do not require real-time access to the data stream, such as ink collection.</span></span>

<span data-ttu-id="03113-109">Bestimmte Aufgaben sind möglicherweise Rechen anspruchsvoll und erfordern trotzdem Echtzeitzugriff auf den Datenstrom, wie z. b. die Erkennung von Zeitgeber-Gesten.</span><span class="sxs-lookup"><span data-stu-id="03113-109">Certain tasks may be computationally demanding yet require real-time access to the data stream, such as multistroke gesture recognition.</span></span> <span data-ttu-id="03113-110">Um diese Anforderungen zu erfüllen, stellen die StylusInput-APIs ein kaskadierenden [**RealTimeStylus**](realtimestylus-class.md) -Modell bereit, das es Ihnen ermöglicht, zwei **RealTimeStylus** -Objekte zu verwenden, die jeweils in einem eigenen Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="03113-110">To address these needs, the StylusInput APIs provide a cascaded [**RealTimeStylus**](realtimestylus-class.md) model that allows you to use two **RealTimeStylus** objects, each running on its own thread.</span></span> <span data-ttu-id="03113-111">Weitere Informationen zum kaskadierenden **RealTimeStylus** -Modell finden Sie [im kaskadierenden RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="03113-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

<span data-ttu-id="03113-112">Sowohl die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Schnittstelle als auch die [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle definieren die gleichen Methoden.</span><span class="sxs-lookup"><span data-stu-id="03113-112">Both the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) and [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interfaces define the same methods.</span></span> <span data-ttu-id="03113-113">Diese Methoden ermöglichen es dem [**RealTimeStylus**](realtimestylus-class.md) -Objekt, die Stift Daten an jedes Plug-in zu übergeben, unabhängig davon, ob es sich um ein asynchrones oder synchrones Plug-in handelt.</span><span class="sxs-lookup"><span data-stu-id="03113-113">These methods allow the [**RealTimeStylus**](realtimestylus-class.md) object to pass the pen data to each plug-in, regardless of whether it is an asynchronous or synchronous plug-in.</span></span> <span data-ttu-id="03113-114">Mit den Eigenschaften " [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) " und " [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) " können alle Plug-ins bestimmte Daten im Tablet Pen-Datenstream abonnieren.</span><span class="sxs-lookup"><span data-stu-id="03113-114">The [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) and [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) properties allow each plug-in to subscribe to specific data in the tablet pen data stream.</span></span> <span data-ttu-id="03113-115">Ein Plug-in sollte nur die Daten abonnieren, die für die Ausführung der Aufgabe erforderlich sind, sodass Leistungsanforderungen minimiert werden.</span><span class="sxs-lookup"><span data-stu-id="03113-115">A plug-in should only subscribe to the data necessary to perform its task, minimizing performance demands.</span></span> <span data-ttu-id="03113-116">Weitere Informationen zum Threading und zur **RealTimeStylus** -Klasse finden Sie unter [Threading Überlegungen für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="03113-116">For more information about threading and the **RealTimeStylus** class, see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="03113-117">Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt verwendet Objekte im [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) -Namespace, um die Stift Daten an die Plug-ins zu übergeben. Der **RealTimeStylus** fängt auch Ausnahmen ab, die von Plug-ins ausgelöst werden. Wenn der **RealTimeStylus** Ausnahmen abfängt, werden die Plug-ins benachrichtigt, indem die [IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) -Methode oder die [IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="03113-117">The [**RealTimeStylus**](realtimestylus-class.md) object uses objects in the [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespace to pass the pen data to its plug-ins. The **RealTimeStylus** also catches exceptions thrown by plug-ins. When the **RealTimeStylus** catches exceptions, it notifies the plug-ins by calling the [IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method.</span></span> <span data-ttu-id="03113-118">Weitere Informationen zur Verwendung von Plug-in-Daten finden Sie unter [Plug-in-Daten und die RealTimeStylus-](plug-in-data-and-the-realtimestylus-class.md) Klasse.</span><span class="sxs-lookup"><span data-stu-id="03113-118">For more information about using plug-in data, see [Plug-in Data and the RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) Class.</span></span> <span data-ttu-id="03113-119">Weitere Informationen zur Fehlerbehandlung finden Sie unter [Überlegungen zur Fehlerbehandlung für die StylusInput-APIs](error-handling-considerations-for-the-stylusinput-apis.md) und im Abschnitt "Fehler Daten" der Plug-in-Daten und der RealTimeStylus-Klasse.</span><span class="sxs-lookup"><span data-stu-id="03113-119">For more information about error handling, see [Error Handling Considerations for the StylusInput APIs](error-handling-considerations-for-the-stylusinput-apis.md) and the Error Data section of Plug-in Data and the RealTimeStylus Class.</span></span>

> [!Note]  
> <span data-ttu-id="03113-120">Mindestens ein Plug-in muss an das [**RealTimeStylus**](realtimestylus-class.md) -Objekt angefügt werden, bevor das **RealTimeStylus** -Objekt aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="03113-120">At least one plug-in must be attached to the [**RealTimeStylus**](realtimestylus-class.md) object before the **RealTimeStylus** object can be enabled.</span></span>

 

<span data-ttu-id="03113-121">In den folgenden Themen werden einige allgemeine Kategorien von Plug-Ins beschrieben.</span><span class="sxs-lookup"><span data-stu-id="03113-121">The following topics describe some common categories of plug-ins.</span></span>

-   [<span data-ttu-id="03113-122">Plug-Ins für die frei Hand Erfassung</span><span class="sxs-lookup"><span data-stu-id="03113-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
-   [<span data-ttu-id="03113-123">Plug-Ins für dynamisches Renderer</span><span class="sxs-lookup"><span data-stu-id="03113-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
-   [<span data-ttu-id="03113-124">Erkennungs-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="03113-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)

## <a name="special-considerations"></a><span data-ttu-id="03113-125">Besondere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="03113-125">Special Considerations</span></span>

<span data-ttu-id="03113-126">Aufgrund der komplexen Natur des [**RealTimeStylus**](realtimestylus-class.md) -Objekts sollten Sie Folgendes beachten:</span><span class="sxs-lookup"><span data-stu-id="03113-126">Because of the complex nature of the [**RealTimeStylus**](realtimestylus-class.md) object, you should take note of the following.</span></span>

<span data-ttu-id="03113-127">Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt löst eine Ausnahme aus, wenn ein Plug-in die Plug-in-Sammlung ändert, an die es angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="03113-127">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in modifies the plug-in collection to which it is attached.</span></span> <span data-ttu-id="03113-128">Dies geschieht nur, wenn das Plug-in Dies bewirkt, während es vom **RealTimeStylus** -Objekt als Member dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="03113-128">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object as a member of that collection.</span></span>

<span data-ttu-id="03113-129">Im folgenden C- \# Beispiel handelt es sich um Code, der bewirkt, dass das [**RealTimeStylus**](realtimestylus-class.md) -Objekt eine Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="03113-129">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.Dispose();
    }
    
    // ...
}
```



<span data-ttu-id="03113-130">Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt löst eine Ausnahme aus, wenn ein Plug-in die verwerfen- [Methode des](/previous-versions/ms825891(v=msdn.10)) **RealTimeStylus** -Objekts aufruft.</span><span class="sxs-lookup"><span data-stu-id="03113-130">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in calls the **RealTimeStylus** object's [Dispose](/previous-versions/ms825891(v=msdn.10)) method.</span></span> <span data-ttu-id="03113-131">Dies geschieht nur, wenn das Plug-in Dies bewirkt, während es vom **RealTimeStylus** -Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="03113-131">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object.</span></span>

<span data-ttu-id="03113-132">Im folgenden C- \# Beispiel handelt es sich um Code, der bewirkt, dass das [**RealTimeStylus**](realtimestylus-class.md) -Objekt eine Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="03113-132">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    Microsoft.StylusInput.GestureRecognizer theGestureRecognizer;

    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.AsyncPluginCollection.Add(this.theGestureRecognizer);
    }
    
    // ...
}
```



<span data-ttu-id="03113-133">Plug-in-Auflistungen können geändert werden, während das [**RealTimeStylus**](realtimestylus-class.md) -Objekt aktiviert ist. Dies kann jedoch die Vorhersage des Verhaltens ihrer Anwendung erschweren.</span><span class="sxs-lookup"><span data-stu-id="03113-133">Plug-in collections can be modified while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled; however, this can make the behavior of your application harder to predict.</span></span> <span data-ttu-id="03113-134">Wenn ein Plug-in hinzugefügt wird, während das **RealTimeStylus** -Objekt aktiviert ist, ruft das **RealTimeStylus** -Objekt die [IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) -Methode oder die [IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) -Methode des Plug-Ins auf.</span><span class="sxs-lookup"><span data-stu-id="03113-134">When a plug-in is added while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) method.</span></span> <span data-ttu-id="03113-135">Wenn ein Plug-in entfernt wird, während das **RealTimeStylus** -Objekt aktiviert ist, ruft das **RealTimeStylus** -Objekt die [IStylusAsyncPlugin. realtimestylusdeaktiviert](/previous-versions/ms824774(v=msdn.10)) -Methode oder die [IStylusSyncPlugin. realtimestylusdeaktiviert](/previous-versions/ms824757(v=msdn.10)) -Methode des Plug-Ins auf.</span><span class="sxs-lookup"><span data-stu-id="03113-135">When a plug-in is removed while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) method.</span></span> <span data-ttu-id="03113-136">Dadurch kann das Plug-in seinen ordnungsgemäßen Zustand beibehalten, ohne die [aktivierte](/previous-versions/ms824832(v=msdn.10)) Eigenschaft des **RealTimeStylus** -Objekts überprüfen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="03113-136">This allows the plug-in to maintain its proper state without having to check the [Enabled](/previous-versions/ms824832(v=msdn.10)) property of the **RealTimeStylus** object.</span></span>

<span data-ttu-id="03113-137">Wenn ein Plug-in hinzugefügt wird, während das [**RealTimeStylus**](realtimestylus-class.md) -Objekt aktiviert ist, enthalten die Plug-in-Daten, die das Plug-in empfängt, möglicherweise nicht genügend Informationen, um den Kontext der anfänglichen Daten adäquat festzulegen.</span><span class="sxs-lookup"><span data-stu-id="03113-137">When a plug-in is added while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled, the plug-in data that the plug-in receives may not contain enough information to adequately establish the context of the initial data.</span></span> <span data-ttu-id="03113-138">Beispielsweise könnte das neu hinzugefügte Plug-in mit dem Empfang von Paketdaten von einem Stift beginnen, der einen Mittel Strich ist.</span><span class="sxs-lookup"><span data-stu-id="03113-138">For example, the newly added plug-in could start receiving packet data from a pen that is mid-stroke.</span></span> <span data-ttu-id="03113-139">Ebenso kann ein Plug-in, das beim Aktivieren des **RealTimeStylus** -Objekts entfernt wurde, nicht ausreichen, um die Verarbeitung der Daten abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="03113-139">Similarly, when a plug-in removed while the **RealTimeStylus** object is enabled, the plug-in data that the plug-in has received may be insufficient to finish processing the data.</span></span>

> [!Note]  
> <span data-ttu-id="03113-140">Setzen Sie für die Gesamtstabilität den internen Zustand eines Plug-ins zurück, wenn entweder die zugehörige [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) -Methode oder die [**realtimestylusdeaktivierte**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="03113-140">For overall stability, reset a plug-in's internal state when either its [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) or [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) method is called.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="03113-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="03113-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03113-142">Das Cascaded RealTimeStylus-Modell</span><span class="sxs-lookup"><span data-stu-id="03113-142">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[<span data-ttu-id="03113-143">Überlegungen zur Fehlerbehandlung für die StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="03113-143">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[<span data-ttu-id="03113-144">Plug-In-Daten und die RealTimeStylus-Klasse</span><span class="sxs-lookup"><span data-stu-id="03113-144">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="03113-145">Threading Überlegungen für die StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="03113-145">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
