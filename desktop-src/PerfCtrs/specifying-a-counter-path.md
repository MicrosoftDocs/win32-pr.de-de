---
description: Das System verwendet Leistungsindikatoren, um Leistungsdaten zu erfassen.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Angeben eines Indikatorpfads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a92f94b4bf3d2252903d92785f43bb0cac110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347362"
---
# <a name="specifying-a-counter-path"></a><span data-ttu-id="10ab4-103">Angeben eines Indikatorpfads</span><span class="sxs-lookup"><span data-stu-id="10ab4-103">Specifying a Counter Path</span></span>

<span data-ttu-id="10ab4-104">Das System verwendet Leistungsindikatoren, um Leistungsdaten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="10ab4-104">The system uses counters to collect performance data.</span></span> <span data-ttu-id="10ab4-105">Jeder Counter wird durch seinen Namen und Pfad bzw. Speicherort eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="10ab4-105">Each counter is uniquely identified through its name and its path, or location.</span></span> <span data-ttu-id="10ab4-106">Die Syntax eines Counter-Pfads lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="10ab4-106">The syntax of a counter path is:</span></span>

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

<span data-ttu-id="10ab4-107">Das Computer Element gibt den Namen oder die IP-Adresse des Computers an, von dem Sie die Leistungsdaten Abfragen möchten.</span><span class="sxs-lookup"><span data-stu-id="10ab4-107">The Computer element specifies the name or IP address of the computer from which you want to query performance data.</span></span> <span data-ttu-id="10ab4-108">Der Computername ist optional, wenn sich der gegen Computer auf dem lokalen Computer befindet.</span><span class="sxs-lookup"><span data-stu-id="10ab4-108">The computer name is optional if the counter is located on the local computer.</span></span>

<span data-ttu-id="10ab4-109">Das perfobject-Element gibt das abzufragende Leistungs Objekt an.</span><span class="sxs-lookup"><span data-stu-id="10ab4-109">The PerfObject element specifies the performance object to query.</span></span> <span data-ttu-id="10ab4-110">Ein Leistungs Objekt kann eine physische Komponente sein, z. b. Prozessoren, Datenträger und Arbeitsspeicher, oder ein Systemobjekt, z. b. Prozesse und Threads.</span><span class="sxs-lookup"><span data-stu-id="10ab4-110">A performance object can be a physical component, such as processors, disks, and memory, or a system object, such as processes and threads.</span></span> <span data-ttu-id="10ab4-111">Jedes Systemobjekt ist mit einem funktionalen Element innerhalb des Computers verknüpft und verfügt über einen Satz von Standard Zählern.</span><span class="sxs-lookup"><span data-stu-id="10ab4-111">Each system object is related to a functional element within the computer and has a set of standard counters assigned to it.</span></span> <span data-ttu-id="10ab4-112">Auf jedem Computer sind möglicherweise andere Leistungs Objekte und Leistungsindikatoren installiert, da Anwendungen eigene Leistungs Objekte und-Indikatoren installieren können.</span><span class="sxs-lookup"><span data-stu-id="10ab4-112">Each computer may have a different set of performance objects and counters installed on it because applications can install their own performance objects and counters.</span></span> <span data-ttu-id="10ab4-113">Eine Liste der Leistungs Objekte und-Indikatoren, die auf Ihrem Computer installiert sind, finden Sie im Dialogfeld Leistungsindikatoren **Hinzufügen** im Leistungs Tool auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="10ab4-113">For a list of the performance objects and counters installed on your computer, see the **Add Counters** dialog box in the Performance tool on your computer.</span></span> <span data-ttu-id="10ab4-114">Diese Objekte werden auch im Dialogfeld PDH-durchsuchen aufgelistet (siehe Such [Zähler](browsing-counters.md)).</span><span class="sxs-lookup"><span data-stu-id="10ab4-114">These objects are also listed in the PDH browse dialog box (see [Browsing Counters](browsing-counters.md)).</span></span> <span data-ttu-id="10ab4-115">Eine Liste der Systemleistungs Objekte und-Indikatoren finden Sie unter Indikatoren [nach Objekt](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="10ab4-115">For a list of system performance objects and counters, see [Counters by Object](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span></span>

<span data-ttu-id="10ab4-116">Die Parametern instance, ObjectInstance und instanceindex sind im Pfad enthalten, wenn mehrere Instanzen des Objekts vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="10ab4-116">The ParentInstance, ObjectInstance, and InstanceIndex are included in the path if multiple instances of the object can exist.</span></span> <span data-ttu-id="10ab4-117">Prozesse und Threads sind z. b. mehrere Instanzobjekte, da mehrere Prozesse oder Threads gleichzeitig ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="10ab4-117">For example, processes and threads are multiple instance objects because more than one process or thread can run at the same time.</span></span> <span data-ttu-id="10ab4-118">Wenn ein Objekt über mehr als eine Instanz verfügen kann, muss der Counter-Pfad eine Objektinstanz angeben.</span><span class="sxs-lookup"><span data-stu-id="10ab4-118">If an object can have more than one instance, the counter path must specify an object instance.</span></span>

<span data-ttu-id="10ab4-119">Das Format der instanzbezogenen Elemente hängt vom Objekttyp ab.</span><span class="sxs-lookup"><span data-stu-id="10ab4-119">The format of the instance related elements depends on the object type.</span></span> <span data-ttu-id="10ab4-120">Wenn das-Objekt über einfache Instanzen verfügt, ist das Format nur der in Klammern eingeschlossene Instanzname.</span><span class="sxs-lookup"><span data-stu-id="10ab4-120">If the object has simple instances, then the format is only the instance name enclosed in parentheses.</span></span> <span data-ttu-id="10ab4-121">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="10ab4-121">For example:</span></span>

``` syntax
(Explorer)
```

<span data-ttu-id="10ab4-122">Wenn für die Instanz dieses Objekts auch ein übergeordneter Instanzname erforderlich ist, muss der Name der übergeordneten Instanz vor der Objektinstanz stehen und durch einen Schrägstrich getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="10ab4-122">If the instance of this object also requires a parent instance name, the parent instance name must come before the object instance and be separated by a forward slash character.</span></span> <span data-ttu-id="10ab4-123">Threads gehören z. b. zu Prozessen.</span><span class="sxs-lookup"><span data-stu-id="10ab4-123">For example, threads belong to processes.</span></span> <span data-ttu-id="10ab4-124">Wenn Sie ein Thread Objekt Abfragen, müssen Sie auch den Prozess angeben, zu dem er gehört, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="10ab4-124">If you query a thread object, you must also specify the process to which it belongs as shown in the following example:</span></span>

``` syntax
(Explorer/0)
```

<span data-ttu-id="10ab4-125">Wenn das Objekt mehrere Instanzen mit derselben namens Zeichenfolge aufweist, können diese sequenziell indiziert werden, indem der Instanzindex angegeben wird, dem ein Nummern Zeichen vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="10ab4-125">If the object has multiple instances that have the same name string, they can be indexed sequentially by specifying the instance index prefixed by a pound sign.</span></span> <span data-ttu-id="10ab4-126">Instanzindizes sind 0-basiert.</span><span class="sxs-lookup"><span data-stu-id="10ab4-126">Instance indexes are 0-based.</span></span> <span data-ttu-id="10ab4-127">Wenn Sie die erste Instanz abfragen möchten, schließen Sie 0 nicht ein \# – Geben Sie einfach den Instanznamen an.</span><span class="sxs-lookup"><span data-stu-id="10ab4-127">If you want to query the first instance, do not include \#0—just specify the instance name.</span></span> <span data-ttu-id="10ab4-128">Um die zweite Instanz anzugeben, verwenden \# Sie 1. um die dritte Instanz anzugeben, verwenden Sie \# 2 usw.</span><span class="sxs-lookup"><span data-stu-id="10ab4-128">To specify the second instance, use \#1; to specify the third instance, use \#2; and so on.</span></span> <span data-ttu-id="10ab4-129">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="10ab4-129">For example:</span></span>

``` syntax
(Explorer/0#1)
```

<span data-ttu-id="10ab4-130">Das Counter-Element gibt den Leistungs Zählers an, den Sie für das angegebene Leistungs Objekt Abfragen möchten.</span><span class="sxs-lookup"><span data-stu-id="10ab4-130">The Counter element specifies the performance counter that you want to query for the given the performance object.</span></span>

<span data-ttu-id="10ab4-131">PDH verwendet die folgenden Sonderzeichen in einem Counter-Pfad.</span><span class="sxs-lookup"><span data-stu-id="10ab4-131">PDH uses the following special characters in a counter path.</span></span> <span data-ttu-id="10ab4-132">Anbieter sollten diese Zeichen nicht in ihren Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="10ab4-132">Providers should not use these characters in their names.</span></span> <span data-ttu-id="10ab4-133">Wenn ein Anbieter diese Sonderzeichen verwendet, kann PDH den vollständigen Counter-Pfad nicht analysieren, um den Namen des Zählers und der Instanzen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="10ab4-133">If a provider uses these special characters, PDH cannot parse the full counter path to obtain the counter and instances names.</span></span>



| <span data-ttu-id="10ab4-134">Zeichen</span><span class="sxs-lookup"><span data-stu-id="10ab4-134">Character</span></span> | <span data-ttu-id="10ab4-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10ab4-135">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| \\        | <span data-ttu-id="10ab4-136">Allgemeines Trennzeichen für Computer, Objekt und Counter.</span><span class="sxs-lookup"><span data-stu-id="10ab4-136">Generic separator for computer, object, and counter.</span></span>       |
| <span data-ttu-id="10ab4-137">(</span><span class="sxs-lookup"><span data-stu-id="10ab4-137">(</span></span>         | <span data-ttu-id="10ab4-138">Anfang des Instanznamens.</span><span class="sxs-lookup"><span data-stu-id="10ab4-138">Beginning of instance name.</span></span>                                |
| <span data-ttu-id="10ab4-139">)</span><span class="sxs-lookup"><span data-stu-id="10ab4-139">)</span></span>         | <span data-ttu-id="10ab4-140">Das Beenden des Instanznamens.</span><span class="sxs-lookup"><span data-stu-id="10ab4-140">Ending of instance name.</span></span>                                   |
| /         | <span data-ttu-id="10ab4-141">Trennt die Instanz und die übergeordnete Instanz.</span><span class="sxs-lookup"><span data-stu-id="10ab4-141">Separates instance and parent instance.</span></span>                    |
| <span data-ttu-id="10ab4-142">\#n</span><span class="sxs-lookup"><span data-stu-id="10ab4-142">\#n</span></span>       | <span data-ttu-id="10ab4-143">Identifiziert ein bestimmtes Vorkommen einer Instanz mit demselben Namen.</span><span class="sxs-lookup"><span data-stu-id="10ab4-143">Identifies a specific occurrence of a same-named instance.</span></span> |
| \*        | <span data-ttu-id="10ab4-144">Platzhalter Zeichen.</span><span class="sxs-lookup"><span data-stu-id="10ab4-144">Wildcard character.</span></span>                                        |



 

<span data-ttu-id="10ab4-145">In den folgenden Beispielen werden die möglichen Formate für-Counter-Pfade veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="10ab4-145">The following examples show the possible formats for counter paths:</span></span>

-   <span data-ttu-id="10ab4-146">\\\\Computer \\ Objekt (übergeordneter/ \# Instanzindex) Indikator \\</span><span class="sxs-lookup"><span data-stu-id="10ab4-146">\\\\computer\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="10ab4-147">\\\\Computer \\ Objekt (über-/Instanz-Counter) \\</span><span class="sxs-lookup"><span data-stu-id="10ab4-147">\\\\computer\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="10ab4-148">\\\\Indikator für Computer \\ Objekt (Instanzindex \# ) \\</span><span class="sxs-lookup"><span data-stu-id="10ab4-148">\\\\computer\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="10ab4-149">\\\\Computer \\ Objekt (Instanz)- \\ Counter</span><span class="sxs-lookup"><span data-stu-id="10ab4-149">\\\\computer\\object(instance)\\counter</span></span>
-   <span data-ttu-id="10ab4-150">\\\\Computer \\ Objekt- \\ Counter</span><span class="sxs-lookup"><span data-stu-id="10ab4-150">\\\\computer\\object\\counter</span></span>
-   <span data-ttu-id="10ab4-151">\\Objekt Indikator (übergeordneter/ \# Instanzindex) \\</span><span class="sxs-lookup"><span data-stu-id="10ab4-151">\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="10ab4-152">\\Objekttyp (übergeordnet/ \\ Instanz)</span><span class="sxs-lookup"><span data-stu-id="10ab4-152">\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="10ab4-153">\\Indikator für Objekt ( \# Instanzindex) \\</span><span class="sxs-lookup"><span data-stu-id="10ab4-153">\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="10ab4-154">\\Objekt-(Instanz-) \\ Counter</span><span class="sxs-lookup"><span data-stu-id="10ab4-154">\\object(instance)\\counter</span></span>
-   <span data-ttu-id="10ab4-155">\\Objekt- \\ Counter</span><span class="sxs-lookup"><span data-stu-id="10ab4-155">\\object\\counter</span></span>

## <a name="using-wildcard-characters"></a><span data-ttu-id="10ab4-156">Verwenden von Platzhalter Zeichen</span><span class="sxs-lookup"><span data-stu-id="10ab4-156">Using wildcard characters</span></span>

<span data-ttu-id="10ab4-157">Die Anzahl der Pfade kann ein Platzhalter Zeichen nur für den Instanznamen enthalten, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="10ab4-157">Counter paths may contain a wildcard character only for the instance name as shown in the following example.</span></span>

``` syntax
\Process(*)\% Processor Time
```

<span data-ttu-id="10ab4-158">Um das Platzhalter Zeichen in eine Liste von Counter-Pfaden zu erweitern, die auf dem Computer oder in der Protokolldatei gefundene Instanzen enthalten, nennen Sie [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span><span class="sxs-lookup"><span data-stu-id="10ab4-158">To expand the wildcard into a list of counter paths that contain instances found on the computer or in the log file, call [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span></span>

 

 
