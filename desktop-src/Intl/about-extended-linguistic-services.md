---
description: Erweiterte linguistische Dienste (Dynamic Link Library, ELS) werden als Dynamic Link Library (dll) implementiert, die eine Vielzahl von Funktionen für die linguistische Unterstützung für Text bereitstellt, den die Anwendung angibt.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: Informationen zu erweiterten linguistischen Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349946"
---
# <a name="about-extended-linguistic-services"></a><span data-ttu-id="babe8-103">Informationen zu erweiterten linguistischen Diensten</span><span class="sxs-lookup"><span data-stu-id="babe8-103">About Extended Linguistic Services</span></span>

<span data-ttu-id="babe8-104">Erweiterte linguistische Dienste (Dynamic Link Library, ELS) werden als Dynamic Link Library (dll) implementiert, die eine Vielzahl von Funktionen für die linguistische Unterstützung für Text bereitstellt, den die Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="babe8-104">Extended Linguistic Services (ELS) is implemented as a dynamic-link library (DLL) that provides a variety of linguistic support functionality for text that the application specifies.</span></span> <span data-ttu-id="babe8-105">Die Technologie umfasst die Els-Plattform und Plug-Ins für mehrere vordefinierte linguistische Dienst Typen, auf die die Anwendung über die Plattform zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="babe8-105">The technology includes the ELS platform and plug-ins for several predefined linguistic service types accessible to the application through the platform.</span></span>

> [!Note]  
> <span data-ttu-id="babe8-106">Das ELS-Modul wird automatisch mit Windows 7 und höher installiert.</span><span class="sxs-lookup"><span data-stu-id="babe8-106">The ELS module is installed automatically with Windows 7 and later.</span></span>

 

## <a name="els-platform"></a><span data-ttu-id="babe8-107">Els-Plattform</span><span class="sxs-lookup"><span data-stu-id="babe8-107">ELS Platform</span></span>

<span data-ttu-id="babe8-108">Die Els-Plattform ist die Schnittstelle zwischen Ihrer Anwendung und den Els-Diensten.</span><span class="sxs-lookup"><span data-stu-id="babe8-108">The ELS platform is the interface between your application and the ELS services.</span></span> <span data-ttu-id="babe8-109">Es bietet eine einfache Möglichkeit, mehrere Arten von linguistischen Funktionen über dieselbe API zu implementieren, sodass die Anwendung auf bestimmte Dienste zugreifen und diese verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="babe8-109">It provides a simple way to implement several kinds of linguistic functionality through the same API, which allows the application to access and use specific services.</span></span> <span data-ttu-id="babe8-110">Weitere Informationen zur API finden Sie unter [Referenz zu erweiterten linguistischen Diensten.](extended-linguistic-services-reference.md)</span><span class="sxs-lookup"><span data-stu-id="babe8-110">For more information about the API, see [Extended Linguistic Services Reference.](extended-linguistic-services-reference.md)</span></span>

> [!Note]  
> <span data-ttu-id="babe8-111">Wenn die Anwendung eine der Els-API-Funktionen aufruft, ordnet die Plattform Arbeitsspeicher und Ressourcen zu, die für die Kommunikation mit den Diensten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="babe8-111">When the application calls any of the ELS API functions, the platform allocates memory and resources as needed for communication with the services.</span></span> <span data-ttu-id="babe8-112">Die Anwendung ist dafür verantwortlich, die Plattform erneut aufrufen zu können, um diese Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="babe8-112">The application is responsible for calling the platform again to free these resources.</span></span>

 

<span data-ttu-id="babe8-113">Die Plattform wird im virtuellen Speicherbereich der Anwendung ausgeführt, und der gesamte zugeordnete Arbeitsspeicher ist Teil dieses Speicherplatzes.</span><span class="sxs-lookup"><span data-stu-id="babe8-113">The platform runs inside the application virtual memory space, and all allocated memory is part of this space.</span></span> <span data-ttu-id="babe8-114">Daher muss Ihre Anwendung nur eine Verknüpfung mit der Els-Komponenten-DLL (Elscore.dll) herstellen, indem Sie eine Verknüpfung mit elscore. lib herstellen oder Elscore.dll dynamisch laden.</span><span class="sxs-lookup"><span data-stu-id="babe8-114">Thus your application only needs to link to the ELS component DLL (Elscore.dll) by linking to Elscore.lib or by dynamically loading Elscore.dll.</span></span>

## <a name="els-services"></a><span data-ttu-id="babe8-115">Els-Dienste</span><span class="sxs-lookup"><span data-stu-id="babe8-115">ELS Services</span></span>

<span data-ttu-id="babe8-116">Für Windows 7 und höher unterstützt die Els-Plattform nur die folgenden vordefinierten Dienste.</span><span class="sxs-lookup"><span data-stu-id="babe8-116">For Windows 7 and later, the ELS platform supports only the following predefined services.</span></span>

-   [<span data-ttu-id="babe8-117">Microsoft-Sprachenerkennung</span><span class="sxs-lookup"><span data-stu-id="babe8-117">Microsoft Language Detection</span></span>](microsoft-language-detection.md)
-   [<span data-ttu-id="babe8-118">Microsoft-Skript Erkennung</span><span class="sxs-lookup"><span data-stu-id="babe8-118">Microsoft Script Detection</span></span>](microsoft-script-detection.md)
-   [<span data-ttu-id="babe8-119">Transliterations Dienste</span><span class="sxs-lookup"><span data-stu-id="babe8-119">Transliteration services</span></span>](transliteration-services.md)

> [!Note]  
> <span data-ttu-id="babe8-120">In zukünftigen Versionen von Els werden zusätzliche Dienste von Microsoft oder Dienstanbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="babe8-120">Future versions of ELS will support additional services provided by Microsoft or service providers.</span></span>

 

<span data-ttu-id="babe8-121">Jeder Dienst ist einer Dienst Kategorie zugeordnet, die beschreibt, wie der Dienst funktioniert.</span><span class="sxs-lookup"><span data-stu-id="babe8-121">Each service is associated with a service category describing what the service does.</span></span> <span data-ttu-id="babe8-122">Die Kategorie wird durch eine nicht lokalisierbare Zeichenfolge dargestellt.</span><span class="sxs-lookup"><span data-stu-id="babe8-122">The category is represented by a nonlocalizable string.</span></span> <span data-ttu-id="babe8-123">Sie wird von Anwendungen zum Auflisten der verfügbaren Dienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="babe8-123">It is used by applications to enumerate available services.</span></span> <span data-ttu-id="babe8-124">Die aktuellen Dienst Kategorien lauten:</span><span class="sxs-lookup"><span data-stu-id="babe8-124">The current service categories are:</span></span>

-   <span data-ttu-id="babe8-125">"Sprachenerkennung"</span><span class="sxs-lookup"><span data-stu-id="babe8-125">"Language Detection"</span></span>
-   <span data-ttu-id="babe8-126">"Skript Erkennung"</span><span class="sxs-lookup"><span data-stu-id="babe8-126">"Script Detection"</span></span>
-   <span data-ttu-id="babe8-127">Transliterations</span><span class="sxs-lookup"><span data-stu-id="babe8-127">"Transliteration"</span></span>

<span data-ttu-id="babe8-128">Die Plattform listet die von der Anwendung angeforderten Dienste mithilfe von Dienst Metadaten auf.</span><span class="sxs-lookup"><span data-stu-id="babe8-128">The platform uses service metadata to enumerate the services requested by the application.</span></span> <span data-ttu-id="babe8-129">Eigenschaften wie der Dienst Globally Unique Identifier (GUID), unterstützte Eingabe-und Ausgabesprachen und Skripts sowie die Dienst Kategorie können von der Anwendung zum Auflisten der gewünschten Els-Dienste verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="babe8-129">Properties such as the service globally unique identifier (GUID), supported input and output languages and scripts, and the service category can be used by the application to enumerate the desired ELS services.</span></span>

<span data-ttu-id="babe8-130">Jeder Els-Dienst wird als Plug-in implementiert, das von einer DLL unterstützt wird, die auf dem Betriebssystem installiert werden kann, damit die Els-Plattform diese erkennen und verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="babe8-130">Each ELS service is implemented as a plug-in supported by a DLL that can be installed on the operating system so that the ELS platform can detect and use it.</span></span> <span data-ttu-id="babe8-131">Dienste können bei Bedarf Ihre eigenen subdienste verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="babe8-131">Services can expose their own subservices, if required.</span></span>

## <a name="main-els-operations"></a><span data-ttu-id="babe8-132">Haupt Vorgänge von Els</span><span class="sxs-lookup"><span data-stu-id="babe8-132">Main ELS Operations</span></span>

<span data-ttu-id="babe8-133">In diesem Abschnitt werden die wichtigsten von der Els-Plattform unterstützten Vorgänge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="babe8-133">This section describes the main operations supported by the ELS platform.</span></span> <span data-ttu-id="babe8-134">Die Plattform unterstützt sowohl synchrone als auch asynchrone Aufruf Modi.</span><span class="sxs-lookup"><span data-stu-id="babe8-134">The platform supports both synchronous and asynchronous calling modes.</span></span> <span data-ttu-id="babe8-135">Der asynchrone Aufruf Modus verwendet einen Anwendungs Thread Pool, um Threads für Verarbeitungsanforderungen zu planen.</span><span class="sxs-lookup"><span data-stu-id="babe8-135">The asynchronous calling mode uses an application thread pool to schedule threads for processing requests.</span></span>

> [!Note]  
> <span data-ttu-id="babe8-136">Da die Plattform einen asynchronen Modus unterstützt, müssen Els-Dienste diese Art von Funktionalität nicht selbst implementieren.</span><span class="sxs-lookup"><span data-stu-id="babe8-136">Since the platform supports an asynchronous mode, ELS services do not have to implement this type of functionality on their own.</span></span>

 

### <a name="service-enumeration"></a><span data-ttu-id="babe8-137">Dienst Enumeration</span><span class="sxs-lookup"><span data-stu-id="babe8-137">Service Enumeration</span></span>

<span data-ttu-id="babe8-138">Die Els-Plattform lädt und verwaltet alle Els-Dienste, sodass der Vorgang für die Anwendung transparent ist.</span><span class="sxs-lookup"><span data-stu-id="babe8-138">The ELS platform loads and manages all ELS services, making operation transparent to the application.</span></span> <span data-ttu-id="babe8-139">Die Anwendung listet die verfügbaren Dienste auf, indem [**mappinggetservices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="babe8-139">The application enumerates the available services by calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span></span> <span data-ttu-id="babe8-140">Weitere Informationen zur Programmierung finden Sie unter Auflisten [und Freigeben von Diensten](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="babe8-140">For programming instructions, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="babe8-141">Aus Leistungsgründen wird empfohlen, dass die Anwendung die verfügbaren Dienste nur einmal aufzählt.</span><span class="sxs-lookup"><span data-stu-id="babe8-141">It is advisable for performance reasons to have your application enumerate the available services only once.</span></span> <span data-ttu-id="babe8-142">Die Els-Plattform prüft die Dienste erneut auf die nächste Enumeration, um sicherzustellen, dass Ihre enumerationsergebnisse immer aktuell sind.</span><span class="sxs-lookup"><span data-stu-id="babe8-142">The ELS platform checks the services again on the next enumeration to ensure that its enumeration results are always current.</span></span>

 

### <a name="text-recognition"></a><span data-ttu-id="babe8-143">Text Erkennung</span><span class="sxs-lookup"><span data-stu-id="babe8-143">Text Recognition</span></span>

<span data-ttu-id="babe8-144">Nach der Dienst Enumeration Ruft die Anwendung die [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) -Funktion auf, um einen beliebigen Textbereich von Eingabetext dem Ausgabetext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="babe8-144">After service enumeration, the application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to use a particular ELS service to map any text range of input text to output text.</span></span> <span data-ttu-id="babe8-145">Ein Beispiel für die Texterkennung ist die Verwendung eines sprach Erkennungs Dienstanbieter, der ein Textsegment empfängt und seine wahrscheinlichste Sprache erkennt.</span><span class="sxs-lookup"><span data-stu-id="babe8-145">An example of text recognition is the use of a language detection service that receives a text segment and detects its most probable language.</span></span>

<span data-ttu-id="babe8-146">Nachdem der Dienst den Text erkannt hat, gibt [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) eine Zuordnung mit einer Eigenschaften Behälter Struktur aus, die mit den vom Dienst erzeugten Ausgabedaten und Eigenschaften aufgefüllt wurde. [**\_ \_**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag)</span><span class="sxs-lookup"><span data-stu-id="babe8-146">After the service has recognized the text, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns with a [**MAPPING\_PROPERTY\_BAG**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) structure populated with output data and properties produced by the service.</span></span> <span data-ttu-id="babe8-147">Um Speicher Verluste zu vermeiden, muss die Anwendung den Eigenschaften Behälter freigeben, indem Sie [**mappingfreepropertybag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) für jedes Mal aufrufen, wenn [**mappingrecognizetext**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) S OK zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="babe8-147">To avoid memory leaks, the application must free the property bag by calling [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) for each time that the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns S\_OK.</span></span> <span data-ttu-id="babe8-148">In der Regel führt die Anwendung dies entweder aus, wenn Sie die Ausgabedaten verwendet, oder wenn die Ausgabedaten nicht mehr relevant sind, weil der Eingabebereich von Text geändert wurde (z. b. bearbeitet oder gelöscht).</span><span class="sxs-lookup"><span data-stu-id="babe8-148">Usually the application does this either when it finishes using the output data or when the output data is no longer relevant because the input region of text has been modified, for example, edited or deleted.</span></span> <span data-ttu-id="babe8-149">Wenn die Eigenschaften Sammlung freigegeben wird, gibt **mappingfrepropertybag** zurück.</span><span class="sxs-lookup"><span data-stu-id="babe8-149">When the property bag is released, **MappingFreePropertyBag** returns.</span></span>

<span data-ttu-id="babe8-150">Programmier Anweisungen für die Texterkennung werden bei der [Anforderung von Texterkennung](requesting-text-recognition.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="babe8-150">Programming instructions for text recognition are provided in [Requesting Text Recognition](requesting-text-recognition.md).</span></span>

### <a name="service-termination"></a><span data-ttu-id="babe8-151">Dienst Beendigung</span><span class="sxs-lookup"><span data-stu-id="babe8-151">Service Termination</span></span>

<span data-ttu-id="babe8-152">Wenn Ihre Anwendung keine Els-Dienste mehr erfordert, wird [**mappingfreeservices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) aufgerufen, bevor Sie beendet wird.</span><span class="sxs-lookup"><span data-stu-id="babe8-152">When your application no longer requires ELS services, it calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) before it terminates.</span></span> <span data-ttu-id="babe8-153">Weitere Informationen finden Sie unter Auflisten [und Freigeben von Diensten](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="babe8-153">For more information, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

### <a name="versioning"></a><span data-ttu-id="babe8-154">Versionskontrolle</span><span class="sxs-lookup"><span data-stu-id="babe8-154">Versioning</span></span>

<span data-ttu-id="babe8-155">In zukünftigen Versionen von Els können die Els-Dienste aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="babe8-155">Future versions of ELS will allow the ELS services to be updated.</span></span> <span data-ttu-id="babe8-156">Die Anwendung kann die Versionsnummern der [**\_ zuordnungsdienstinfostruktur \_**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) überprüfen, um Änderungen in den Diensten zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="babe8-156">The application will be able to check the version numbers of the [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure to detect any changes in the services.</span></span>

> [!Note]  
> <span data-ttu-id="babe8-157">Ihre Els-Anwendung sollte nicht die Annahme machen, dass unterschiedliche Versionen desselben Dienstanbieter genau die gleichen Ergebnisse abrufen können.</span><span class="sxs-lookup"><span data-stu-id="babe8-157">Your ELS application should not make the assumption that different versions of the same service can retrieve exactly the same results.</span></span>

 

 

 



