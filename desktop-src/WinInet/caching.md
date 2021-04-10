---
title: Caching (Windows Internet)
description: Die WinInet-Funktionen verfügen über eine einfache, aber flexible integrierte Cache Unterstützung.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102679"
---
# <a name="caching-windows-internet"></a><span data-ttu-id="00ffa-103">Caching (Windows Internet)</span><span class="sxs-lookup"><span data-stu-id="00ffa-103">Caching (Windows Internet)</span></span>

<span data-ttu-id="00ffa-104">Die WinInet-Funktionen verfügen über eine einfache, aber flexible integrierte Cache Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="00ffa-104">The WinINet functions have simple, yet flexible, built-in caching support.</span></span> <span data-ttu-id="00ffa-105">Alle aus dem Netzwerk abgerufenen Daten werden auf der Festplatte zwischengespeichert und für nachfolgende Anforderungen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-105">Any data retrieved from the network is cached on the hard disk and retrieved for subsequent requests.</span></span> <span data-ttu-id="00ffa-106">Die Anwendung kann das Caching für jede Anforderung steuern.</span><span class="sxs-lookup"><span data-stu-id="00ffa-106">The application can control the caching on each request.</span></span> <span data-ttu-id="00ffa-107">Bei HTTP-Anforderungen vom Server werden die meisten empfangenen Header ebenfalls zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="00ffa-107">For http requests from the server, most headers received are also cached.</span></span> <span data-ttu-id="00ffa-108">Wenn eine HTTP-Anforderung aus dem Cache erfüllt wird, werden die zwischengespeicherten Header auch an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00ffa-108">When an http request is satisfied from the cache, the cached headers are also returned to the caller.</span></span> <span data-ttu-id="00ffa-109">Dadurch werden Daten nahtlos heruntergeladen, unabhängig davon, ob die Daten aus dem Cache oder aus dem Netzwerk stammen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-109">This makes data download seamless, whether the data is coming from the cache or from the network.</span></span>

<span data-ttu-id="00ffa-110">Anwendungen müssen einen Puffer ordnungsgemäß zuordnen, um die gewünschten Ergebnisse zu erhalten, wenn Sie die persistenten URL-zwischen Speicherungs Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-110">Applications must properly allocate a buffer in order to get the desired results when using the persistent URL caching functions.</span></span> <span data-ttu-id="00ffa-111">Weitere Informationen finden Sie unter [Verwenden von Puffern](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="00ffa-111">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>

## <a name="cache-behavior-during-response-processing"></a><span data-ttu-id="00ffa-112">Cache Verhalten während der Antwort Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="00ffa-112">Cache Behavior During Response Processing</span></span>

<span data-ttu-id="00ffa-113">Der WinInet-Cache ist kompatibel mit den HTTP-Cache-Control-Direktiven, die in RFC 2616 beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-113">The WinINet cache is compliant with the HTTP cache-control directives described in RFC 2616.</span></span> <span data-ttu-id="00ffa-114">Die Cache-Control-Direktiven und anwendungssetflags bestimmen, was zwischengespeichert werden kann. Allerdings bestimmt WinInet, was nach dem folgenden Kriterium tatsächlich zwischengespeichert wird:</span><span class="sxs-lookup"><span data-stu-id="00ffa-114">The cache-control directives and application set flags determine what may be cached; however, WinINet determines what is actually cached based on the following criterion:</span></span>

-   <span data-ttu-id="00ffa-115">WinInet speichert nur http-und FTP-Antworten zwischen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-115">WinINet only caches HTTP and FTP responses.</span></span>
-   <span data-ttu-id="00ffa-116">Nur gut verhaltene Antworten können von einem Cache gespeichert und in einer Antwort auf eine nachfolgende Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-116">Only well behaved responses may be stored by a cache and used in a reply to a subsequent Request.</span></span> <span data-ttu-id="00ffa-117">Wohl verhaltene Antworten werden als Antworten definiert, die erfolgreich zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-117">Well behaved responses are defined as responses that return successfully.</span></span>
-   <span data-ttu-id="00ffa-118">Standardmäßig speichert WinInet erfolgreiche Antworten zwischen, es sei denn, entweder eine Cache Steuerungs Direktive vom Server oder ein Anwendungs definiertes Flag gibt ausdrücklich an, dass die Antwort nicht zwischengespeichert werden darf.</span><span class="sxs-lookup"><span data-stu-id="00ffa-118">By default, WinINet will cache successful responses unless either a cache-control directive from the server, or an application-defined flag specifically denote that the response may not be cached.</span></span>
-   <span data-ttu-id="00ffa-119">Im Allgemeinen werden Antworten auf das Get-Verb zwischengespeichert, wenn die oben aufgeführten Anforderungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="00ffa-119">In general, responses to the GET verb are cached if the requirements listed above are met.</span></span> <span data-ttu-id="00ffa-120">Antworten auf Put-und Post-Verben werden unter keinen Umständen zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="00ffa-120">Responses to PUT and POST verbs are not cached under any circumstances.</span></span>
-   <span data-ttu-id="00ffa-121">Elemente werden zwischengespeichert, auch wenn der Cache voll ist.</span><span class="sxs-lookup"><span data-stu-id="00ffa-121">Items will be cached even when the cache is full.</span></span> <span data-ttu-id="00ffa-122">Wenn ein hinzugefügtes Element den Cache über der Größenbeschränkung überschreitet, wird die Cache-Scavenger geplant.</span><span class="sxs-lookup"><span data-stu-id="00ffa-122">If an added item is puts the cache over the size limit, the cache scavenger is scheduled.</span></span> <span data-ttu-id="00ffa-123">Standardmäßig ist es nicht sichergestellt, dass Elemente im Cache mehr als 10 Minuten verbleiben.</span><span class="sxs-lookup"><span data-stu-id="00ffa-123">By default, items are not guaranteed to remain more than 10 minutes in the cache.</span></span> <span data-ttu-id="00ffa-124">Weitere Informationen finden Sie im Abschnitt [Cache Scavenger](#cache-scavenger) weiter unten.</span><span class="sxs-lookup"><span data-stu-id="00ffa-124">For more information, see the [Cache Scavenger](#cache-scavenger) section below.</span></span>
-   <span data-ttu-id="00ffa-125">HTTPS wird standardmäßig zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="00ffa-125">Https is cached by default.</span></span> <span data-ttu-id="00ffa-126">Dies wird durch eine globale Einstellung verwaltet, die nicht durch Anwendungs definierte Cache Direktiven überschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="00ffa-126">This is managed by a global setting that cannot be overridden by application-defined cache directives.</span></span> <span data-ttu-id="00ffa-127">Wenn Sie die globale Einstellung außer Kraft setzen möchten, wählen Sie in der Systemsteuerung das Applet Internet Optionen aus, und navigieren Sie zur Registerkarte Erweitert. Aktivieren Sie das Kontrollkästchen "verschlüsselte Seiten auf dem Datenträger nicht speichern" im Abschnitt "Sicherheit".</span><span class="sxs-lookup"><span data-stu-id="00ffa-127">To override the global setting, select the Internet Options applet in the control panel, and go to the advanced tab. Check the "Do not save encrypted pages to disk" box under the "Security" section.</span></span>

## <a name="cache-scavenger"></a><span data-ttu-id="00ffa-128">Scavenger Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="00ffa-128">Cache Scavenger</span></span>

<span data-ttu-id="00ffa-129">Der Cache Scavenger bereinigt regelmäßig Elemente aus dem Cache.</span><span class="sxs-lookup"><span data-stu-id="00ffa-129">The cache scavenger periodically cleans items from the cache.</span></span> <span data-ttu-id="00ffa-130">Wenn ein Element dem Cache hinzugefügt wird und der Cache voll ist, wird das Element dem Cache hinzugefügt, und der Cache Scavenger ist geplant.</span><span class="sxs-lookup"><span data-stu-id="00ffa-130">If an item is added to the cache and the cache is full, the item is added to the cache and the cache scavenger is scheduled.</span></span> <span data-ttu-id="00ffa-131">Wenn die Cache-Scavenger eine Rundungs Runde abgeschlossen hat und der Cache das Cache Limit nicht erreicht hat, wird für die Scavenger eine weitere Runde eingeplant, wenn dem Cache ein anderes Element hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="00ffa-131">If the cache scavenger completes a round of scavenging and the cache has not reached the cache limit, the scavenger is scheduled for another round when another item is added to the cache.</span></span> <span data-ttu-id="00ffa-132">Im Allgemeinen wird die Scavenger geplant, wenn ein hinzugefügtes Element den Cache über das Größenlimit hinaus verschiebt.</span><span class="sxs-lookup"><span data-stu-id="00ffa-132">In general, the scavenger is scheduled when an added item puts the cache over its size limit.</span></span> <span data-ttu-id="00ffa-133">Standardmäßig ist die minimale Gültigkeitsdauer im Cache auf 10 Minuten festgelegt, sofern in einer Cache Steuerungs Anweisung nichts anderes angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="00ffa-133">By default, the minimum time to live in the cache is set to 10 minutes unless otherwise specified in a cache-control directive.</span></span> <span data-ttu-id="00ffa-134">Wenn die Cache-Scavenger initiiert wird, gibt es keine Garantie dafür, dass die ältesten Elemente als erstes aus dem Cache gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-134">When the cache scavenger is initiated, there is no guarantee that the oldest items are the first to be deleted from the cache.</span></span>

<span data-ttu-id="00ffa-135">Der Cache wird für denselben Benutzer für alle WinINet-Anwendungen auf dem Computer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="00ffa-135">The cache is shared across all WinINet applications on the computer for the same user.</span></span> <span data-ttu-id="00ffa-136">Ab Windows Vista und Windows Server 2008 ist die Cache Größe auf 1/32 ND die Größe des Datenträgers mit einer Mindestgröße von 8 MB und einer maximalen Größe von 50 MB festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00ffa-136">Starting with Windows Vista and Windows Server 2008 the cache size is set to 1/32nd the size of the disk, with a minimum size of 8MB and a maximum size of 50MB.</span></span>

## <a name="using-flags-to-control-caching"></a><span data-ttu-id="00ffa-137">Verwenden von Flags zum Steuern der Zwischenspeicherung</span><span class="sxs-lookup"><span data-stu-id="00ffa-137">Using Flags to Control Caching</span></span>

<span data-ttu-id="00ffa-138">Mithilfe der cacheflags kann eine Anwendung steuern, wann und wie Sie den Cache verwendet.</span><span class="sxs-lookup"><span data-stu-id="00ffa-138">The caching flags allow an application to control when and how it uses the cache.</span></span> <span data-ttu-id="00ffa-139">Diese Flags können allein oder in Kombination mit dem *dwFlags* -Parameter in Funktionen verwendet werden, die auf Informationen oder Ressourcen im Internet zugreifen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-139">These flags can be used alone or in combination with the *dwFlags* parameter in functions that access information or resources on the Internet.</span></span> <span data-ttu-id="00ffa-140">Standardmäßig werden von den Funktionen alle aus dem Internet heruntergeladenen Daten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="00ffa-140">By default, the functions store all data downloaded from the Internet.</span></span>

<span data-ttu-id="00ffa-141">Die folgenden Flags können verwendet werden, um das Zwischenspeichern zu steuern.</span><span class="sxs-lookup"><span data-stu-id="00ffa-141">The following flags can be used to control caching.</span></span>



| <span data-ttu-id="00ffa-142">Wert</span><span class="sxs-lookup"><span data-stu-id="00ffa-142">Value</span></span>                                                                                                                                                  | <span data-ttu-id="00ffa-143">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="00ffa-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00ffa-144">**Internet- \_ Flag- \_ Cache \_ Async**</span><span class="sxs-lookup"><span data-stu-id="00ffa-144">**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>](api-flags.md)                                                                            | <span data-ttu-id="00ffa-145">Dieses Flag hat keine Wirkung.</span><span class="sxs-lookup"><span data-stu-id="00ffa-145">This flag has no effect.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="00ffa-146">**Internet- \_ Flag- \_ Cache, \_ Wenn \_ net \_ fehlschlägt**</span><span class="sxs-lookup"><span data-stu-id="00ffa-146">**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>](api-flags.md)                                                              | <span data-ttu-id="00ffa-147">Gibt die Ressource aus dem Cache zurück, wenn die Netzwerk Anforderung für die Ressource aufgrund eines [Fehlers \_ beim \_ \_ Zurücksetzen der Internetverbindung](wininet-errors.md) oder des Fehlers " [ \_ Internet \_ kann nicht \_ verbunden](wininet-errors.md) werden" fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="00ffa-147">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="00ffa-148">Dieses Flag wird von [**httpoperrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)verwendet.</span><span class="sxs-lookup"><span data-stu-id="00ffa-148">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                                                                              |
| [<span data-ttu-id="00ffa-149">**internetflag nicht zwischen \_ \_ \_ Speichern**</span><span class="sxs-lookup"><span data-stu-id="00ffa-149">**INTERNET\_FLAG\_DONT\_CACHE**</span></span>](api-flags.md)                                                                              | <span data-ttu-id="00ffa-150">Speichert die Daten weder lokal noch in Gateways.</span><span class="sxs-lookup"><span data-stu-id="00ffa-150">Does not cache the data, either locally or in any gateways.</span></span> <span data-ttu-id="00ffa-151">Identisch mit dem bevorzugten Wert, [**Internet \_ Flag \_ kein \_ Cache \_ Schreibvorgang**](api-flags.md).</span><span class="sxs-lookup"><span data-stu-id="00ffa-151">Identical to the preferred value, [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | <span data-ttu-id="00ffa-152">Gibt an, dass dies eine Formular Übermittlung ist.</span><span class="sxs-lookup"><span data-stu-id="00ffa-152">Indicates that this is a Forms submission.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="00ffa-153">[**Internet \_ Flag \_ aus \_ Cache**](api-flags.md)[**Internet \_ Flag zum über \_ \_ Mitteln von Formularen**](api-flags.md)</span><span class="sxs-lookup"><span data-stu-id="00ffa-153">[**INTERNET\_FLAG\_FROM\_CACHE**](api-flags.md)[**INTERNET\_FLAG\_FORMS\_SUBMIT**](api-flags.md)</span></span> | <span data-ttu-id="00ffa-154">Keine Netzwerk Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-154">Does not make network requests.</span></span> <span data-ttu-id="00ffa-155">Alle Entitäten werden aus dem Cache zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00ffa-155">All entities are returned from the cache.</span></span> <span data-ttu-id="00ffa-156">Wenn sich das angeforderte Element nicht im Cache befindet, wird ein geeigneter Fehler (z \_ . b. Fehler Datei \_ nicht \_ gefunden) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00ffa-156">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="00ffa-157">Nur die [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion verwendet dieses Flag.</span><span class="sxs-lookup"><span data-stu-id="00ffa-157">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>                                                                                                                                                                                                       |
| [<span data-ttu-id="00ffa-158">**Internet Kennzeichen- \_ Flag \_ \_ zurück**</span><span class="sxs-lookup"><span data-stu-id="00ffa-158">**INTERNET\_FLAG\_FWD\_BACK**</span></span>](api-flags.md)                                                                                  | <span data-ttu-id="00ffa-159">Gibt an, dass die Funktion die Kopie der Ressource verwenden soll, die sich derzeit im Internet Cache befindet.</span><span class="sxs-lookup"><span data-stu-id="00ffa-159">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="00ffa-160">Das Ablaufdatum und andere Informationen über die Ressource werden nicht geprüft.</span><span class="sxs-lookup"><span data-stu-id="00ffa-160">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="00ffa-161">Wenn das angeforderte Element nicht im Internet Cache gefunden wird, versucht das System, die Ressource im Netzwerk zu finden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-161">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="00ffa-162">Dieser Wert wurde in Microsoft Internet Explorer 5 eingeführt und ist den vorwärts-und **rückwärts** -Schaltflächen **Vorgängen** von Internet Explorer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="00ffa-162">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span> |
| [<span data-ttu-id="00ffa-163">**Hyperlink zum Internet Kennzeichen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00ffa-163">**INTERNET\_FLAG\_HYPERLINK**</span></span>](api-flags.md)                                                                                 | <span data-ttu-id="00ffa-164">Zwingt die Anwendung, eine Ressource erneut zu laden, wenn keine Ablaufzeit und keine Zeit für die letzte Änderung zurückgegeben wurden, als die Ressource im Cache gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="00ffa-164">Forces the application to reload a resource if no expire time and no last-modified time were returned when the resource was stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="00ffa-165">**\_internetflag \_ \_ dauerhaft machen**</span><span class="sxs-lookup"><span data-stu-id="00ffa-165">**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>](api-flags.md)                                                                    | <span data-ttu-id="00ffa-166">Wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00ffa-166">No longer supported.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="00ffa-167">**Internet \_ Kennzeichen \_ muss \_ Anforderung Zwischenspeichern \_**</span><span class="sxs-lookup"><span data-stu-id="00ffa-167">**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>](api-flags.md)                                                             | <span data-ttu-id="00ffa-168">Bewirkt, dass eine temporäre Datei erstellt wird, wenn die Datei nicht zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="00ffa-168">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="00ffa-169">Dies ist identisch mit dem bevorzugten Wert, [**Internet \_ Flag \_ benötigt \_ Datei**](api-flags.md).</span><span class="sxs-lookup"><span data-stu-id="00ffa-169">This is identical to the preferred value, [**INTERNET\_FLAG\_NEED\_FILE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="00ffa-170">**Internet- \_ Flag \_ benötigt \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="00ffa-170">**INTERNET\_FLAG\_NEED\_FILE**</span></span>](api-flags.md)                                                                                | <span data-ttu-id="00ffa-171">Bewirkt, dass eine temporäre Datei erstellt wird, wenn die Datei nicht zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="00ffa-171">Causes a temporary file to be created if the file cannot be cached.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="00ffa-172">**Internet \_ Kennzeichen \_ ohne \_ Cache \_ Schreibvorgang**</span><span class="sxs-lookup"><span data-stu-id="00ffa-172">**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>](api-flags.md)                                                                     | <span data-ttu-id="00ffa-173">Lehnt den Versuch der Funktion ab, aus dem Internet heruntergeladene Daten im Cache zu speichern.</span><span class="sxs-lookup"><span data-stu-id="00ffa-173">Rejects any attempt by the function to store data downloaded from the Internet in the cache.</span></span> <span data-ttu-id="00ffa-174">Dieses Flag ist erforderlich, wenn die Anwendung nicht möchten, dass heruntergeladene Ressourcen lokal gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-174">This flag is necessary if the application does not want any downloaded resources to be stored locally.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="00ffa-175">**Internet \_ Flag \_ keine \_ Benutzeroberfläche**</span><span class="sxs-lookup"><span data-stu-id="00ffa-175">**INTERNET\_FLAG\_NO\_UI**</span></span>](api-flags.md)                                                                                        | <span data-ttu-id="00ffa-176">Deaktiviert das Cookie-Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="00ffa-176">Disables the cookie dialog box.</span></span> <span data-ttu-id="00ffa-177">Dieses Flag kann von [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwendet werden (nur HTTP-Anforderungen).</span><span class="sxs-lookup"><span data-stu-id="00ffa-177">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="00ffa-178">**Internet- \_ Flag \_ Offline**</span><span class="sxs-lookup"><span data-stu-id="00ffa-178">**INTERNET\_FLAG\_OFFLINE**</span></span>](api-flags.md)                                                                                     | <span data-ttu-id="00ffa-179">Verhindert, dass die Anwendung Anforderungen an das Netzwerk sendet.</span><span class="sxs-lookup"><span data-stu-id="00ffa-179">Prevents the application from sending requests to the network.</span></span> <span data-ttu-id="00ffa-180">Alle Anforderungen werden mithilfe der im Cache gespeicherten Ressourcen aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="00ffa-180">All requests are resolved using the resources stored in the cache.</span></span> <span data-ttu-id="00ffa-181">Wenn sich die Ressource nicht im Cache befindet, wird ein geeigneter Fehler (z \_ . b. Fehler Datei \_ nicht gefunden) \_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00ffa-181">If the resource is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span>                                                                                                                                                                                                                            |
| [<span data-ttu-id="00ffa-182">**Internet \_ Flag \_ pragma \_ NoCache**</span><span class="sxs-lookup"><span data-stu-id="00ffa-182">**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>](api-flags.md)                                                                      | <span data-ttu-id="00ffa-183">Erzwingt, dass die Anforderung vom Ursprungsserver aufgelöst wird, auch wenn eine zwischengespeicherte Kopie auf dem Proxy vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="00ffa-183">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="00ffa-184">Die Funktion " [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) " (nur bei http-und HTTPS-Anforderungen) und die Funktion " [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) " verwenden dieses Flag.</span><span class="sxs-lookup"><span data-stu-id="00ffa-184">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="00ffa-185">**Internet Kennzeichen erneut \_ \_ Laden**</span><span class="sxs-lookup"><span data-stu-id="00ffa-185">**INTERNET\_FLAG\_RELOAD**</span></span>](api-flags.md)                                                                                       | <span data-ttu-id="00ffa-186">Erzwingt, dass die Funktion die angeforderte Ressource direkt aus dem Internet abruft.</span><span class="sxs-lookup"><span data-stu-id="00ffa-186">Forces the function to retrieve the requested resource directly from the Internet.</span></span> <span data-ttu-id="00ffa-187">Die heruntergeladenen Informationen werden im Cache gespeichert.</span><span class="sxs-lookup"><span data-stu-id="00ffa-187">The information that is downloaded is stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="00ffa-188">**Internet- \_ Flag \_ erneut synchronisieren**</span><span class="sxs-lookup"><span data-stu-id="00ffa-188">**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>](api-flags.md)                                                                         | <span data-ttu-id="00ffa-189">Bewirkt, dass eine Anwendung einen bedingten Download der Ressource aus dem Internet ausführt.</span><span class="sxs-lookup"><span data-stu-id="00ffa-189">Causes an application to perform a conditional download of the resource from the Internet.</span></span> <span data-ttu-id="00ffa-190">Wenn die im Cache gespeicherte Version aktuell ist, werden die Informationen aus dem Cache heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-190">If the version stored in the cache is current, the information is downloaded from the cache.</span></span> <span data-ttu-id="00ffa-191">Andernfalls werden die Informationen vom Server erneut geladen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-191">Otherwise, the information is reloaded from the server.</span></span>                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a><span data-ttu-id="00ffa-192">Persistente Caching-Funktionen</span><span class="sxs-lookup"><span data-stu-id="00ffa-192">Persistent Caching Functions</span></span>

<span data-ttu-id="00ffa-193">Clients, die persistente Cache Dienste benötigen, verwenden die persistenten Caching-Funktionen, um Ihren Anwendungen das Speichern von Daten im lokalen Dateisystem für die nachfolgende Verwendung zu ermöglichen, z. b. in Situationen, in denen eine Verbindung mit geringer Bandbreite den Zugriff auf die Daten einschränkt oder der Zugriff überhaupt nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="00ffa-193">Clients that need persistent caching services use the persistent caching functions to allow their applications to save data in the local file system for subsequent use, such as in situations where a low-bandwidth link limits access to the data, or the access is not available at all.</span></span>

<span data-ttu-id="00ffa-194">Die Cache Funktionen bieten persistentes Zwischenspeichern und Offline-Browsen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-194">The cache functions provide persistent caching and offline browsing.</span></span> <span data-ttu-id="00ffa-195">Wenn das [**Internet \_ Flag \_ kein \_ Cache \_ Schreib**](api-flags.md) Flag explizit das Zwischenspeichern angibt, werden von den Funktionen alle aus dem Netzwerk heruntergeladenen Daten zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="00ffa-195">Unless the [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md) flag explicitly specifies no caching, the functions cache all data downloaded from the network.</span></span> <span data-ttu-id="00ffa-196">Die Antworten auf Post-Daten werden nicht zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="00ffa-196">The responses to POST data are not cached.</span></span>

## <a name="using-the-persistent-url-cache-functions"></a><span data-ttu-id="00ffa-197">Verwenden der persistenten URL-Cache Funktionen</span><span class="sxs-lookup"><span data-stu-id="00ffa-197">Using the Persistent URL Cache Functions</span></span>

<span data-ttu-id="00ffa-198">Mit den folgenden permanenten URL-Cache Funktionen kann eine Anwendung auf im Cache gespeicherte Informationen zugreifen und diese bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="00ffa-198">The following persistent URL cache functions allow an application to access and manipulate information stored in the cache.</span></span>



| <span data-ttu-id="00ffa-199">Funktion</span><span class="sxs-lookup"><span data-stu-id="00ffa-199">Function</span></span>                                                           | <span data-ttu-id="00ffa-200">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00ffa-200">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00ffa-201">**Commiturlcacheentrya**</span><span class="sxs-lookup"><span data-stu-id="00ffa-201">**CommitUrlCacheEntryA**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | <span data-ttu-id="00ffa-202">Speichert Daten in der angegebenen Datei im Cache Speicher zwischen und ordnet Sie der angegebenen URL zu.</span><span class="sxs-lookup"><span data-stu-id="00ffa-202">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="00ffa-203">**Commiturlcacheentryw**</span><span class="sxs-lookup"><span data-stu-id="00ffa-203">**CommitUrlCacheEntryW**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | <span data-ttu-id="00ffa-204">Speichert Daten in der angegebenen Datei im Cache Speicher zwischen und ordnet Sie der angegebenen URL zu.</span><span class="sxs-lookup"><span data-stu-id="00ffa-204">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="00ffa-205">**"Kreateurlcacheentry"**</span><span class="sxs-lookup"><span data-stu-id="00ffa-205">**CreateUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | <span data-ttu-id="00ffa-206">Ordnet den angeforderten Cache Speicher zu und erstellt einen lokalen Dateinamen zum Speichern des Cache Eintrags, der dem Quellnamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="00ffa-206">Allocates the requested cache storage and creates a local file name for saving the cache entry that corresponds to the source name.</span></span>                           |
| [<span data-ttu-id="00ffa-207">**"Kreateurlcachegroup"**</span><span class="sxs-lookup"><span data-stu-id="00ffa-207">**CreateUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | <span data-ttu-id="00ffa-208">Generiert eine Cache Gruppenidentifikation.</span><span class="sxs-lookup"><span data-stu-id="00ffa-208">Generates a cache group identification.</span></span>                                                                                                                       |
| [<span data-ttu-id="00ffa-209">**Deleteurlcacheentry**</span><span class="sxs-lookup"><span data-stu-id="00ffa-209">**DeleteUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | <span data-ttu-id="00ffa-210">Entfernt die Datei, die dem Quellnamen zugeordnet ist, aus dem Cache, wenn die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="00ffa-210">Removes the file associated with the source name from the cache, if the file exists.</span></span>                                                                          |
| [<span data-ttu-id="00ffa-211">**Deleteurlcachegroup**</span><span class="sxs-lookup"><span data-stu-id="00ffa-211">**DeleteUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | <span data-ttu-id="00ffa-212">Gibt eine **GroupID** und einen beliebigen zugeordneten Zustand in der Cache Indexdatei frei.</span><span class="sxs-lookup"><span data-stu-id="00ffa-212">Releases a **GROUPID** and any associated state in the cache index file.</span></span>                                                                                      |
| [<span data-ttu-id="00ffa-213">**Findcloseurlcache**</span><span class="sxs-lookup"><span data-stu-id="00ffa-213">**FindCloseUrlCache**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | <span data-ttu-id="00ffa-214">Schließt das angegebene enumerationshandle.</span><span class="sxs-lookup"><span data-stu-id="00ffa-214">Closes the specified enumeration handle.</span></span>                                                                                                                      |
| [<span data-ttu-id="00ffa-215">**Findfirsturlcacheentry**</span><span class="sxs-lookup"><span data-stu-id="00ffa-215">**FindFirstUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | <span data-ttu-id="00ffa-216">Beginnt die Enumeration des Caches.</span><span class="sxs-lookup"><span data-stu-id="00ffa-216">Begins the enumeration of the cache.</span></span>                                                                                                                          |
| [<span data-ttu-id="00ffa-217">**Findfirsturlcacheentryex**</span><span class="sxs-lookup"><span data-stu-id="00ffa-217">**FindFirstUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | <span data-ttu-id="00ffa-218">Beginnt eine gefilterte Enumeration des Caches.</span><span class="sxs-lookup"><span data-stu-id="00ffa-218">Begins a filtered enumeration of the cache.</span></span>                                                                                                                   |
| [<span data-ttu-id="00ffa-219">**Findnexturlcacheentry**</span><span class="sxs-lookup"><span data-stu-id="00ffa-219">**FindNextUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | <span data-ttu-id="00ffa-220">Ruft den nächsten Eintrag im Cache ab.</span><span class="sxs-lookup"><span data-stu-id="00ffa-220">Retrieves the next entry in the cache.</span></span>                                                                                                                        |
| [<span data-ttu-id="00ffa-221">**Findnexturlcacheentryex**</span><span class="sxs-lookup"><span data-stu-id="00ffa-221">**FindNextUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | <span data-ttu-id="00ffa-222">Ruft den nächsten Eintrag in einer gefilterten Cache Enumeration ab.</span><span class="sxs-lookup"><span data-stu-id="00ffa-222">Retrieves the next entry in a filtered cache enumeration.</span></span>                                                                                                     |
| [<span data-ttu-id="00ffa-223">**Geturlcacheentryinfo**</span><span class="sxs-lookup"><span data-stu-id="00ffa-223">**GetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | <span data-ttu-id="00ffa-224">Ruft Informationen zu einem Cache Eintrag ab.</span><span class="sxs-lookup"><span data-stu-id="00ffa-224">Retrieves information about a cache entry.</span></span>                                                                                                                    |
| [<span data-ttu-id="00ffa-225">**Geturlcacheentryinfoex**</span><span class="sxs-lookup"><span data-stu-id="00ffa-225">**GetUrlCacheEntryInfoEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | <span data-ttu-id="00ffa-226">Sucht nach der URL, nachdem alle zwischengespeicherten Umleitungen übertragen wurden, die von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)im Offline Modus angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-226">Searches for the URL after translating any cached redirections that would be applied in offline mode by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>           |
| [<span data-ttu-id="00ffa-227">**"Read urlcacheentrystream"**</span><span class="sxs-lookup"><span data-stu-id="00ffa-227">**ReadUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | <span data-ttu-id="00ffa-228">Liest die zwischengespeicherten Daten aus einem Stream, der mithilfe von " [**retrieveurlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)" geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="00ffa-228">Reads the cached data from a stream that has been opened using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                            |
| [<span data-ttu-id="00ffa-229">**"Retrieveurlcacheentryfile"**</span><span class="sxs-lookup"><span data-stu-id="00ffa-229">**RetrieveUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | <span data-ttu-id="00ffa-230">Ruft einen Cache Eintrag aus dem Cache in Form einer Datei ab.</span><span class="sxs-lookup"><span data-stu-id="00ffa-230">Retrieves a cache entry from the cache in the form of a file.</span></span>                                                                                                 |
| [<span data-ttu-id="00ffa-231">**"Retrieveurlcacheentrystream"**</span><span class="sxs-lookup"><span data-stu-id="00ffa-231">**RetrieveUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | <span data-ttu-id="00ffa-232">Bietet die effizienteste und Implementierungs unabhängige Möglichkeit des Zugriffs auf die Cache Daten.</span><span class="sxs-lookup"><span data-stu-id="00ffa-232">Provides the most efficient and implementation-independent way of accessing the cache data.</span></span>                                                                   |
| [<span data-ttu-id="00ffa-233">**"Tarturlcacheentrygroup"**</span><span class="sxs-lookup"><span data-stu-id="00ffa-233">**SetUrlCacheEntryGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | <span data-ttu-id="00ffa-234">Fügt Einträge aus einer Cache Gruppe hinzu oder entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="00ffa-234">Adds or removes entries from a cache group.</span></span>                                                                                                                   |
| [<span data-ttu-id="00ffa-235">**"Tarturlcacheentryinfo"**</span><span class="sxs-lookup"><span data-stu-id="00ffa-235">**SetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | <span data-ttu-id="00ffa-236">Legt die angegebenen Elemente der [**Internet \_ Cache- \_ Eintrags \_ Informations**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="00ffa-236">Sets the specified members of the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span>                                                |
| [<span data-ttu-id="00ffa-237">**Unlockurlcacheentryfile**</span><span class="sxs-lookup"><span data-stu-id="00ffa-237">**UnlockUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | <span data-ttu-id="00ffa-238">Entsperrt den Cache Eintrag, der gesperrt war, als die Datei für die Verwendung im Cache durch " [**retrieveurlcacheentryfile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)" abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="00ffa-238">Unlocks the cache entry that was locked when the file was retrieved for use from the cache by [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span></span> |
| [<span data-ttu-id="00ffa-239">**Unlockurlcacheentrystream**</span><span class="sxs-lookup"><span data-stu-id="00ffa-239">**UnlockUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | <span data-ttu-id="00ffa-240">Schließt den Datenstrom, der mithilfe von " [**retrieveurlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)" abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="00ffa-240">Closes the stream that has been retrieved using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                                           |



 

### <a name="enumerating-the-cache"></a><span data-ttu-id="00ffa-241">Auflisten des Caches</span><span class="sxs-lookup"><span data-stu-id="00ffa-241">Enumerating the Cache</span></span>

<span data-ttu-id="00ffa-242">Die Funktionen [**findfirsturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) und [**findnexturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) zählen die im Cache gespeicherten Informationen auf.</span><span class="sxs-lookup"><span data-stu-id="00ffa-242">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) and [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) functions enumerate the information stored in the cache.</span></span> <span data-ttu-id="00ffa-243">[**Findfirsturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) startet die Enumeration, indem ein Suchmuster, ein Puffer und eine Puffergröße zum Erstellen eines Handles und zum Zurückgeben des ersten Cache Eintrags übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) starts the enumeration by taking a search pattern, a buffer, and a buffer size to create a handle and return the first cache entry.</span></span> <span data-ttu-id="00ffa-244">[**Findnexturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) übernimmt das von [**findfirsturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)erstellte handle, einen Puffer und eine Puffergröße, um den nächsten Cache Eintrag zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="00ffa-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) takes the handle created by [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), a buffer, and a buffer size to return the next cache entry.</span></span>

<span data-ttu-id="00ffa-245">Beide Funktionen speichern eine [**Internet \_ Cache- \_ Eintrags \_ Informations**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Struktur im Puffer.</span><span class="sxs-lookup"><span data-stu-id="00ffa-245">Both functions store an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure in the buffer.</span></span> <span data-ttu-id="00ffa-246">Die Größe dieser Struktur variiert je nach Eintrag.</span><span class="sxs-lookup"><span data-stu-id="00ffa-246">The size of this structure varies for each entry.</span></span> <span data-ttu-id="00ffa-247">Wenn die an eine der beiden Funktionen über gegebene Puffergröße unzureichend ist, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen fehlerhaften \_ \_ Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="00ffa-247">If the buffer size passed to either function is insufficient, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="00ffa-248">Die Puffergrößen Variable enthält die Puffergröße, die zum Abrufen dieses Cache Eintrags benötigt wurde.</span><span class="sxs-lookup"><span data-stu-id="00ffa-248">The buffer size variable contains the buffer size that was needed to retrieve that cache entry.</span></span> <span data-ttu-id="00ffa-249">Ein Puffer der Größe, die durch die Puffergrößen Variable angegeben wird, muss zugeordnet werden, und die Funktion sollte erneut mit dem neuen Puffer aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-249">A buffer of the size indicated by the buffer size variable should be allocated, and the function should be called again with the new buffer.</span></span>

<span data-ttu-id="00ffa-250">Die Informationsstruktur " [**Internet \_ Cache \_ Entry \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) " enthält die Struktur Größe, die URL der zwischengespeicherten Informationen, den lokalen Dateinamen, den Cache Eintrags Typ, die Anzahl der Treffer, die Treffer Rate, die Uhrzeit der letzten Änderung, den Ablauf, den letzten Zugriff, den Zeitpunkt der letzten Synchronisierung, Header Informationen, die Größe der Header Informationen und die Datei</span><span class="sxs-lookup"><span data-stu-id="00ffa-250">The [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="00ffa-251">Die [**findfirsturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) -Funktion nimmt ein Suchmuster, einen Puffer, in dem die Informationsstruktur für den [**Internet \_ Cache \_ Eintrag \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) gespeichert ist, und die Puffergröße.</span><span class="sxs-lookup"><span data-stu-id="00ffa-251">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) function takes a search pattern, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="00ffa-252">Derzeit wird nur das Standard Suchmuster implementiert, das alle Cache Einträge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="00ffa-252">Currently, only the default search pattern, which returns all cache entries, is implemented.</span></span>

<span data-ttu-id="00ffa-253">Nachdem der Cache aufgezählt wurde, sollte die Anwendung [**findcloseurlcache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) aufrufen, um das Cache-enumerationshandle zu schließen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-253">After the cache is enumerated, the application should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) to close the cache enumeration handle.</span></span>

<span data-ttu-id="00ffa-254">Im folgenden Beispiel wird die URL jedes Cache Eintrags in einem Listenfeld, **IDC \_ cachelist**, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="00ffa-254">The following example displays each cache entry's URL in a list box, **IDC\_CacheList**.</span></span> <span data-ttu-id="00ffa-255">Sie verwendet \_ die maximale Größe der Cache \_ Eintrags \_ Informationen, \_ um anfänglich einen Puffer zuzuweisen, da die frühen Versionen der WinInet-API den Cache nicht ordnungsgemäß auflisten.</span><span class="sxs-lookup"><span data-stu-id="00ffa-255">It uses MAX\_CACHE\_ENTRY\_INFO\_SIZE to initially allocate a buffer, since early versions of the WinINet API do not enumerate the cache properly otherwise.</span></span> <span data-ttu-id="00ffa-256">Spätere Versionen zählen den Cache ordnungsgemäß auf, und es gibt keine Cache Größenbeschränkung.</span><span class="sxs-lookup"><span data-stu-id="00ffa-256">Later versions do enumerate the cache properly and there is no cache size limit.</span></span> <span data-ttu-id="00ffa-257">Alle Anwendungen, die auf Computern mit der Version der WinInet-API aus Internet Explorer 4,0 ausgeführt werden, müssen einen Puffer mit der erforderlichen Größe zuordnen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-257">All applications that run on computers with the version of the WinINet API from Internet Explorer 4.0 must allocate a buffer of the required size.</span></span> <span data-ttu-id="00ffa-258">Weitere Informationen finden Sie unter [Verwenden von Puffern](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="00ffa-258">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a><span data-ttu-id="00ffa-259">Abrufen von Informationen zum Cache Eintrag</span><span class="sxs-lookup"><span data-stu-id="00ffa-259">Retrieving Cache Entry Information</span></span>

<span data-ttu-id="00ffa-260">Mit der [**geturlcacheentryinfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) -Funktion können Sie die [**Internet \_ Cache \_ Entry \_ Info**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) -Struktur für die angegebene URL abrufen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-260">The [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) function lets you retrieve the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure for the specified URL.</span></span> <span data-ttu-id="00ffa-261">Diese Struktur enthält die Struktur Größe, die URL der zwischengespeicherten Informationen, den lokalen Dateinamen, den Cache Eintrags Typ, die Anzahl, die Treffer Rate, die Größe, die Uhrzeit der letzten Änderung, den Ablauf, den letzten Zugriff, den Zeitpunkt der letzten Synchronisierung, Header Informationen, die Header Informations Größe und die Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="00ffa-261">This structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="00ffa-262">[**Geturlcacheentryinfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) akzeptiert eine URL, einen Puffer für eine [**Internet \_ Cache- \_ Eintrags \_ Informations**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Struktur und die Puffergröße.</span><span class="sxs-lookup"><span data-stu-id="00ffa-262">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accepts a URL, a buffer for an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="00ffa-263">Wenn die URL gefunden wird, werden die Informationen in den Puffer kopiert.</span><span class="sxs-lookup"><span data-stu-id="00ffa-263">If the URL is found, the information is copied into the buffer.</span></span> <span data-ttu-id="00ffa-264">Andernfalls schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt die Fehler \_ Datei \_ nicht \_ gefunden zurück.</span><span class="sxs-lookup"><span data-stu-id="00ffa-264">Otherwise, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="00ffa-265">Wenn die Puffergröße zum Speichern der Cache Eintrags Informationen unzureichend ist, tritt bei der Funktion ein Fehler auf, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen \_ nicht ausreichenden \_ Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="00ffa-265">If the buffer size is insufficient to store the cache entry information, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="00ffa-266">Die zum Abrufen der Informationen erforderliche Größe wird in der Puffergrößen Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="00ffa-266">The size required to retrieve the information is stored in the buffer size variable.</span></span>

<span data-ttu-id="00ffa-267">" [**Geturlcacheentryinfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) " führt keine URL-Verarbeitung aus, sodass eine URL, die einen Anker ( \# ) enthält, nicht im Cache gefunden wird, auch wenn die Ressource zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="00ffa-267">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="00ffa-268">Wenn z. b. die URL " https://example.com/example.htm\#sample " übermittelt wird, gibt die Funktion die Fehler \_ Datei nicht gefunden zurück, \_ \_ auch wenn https://example.com/example.htm sich "" im Cache befindet.</span><span class="sxs-lookup"><span data-stu-id="00ffa-268">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="00ffa-269">Im folgenden Beispiel werden die Cache Eintrags Informationen für die angegebene URL abgerufen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-269">The following example retrieves the cache entry information for the specified URL.</span></span> <span data-ttu-id="00ffa-270">Die-Funktion zeigt dann die Header Informationen im Fenster " **IDC \_ cachedump** Edit" an.</span><span class="sxs-lookup"><span data-stu-id="00ffa-270">The function then displays the header information in the **IDC\_CacheDump** edit box.</span></span>


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a><span data-ttu-id="00ffa-271">Erstellen eines Cache Eintrags</span><span class="sxs-lookup"><span data-stu-id="00ffa-271">Creating a Cache Entry</span></span>

<span data-ttu-id="00ffa-272">Eine Anwendung erstellt einen Cache Eintrag mithilfe der Funktionen " [**comateurlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) " und " [**commiturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) ".</span><span class="sxs-lookup"><span data-stu-id="00ffa-272">An application uses the [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) and [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) functions to create a cache entry.</span></span>

<span data-ttu-id="00ffa-273">" [**Kreateurlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) " akzeptiert die URL, die erwartete Dateigröße und die Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="00ffa-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) accepts the URL, expected file size, and file name extension.</span></span> <span data-ttu-id="00ffa-274">Die-Funktion erstellt dann einen lokalen Dateinamen zum Speichern des Cache Eintrags, der der URL-und Dateinamenerweiterung entspricht.</span><span class="sxs-lookup"><span data-stu-id="00ffa-274">The function then creates a local file name for saving the cache entry that corresponds to the URL and file name extension.</span></span>

<span data-ttu-id="00ffa-275">Schreiben Sie die Daten mit dem Namen der lokalen Datei in die lokale Datei.</span><span class="sxs-lookup"><span data-stu-id="00ffa-275">Using the local file name, write the data into the local file.</span></span> <span data-ttu-id="00ffa-276">Nachdem die Daten in die lokale Datei geschrieben wurden, sollte die Anwendung [**commiturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)aufruft.</span><span class="sxs-lookup"><span data-stu-id="00ffa-276">After the data has been written to the local file, the application should call [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>

<span data-ttu-id="00ffa-277">[**Commiturlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) akzeptiert die URL, den lokalen Dateinamen, den Ablauf, den Zeitpunkt der letzten Änderung, den Cache Eintrags Typ, die Header Informationen, die Header Informations Größe und die Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="00ffa-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) accepts the URL, local file name, expiration, last modified time, cache entry type, header information, header information size, and file name extension.</span></span> <span data-ttu-id="00ffa-278">Die Funktion speichert dann Daten in der im Cache Speicher angegebenen Datei zwischen und ordnet Sie der angegebenen URL zu.</span><span class="sxs-lookup"><span data-stu-id="00ffa-278">The function then caches data in the file specified in the cache storage and associates it with the given URL.</span></span>

<span data-ttu-id="00ffa-279">Im folgenden Beispiel wird der lokale [**Dateiname**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)verwendet, der von einem vorherigen aufgerufen wurde, der im Textfeld **IDC \_ LocalFile** gespeichert wurde, um den Text aus dem Textfeld **IDC \_ cachedump** im Cache Eintrag zu speichern.</span><span class="sxs-lookup"><span data-stu-id="00ffa-279">The following example uses the local file name, created by a previous call to [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), stored in the text box, **IDC\_LocalFile**, to store the text from the text box, **IDC\_CacheDump**, in the cache entry.</span></span> <span data-ttu-id="00ffa-280">Nachdem die Daten mithilfe von **fopen**, **fprintf** und **fclose** in die Datei geschrieben wurden, wird für den Eintrag mithilfe von [**commiturlcacheentry ein Commit**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00ffa-280">After the data has been written to the file using **fopen**, **fprintf**, and **fclose**, the entry is committed using [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a><span data-ttu-id="00ffa-281">Löschen eines Cache Eintrags</span><span class="sxs-lookup"><span data-stu-id="00ffa-281">Deleting a Cache Entry</span></span>

<span data-ttu-id="00ffa-282">Die [**deleteurlcacheentry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) -Funktion nimmt eine URL an und entfernt die zugeordnete Cachedatei.</span><span class="sxs-lookup"><span data-stu-id="00ffa-282">The [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) function takes a URL and removes the cache file associated with it.</span></span> <span data-ttu-id="00ffa-283">Wenn die Cachedatei nicht vorhanden ist, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt die Fehler \_ Datei \_ nicht \_ gefunden zurück.</span><span class="sxs-lookup"><span data-stu-id="00ffa-283">If the cache file does not exist, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="00ffa-284">Wenn die Cachedatei zurzeit gesperrt ist oder verwendet wird, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehler \_ Zugriff \_ verweigert zurück.</span><span class="sxs-lookup"><span data-stu-id="00ffa-284">If the cache file is currently locked or in use, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="00ffa-285">Die Datei wird gelöscht, wenn Sie entsperrt wird.</span><span class="sxs-lookup"><span data-stu-id="00ffa-285">The file is deleted when unlocked.</span></span>

### <a name="retrieving-cache-entry-files"></a><span data-ttu-id="00ffa-286">Abrufen von Cache Eintrags Dateien</span><span class="sxs-lookup"><span data-stu-id="00ffa-286">Retrieving Cache Entry Files</span></span>

<span data-ttu-id="00ffa-287">Verwenden Sie für Anwendungen, für die der Dateiname einer Ressource erforderlich ist, die Funktionen " [**retrieveurlcacheentryfile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) " und " [**unlockurlcacheentryfile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) ".</span><span class="sxs-lookup"><span data-stu-id="00ffa-287">For applications that require the file name of a resource, use the [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) and [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) functions.</span></span> <span data-ttu-id="00ffa-288">Anwendungen, für die der Dateiname nicht erforderlich ist, müssen die Funktionen " [**retrieveurlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)", " [**infourlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)" und " [**unlockurlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) " verwenden, um die Informationen im Cache abzurufen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-288">Applications that do not require the file name should use the [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream), and [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) functions to retrieve the information in the cache.</span></span>

<span data-ttu-id="00ffa-289">" [**Retrieveurlcacheentrystream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) " führt keine URL-Verarbeitung aus, sodass eine URL, die einen Anker ( \# ) enthält, nicht im Cache gefunden wird, auch wenn die Ressource zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="00ffa-289">[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="00ffa-290">Wenn z. b. die URL " https://example.com/example.htm\#sample " übermittelt wird, gibt die Funktion die Fehler \_ Datei nicht gefunden zurück, \_ \_ auch wenn https://example.com/example.htm sich "" im Cache befindet.</span><span class="sxs-lookup"><span data-stu-id="00ffa-290">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="00ffa-291">" [**Retrieveurlcacheentryfile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) " akzeptiert eine URL, einen Puffer, in dem die Informationsstruktur für den [**Internet \_ Cache \_ Eintrag \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) gespeichert ist, und die Puffergröße.</span><span class="sxs-lookup"><span data-stu-id="00ffa-291">[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accepts a URL, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="00ffa-292">Die Funktion wird für den Aufrufer abgerufen und gesperrt.</span><span class="sxs-lookup"><span data-stu-id="00ffa-292">The function is retrieved and locked for the caller.</span></span>

<span data-ttu-id="00ffa-293">Nachdem die Informationen in der Datei verwendet wurden, sollte die Anwendung [**unlockurlcacheentryfile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) zum Entsperren der Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-293">After the information in the file has been used, the application should call [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) to unlock the file.</span></span>

### <a name="cache-groups"></a><span data-ttu-id="00ffa-294">Cache Gruppen</span><span class="sxs-lookup"><span data-stu-id="00ffa-294">Cache Groups</span></span>

<span data-ttu-id="00ffa-295">Um eine Cache Gruppe zu erstellen, muss [**die Funktion "**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) Funktion" von "" die Funktion "" für die Cache Gruppe aufgerufen werden, um eine **GroupID** zu generieren.</span><span class="sxs-lookup"><span data-stu-id="00ffa-295">To create a cache group, the [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) function must be called to generate a **GROUPID** for the cache group.</span></span> <span data-ttu-id="00ffa-296">Einträge können der Cache Gruppe hinzugefügt werden, indem die URL des Cache Eintrags und das \_ Add-Flag der Internet Cache \_ Gruppe der \_ [**seturlcacheentrygroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) -Funktion bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-296">Entries can be added to the cache group by supplying the cache entry's URL and the INTERNET\_CACHE\_GROUP\_ADD flag to the [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) function.</span></span> <span data-ttu-id="00ffa-297">Wenn Sie einen Cache Eintrag aus einer Gruppe entfernen möchten, übergeben Sie die URL des Cache Eintrags und das Remove-Flag der Internet \_ Cache \_ Gruppe \_ an [**seturlcacheentrygroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span><span class="sxs-lookup"><span data-stu-id="00ffa-297">To remove a cache entry from a group, pass the cache entry's URL and the INTERNET\_CACHE\_GROUP\_REMOVE flag to [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span></span>

<span data-ttu-id="00ffa-298">Die Funktionen " [**findfirsturlcacheentryex**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) " und " [**findnexturlcacheentryex**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) " können zum Auflisten der Einträge in einer angegebenen Cache Gruppe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-298">The [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) and [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) functions can be used to enumerate the entries in a specified cache group.</span></span> <span data-ttu-id="00ffa-299">Nachdem die Enumeration abgeschlossen ist, sollte die Funktion [**findcloseurlcache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-299">After the enumeration is complete, the function should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span></span>

## <a name="handling-structures-with-variable-size-information"></a><span data-ttu-id="00ffa-300">Behandeln von Strukturen mit Variablen Größen Informationen</span><span class="sxs-lookup"><span data-stu-id="00ffa-300">Handling Structures with Variable Size Information</span></span>

<span data-ttu-id="00ffa-301">Der Cache kann Informationen variabler Größe für jede gespeicherte URL enthalten.</span><span class="sxs-lookup"><span data-stu-id="00ffa-301">The cache can contain variable size information for each URL stored.</span></span> <span data-ttu-id="00ffa-302">Dies wird in der Info Struktur des [**Internet \_ Cache \_ Eintrags \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="00ffa-302">This is reflected in the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span> <span data-ttu-id="00ffa-303">Wenn die Cache Funktionen diese Struktur zurückgeben, erstellen Sie einen Puffer, der immer die Größe der [**Internet \_ Cache- \_ Eintrags \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Informationen zuzüglich aller Variablen Größen Informationen ist.</span><span class="sxs-lookup"><span data-stu-id="00ffa-303">When the cache functions return this structure, they create a buffer that is always the size of [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) plus any variable size information.</span></span> <span data-ttu-id="00ffa-304">Wenn ein Zeiger Element nicht **null** ist, zeigt es auf den Speicherbereich direkt hinter der Struktur.</span><span class="sxs-lookup"><span data-stu-id="00ffa-304">If a pointer member is not **NULL**, it points to the memory area immediately after the structure.</span></span> <span data-ttu-id="00ffa-305">Beim Kopieren des von einer Funktion zurückgegebenen Puffers in einen anderen Puffer sollten die Zeiger Elemente so korrigiert werden, dass Sie auf die entsprechende Stelle im neuen Puffer zeigen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="00ffa-305">While copying the buffer returned by a function into another buffer, the pointer members should be fixed to point to the appropriate place in the new buffer, as the following example shows.</span></span>

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

<span data-ttu-id="00ffa-306">Bei einigen Cache Funktionen \_ \_ tritt ein Fehler auf, wenn Sie einen Puffer angeben, der zu klein ist, um die von der Funktion abgerufenen Cache Eintrags Informationen zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="00ffa-306">Some cache functions fail with the ERROR\_INSUFFICIENT\_BUFFER error message if you specify a buffer that is too small to contain the cache entry information retrieved by the function.</span></span> <span data-ttu-id="00ffa-307">In diesem Fall gibt die Funktion auch die erforderliche Größe des Puffers zurück.</span><span class="sxs-lookup"><span data-stu-id="00ffa-307">In this case, the function also returns the required size of the buffer.</span></span> <span data-ttu-id="00ffa-308">Anschließend können Sie einen Puffer der entsprechenden Größe zuordnen und die Funktion erneut aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-308">You can then allocate a buffer of the appropriate size and call the function again.</span></span>

> [!Note]  
> <span data-ttu-id="00ffa-309">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="00ffa-309">WinINet does not support server implementations.</span></span> <span data-ttu-id="00ffa-310">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00ffa-310">In addition, it should not be used from a service.</span></span> <span data-ttu-id="00ffa-311">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="00ffa-311">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
