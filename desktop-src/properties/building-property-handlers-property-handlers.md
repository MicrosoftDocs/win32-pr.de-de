---
description: In diesem Thema wird erläutert, wie Sie Eigenschafts Handler erstellen und registrieren, um mit dem Windows-Eigenschaften System zu arbeiten.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Initialisieren von Eigenschaften Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8eb11bc44217e508313bfb477c65925b44216e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216260"
---
# <a name="initializing-property-handlers"></a><span data-ttu-id="310f9-103">Initialisieren von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="310f9-103">Initializing Property Handlers</span></span>

<span data-ttu-id="310f9-104">In diesem Thema wird erläutert, wie Sie Eigenschafts Handler erstellen und registrieren, um mit dem Windows-Eigenschaften System zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="310f9-104">This topic explains how to create and register property handlers to work with the Windows property system.</span></span>

<span data-ttu-id="310f9-105">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="310f9-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="310f9-106">Eigenschaften Handler</span><span class="sxs-lookup"><span data-stu-id="310f9-106">Property Handlers</span></span>](#property-handlers)
-   [<span data-ttu-id="310f9-107">Vorbereitungen</span><span class="sxs-lookup"><span data-stu-id="310f9-107">Before You Begin</span></span>](#before-you-begin)
-   [<span data-ttu-id="310f9-108">Initialisieren von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="310f9-108">Initializing Property Handlers</span></span>](#initializing-property-handlers)
-   [<span data-ttu-id="310f9-109">In-Memory-Eigenschaften Speicher</span><span class="sxs-lookup"><span data-stu-id="310f9-109">In-Memory Property Store</span></span>](#in-memory-property-store)
-   [<span data-ttu-id="310f9-110">Umgang mit PROPVARIANT-Based Werten</span><span class="sxs-lookup"><span data-stu-id="310f9-110">Dealing with PROPVARIANT-Based Values</span></span>](#dealing-with-propvariant-based-values)
-   [<span data-ttu-id="310f9-111">Unterstützen offener Metadaten</span><span class="sxs-lookup"><span data-stu-id="310f9-111">Supporting Open Metadata</span></span>](#supporting-open-metadata)
-   [<span data-ttu-id="310f9-112">Voll Text Inhalte</span><span class="sxs-lookup"><span data-stu-id="310f9-112">Full-Text Contents</span></span>](#full-text-contents)
-   [<span data-ttu-id="310f9-113">Angeben von Werten für Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="310f9-113">Providing Values for Properties</span></span>](#providing-values-for-properties)
-   [<span data-ttu-id="310f9-114">Zurückschreiben von Werten</span><span class="sxs-lookup"><span data-stu-id="310f9-114">Writing Back Values</span></span>](#writing-back-values)
-   [<span data-ttu-id="310f9-115">Implementieren von ipropertystorecapabilitäten</span><span class="sxs-lookup"><span data-stu-id="310f9-115">Implementing IPropertyStoreCapabilities</span></span>](#implementing-ipropertystorecapabilities)
-   [<span data-ttu-id="310f9-116">Registrieren und Verteilen von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="310f9-116">Registering and Distributing Property Handlers</span></span>](#registering-and-distributing-property-handlers)
-   [<span data-ttu-id="310f9-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="310f9-117">Related topics</span></span>](#related-topics)

## <a name="property-handlers"></a><span data-ttu-id="310f9-118">Eigenschaften Handler</span><span class="sxs-lookup"><span data-stu-id="310f9-118">Property Handlers</span></span>

<span data-ttu-id="310f9-119">Eigenschaften Handler sind ein wesentlicher Bestandteil des Eigenschaften Systems.</span><span class="sxs-lookup"><span data-stu-id="310f9-119">Property handlers are a crucial part of the property system.</span></span> <span data-ttu-id="310f9-120">Sie werden vom Indexer Prozess Weise aufgerufen, um Eigenschaftswerte zu lesen und zu indizieren. Außerdem werden Sie von Windows-Explorer in-Process aufgerufen, um Eigenschaftswerte direkt in den Dateien zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="310f9-120">They are invoked in-process by the indexer to read and index property values, and are also invoked by Windows Explorer in-process to read and write property values directly in the files.</span></span> <span data-ttu-id="310f9-121">Diese Handler müssen sorgfältig geschrieben und getestet werden, um eine Beeinträchtigung der Leistung oder des Verlusts von Daten in den betroffenen Dateien zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="310f9-121">These handlers need to be carefully written and tested to prevent degraded performance or the loss of data in the affected files.</span></span> <span data-ttu-id="310f9-122">Weitere Informationen zu indexerspezifischen Überlegungen, die sich auf die Implementierung von Eigenschaften Handlern auswirken, finden Sie unter [entwickeln von Eigenschaften Handlern für Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span><span class="sxs-lookup"><span data-stu-id="310f9-122">For more information on indexer-specific considerations that affect property handler implementation, see [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span></span>

<span data-ttu-id="310f9-123">In diesem Thema wird ein Beispiel für ein XML-basiertes Dateiformat erläutert, das eine Anleitung mit der Dateinamenerweiterung ". Rezept" beschreibt.</span><span class="sxs-lookup"><span data-stu-id="310f9-123">This topic discusses a sample XML-based file format that describes a recipe with a .recipe file name extension.</span></span> <span data-ttu-id="310f9-124">Die Dateinamenerweiterung ". Rezept" ist als eigenes, eindeutiges Dateiformat registriert, anstatt sich auf das allgemeinere XML-Dateiformat zu verlassen, dessen Handler einen sekundären Stream zum Speichern von Eigenschaften verwendet.</span><span class="sxs-lookup"><span data-stu-id="310f9-124">The .recipe file name extension is registered as its own distinct file format rather than relying on the more generic .xml file format, whose handler uses a secondary stream to store properties.</span></span> <span data-ttu-id="310f9-125">Es wird empfohlen, dass Sie eindeutige Dateinamen Erweiterungen für die Dateitypen registrieren.</span><span class="sxs-lookup"><span data-stu-id="310f9-125">We recommend that you register unique file name extensions for your file types.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="310f9-126">Vorbereitungen</span><span class="sxs-lookup"><span data-stu-id="310f9-126">Before You Begin</span></span>

<span data-ttu-id="310f9-127">Eigenschaften Handler sind COM-Objekte, die die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Abstraktion für ein bestimmtes Dateiformat erstellen.</span><span class="sxs-lookup"><span data-stu-id="310f9-127">Property handlers are COM objects that create the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) abstraction for a specific file format.</span></span> <span data-ttu-id="310f9-128">Sie lesen (analysieren) und Schreiben dieses Dateiformat auf eine Weise, die der Spezifikation entspricht.</span><span class="sxs-lookup"><span data-stu-id="310f9-128">They read (parse) and write this file format in a manner that conforms to its specification.</span></span> <span data-ttu-id="310f9-129">Einige Eigenschaften Handler arbeiten auf der Grundlage von APIs, die den Zugriff auf ein bestimmtes Dateiformat abstrahieren.</span><span class="sxs-lookup"><span data-stu-id="310f9-129">Some property handlers do their work based on APIs that abstract access to a specific file format.</span></span> <span data-ttu-id="310f9-130">Bevor Sie einen Eigenschaften Handler für das Dateiformat entwickeln, müssen Sie verstehen, wie das Dateiformat Eigenschaften speichert, und wie diese Eigenschaften (Namen und Werte) der Eigenschafts Speicher Abstraktion zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="310f9-130">Before you develop a property handler for your file format, you need to understand how your file format stores properties, and how those properties (names and values) are mapped into the property store abstraction.</span></span>

<span data-ttu-id="310f9-131">Beachten Sie beim Planen der Implementierung, dass es sich bei den Eigenschaften Handlern um Komponenten auf niedriger Ebene handelt, die im Kontext von Prozessen wie Windows-Explorer, dem Windows Search-Indexer und Anwendungen von Drittanbietern geladen werden, die das shellelement-Programmiermodell verwenden.</span><span class="sxs-lookup"><span data-stu-id="310f9-131">When planning your implementation, remember that property handlers are low-level components that are loaded in the context of processes like Windows Explorer, the Windows Search indexer, and third-party applications that use the Shell item programming model.</span></span> <span data-ttu-id="310f9-132">Folglich können Eigenschafts Handler nicht in verwaltetem Code implementiert werden und sollten in C++ implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="310f9-132">As a result, property handlers cannot be implemented in managed code, and should be implemented in C++.</span></span> <span data-ttu-id="310f9-133">Wenn Ihr Handler für seine Arbeit APIs oder Dienste verwendet, müssen Sie sicherstellen, dass diese Dienste ordnungsgemäß in den Umgebungen funktionieren, in denen der Eigenschafts Handler geladen wird.</span><span class="sxs-lookup"><span data-stu-id="310f9-133">If your handler uses any APIs or services to do its work, you must ensure that those services can function properly in the environment(s) in which your property handler is loaded.</span></span>

> [!Note]  
> <span data-ttu-id="310f9-134">Eigenschaften Handler sind immer bestimmten Dateitypen zugeordnet. Wenn das Dateiformat Eigenschaften enthält, die einen benutzerdefinierten Eigenschaften Handler erfordern, sollten Sie daher immer eine eindeutige Dateinamenerweiterung für jedes Dateiformat registrieren.</span><span class="sxs-lookup"><span data-stu-id="310f9-134">Property handlers are always associated with specific file types; thus, if your file format contains properties that require a custom property handler, you should always register a unique file name extension for each file format.</span></span>

 

## <a name="initializing-property-handlers"></a><span data-ttu-id="310f9-135">Initialisieren von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="310f9-135">Initializing Property Handlers</span></span>

<span data-ttu-id="310f9-136">Bevor eine Eigenschaft vom System verwendet wird, wird Sie initialisiert, indem eine Implementierung von [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="310f9-136">Before a property is used by the system, it is initialized by calling an implementation of [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span></span> <span data-ttu-id="310f9-137">Der Eigenschafts Handler sollte initialisiert werden, indem das System ihm einen Stream zuweist, anstatt diese Zuweisung der Handlerimplementierung zu überlassen.</span><span class="sxs-lookup"><span data-stu-id="310f9-137">The property handler should be initialized by having the system assign it a stream rather than leaving that assignment to the handler implementation.</span></span> <span data-ttu-id="310f9-138">Diese Methode der Initialisierung stellt Folgendes sicher:</span><span class="sxs-lookup"><span data-stu-id="310f9-138">This method of initialization ensures the following things:</span></span>

-   <span data-ttu-id="310f9-139">Der Eigenschaften Handler kann in einem eingeschränkten Prozess (einem wichtigen Sicherheits Feature) ausgeführt werden, ohne dass er über Zugriffsrechte verfügt, um Dateien direkt zu lesen oder zu schreiben, anstatt auf seinen Inhalt über den Stream zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="310f9-139">The property handler can run in a restricted process (an important security feature) without having access rights to directly read or write files, rather accessing their content through the stream.</span></span>
-   <span data-ttu-id="310f9-140">Das System kann als vertrauenswürdig eingestuft werden, um die Datei-oplocks ordnungsgemäß zu verarbeiten, was ein wichtiges Maß an Zuverlässigkeit ist.</span><span class="sxs-lookup"><span data-stu-id="310f9-140">The system can be trusted to handle the file oplocks correctly, which is an important reliability measure.</span></span>
-   <span data-ttu-id="310f9-141">Das-Eigenschaften System stellt einen automatisch sicheren speicheringdienst bereit, ohne dass zusätzliche Funktionen von der Implementierung des Eigenschaften Handlers benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="310f9-141">The property system provides an automatic safe saving service without any extra functionality required from the property handler implementation.</span></span> <span data-ttu-id="310f9-142">Weitere Informationen zu Streams finden Sie im Abschnitt [Zurückschreiben von Werten](#writing-back-values) .</span><span class="sxs-lookup"><span data-stu-id="310f9-142">See the [Writing Back Values](#writing-back-values) section for more information about streams.</span></span>
-   <span data-ttu-id="310f9-143">Durch die Verwendung von [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) wird die Implementierung aus den Dateisystem Details abstrahiert.</span><span class="sxs-lookup"><span data-stu-id="310f9-143">Use of the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstracts your implementation from file system details.</span></span> <span data-ttu-id="310f9-144">Dies ermöglicht es dem Handler, die Initialisierung durch alternative Speicher, z. b. einen File Transfer Protocol (FTP)-Ordner oder eine komprimierte Datei mit der Dateinamenerweiterung ". zip", zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="310f9-144">This enables the handler to support initialization through alternative storages such as a File Transfer Protocol (FTP) folder or a compressed file with a .zip file name extension.</span></span>

<span data-ttu-id="310f9-145">Es gibt Fälle, in denen die Initialisierung mit Streams nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="310f9-145">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="310f9-146">In diesen Fällen gibt es zwei weitere Schnittstellen, die von Eigenschaften Handlern implementiert werden können: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) und [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span><span class="sxs-lookup"><span data-stu-id="310f9-146">In those situations, there are two further interfaces that property handlers can implement: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) and [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span></span> <span data-ttu-id="310f9-147">Wenn ein Eigenschaften Handler den [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)nicht implementiert, muss er die Ausführung im isolierten Prozess ablehnen, in den der systemindexer ihn standardmäßig platzieren würde, wenn es eine Änderung am Stream gäbe.</span><span class="sxs-lookup"><span data-stu-id="310f9-147">If a property handler does not implement the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process into which the system indexer would place it by default if there were a change to the stream.</span></span> <span data-ttu-id="310f9-148">Wenn Sie dieses Feature ablehnen möchten, legen Sie den folgenden Registrierungs Wert fest.</span><span class="sxs-lookup"><span data-stu-id="310f9-148">To opt out of this feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

<span data-ttu-id="310f9-149">Es ist jedoch weitaus besser, [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) zu implementieren und eine streambasierte Initialisierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="310f9-149">However, it is far better to implement [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization.</span></span> <span data-ttu-id="310f9-150">Der Eigenschafts Handler ist als Ergebnis sicherer und zuverlässiger.</span><span class="sxs-lookup"><span data-stu-id="310f9-150">Your property handler will be safer and more reliable as a result.</span></span> <span data-ttu-id="310f9-151">Die Deaktivierung der Prozess Isolation ist in der Regel nur für Legacy-Eigenschaften Handler vorgesehen und sollte durch neuen Code energisch vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="310f9-151">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

<span data-ttu-id="310f9-152">Wenn Sie die Implementierung eines Eigenschaften Handlers detailliert untersuchen möchten, betrachten Sie das folgende Codebeispiel, das eine Implementierung von [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize)ist.</span><span class="sxs-lookup"><span data-stu-id="310f9-152">To examine the implementation of a property handler in detail, look at the following code example, which is an implementation of [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span> <span data-ttu-id="310f9-153">Der-Handler wird initialisiert, indem ein XML-basiertes Rezept Dokument über einen Zeiger auf die zugeordnete [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Instanz dieses Dokuments geladen wird.</span><span class="sxs-lookup"><span data-stu-id="310f9-153">The handler is initialized by loading an XML-based recipe document through a pointer to that document's associated [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) instance.</span></span> <span data-ttu-id="310f9-154">Die **\_ spdocele** -Variable, die in der Nähe des Endes des Code Beispiels verwendet wird, wird weiter oben im Beispiel als msxml2:: ixmldomelementptr definiert.</span><span class="sxs-lookup"><span data-stu-id="310f9-154">The **\_spDocEle** variable used near the end of the code example is defined earlier in the sample as an MSXML2::IXMLDOMElementPtr.</span></span>

> [!Note]  
> <span data-ttu-id="310f9-155">Die folgenden und alle nachfolgenden Codebeispiele stammen aus dem Rezept Handler-Beispiel, das im Windows Software Development Kit (SDK) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="310f9-155">The following and all subsequent code examples are taken from the recipe handler sample included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="310f9-156">.</span><span class="sxs-lookup"><span data-stu-id="310f9-156">.</span></span>

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



<span data-ttu-id="310f9-157">Â</span><span class="sxs-lookup"><span data-stu-id="310f9-157">Â</span></span> 

<span data-ttu-id="310f9-158">Nachdem das Dokument selbst geladen wurde, werden die Eigenschaften, die im Windows-Explorer angezeigt werden sollen, durch Aufrufen der geschützten **\_ LoadProperties** -Methode geladen, wie im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="310f9-158">After the document itself is loaded, the properties to be displayed in Windows Explorer are loaded by calling the protected **\_LoadProperties** method, as illustrated in the following code example.</span></span> <span data-ttu-id="310f9-159">Dieser Prozess wird im nächsten Abschnitt ausführlich untersucht.</span><span class="sxs-lookup"><span data-stu-id="310f9-159">This process is examined in detail in the next section.</span></span>


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



<span data-ttu-id="310f9-160">Wenn der Stream schreibgeschützt ist, aber der *grfMode* -Parameter das STGM-Flag zum Lesen von Lese Voreinstellungen enthält \_ , sollte die Initialisierung fehlschlagen und STG \_ E \_ AccessDenied zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="310f9-160">If the stream is read-only but the *grfMode* parameter contains the STGM\_READWRITE flag, the initialization should fail and return STG\_E\_ACCESSDENIED.</span></span> <span data-ttu-id="310f9-161">Ohne diese Überprüfung zeigt Windows Explorer die Eigenschaftswerte als beschreibbar an, auch wenn dies nicht der Fall ist, was zu einem verwirrenden Endbenutzer Prozess führt.</span><span class="sxs-lookup"><span data-stu-id="310f9-161">Without this check, Windows Explorer shows the property values as writable even though they are not, leading to a confusing end-user experience.</span></span>

<span data-ttu-id="310f9-162">Der Eigenschafts Handler wird in seiner Lebensdauer nur einmal initialisiert.</span><span class="sxs-lookup"><span data-stu-id="310f9-162">The property handler is initialized only once in its lifetime.</span></span> <span data-ttu-id="310f9-163">Wenn eine zweite Initialisierung angefordert wird, sollte der Handler zurückgeben `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .</span><span class="sxs-lookup"><span data-stu-id="310f9-163">If a second initialization is requested, the handler should return `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)`.</span></span>

## <a name="in-memory-property-store"></a><span data-ttu-id="310f9-164">Eigenschaften Speicher In-Memory</span><span class="sxs-lookup"><span data-stu-id="310f9-164">In-Memory Property Store</span></span>

<span data-ttu-id="310f9-165">Bevor Sie sich mit der Implementierung von **\_ LoadProperties** befassen, sollten Sie das **PropertyMap** -Array verstehen, das im Beispiel verwendet wird, um Eigenschaften im XML-Dokument vorhandenen Eigenschaften im Eigenschaften System über Ihre pkey-Werte zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="310f9-165">Before looking at the implementation of **\_LoadProperties**, you should understand the **PropertyMap** array used in the sample to map properties in the XML document to existing properties in the property system through their PKEY values.</span></span>

<span data-ttu-id="310f9-166">Sie sollten nicht jedes Element und Attribut in der XML-Datei als Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="310f9-166">You should not expose every element and attribute in the XML file as a property.</span></span> <span data-ttu-id="310f9-167">Wählen Sie stattdessen nur diejenigen aus, die für Endbenutzer in der Organisation Ihrer Dokumente (in diesem Fall Rezepte) nützlich sein werden.</span><span class="sxs-lookup"><span data-stu-id="310f9-167">Instead, select only those that you believe will be useful to end users in the organization of their documents (in this case, recipes).</span></span> <span data-ttu-id="310f9-168">Dies ist ein wichtiges Konzept, das bei der Entwicklung von Eigenschaften Handlern beachtet werden muss: der Unterschied zwischen Informationen, die für Organisations Szenarios wirklich nützlich sind, und Informationen, die zu den Details Ihrer Datei gehören und durch das Öffnen der Datei selbst angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="310f9-168">This is an important concept to keep in mind as you develop your property handlers: the difference between information that is truly useful for organizational scenarios, and information that belongs to the details of your file and can be seen by opening the file itself.</span></span> <span data-ttu-id="310f9-169">Eigenschaften sind nicht als vollständige Duplizierung einer XML-Datei vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="310f9-169">Properties are not intended to be a full duplication of an XML file.</span></span>


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



<span data-ttu-id="310f9-170">Hier ist die vollständige Implementierung der **\_ LoadProperties** -Methode, die von [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="310f9-170">Here is the full implementation of the **\_LoadProperties** method called by [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



<span data-ttu-id="310f9-171">Die **\_ LoadProperties** -Methode ruft die shellhilfsfunktion " [**pscreatememorypropertystore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) " auf, um einen Speicher internen Eigenschafts Speicher (Cache) für die behandelten Eigenschaften zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="310f9-171">The **\_LoadProperties** method calls the Shell helper function [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create an in-memory property store (cache) for the handled properties.</span></span> <span data-ttu-id="310f9-172">Wenn Sie einen Cache verwenden, werden die Änderungen für Sie nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="310f9-172">By using a cache, changes are tracked for you.</span></span> <span data-ttu-id="310f9-173">Dadurch können Sie nachverfolgen, ob ein Eigenschafts Wert im Cache geändert, aber noch nicht im persistenten Speicher gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="310f9-173">This frees you from tracking whether a property value has been changed in the cache but not yet saved to persisted storage.</span></span> <span data-ttu-id="310f9-174">Außerdem werden Sie von unnötigerweise Beibehaltung von Eigenschafts Werten freigegeben, die sich nicht geändert haben.</span><span class="sxs-lookup"><span data-stu-id="310f9-174">It also frees you from needlessly persisting property values that have not changed.</span></span>

<span data-ttu-id="310f9-175">Die **\_ LoadProperties** -Methode ruft auch **\_ LoadProperty** auf, deren Implementierung im folgenden Code dargestellt wird, und zwar einmal für jede zugeordnete Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="310f9-175">The **\_LoadProperties** method also calls **\_LoadProperty** whose implementation is illustrated in the following code) once for each mapped property.</span></span> <span data-ttu-id="310f9-176">**\_ LoadProperty** Ruft den Wert der Eigenschaft ab, wie im **PropertyMap** -Element im XML-Stream angegeben, und weist ihn mithilfe eines [**Ansichts namens ipropertystorecache:: setvalueandstate**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate)dem in-Memory-Cache zu.</span><span class="sxs-lookup"><span data-stu-id="310f9-176">**\_LoadProperty** gets the value of the property as specified in the **PropertyMap** element in the XML stream and assigns it to the in-memory cache through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span></span> <span data-ttu-id="310f9-177">Das normale PSC- \_ Flag im Aufruf von **ipropertystorecache:: setvalueandstate** gibt an, dass der Eigenschafts Wert seit dem Zeitpunkt, zu dem er in den Cache eingetreten ist, nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="310f9-177">The PSC\_NORMAL flag in the call to **IPropertyStoreCache::SetValueAndState** indicates that the property value has not been altered since the time it entered the cache.</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a><span data-ttu-id="310f9-178">Umgang mit PROPVARIANT-Based Werten</span><span class="sxs-lookup"><span data-stu-id="310f9-178">Dealing with PROPVARIANT-Based Values</span></span>

<span data-ttu-id="310f9-179">In der Implementierung von **\_ LoadProperty** wird ein Eigenschafts Wert in Form einer [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="310f9-179">In the implementation of **\_LoadProperty**, a property value is provided in the form of a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="310f9-180">Ein Satz von APIs im Software Development Kit (SDK) wird bereitgestellt, um von primitiven Typen wie **pwstr** oder **int** in oder aus **PROPVARIANT** -Typen zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="310f9-180">A set of APIs in the software development kit (SDK) is provided to convert from primitive types such as **PWSTR** or **int** to or from **PROPVARIANT** types.</span></span> <span data-ttu-id="310f9-181">Diese APIs finden Sie in "propvarutil. h".</span><span class="sxs-lookup"><span data-stu-id="310f9-181">These APIs are found in Propvarutil.h.</span></span>

<span data-ttu-id="310f9-182">Wenn Sie z. b. eine [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in eine Zeichenfolge konvertieren möchten, können Sie " [**propvariantto String**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) " verwenden, wie hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="310f9-182">For example, to convert a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to a string, you can use [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) as illustrated here.</span></span>


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



<span data-ttu-id="310f9-183">Um eine PROPVARIANT aus einer Zeichenfolge zu initialisieren, können Sie [**initpropvariantfromstring**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring)verwenden.</span><span class="sxs-lookup"><span data-stu-id="310f9-183">To initialize a PROPVARIANT from a string, you can use [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span></span>


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



<span data-ttu-id="310f9-184">Wie Sie in jeder der im Beispiel enthaltenen Rezept Dateien sehen können, können in jeder Datei mehr als ein Schlüsselwort vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="310f9-184">As you can see in any of the recipe files included in the sample, there can be more than one keyword in each file.</span></span> <span data-ttu-id="310f9-185">Um dies zu berücksichtigen, unterstützt das Eigenschaften System mehrwertige Zeichen folgen, die als Zeichen folgen Vektor dargestellt werden (z \_ . a. "VT Vector \| VT \_ LPWSTR").</span><span class="sxs-lookup"><span data-stu-id="310f9-185">To account for this, the property system supports multi-valued strings represented as a vector of strings (for instance "VT\_VECTOR \| VT\_LPWSTR").</span></span> <span data-ttu-id="310f9-186">Die **\_ loadvectorproperty** -Methode im Beispiel verwendet vektorbasierte Werte.</span><span class="sxs-lookup"><span data-stu-id="310f9-186">The **\_LoadVectorProperty** method in the example uses vector-based values.</span></span>


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



<span data-ttu-id="310f9-187">Wenn ein Wert in der Datei nicht vorhanden ist, wird kein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="310f9-187">If a value does not exist in the file, do not return an error.</span></span> <span data-ttu-id="310f9-188">Legen Sie den Wert stattdessen auf VT \_ Empty fest, und geben Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="310f9-188">Instead, set the value to VT\_EMPTY and return **S\_OK**.</span></span> <span data-ttu-id="310f9-189">"VT Empty" gibt an \_ , dass der Eigenschafts Wert nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="310f9-189">VT\_EMPTY indicates that the property value does not exist.</span></span>

## <a name="supporting-open-metadata"></a><span data-ttu-id="310f9-190">Unterstützen offener Metadaten</span><span class="sxs-lookup"><span data-stu-id="310f9-190">Supporting Open Metadata</span></span>

<span data-ttu-id="310f9-191">In diesem Beispiel wird ein XML-basiertes Dateiformat verwendet.</span><span class="sxs-lookup"><span data-stu-id="310f9-191">This example uses an XML-based file format.</span></span> <span data-ttu-id="310f9-192">Das Schema kann erweitert werden, um Eigenschaften zu unterstützen, die während der Entwicklung nicht berücksichtigt wurden, z. b..</span><span class="sxs-lookup"><span data-stu-id="310f9-192">Its schema can be extended to support properties that were not thought of during developmet, for example.</span></span> <span data-ttu-id="310f9-193">Dieses System wird als Open Metadata bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="310f9-193">This system is known as open metadata.</span></span> <span data-ttu-id="310f9-194">In diesem Beispiel wird das Eigenschaften System erweitert, indem unter dem **Rezept** Element **ExtendedProperties** ein Knoten erstellt wird, wie im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="310f9-194">This example extends the property system by creating a node under the **Recipe** element called **ExtendedProperties**, as illustrated in the following code example.</span></span>


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



<span data-ttu-id="310f9-195">Wenn Sie persistente erweiterte Eigenschaften während der Initialisierung laden möchten, implementieren Sie die **\_ loadextendedproperties** -Methode, wie im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="310f9-195">To load persisted extended properties during initialization, implement the **\_LoadExtendedProperties** method, as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



<span data-ttu-id="310f9-196">Die in "propsys. h" deklarierten Serialisierungs-APIs werden zum Serialisieren und Deserialisieren von [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Typen in blobdaten verwendet, und anschließend wird die Base64-Codierung zum Serialisieren dieser blobzeichen in Zeichen folgen verwendet, die in der XML-Datei gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="310f9-196">Serialization APIs declared in Propsys.h are used to serialize and deserialize [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types into blobs of data, and then Base64 encoding is used to serialize those blobs into strings that can be saved in the XML.</span></span> <span data-ttu-id="310f9-197">Diese Zeichen folgen werden im **encodedValue** -Attribut des **ExtendedProperties** -Elements gespeichert.</span><span class="sxs-lookup"><span data-stu-id="310f9-197">These strings are stored in the **EncodedValue** attribute of the **ExtendedProperties** element.</span></span> <span data-ttu-id="310f9-198">Die folgende Hilfsmethode, die in der Datei "util. cpp" des Beispiels implementiert ist, führt die Serialisierung aus.</span><span class="sxs-lookup"><span data-stu-id="310f9-198">The following utility method, implemented in the sample's Util.cpp file, performs the serialization.</span></span> <span data-ttu-id="310f9-199">Er beginnt mit einem Aufrufen der [**stgserializepropvariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) -Funktion, um die binäre Serialisierung auszuführen, wie im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="310f9-199">It begins with a call to the [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) function to perform the binary serialization, as illustrated in the following code example.</span></span>


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



<span data-ttu-id="310f9-200">Anschließend führt die Funktion " [**cryptbinarydestring**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)", die in Wincrypt. h deklariert ist, die Base64-Konvertierung aus.</span><span class="sxs-lookup"><span data-stu-id="310f9-200">Next, the [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â function, declared in Wincrypt.h, performs the Base64 conversion.</span></span>


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



<span data-ttu-id="310f9-201">Die **deserializepropvariantfromstring** -Funktion, die auch in util. cpp enthalten ist, kehrt den Vorgang um und deserialisiert Werte aus der XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="310f9-201">The **DeserializePropVariantFromString** function, also found in Util.cpp, reverses the operation, deserializing values from the XML file.</span></span>

<span data-ttu-id="310f9-202">Weitere Informationen zur Unterstützung offener Metadaten finden Sie unter "Dateitypen, die offene Metadaten unterstützen" in [Dateitypen](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="310f9-202">For information about support for open metadata, see "File Types that Support Open Metadata" in [File Types](../shell/fa-file-types.md).</span></span>

## <a name="full-text-contents"></a><span data-ttu-id="310f9-203">Inhalt Full-Text</span><span class="sxs-lookup"><span data-stu-id="310f9-203">Full-Text Contents</span></span>

<span data-ttu-id="310f9-204">Eigenschaften Handler können auch eine Volltextsuche der Dateiinhalte vereinfachen, und Sie sind eine einfache Möglichkeit, diese Funktionalität bereitzustellen, wenn das Dateiformat nicht übermäßig kompliziert ist.</span><span class="sxs-lookup"><span data-stu-id="310f9-204">Property handlers can also facilitate a full-text search of the file contents, and they are an easy way to provide that functionality if the file format is not overly complicated.</span></span> <span data-ttu-id="310f9-205">Es gibt eine Alternative, leistungsfähigere Möglichkeit, den vollständigen Text der Datei über die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="310f9-205">There is an alternative, more powerful way to provide the full text of the file through the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface implementation.</span></span>

<span data-ttu-id="310f9-206">In der folgenden Tabelle werden die Vorteile der einzelnen Ansätze mithilfe von [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) oder [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="310f9-206">The following table summarizes the benefits of each approach using either [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>



| <span data-ttu-id="310f9-207">Funktion</span><span class="sxs-lookup"><span data-stu-id="310f9-207">Capability</span></span>                                   | <span data-ttu-id="310f9-208">IFilter</span><span class="sxs-lookup"><span data-stu-id="310f9-208">IFilter</span></span>                      | <span data-ttu-id="310f9-209">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="310f9-209">IPropertyStore</span></span> |
|----------------------------------------------|------------------------------|----------------|
| <span data-ttu-id="310f9-210">Ermöglicht das Zurückschreiben in Dateien?</span><span class="sxs-lookup"><span data-stu-id="310f9-210">Allows write back to files?</span></span>                  | <span data-ttu-id="310f9-211">Nein</span><span class="sxs-lookup"><span data-stu-id="310f9-211">No</span></span>                           | <span data-ttu-id="310f9-212">Ja</span><span class="sxs-lookup"><span data-stu-id="310f9-212">Yes</span></span>            |
| <span data-ttu-id="310f9-213">Bietet eine Mischung aus Inhalt und Eigenschaften?</span><span class="sxs-lookup"><span data-stu-id="310f9-213">Provides mix of content and properties?</span></span>      | <span data-ttu-id="310f9-214">Ja</span><span class="sxs-lookup"><span data-stu-id="310f9-214">Yes</span></span>                          | <span data-ttu-id="310f9-215">Ja</span><span class="sxs-lookup"><span data-stu-id="310f9-215">Yes</span></span>            |
| <span data-ttu-id="310f9-216">Mehrsprachige?</span><span class="sxs-lookup"><span data-stu-id="310f9-216">Multilingual?</span></span>                                | <span data-ttu-id="310f9-217">Ja</span><span class="sxs-lookup"><span data-stu-id="310f9-217">Yes</span></span>                          | <span data-ttu-id="310f9-218">Nein</span><span class="sxs-lookup"><span data-stu-id="310f9-218">No</span></span>             |
| <span data-ttu-id="310f9-219">MIME/Embedded?</span><span class="sxs-lookup"><span data-stu-id="310f9-219">MIME/Embedded?</span></span>                               | <span data-ttu-id="310f9-220">Ja</span><span class="sxs-lookup"><span data-stu-id="310f9-220">Yes</span></span>                          | <span data-ttu-id="310f9-221">Nein</span><span class="sxs-lookup"><span data-stu-id="310f9-221">No</span></span>             |
| <span data-ttu-id="310f9-222">Text Begrenzungen?</span><span class="sxs-lookup"><span data-stu-id="310f9-222">Text boundaries?</span></span>                             | <span data-ttu-id="310f9-223">Satz, Absatz, Kapitel</span><span class="sxs-lookup"><span data-stu-id="310f9-223">Sentence, paragraph, chapter</span></span> | <span data-ttu-id="310f9-224">Keine</span><span class="sxs-lookup"><span data-stu-id="310f9-224">None</span></span>           |
| <span data-ttu-id="310f9-225">Implementierung wird für SPS/SQL Server unterstützt?</span><span class="sxs-lookup"><span data-stu-id="310f9-225">Implementation supported for SPS/SQL Server?</span></span> | <span data-ttu-id="310f9-226">Ja</span><span class="sxs-lookup"><span data-stu-id="310f9-226">Yes</span></span>                          | <span data-ttu-id="310f9-227">Nein</span><span class="sxs-lookup"><span data-stu-id="310f9-227">No</span></span>             |
| <span data-ttu-id="310f9-228">Implementierung</span><span class="sxs-lookup"><span data-stu-id="310f9-228">Implementation</span></span>                               | <span data-ttu-id="310f9-229">Komplex</span><span class="sxs-lookup"><span data-stu-id="310f9-229">Complex</span></span>                      | <span data-ttu-id="310f9-230">Einfach</span><span class="sxs-lookup"><span data-stu-id="310f9-230">Simple</span></span>         |



 

<span data-ttu-id="310f9-231">Im Rezept handlerbeispiel hat das Rezeptdatei Format keine komplexen Anforderungen, sodass nur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) für die voll Textunterstützung implementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="310f9-231">In the recipe handler sample, the recipe file format does not have any complex requirements, so only [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) has been implemented for full-text support.</span></span> <span data-ttu-id="310f9-232">Die Volltextsuche wird für die XML-Knoten implementiert, die im folgenden Array benannt werden.</span><span class="sxs-lookup"><span data-stu-id="310f9-232">Full-text search is implemented for the XML nodes named in the following array.</span></span>


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



<span data-ttu-id="310f9-233">Das-Eigenschaften System enthält die `System.Search.Contents` Eigenschaft (pkey \_ Search \_ Content), die zum Bereitstellen von voll Text Inhalt für den Indexer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="310f9-233">The property system contains the `System.Search.Contents` (PKEY\_Search\_Contents) property, which was created to provide full-text content to the indexer.</span></span> <span data-ttu-id="310f9-234">Der Wert dieser Eigenschaft wird nie direkt in der Benutzeroberfläche angezeigt. der Text von allen XML-Knoten, die im obigen Array benannt werden, wird zu einer einzelnen Zeichenfolge verkettet.</span><span class="sxs-lookup"><span data-stu-id="310f9-234">This property's value is never displayed directly in the UI; the text from all of the XML nodes named in the array above are concatenated into a single string.</span></span> <span data-ttu-id="310f9-235">Diese Zeichenfolge wird dann dem Indexer als voll Text Inhalt der Rezeptdatei über einen Aufruf von [**ipropertystorecache:: setvalueandstate**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) bereitgestellt, wie im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="310f9-235">That string is then provided to the indexer as the full-text content of the recipe file through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a><span data-ttu-id="310f9-236">Angeben von Werten für Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="310f9-236">Providing Values for Properties</span></span>

<span data-ttu-id="310f9-237">Wenn Sie zum Lesen von Werten verwendet werden, werden Eigenschaften Handler in der Regel aus einem der folgenden Gründe aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="310f9-237">When used to read values, property handlers are usually invoked for one of the following reasons:</span></span>

-   <span data-ttu-id="310f9-238">, Um alle Eigenschaftswerte aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="310f9-238">To enumerate all property values.</span></span>
-   <span data-ttu-id="310f9-239">, Um den Wert einer bestimmten Eigenschaft zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="310f9-239">To get the value of a specific property.</span></span>

<span data-ttu-id="310f9-240">Bei der Enumeration wird ein Eigenschaften Handler aufgefordert, seine Eigenschaften entweder während der Indizierung aufzulisten, oder wenn im Dialogfeld Eigenschaften nach Eigenschaften zur Anzeige in der **anderen** Gruppe gefragt werden.</span><span class="sxs-lookup"><span data-stu-id="310f9-240">For enumeration, a property handler is asked to enumerate its properties either during indexing or when the properties dialog box asks for properties to display in the **Other** group.</span></span> <span data-ttu-id="310f9-241">Die Indizierung erfolgt ständig als Hintergrund Vorgang.</span><span class="sxs-lookup"><span data-stu-id="310f9-241">Indexing goes on constantly as a background operation.</span></span> <span data-ttu-id="310f9-242">Wenn sich eine Datei ändert, wird der Indexer benachrichtigt, und die Datei wird neu indiziert, indem der Eigenschaften Handler aufgefordert wird, seine Eigenschaften aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="310f9-242">Whenever a file changes, the indexer is notified, and it re-indexes the file by asking the property handler to enumerate its properties.</span></span> <span data-ttu-id="310f9-243">Daher ist es wichtig, dass Eigenschaften Handler effizient implementiert werden und Eigenschaftswerte so schnell wie möglich zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="310f9-243">Therefore, it is critical that property handlers are implemented efficiently and return property values as quickly as possible.</span></span> <span data-ttu-id="310f9-244">Zählen Sie alle Eigenschaften, für die Sie Werte haben, genauso wie für jede beliebige Sammlung, aber keine Eigenschaften, die speicherintensive Berechnungen oder Netzwerk Anforderungen umfassen, die Sie langsam abrufen können.</span><span class="sxs-lookup"><span data-stu-id="310f9-244">Enumerate all the properties for which you have values, just as you would for any collection, but do not enumerate properties that involve memory-intensive calculations or network requests that could make them slow to retrieve.</span></span>

<span data-ttu-id="310f9-245">Beim Schreiben eines Eigenschaften Handlers müssen Sie in der Regel die folgenden beiden Sätze von Eigenschaften in Erwägung gezogen werden.</span><span class="sxs-lookup"><span data-stu-id="310f9-245">When writing a property handler, you usually need to consider the following two sets of properties.</span></span>

-   <span data-ttu-id="310f9-246">Primäre Eigenschaften: Eigenschaften, die der Dateityp nativ unterstützt.</span><span class="sxs-lookup"><span data-stu-id="310f9-246">Primary properties: Properties that your file type supports natively.</span></span> <span data-ttu-id="310f9-247">Beispielsweise unterstützt ein Foto-Eigenschaften Handler für die Metadaten für die austauschbare Bilddatei (EXIF) nativ `System.Photo.FNumber` .</span><span class="sxs-lookup"><span data-stu-id="310f9-247">For example, a photo property handler for Exchangeable Image File (EXIF) metadata natively supports `System.Photo.FNumber`.</span></span>
-   <span data-ttu-id="310f9-248">Erweiterte Eigenschaften: Eigenschaften, die vom Dateityp als Teil der geöffneten Metadaten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="310f9-248">Extended properties: Properties that your file type supports as part of open metadata.</span></span>

<span data-ttu-id="310f9-249">Da im Beispiel der in-Memory-Cache verwendet wird, ist die Implementierung von [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Methoden lediglich eine Frage der Delegierung an diesen Cache, wie im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="310f9-249">Because the sample uses in-memory cache, implementing [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods is just a matter of delegating to that cache, as illustrated in the following code example.</span></span>


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



<span data-ttu-id="310f9-250">Wenn Sie sich entscheiden, nicht an den in-Memory-Cache zu delegieren, müssen Sie die-Methoden implementieren, um> das folgende erwartete Verhalten bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="310f9-250">If you choose not to delegate to the in-memory cache, you must implement your methods to provide> the following expected behavior:</span></span>

-   <span data-ttu-id="310f9-251">[**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): Wenn keine Eigenschaften vorhanden sind, gibt diese Methode " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="310f9-251">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): If there are no properties, this method returns **S\_OK**.</span></span>
-   <span data-ttu-id="310f9-252">[**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): Wenn *iprop* größer oder gleich *cproperist*, gibt diese Methode E \_ invalidArg zurück, und die Struktur, auf die durch den *pkey* -Parameter verwiesen wird, wird mit Nullen gefüllt.</span><span class="sxs-lookup"><span data-stu-id="310f9-252">[**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): If *iProp* is greater than or equal to *cProps*, this method returns E\_INVALIDARG and the structure pointed to by the *pkey* parameter is filled with zeroes.</span></span>
-   <span data-ttu-id="310f9-253">[**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) und [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) spiegeln den aktuellen Zustand des Eigenschaften Handlers wider.</span><span class="sxs-lookup"><span data-stu-id="310f9-253">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) and [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflect the current state of the property handler.</span></span> <span data-ttu-id="310f9-254">Wenn ein [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) durch [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))der Datei hinzugefügt oder daraus entfernt wird, müssen diese beiden Methoden diese Änderung beim nächsten Aufrufen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="310f9-254">If a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) is added to or removed from the file through [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), these two methods must reflect that change the next time they are called.</span></span>
-   <span data-ttu-id="310f9-255">[**IPropertyStore:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): Wenn diese Methode für einen Wert, der nicht vorhanden ist, angefordert wird, gibt Sie " **S \_ OK** " zurück, wobei der als "VT Empty" gemeldete Wert angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="310f9-255">[**IPropertyStore::GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): If this method is asked for a value that does not exist, it returns **S\_OK** with the value reported as VT\_EMPTY.</span></span>

## <a name="writing-back-values"></a><span data-ttu-id="310f9-256">Zurückschreiben von Werten</span><span class="sxs-lookup"><span data-stu-id="310f9-256">Writing Back Values</span></span>

<span data-ttu-id="310f9-257">Wenn der Eigenschafts Handler den Wert einer Eigenschaft mithilfe von [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))schreibt, schreibt er erst den Wert in die Datei, wenn [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="310f9-257">When the property handler writes the value of a property using [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), it does not write the value to the file until [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) is called.</span></span> <span data-ttu-id="310f9-258">Der in-Memory-Cache kann bei der Implementierung dieses Schemas nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="310f9-258">The in-memory cache can be useful in implementing this scheme.</span></span> <span data-ttu-id="310f9-259">Im Beispielcode legt die **IPropertyStore:: SetValue** -Implementierung einfach den neuen Wert im in-Memory-Cache fest und legt den Zustand dieser Eigenschaft auf PSC \_ Dirty fest.</span><span class="sxs-lookup"><span data-stu-id="310f9-259">In the sample code the **IPropertyStore::SetValue** implementation simply sets the new value in the in-memory cache and sets the state of that property to PSC\_DIRTY.</span></span>


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



<span data-ttu-id="310f9-260">In jeder [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Implementierung wird das folgende Verhalten von [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))erwartet:</span><span class="sxs-lookup"><span data-stu-id="310f9-260">In any [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, the following behavior is expected from [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):</span></span>

-   <span data-ttu-id="310f9-261">Wenn die Eigenschaft bereits vorhanden ist, wird der Wert der Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="310f9-261">If the property already exists, the value of the property is set.</span></span>
-   <span data-ttu-id="310f9-262">Wenn die Eigenschaft nicht vorhanden ist, wird die neue Eigenschaft hinzugefügt und der Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="310f9-262">If the property does not exist, the new property is added and its value set.</span></span>
-   <span data-ttu-id="310f9-263">Wenn der Eigenschafts Wert nicht mit derselben Genauigkeit wie angegeben beibehalten werden kann (beispielsweise aufgrund von Größenbeschränkungen im Dateiformat), wird der Wert so weit wie möglich festgelegt, und es wird eine Unterbindung von "Inplace \_ S" \_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="310f9-263">If the property value cannot be persisted at the same accuracy as given (for instance, truncation due to size limitations in the file format), the value is set as far as possible and INPLACE\_S\_TRUNCATED is returned.</span></span>
-   <span data-ttu-id="310f9-264">Wenn die Eigenschaft nicht vom Eigenschaften Handler unterstützt wird, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="310f9-264">If the property is not supported by the property handler, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` is returned.</span></span>
-   <span data-ttu-id="310f9-265">Wenn ein anderer Grund dafür vorliegt, dass der Eigenschafts Wert nicht festgelegt werden kann, z. b. wenn die Datei gesperrt ist oder keine Rechte zum Bearbeiten über Zugriffs Steuerungs Listen (Access Control Lists, ACLs) vorhanden sind, wird STG \_ E \_ AccessDenied zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="310f9-265">If there is another reason that the property value cannot be set, such as the file being locked or lack of rights to edit through access control lists (ACLs), then STG\_E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="310f9-266">Ein wichtiger Vorteil der Verwendung von Streams als Beispiel ist die Zuverlässigkeit.</span><span class="sxs-lookup"><span data-stu-id="310f9-266">One major advantage of using streams, as the sample, is reliability.</span></span> <span data-ttu-id="310f9-267">Eigenschaften Handler müssen immer in Erwägung ziehen, dass eine Datei im Falle eines schwerwiegenden Fehlers nicht in einem inkonsistenten Zustand belassen wird.</span><span class="sxs-lookup"><span data-stu-id="310f9-267">Property handlers must always consider that they cannot leave a file in an inconsistent state in the case of a catastrophic failure.</span></span> <span data-ttu-id="310f9-268">Das beschädigen der Dateien eines Benutzers sollte offensichtlich vermieden werden, und die beste Vorgehensweise hierfür ist ein "Copy-on-Write"-Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="310f9-268">Corrupting a user's files obviously should be avoided, and the best way to do this is with a "copy-on-write" mechanism.</span></span> <span data-ttu-id="310f9-269">Wenn Ihr Eigenschaften Handler einen Stream für den Zugriff auf eine Datei verwendet, erhalten Sie dieses Verhalten automatisch. Das System schreibt alle Änderungen in den Stream und ersetzt die Datei nur während des Commitvorgangs durch die neue Kopie.</span><span class="sxs-lookup"><span data-stu-id="310f9-269">If your property handler uses a stream to access a file, you get this behavior automatically; the system writes any changes to the stream, replacing the file with the new copy only during the commit operation.</span></span>

<span data-ttu-id="310f9-270">Wenn Sie dieses Verhalten außer Kraft setzen und den Datei Speicherungs Prozess manuell steuern möchten, können Sie das sichere Speicherverhalten ablehnen, indem Sie den Wert von manualsafesave in den Registrierungs Eintrag Ihres Handlers festlegen, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="310f9-270">To override this behavior and control the file saving process manually, you can opt out of the safe save behavior by setting the ManualSafeSave value in your handler's registry entry as illustrated here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

<span data-ttu-id="310f9-271">Wenn ein Handler den Wert manualsafesave angibt, ist der Stream, mit dem er initialisiert wird, kein transaktiver Datenstrom (STGM \_ transaktiv).</span><span class="sxs-lookup"><span data-stu-id="310f9-271">When a handler specifies the ManualSafeSave value, the stream with which it is initialized is not a transacted stream (STGM\_TRANSACTED).</span></span> <span data-ttu-id="310f9-272">Der Handler selbst muss die Safe Save-Funktion implementieren, um sicherzustellen, dass die Datei nicht beschädigt ist, wenn der Speichervorgang unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="310f9-272">The handler itself must implement the safe save function to ensure that the file is not corrupted if the save operation is interrupted.</span></span> <span data-ttu-id="310f9-273">Wenn der Handler direkte Schreibvorgänge implementiert, wird er in den Stream geschrieben, den er erhält.</span><span class="sxs-lookup"><span data-stu-id="310f9-273">If the handler implements in-place writing, it will write to the stream that it is given.</span></span> <span data-ttu-id="310f9-274">Wenn der Handler dieses Feature nicht unterstützt, muss er einen Stream abrufen, mit dem die aktualisierte Kopie der Datei mit [**idestinationstreamfactory:: getdestinationstream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream)geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="310f9-274">If the handler does not support this feature, then it must retrieve a stream with which to write the updated copy of the file using [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span></span> <span data-ttu-id="310f9-275">Nachdem der Handler das Schreiben abgeschlossen hat, sollte er im ursprünglichen Stream [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) aufrufen, um den Vorgang abzuschließen, und den Inhalt des ursprünglichen Streams durch die neue Kopie der Datei ersetzen.</span><span class="sxs-lookup"><span data-stu-id="310f9-275">After the handler is done writing, it should call [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) on the original stream to complete the operation, and replace the contents of the original stream with the new copy of the file.</span></span>

<span data-ttu-id="310f9-276">Manualsafesave ist auch die Standardsituation, wenn Sie den Handler nicht mit einem Stream initialisieren.</span><span class="sxs-lookup"><span data-stu-id="310f9-276">ManualSafeSave is also the default situation if you do not initialize your handler with a stream.</span></span> <span data-ttu-id="310f9-277">Ohne einen ursprünglichen Stream zum Empfangen der Inhalte des temporären Streams müssen Sie [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) verwenden, um eine atomarische Ersetzung der Quelldatei vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="310f9-277">Without an original stream to receive the contents of the temporary stream, you must use [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) to perform an atomic replacement of the source file.</span></span>

<span data-ttu-id="310f9-278">Große Dateiformate, die auf eine Weise verwendet werden, um Dateien zu erstellen, die größer als 1 MB sind, sollten die Unterstützung für direktes Schreiben von Eigenschaften implementieren. Andernfalls erfüllt das Leistungsverhalten nicht die Erwartungen von Clients des Eigenschaften Systems.</span><span class="sxs-lookup"><span data-stu-id="310f9-278">Large file formats that will be used in a way that produces files greater than 1 MB should implement support for in-place property writing; otherwise, the performance behavior does not meet the expectations of clients of the property system.</span></span> <span data-ttu-id="310f9-279">In diesem Szenario sollte die für das Schreiben von Eigenschaften erforderliche Zeit nicht von der Dateigröße betroffen sein.</span><span class="sxs-lookup"><span data-stu-id="310f9-279">In this scenario, the time required to write properties should not be affected by the file size.</span></span>

<span data-ttu-id="310f9-280">Für sehr große Dateien, z. b. eine Videodatei mit 1 GB oder mehr, ist eine andere Lösung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="310f9-280">For very large files, for example a video file of 1 GB or more, a different solution is required.</span></span> <span data-ttu-id="310f9-281">Wenn in der Datei nicht genügend Speicherplatz für das direkte Schreiben vorhanden ist, kann es sein, dass der Handler die Aktualisierung der Eigenschaft misslingt, wenn der Speicherplatz, der für das Schreiben von direkten Eigenschaften reserviert ist, erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="310f9-281">If there is not enough space in the file to perform in-place writing, the handler may fail the property update if the amount of space reserved for in-place property writing has been exhausted.</span></span> <span data-ttu-id="310f9-282">Dieser Fehler tritt auf, um eine schlechte Leistung zu vermeiden, die von 2 GB e/a verursacht wird (1 zum Lesen, 1 zum Schreiben).</span><span class="sxs-lookup"><span data-stu-id="310f9-282">This failure occurs to avoid poor performance arising from 2 GB of IO (1 to read, 1 to write).</span></span> <span data-ttu-id="310f9-283">Aufgrund dieses möglichen Fehlers sollten diese Dateiformate ausreichend Speicherplatz für das Schreiben von direkten Eigenschaften reservieren.</span><span class="sxs-lookup"><span data-stu-id="310f9-283">Because of this potential failure, these file formats should reserve enough space for in-place property writing.</span></span>

<span data-ttu-id="310f9-284">Wenn die Datei über genügend Speicherplatz verfügt, um Metadaten zu schreiben, und wenn das Schreiben dieser Metadaten nicht bewirkt, dass die Datei vergrößert oder verkleinert wird, ist es möglicherweise sicher, direkt zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="310f9-284">If the file has enough space in its header to write metadata, and if the writing of that metadata does not cause the file to grow or shrink, it might be safe to write in-place.</span></span> <span data-ttu-id="310f9-285">Wir empfehlen 64 KB als Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="310f9-285">We recommend 64 KB as a starting point.</span></span> <span data-ttu-id="310f9-286">Das Schreiben direkt ist äquivalent zum Handler, der manualsafesave anfordert und [**IStream:: Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) in der Implementierung von [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))anfordert und eine viel bessere Leistung als Copy-on-Write-Vorgänge aufweist.</span><span class="sxs-lookup"><span data-stu-id="310f9-286">Writing in-place is equivalent to the handler asking for ManualSafeSave and calling [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) in the implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), and has much better performance than copy-on-write.</span></span> <span data-ttu-id="310f9-287">Wenn sich die Dateigröße aufgrund von Eigenschafts Wertänderungen ändert, sollte das Schreiben direkt erfolgen, weil eine beschädigte Datei im Falle einer nicht ordnungsgemäßen Beendigung nicht ordnungsgemäß geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="310f9-287">If the file size changes due to property value changes, writing in-place should not be attempted because of the potential for a corrupted file in the event of an abnormal termination.</span></span>

> [!Note]  
> <span data-ttu-id="310f9-288">Aus Leistungsgründen wird empfohlen, die Option manualsafesave mit Eigenschaften Handlern zu verwenden, die mit Dateien arbeiten, die 100 KB oder größer sind.</span><span class="sxs-lookup"><span data-stu-id="310f9-288">For performance reasons we recommend that the ManualSafeSave option be used with property handlers working with files that are 100 KB or larger.</span></span>

 

<span data-ttu-id="310f9-289">Wie in der folgenden Beispiel Implementierung von [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))veranschaulicht, wird der Handler für manualsafesave registriert, um die Option für die manuelle sichere Speicherung zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="310f9-289">As illustrated in the following sample implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), the handler for ManualSafeSave is registered to illustrate the manual safe save option.</span></span> <span data-ttu-id="310f9-290">Die **\_ savecachetodom** -Methode schreibt die im Arbeitsspeicher Cache gespeicherten Eigenschaftswerte in das XmlDocument-Objekt.</span><span class="sxs-lookup"><span data-stu-id="310f9-290">The **\_SaveCacheToDom** method writes the property values stored in the in-memory cache to the XMLdocument object.</span></span>


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



<span data-ttu-id="310f9-291">Stellen Sie als nächstes die Frage, ob das pcified [**idestinationstreamfactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="310f9-291">Next, ask whether the pecified supports [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).</span></span>


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



<span data-ttu-id="310f9-292">Übertragen Sie als nächstes den ursprünglichen Stream, der die Daten auf sichere Weise in die ursprüngliche Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="310f9-292">Next, commit the original stream, which writes the data back to the original file in a safe manner.</span></span>


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



<span data-ttu-id="310f9-293">Untersuchen Sie dann die **\_ savecachetodom** -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="310f9-293">Then examine the **\_SaveCacheToDom** implementation.</span></span>


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



<span data-ttu-id="310f9-294">Im nächsten Schritt wird die Anzahl der Eigenschaften, die im Arbeitsspeicher Cache gespeichert werden, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="310f9-294">Next, get the number of properties stored in the in-memory cache.</span></span>


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



<span data-ttu-id="310f9-295">Durchlaufen Sie nun die Eigenschaften, um zu bestimmen, ob der Wert einer Eigenschaft geändert wurde, seit Sie in den Arbeitsspeicher geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="310f9-295">Now iterate through the properties to determine whether the value of a property has been changed since it was loaded into memory.</span></span>


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



<span data-ttu-id="310f9-296">Mit der [**ipropertystorecache:: GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) -Methode wird der Zustand der Eigenschaft im Cache abgerufen.</span><span class="sxs-lookup"><span data-stu-id="310f9-296">The [**IPropertyStoreCache::GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) method gets the state of the property in the cache.</span></span> <span data-ttu-id="310f9-297">Das PSC- \_ Flag "Dirty", das in der [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) -Implementierung festgelegt wurde, markiert eine Eigenschaft als geändert.</span><span class="sxs-lookup"><span data-stu-id="310f9-297">The PSC\_DIRTY flag, which was set in the [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) implementation, marks a property as changed.</span></span>


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



<span data-ttu-id="310f9-298">Ordnen Sie die-Eigenschaft dem XML-Knoten zu, wie im Feld z. b. **\_ rgpropertymap** angegeben.</span><span class="sxs-lookup"><span data-stu-id="310f9-298">Map the property to the XML node as specified in the **eg\_rgPropertyMap** array.</span></span>


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



<span data-ttu-id="310f9-299">Wenn eine Eigenschaft nicht in der Zuordnung angezeigt wird, handelt es sich um eine neue Eigenschaft, die von Windows Explorer festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="310f9-299">If a property is not in the map, it is a new property that was set by Windows Explorer.</span></span> <span data-ttu-id="310f9-300">Da Open Metadata unterstützt wird, speichern Sie die neue Eigenschaft im **ExtendedProperties** -Abschnitt der XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="310f9-300">Because open metadata is supported, save the new property in the **ExtendedProperties** section of the XML.</span></span>


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a><span data-ttu-id="310f9-301">Implementieren von ipropertystorecapabilitäten</span><span class="sxs-lookup"><span data-stu-id="310f9-301">Implementing IPropertyStoreCapabilities</span></span>

<span data-ttu-id="310f9-302">[**Ipropertystorecapabiliinformiert**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) die Shell-Benutzeroberfläche, ob eine bestimmte Eigenschaft in der Shellbenutzeroberfläche bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="310f9-302">[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informs the Shell UI whether a particular property can be edited in the Shell UI.</span></span> <span data-ttu-id="310f9-303">Beachten Sie, dass sich dies nur auf die Möglichkeit bezieht, die Eigenschaft in der Benutzeroberfläche zu bearbeiten, nicht, ob Sie [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) für die Eigenschaft erfolgreich aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="310f9-303">It is important to note that this relates only to the ability to edit the property in the UI, not whether you can successfully call [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) on the property.</span></span> <span data-ttu-id="310f9-304">Eine Eigenschaft, die den Rückgabewert S \_ false aus [**ipropertystorecapabili:: ispropertywrite Table**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) provoziert, kann möglicherweise trotzdem über eine Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="310f9-304">A property that provokes a return value of S\_FALSE from [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) might still be capable of being set through an application.</span></span>


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



<span data-ttu-id="310f9-305">[**Ispropertywrite Table**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) gibt **S \_ OK** zurück, um anzugeben, dass Endbenutzer die Eigenschaft direkt bearbeiten dürfen. \_False gibt an, dass dies nicht der Fall sein sollte.</span><span class="sxs-lookup"><span data-stu-id="310f9-305">[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) returns **S\_OK** to indicate that end users should be allowed to edit the property directly; S\_FALSE indicates that they should not.</span></span> <span data-ttu-id="310f9-306">' \_ False ' kann bedeuten, dass Anwendungen für das Schreiben der Eigenschaft zuständig sind, nicht für Benutzer.</span><span class="sxs-lookup"><span data-stu-id="310f9-306">S\_FALSE can mean that applications are responsible for writing the property, not users.</span></span> <span data-ttu-id="310f9-307">Die Shell deaktiviert Bearbeitungs Steuerelemente entsprechend den Ergebnissen von Aufrufen dieser Methode je nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="310f9-307">The Shell disables editing controls as appropriate based on the results of calls to this method.</span></span> <span data-ttu-id="310f9-308">Bei einem Handler, der [**ipropertystorecapabilinicht**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) implementiert, wird angenommen, dass er Open Metadata durch Unterstützung für das Schreiben einer beliebigen Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="310f9-308">A handler that does not implement [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) is assumed to support open metadata through support for the writing of any property.</span></span>

<span data-ttu-id="310f9-309">Wenn Sie einen Handler erstellen, der nur schreibgeschützte Eigenschaften behandelt, sollten Sie die **Initialize** -Methode ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)oder [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) implementieren, damit Sie STG \_ E AccessDenied zurückgibt, wenn Sie \_ mit dem STGM- \_ leseschreib Flag aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="310f9-309">If you are building a handler that handles only read-only properties, then you should implement your **Initialize** method ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem), or [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) so that it returns STG\_E\_ACCESSDENIED when called with the STGM\_READWRITE flag.</span></span>

<span data-ttu-id="310f9-310">Für einige Eigenschaften ist das [isinnate](./propdesc-schema-typeinfo.md) -Attribut auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="310f9-310">Some properties have their [isInnate](./propdesc-schema-typeinfo.md) attribute set to **true**.</span></span> <span data-ttu-id="310f9-311">Angeborene Eigenschaften haben die folgenden Merkmale:</span><span class="sxs-lookup"><span data-stu-id="310f9-311">Innate properties have the following characteristics:</span></span>

-   <span data-ttu-id="310f9-312">Die-Eigenschaft wird in der Regel auf irgendeine Weise berechnet.</span><span class="sxs-lookup"><span data-stu-id="310f9-312">The property is usually calculated in some way.</span></span> <span data-ttu-id="310f9-313">Beispielsweise `System.Image.BitDepth` wird anhand des Bilds berechnet.</span><span class="sxs-lookup"><span data-stu-id="310f9-313">For instance, `System.Image.BitDepth` is calculated from the image itself.</span></span>
-   <span data-ttu-id="310f9-314">Das Ändern der Eigenschaft wäre nicht sinnvoll, ohne die Datei zu ändern.</span><span class="sxs-lookup"><span data-stu-id="310f9-314">Changing the property would not make sense without changing the file.</span></span> <span data-ttu-id="310f9-315">Wenn Sie beispielsweise `System.Image.Dimensions` die Größe des Bilds ändern, wird die Größe des Bilds nicht geändert, daher ist es nicht sinnvoll, es dem Benutzer zu gestatten.</span><span class="sxs-lookup"><span data-stu-id="310f9-315">For instance, changing `System.Image.Dimensions` would not resize the image, so it does not make sense to allow the user to change it.</span></span>
-   <span data-ttu-id="310f9-316">In einigen Fällen werden diese Eigenschaften vom System automatisch bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="310f9-316">In some cases, these properties are provided automatically by the system.</span></span> <span data-ttu-id="310f9-317">Zu den Beispielen gehören `System.DateModified` , die vom Dateisystem bereitgestellt werden, und `System.SharedWith` , der darauf basiert, wer der Benutzer für die Datei freigegeben hat.</span><span class="sxs-lookup"><span data-stu-id="310f9-317">Examples include `System.DateModified`, which is provided by the file system, and `System.SharedWith`, which is based on who the user is sharing the file with.</span></span>

<span data-ttu-id="310f9-318">Aufgrund dieser Merkmale werden Eigenschaften, die als *isinnate* gekennzeichnet sind, dem Benutzer nur als schreibgeschützte Eigenschaften in der Shell-Benutzeroberfläche bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="310f9-318">Due to these characteristics, properties marked as *IsInnate* are provided to the user in the Shell UI only as read-only properties.</span></span> <span data-ttu-id="310f9-319">Wenn eine Eigenschaft als *isinnate* gekennzeichnet ist, speichert das Eigenschaften System diese Eigenschaft nicht im Eigenschaften Handler.</span><span class="sxs-lookup"><span data-stu-id="310f9-319">If a property is marked as *IsInnate*, the property system does not store that property in the property handler.</span></span> <span data-ttu-id="310f9-320">Daher benötigen Eigenschaften Handler keinen speziellen Code, um diese Eigenschaften in ihren Implementierungen zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="310f9-320">Therefore, property handlers do not need special code to account for these properties in their implementations.</span></span> <span data-ttu-id="310f9-321">Wenn der Wert des *isinnate* -Attributs nicht explizit für eine bestimmte Eigenschaft angegeben wird, ist der Standardwert **false**.</span><span class="sxs-lookup"><span data-stu-id="310f9-321">If the value of the *IsInnate* attribute is not explicitly stated for a particular property, the default value is **false**.</span></span>

## <a name="registering-and-distributing-property-handlers"></a><span data-ttu-id="310f9-322">Registrieren und Verteilen von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="310f9-322">Registering and Distributing Property Handlers</span></span>

<span data-ttu-id="310f9-323">Nachdem der Eigenschaften Handler implementiert wurde, muss er registriert und seine Dateinamenerweiterung dem Handler zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="310f9-323">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="310f9-324">Weitere Informationen finden Sie unter [registrieren und Verteilen von Eigenschaften Handlern](./prophand-reg-dist.md).</span><span class="sxs-lookup"><span data-stu-id="310f9-324">For more information, see [Registering and Distributing Property Handlers](./prophand-reg-dist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="310f9-325">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="310f9-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="310f9-326">Grundlegendes zu Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="310f9-326">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="310f9-327">Verwenden von Kind-Namen</span><span class="sxs-lookup"><span data-stu-id="310f9-327">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="310f9-328">Verwenden von Eigenschaften Listen</span><span class="sxs-lookup"><span data-stu-id="310f9-328">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="310f9-329">Registrieren und Verteilen von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="310f9-329">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="310f9-330">Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="310f9-330">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
