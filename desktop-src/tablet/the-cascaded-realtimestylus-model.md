---
description: Übersicht über das kaskadierenden-Modell für die RealTimeStylus-Klasse.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: Das Cascaded RealTimeStylus-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2f61ea3cd44753d1d91fb2662226a716ee5590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561841"
---
# <a name="the-cascaded-realtimestylus-model"></a><span data-ttu-id="d4fa6-103">Das Cascaded RealTimeStylus-Modell</span><span class="sxs-lookup"><span data-stu-id="d4fa6-103">The Cascaded RealTimeStylus Model</span></span>

<span data-ttu-id="d4fa6-104">Das kaskadierenden [**RealTimeStylus**](realtimestylus-class.md) -Modell ermöglicht es Ihnen, zwei **RealTimeStylus** -Objekte zu verwenden, die jeweils in einem anderen Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-104">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model enables you to use two **RealTimeStylus** objects, each running on a different thread.</span></span> <span data-ttu-id="d4fa6-105">Mit diesem Modell fügen Sie ein sekundäres **RealTimeStylus** -Objekt an ein primäres **RealTimeStylus** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-105">With this model, you attach a secondary **RealTimeStylus** object to a primary **RealTimeStylus** object.</span></span> <span data-ttu-id="d4fa6-106">Das sekundäre **RealTimeStylus** -Objekt wird als einziges asynchrones Plug-in in die asynchrone Plug-in-Auflistung des primären **RealTimeStylus** -Objekts angefügt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-106">The secondary **RealTimeStylus** object is attached as the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>

<span data-ttu-id="d4fa6-107">Das kaskadierenden [**RealTimeStylus**](realtimestylus-class.md) -Modell kann in den folgenden Szenarien nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-107">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model may be useful in the following scenarios.</span></span>

-   <span data-ttu-id="d4fa6-108">Sie können bestimmte Aufgaben hinzufügen, die rechnerisch anspruchsvoll sind, aber trotzdem in Echtzeit auf den Datenstrom des Tablettstifts zugreifen müssen, z. b. die Erkennung von Zeitgeber-Gesten, um die synchrone Plug-in-Auflistung des sekundären [**RealTimeStylus**](realtimestylus-class.md) -Objekts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-108">You can add certain tasks that may be computationally demanding yet still require real-time access to the tablet pen's data stream, such as multistroke gesture recognition, to the secondary [**RealTimeStylus**](realtimestylus-class.md) object's synchronous plug-in collection.</span></span>
-   <span data-ttu-id="d4fa6-109">Sie können die computingressource ihrer synchronen Plug-Ins auf zwei Threads verteilen und so Verzögerungen bei der frei Hand Erfassung auf einigen Tablet PCs verringern.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-109">You can spread the computational load of your synchronous plug-ins over two threads, reducing delays in ink collection on some Tablet PCs.</span></span>

<span data-ttu-id="d4fa6-110">Das folgende Diagramm veranschaulicht den Fluss von Tablet Pen-Daten durch zwei kaskadierenden- [**RealTimeStylus**](realtimestylus-class.md) -Objekte und deren Plug-in-Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-110">The following diagram illustrates the flow of tablet pen data through two cascaded [**RealTimeStylus**](realtimestylus-class.md) objects and their plug-in collections.</span></span>

![Abbildung mit einem kaskadierenden RealTimeStylus-Datenfluss](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

<span data-ttu-id="d4fa6-112">In diesem Diagramm stellt der Kreis "A" Tablet Pen-Daten dar, die bereits von den primären und sekundären [**RealTimeStylus**](realtimestylus-class.md) -Objekten verarbeitet und in der Ausgabe Warteschlange des sekundären **RealTimeStylus** -Objekts abgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-112">In this diagram the circle lettered "A" represents tablet pen data that has already been processed by both the primary and secondary [**RealTimeStylus**](realtimestylus-class.md) objects and has been placed on the secondary **RealTimeStylus** object's output queue.</span></span> <span data-ttu-id="d4fa6-113">Der Kreis mit dem Wert "B" stellt Tablet-Stift Daten dar, die bereits vom primären **RealTimeStylus** -Objekt verarbeitet und der Ausgabe Warteschlange des primären **RealTimeStylus** -Objekts hinzugefügt wurden und noch nicht an das sekundäre **RealTimeStylus** -Objekt gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-113">The circle lettered "B" represents tablet pen data that has already been processed by the primary **RealTimeStylus** object and added to the primary **RealTimeStylus** object's output queue and has not yet been sent to the secondary **RealTimeStylus** object.</span></span> <span data-ttu-id="d4fa6-114">Der Kreis mit dem Wert "C" stellt die Tablet Pen-Daten dar, die das primäre **RealTimeStylus** -Objekt gerade verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-114">The circle lettered "C" represents the tablet pen data that the primary **RealTimeStylus** object is currently processing.</span></span> <span data-ttu-id="d4fa6-115">Sie wird an die synchrone Plug-in-Auflistung gesendet und in der Ausgabe Warteschlange abgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-115">It is sent to the synchronous plug-in collection and placed on the output queue.</span></span> <span data-ttu-id="d4fa6-116">Der leere Kreis stellt die Position in der Ausgabe Warteschlange dar, an der zukünftige Tablet Pen-Daten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-116">The empty circle represents the position in the output queue where future tablet pen data is added.</span></span>

## <a name="constraints"></a><span data-ttu-id="d4fa6-117">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d4fa6-117">Constraints</span></span>

<span data-ttu-id="d4fa6-118">Wenn Sie den standardmäßigen [**RealTimeStylus**](realtimestylus-class.md) -Konstruktor verwenden, erstellen Sie ein **RealTimeStylus** -Objekt, das nur Eingaben von einem anderen **RealTimeStylus** -Objekt akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-118">If you use the default [**RealTimeStylus**](realtimestylus-class.md) constructor, you create a **RealTimeStylus** object that can only accept input from another **RealTimeStylus** object.</span></span>

<span data-ttu-id="d4fa6-119">In der folgenden Liste werden die Einschränkungen beschrieben, die mit der Verwendung des kaskadierenden [**RealTimeStylus**](realtimestylus-class.md) -Modells verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-119">The following list describes the constraints associated with using the cascaded [**RealTimeStylus**](realtimestylus-class.md) model.</span></span>

-   <span data-ttu-id="d4fa6-120">Es können nur zwei [**RealTimeStylus**](realtimestylus-class.md) -Objekte verwendet werden, ein primäres **RealTimeStylus** -Objekt und ein sekundäres **RealTimeStylus** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-120">Only two [**RealTimeStylus**](realtimestylus-class.md) objects may be used, a primary **RealTimeStylus** object and a secondary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="d4fa6-121">Das primäre [**RealTimeStylus**](realtimestylus-class.md) -Objekt muss mit einem Konstruktor erstellt werden, der den Parameter " **AttachedControl** " oder " *handle* " verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-121">The primary [**RealTimeStylus**](realtimestylus-class.md) object must be created with a constructor that uses the **attachedControl** or *handle* parameter.</span></span> <span data-ttu-id="d4fa6-122">Das sekundäre **RealTimeStylus** -Objekt muss mit dem No-Argument-Konstruktor erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-122">The secondary **RealTimeStylus** object must be created with the no-argument constructor.</span></span>
-   <span data-ttu-id="d4fa6-123">Das sekundäre [**RealTimeStylus**](realtimestylus-class.md) -Objekt muss das einzige asynchrone Plug-in in der asynchronen Plug-in-Auflistung des primären **RealTimeStylus** -Objekts sein.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-123">The secondary [**RealTimeStylus**](realtimestylus-class.md) object must be the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>
-   <span data-ttu-id="d4fa6-124">Ein sekundäres [**RealTimeStylus**](realtimestylus-class.md) -Objekt kann jeweils nur an ein primäres **RealTimeStylus** -Objekt angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-124">A secondary [**RealTimeStylus**](realtimestylus-class.md) object can only be attached to one primary **RealTimeStylus** object at a time.</span></span> <span data-ttu-id="d4fa6-125">Wenn Sie einem zweiten primären **RealTimeStylus** -Objekt hinzugefügt wird, löst die [Add](/previous-versions/ms824814(v=msdn.10)) -Methode eine Ausnahme aus, und das sekundäre **RealTimeStylus** -Objekt ist nicht an das zweite primäre **RealTimeStylus** -Objekt angefügt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-125">If it is added to a second primary **RealTimeStylus** object, the [Add](/previous-versions/ms824814(v=msdn.10)) method throws an exception, and the secondary **RealTimeStylus** object is not attached to the second primary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="d4fa6-126">Das Verhalten einiger der Elemente des sekundären [**RealTimeStylus**](realtimestylus-class.md) -Objekts wird geändert.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-126">The behavior of some of the secondary [**RealTimeStylus**](realtimestylus-class.md) object's members is modified.</span></span> <span data-ttu-id="d4fa6-127">In der folgenden Tabelle wird das geänderte Verhalten dieser Member beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-127">The following table describes the modified behavior of these members.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d4fa6-128">Member</span><span class="sxs-lookup"><span data-stu-id="d4fa6-128">Member</span></span></th>
    <th><span data-ttu-id="d4fa6-129">Verhalten</span><span class="sxs-lookup"><span data-stu-id="d4fa6-129">Behavior</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="d4fa6-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="d4fa6-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="d4fa6-131">Diese Methode gibt die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-131">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="d4fa6-132">Wenn der sekundäre <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus</strong> -Objekt angefügt ist, gibt diese Methode den Standardwert zurück.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-132">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns the default value.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d4fa6-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="d4fa6-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="d4fa6-134">Diese Methode löst eine <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> -Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-134">This method raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="d4fa6-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span><span class="sxs-lookup"><span data-stu-id="d4fa6-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span></span></td>
    <td><span data-ttu-id="d4fa6-136">Diese Methode gibt die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-136">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="d4fa6-137">Wenn der sekundäre <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus</strong> -Objekt angefügt ist, gibt diese Methode ein leeres Array zurück.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-137">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns an empty array.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d4fa6-138"><a href="/previous-versions/ms824832(v=msdn.10)">Aktiviert</a></span><span class="sxs-lookup"><span data-stu-id="d4fa6-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span></span></td>
    <td><span data-ttu-id="d4fa6-139">Wenn Sie diese Eigenschaft erhalten, werden die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-139">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="d4fa6-140">Wenn der sekundäre <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus</strong> -Objekt angefügt ist, wird beim erhalten dieser Eigenschaft der Standardwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-140">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="d4fa6-141">Durch Festlegen dieser Eigenschaft wird eine <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> -Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-141">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="d4fa6-142"><a href="/previous-versions/ms824834(v=msdn.10)">Windowinputrechteck</a></span><span class="sxs-lookup"><span data-stu-id="d4fa6-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span></span></td>
    <td><span data-ttu-id="d4fa6-143">Wenn Sie diese Eigenschaft erhalten, werden die Informationen aus dem primären <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-143">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="d4fa6-144">Wenn der sekundäre <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> nicht an ein primäres <strong>RealTimeStylus</strong> -Objekt angefügt ist, wird beim erhalten dieser Eigenschaft der Standardwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-144">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="d4fa6-145">Durch Festlegen dieser Eigenschaft wird eine <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> -Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-145">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   <span data-ttu-id="d4fa6-146">Es wird erwartet, dass das übergeordnete [**RealTimeStylus**](realtimestylus-class.md) -Objekt nicht mehr funktioniert, wenn der untergeordnete **RealTimeStylus** verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-146">The parent [**RealTimeStylus**](realtimestylus-class.md) object is expected to stop functioning when the child **RealTimeStylus** is Disposed.</span></span>

 

 
