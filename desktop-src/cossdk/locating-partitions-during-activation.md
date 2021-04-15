---
description: Suchen von Partitionen während der Aktivierung
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Suchen von Partitionen während der Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104569782"
---
# <a name="locating-partitions-during-activation"></a><span data-ttu-id="de701-103">Suchen von Partitionen während der Aktivierung</span><span class="sxs-lookup"><span data-stu-id="de701-103">Locating Partitions During Activation</span></span>

<span data-ttu-id="de701-104">Das Auffinden der richtigen Partition, in der eine Komponente aktiviert werden soll, hängt von folgendem ab:</span><span class="sxs-lookup"><span data-stu-id="de701-104">Locating the correct partition in which to activate a component depends on the following:</span></span>

-   <span data-ttu-id="de701-105">Der Funktionsaufruf und die Parameter, die im aufrufenden Programm zum Aktivieren der Komponente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de701-105">The function call and parameters used in the calling program to activate the component</span></span>
-   <span data-ttu-id="de701-106">Gibt an, ob die aktivierte Komponente lokal oder Remote ist.</span><span class="sxs-lookup"><span data-stu-id="de701-106">Whether the component being activated is local or remote</span></span>
-   <span data-ttu-id="de701-107">Die interne Verwendung des Partitions Caches</span><span class="sxs-lookup"><span data-stu-id="de701-107">The internal use of the partition cache</span></span>

## <a name="the-calling-program"></a><span data-ttu-id="de701-108">Das Aufruf Programm</span><span class="sxs-lookup"><span data-stu-id="de701-108">The Calling Program</span></span>

<span data-ttu-id="de701-109">Com+ wählt die Partition für die Komponenten Aktivierung basierend darauf aus, wie das aufrufenden Programm die Komponente aktiviert.</span><span class="sxs-lookup"><span data-stu-id="de701-109">COM+ selects the partition for component activation based on how the calling program activates the component.</span></span>

<span data-ttu-id="de701-110">Es gibt drei verschiedene Aktionen, die com+ durchführen kann, wenn eine Partition für die Komponenten Aktivierung ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="de701-110">There are three different actions that COM+ can take when selecting a partition for component activation.</span></span> <span data-ttu-id="de701-111">Die ausgeführte Aktion hängt davon ab, wie das aufrufende Programm das Objekt instanziiert, das heißt, ob der Funktionsaufruf einen partitionmoniker enthält, der aus einer Partitions-ID und einer CLSID besteht, oder nur eine CLSID enthält.</span><span class="sxs-lookup"><span data-stu-id="de701-111">The action taken depends on how the calling program instantiates the object that is, whether the function call includes a partition moniker, which consists of a partition ID and a CLSID, or includes a CLSID only.</span></span>

<span data-ttu-id="de701-112">In der folgenden Tabelle sind die verschiedenen Aktionen aufgeführt, die com+ in der Rangfolge durchführen kann, um eine Partition zu suchen.</span><span class="sxs-lookup"><span data-stu-id="de701-112">The following table shows the various actions that COM+ can take, in order of precedence, to locate a partition.</span></span>



| <span data-ttu-id="de701-113">Funktionsaufruf</span><span class="sxs-lookup"><span data-stu-id="de701-113">Function call</span></span>                                                  | <span data-ttu-id="de701-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="de701-114">Parameter</span></span>                                                      | <span data-ttu-id="de701-115">Com+-Aktion</span><span class="sxs-lookup"><span data-stu-id="de701-115">COM+ action</span></span>                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de701-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) oder **GetObject**</span><span class="sxs-lookup"><span data-stu-id="de701-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) or **GetObject**</span></span><br/> | <span data-ttu-id="de701-117">Partitionsmoniker (einschließlich Partitions-ID und CLSID)</span><span class="sxs-lookup"><span data-stu-id="de701-117">Partition moniker (includes partition ID and CLSID)</span></span><br/> | <span data-ttu-id="de701-118">Verwendet die im partitionsmoniker angegebene Partitions-ID.</span><span class="sxs-lookup"><span data-stu-id="de701-118">Uses the partition ID specified in the partition moniker.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="de701-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="de701-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | <span data-ttu-id="de701-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="de701-120">CLSID</span></span><br/>                                               | <span data-ttu-id="de701-121">Verwendet entweder die Partitions-ID der Standard Partition der Benutzeridentität oder die Partitions-ID, die dem Kontext während einer vorherigen Komponenten Aktivierung im selben Prozess hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="de701-121">Uses either the partition ID of the user identity's default partition or the partition ID that was added to the context during a previous component activation in the same process.</span></span><br/> |



 

<span data-ttu-id="de701-122">Die in der obigen Tabelle aufgeführten com+-Aktionen werden in den folgenden Abschnitten erläutert.</span><span class="sxs-lookup"><span data-stu-id="de701-122">The COM+ actions listed in the preceding table are explained in the following sections.</span></span>

## <a name="use-of-partition-monikers"></a><span data-ttu-id="de701-123">Verwendung von partitionmonikern</span><span class="sxs-lookup"><span data-stu-id="de701-123">Use of Partition Monikers</span></span>

<span data-ttu-id="de701-124">Eine Partition kann innerhalb eines Funktions Aufrufes mithilfe eines *partitionsmonikers* explizit ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="de701-124">A partition can be selected explicitly within a function call by using a *partition moniker*.</span></span> <span data-ttu-id="de701-125">Ein partitionsmoniker wird im Code verwendet, um die Partition der aktivierten Komponente explizit anzugeben.</span><span class="sxs-lookup"><span data-stu-id="de701-125">A partition moniker is used within code to explicitly specify the partition of the activated component.</span></span> <span data-ttu-id="de701-126">Wenn ein partitionsmoniker zum Auffinden der Partition verwendet wird, erfolgt die Aktivierung von dieser Partition.</span><span class="sxs-lookup"><span data-stu-id="de701-126">If a partition moniker is used to locate the partition, the activation occurs from that partition.</span></span> <span data-ttu-id="de701-127">Das heißt, die Partitions-ID, die im Moniker enthalten ist, hat Vorrang vor der Standard Partition des Benutzers oder über eine Partitions-ID, die im Kontext des Aufrufers vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="de701-127">That is, the partition ID included in the moniker takes precedence over the user's default partition or over a partition ID that exists in the caller's context.</span></span>

<span data-ttu-id="de701-128">In C++-Code lautet die Syntax für die Verwendung eines partitionsmonikers wie folgt:</span><span class="sxs-lookup"><span data-stu-id="de701-128">In C++ code, the syntax for the use of a partition moniker is as follows:</span></span>


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



<span data-ttu-id="de701-129">Das folgende Beispiel zeigt einen Code Ausschnitt von C++-Code, in dem ein partitionsmoniker als Argument für die [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) -Funktion verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="de701-129">The following example shows a snippet of C++ code, in which a partition moniker is being used as an argument to the [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function:</span></span>


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



<span data-ttu-id="de701-130">In Visual Basic Code lautet die Syntax für einen partitionsmoniker wie folgt:</span><span class="sxs-lookup"><span data-stu-id="de701-130">In Visual Basic code, the syntax for a partition moniker is as follows:</span></span>


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



<span data-ttu-id="de701-131">Das folgende Beispiel zeigt einen Ausschnitt von Visual Basic-Code, in dem ein partitionsmoniker als Argument für die **GetObject** -Funktion verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="de701-131">The following example shows a snippet of Visual Basic code, in which a partition moniker is being used as an argument to the **GetObject** function:</span></span>


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a><span data-ttu-id="de701-132">Verwendung der Standard Zuordnung</span><span class="sxs-lookup"><span data-stu-id="de701-132">Use of Default Mapping</span></span>

<span data-ttu-id="de701-133">Wenn die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion verwendet wird, um eine Komponente mithilfe der CLSID der Komponente zu aktivieren, verwendet com+ die standardmäßige Benutzer Identitäts Zuordnung, d. h. den Partitions Satz, dem der Benutzer in Active Directory zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="de701-133">When the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function is used to activate a component, using the component's CLSID, COM+ uses the default user-identity mapping that is, the partition set that the user is mapped to within Active Directory.</span></span> <span data-ttu-id="de701-134">Wenn der Benutzer jedoch keinem in Active Directory zugeordneten Partitions Satz zugeordnet ist, wird die globale Partition ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="de701-134">However, if the user is not mapped to a partition set within Active Directory, the Global Partition is selected.</span></span>

## <a name="use-of-partition-ids-and-object-context"></a><span data-ttu-id="de701-135">Verwendung von Partitions-IDs und Objekt Kontext</span><span class="sxs-lookup"><span data-stu-id="de701-135">Use of Partition IDs and Object Context</span></span>

<span data-ttu-id="de701-136">Eine der fünf Eigenschaften, die einer neuen Partition zugewiesen ist, ist die Partitions-ID.</span><span class="sxs-lookup"><span data-stu-id="de701-136">One of the five properties assigned to a new partition is the partition ID.</span></span> <span data-ttu-id="de701-137">Wenn das Client Programm die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufruft, um ein Objekt zu instanziieren, wird die Partitions-ID dem Kontext hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="de701-137">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to instantiate an object, the partition ID is added to the context.</span></span> <span data-ttu-id="de701-138">Die Verwendung der Partitions-ID aus dem Kontext zum Suchen der Partition ist wichtig, da sie sicherstellt, dass nach Beginn einer Kette von Aktivierungen die Partitions-ID unverändert bleibt, es sei denn, Sie wird explizit durch einen partitionmoniker geändert.</span><span class="sxs-lookup"><span data-stu-id="de701-138">Using the partition ID from the context to locate the partition is important because it ensures that after a chain of activations has begun, the partition ID remains the same unless it is changed explicitly through a partition moniker.</span></span>

<span data-ttu-id="de701-139">Weitere Informationen zum Suchen von Partitionen während der Aktivierung finden Sie unter [com+-in der Warteschlange befindliche Komponenten und Partitionen](com--queued-components-and-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="de701-139">For additional information on locating partitions during activation, see [COM+ Queued Components and Partitions](com--queued-components-and-partitions.md).</span></span>

## <a name="local-and-remote-activation"></a><span data-ttu-id="de701-140">Lokale Aktivierung und Remote Aktivierung</span><span class="sxs-lookup"><span data-stu-id="de701-140">Local and Remote Activation</span></span>

-   <span data-ttu-id="de701-141">Wenn die aufgerufene Komponente auf einem anderen Computer vorhanden ist, werden die Partitions Eigenschaften (einschließlich der Partitions-ID) an den anderen Computer gemarshallt, und die Komponente wird von der gemarshallten Partition aus aktiviert.</span><span class="sxs-lookup"><span data-stu-id="de701-141">If the component being called exists on another computer, the partition properties (including the partition ID) are marshaled to the other computer and the component is activated from the marshaled partition.</span></span> <span data-ttu-id="de701-142">Wenn keine Partitions-ID gemarshallt wurde, verwendet com+ den Standard Partitions Satz, der der Benutzeridentität in Active Directory zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="de701-142">If no partition ID was marshaled, COM+ uses the default partition set mapped to the user identity within Active Directory.</span></span>

## <a name="the-partition-cache"></a><span data-ttu-id="de701-143">Der Partitions Cache</span><span class="sxs-lookup"><span data-stu-id="de701-143">The Partition Cache</span></span>

<span data-ttu-id="de701-144">In einer Domänen Umgebung verwendet com+ die Zuordnungen in Active Directory, um die richtige Partition für die Komponenten Aktivierung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="de701-144">In a domain environment, COM+ uses the mappings in Active Directory to locate the correct partition for component activation.</span></span> <span data-ttu-id="de701-145">Häufige Suchvorgänge in Active Directory können jedoch zu einem übermäßigen Netzwerkverkehr führen.</span><span class="sxs-lookup"><span data-stu-id="de701-145">However, frequent lookups in Active Directory can result in excessive network traffic.</span></span> <span data-ttu-id="de701-146">Um den Netzwerk Datenverkehr zu minimieren, der sich aus häufigen suchen der Zuordnung zwischen Benutzern und Partitionen in Active Directory ergibt, verwendet com+ einen *Partitions Cache*.</span><span class="sxs-lookup"><span data-stu-id="de701-146">To minimize network traffic resulting from frequent lookups of user-to-partition-set mapping in Active Directory, COM+ uses a *partition cache*.</span></span>

<span data-ttu-id="de701-147">Der Partitions Cache enthält die Zuordnungen, die in Active Directory zwischen Benutzer Identitäten oder Organisationseinheiten und deren Partitions Sätzen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="de701-147">The partition cache contains the mappings that were made in Active Directory between user identities or OUs and their partition sets.</span></span> <span data-ttu-id="de701-148">Dieser Partitions Cache befindet sich auf dem Anwendungsserver, auf dem sich die com+-Anwendungen befinden.</span><span class="sxs-lookup"><span data-stu-id="de701-148">This partition cache is located on the application server on which the COM+ applications reside.</span></span>

<span data-ttu-id="de701-149">Wenn com+ die Standard Partition eines Benutzers bestimmen oder die Zugriffsrechte eines Benutzers auf eine Partition überprüfen muss, wird der Partitions Cache lokal überprüft, um die Zuordnung des Benutzers zu überprüfen, anstatt Active Directory Remote zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="de701-149">When COM+ needs to determine a user's default partition or validate a user's access rights to a partition, it checks the partition cache locally to look up the user's mapping, instead of checking Active Directory remotely.</span></span>

<span data-ttu-id="de701-150">Wenn die Suche im Partitions Cache fehlschlägt, prüft com+ Active Directory.</span><span class="sxs-lookup"><span data-stu-id="de701-150">If the lookup in the partition cache fails, COM+ then checks Active Directory.</span></span> <span data-ttu-id="de701-151">Wenn die Suche in Active Directory erfolgreich ist, speichert com+ diese Zuordnung im Partitions Cache.</span><span class="sxs-lookup"><span data-stu-id="de701-151">If the lookup is successful in Active Directory, COM+ stores that mapping in the partition cache.</span></span> <span data-ttu-id="de701-152">Wenn Sie das nächste Mal eine Suche für die Zuordnung zwischen Benutzern und Partitionen durchführt, wird Sie von com+ im Partitions Cache gefunden.</span><span class="sxs-lookup"><span data-stu-id="de701-152">The next time a lookup is done for that user-to-partition mapping, COM+ will find it in the partition cache.</span></span>

<span data-ttu-id="de701-153">Die folgende Abbildung zeigt den Prozess, den com+ verwendet, um eine Partition für die Komponenten Aktivierung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="de701-153">The following illustration shows the process that COM+ uses to locate a partition for component activation.</span></span>

![Diagramm, das eine Problem Behandlungs Struktur für den Prozess anzeigt, den com+ zum Suchen einer Partition für die Komponenten Aktivierung verwendet.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

<span data-ttu-id="de701-155">Die Größe des Caches und die Ablaufzeit für die Cache Einträge werden über Registrierungsschlüssel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="de701-155">The size of the cache and the expiration time for the cache entries are set via registry keys.</span></span> <span data-ttu-id="de701-156">Weitere Informationen zum Konfigurieren dieser Registrierungsschlüssel finden Sie unter [Erstellen und Konfigurieren von COM+-Partitionen](creating-and-configuring-com--partitions.md).</span><span class="sxs-lookup"><span data-stu-id="de701-156">For information on configuring these registry keys, see [Creating and Configuring COM+ Partitions](creating-and-configuring-com--partitions.md).</span></span>

> [!Note]  
> <span data-ttu-id="de701-157">Wenn ein Server Computer vom Netzwerk getrennt ist und die Zuordnung zwischen Benutzer und Partition geändert wird, während der Server getrennt wird, kann der Partitions Cache eine veraltete Zuordnung zwischen Benutzern und Partitionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="de701-157">If a server computer is disconnected from the network and the user-to-partition mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition mapping.</span></span> <span data-ttu-id="de701-158">Dies kann zu einem Aktivierungs Fehler führen, wenn die Zuordnung zwischen Benutzer und Partition der Mechanismus ist, der zum Aktivieren einer Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="de701-158">This could result in an activation error if user-to-partition mapping is the mechanism used to activate a component.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="de701-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="de701-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de701-160">Suchen einer Komponente zur Aktivierung</span><span class="sxs-lookup"><span data-stu-id="de701-160">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)
</dt> </dl>

 

