---
description: Der Filter Handler muss registriert werden. Sie können auch einen vorhandenen Filter Handler für eine angegebene Dateinamenerweiterung entweder über die Registrierung oder mithilfe der iloadfilter-Schnittstelle suchen.
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: Registrieren von Filter Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f39688bbea3bb0dd73ef28a0ba6e8b0dcf7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128565"
---
# <a name="registering-filter-handlers"></a><span data-ttu-id="f106a-104">Registrieren von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="f106a-104">Registering Filter Handlers</span></span>

<span data-ttu-id="f106a-105">Der Filter Handler muss registriert werden.</span><span class="sxs-lookup"><span data-stu-id="f106a-105">Your filter handler must be registered.</span></span> <span data-ttu-id="f106a-106">Sie können auch einen vorhandenen Filter Handler für eine angegebene Dateinamenerweiterung entweder über die Registrierung oder mithilfe der [**iloadfilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) -Schnittstelle suchen.</span><span class="sxs-lookup"><span data-stu-id="f106a-106">You can also locate an existing filter handler for a given file name extension either through the registry or by using the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface.</span></span>

<span data-ttu-id="f106a-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="f106a-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="f106a-108">Registrieren von Filter Handlern für Windows Search</span><span class="sxs-lookup"><span data-stu-id="f106a-108">Registering Filters Handlers for Windows Search</span></span>](#registering-filter-handlers)
  - [<span data-ttu-id="f106a-109">Veralteter Ansatz zum Registrieren von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="f106a-109">Obsolete Approach for Registering Filters Handlers</span></span>](#obsolete-approach-for-registering-filters-handlers)
- [<span data-ttu-id="f106a-110">Ersetzen von vorhandenen Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="f106a-110">Replacing Existing Filter Handlers</span></span>](#replacing-existing-filter-handlers)
- [<span data-ttu-id="f106a-111">Suchen eines Filter Handlers für eine bestimmte Dateierweiterung</span><span class="sxs-lookup"><span data-stu-id="f106a-111">Finding a Filter Handler for a Given File Extension</span></span>](#finding-a-filter-handler-for-a-given-file-extension)
- [<span data-ttu-id="f106a-112">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f106a-112">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="f106a-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f106a-113">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="f106a-114">Ein Filter Handler ist eine Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f106a-114">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

## <a name="registering-filters-handlers-for-windows-search"></a><span data-ttu-id="f106a-115">Registrieren von Filter Handlern für Windows Search</span><span class="sxs-lookup"><span data-stu-id="f106a-115">Registering Filters Handlers for Windows Search</span></span>

<span data-ttu-id="f106a-116">Die GUIDs, die Sie zum Registrieren eines neuen Protokoll Handlers oder zum Suchen eines vorhandenen Protokoll Handlers benötigen, sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f106a-116">The GUIDs you need for registering a new protocol handler or to find an existing protocol handler are listed in the following table.</span></span>

| <span data-ttu-id="f106a-117">GUID</span><span class="sxs-lookup"><span data-stu-id="f106a-117">GUID</span></span>                                     | <span data-ttu-id="f106a-118">Benutzer oder Anwendung definiert</span><span class="sxs-lookup"><span data-stu-id="f106a-118">User or application defined</span></span> | <span data-ttu-id="f106a-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f106a-119">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f106a-120">**89bcb740-6119-101A-bcb7-00dd010655af**</span><span class="sxs-lookup"><span data-stu-id="f106a-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span></span> | <span data-ttu-id="f106a-121">Application</span><span class="sxs-lookup"><span data-stu-id="f106a-121">Application</span></span>                 | <span data-ttu-id="f106a-122">Der GUID der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle ist eine Konstante für den Registrierungsschlüssel für alle Filter Handler.</span><span class="sxs-lookup"><span data-stu-id="f106a-122">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface GUID is a registry key constant for all filter handlers.</span></span> |
| <span data-ttu-id="f106a-123">**{Persistenthandlerguid}**</span><span class="sxs-lookup"><span data-stu-id="f106a-123">**{PersistentHandlerGUID}**</span></span>              | <span data-ttu-id="f106a-124">Benutzer</span><span class="sxs-lookup"><span data-stu-id="f106a-124">User</span></span>                        | <span data-ttu-id="f106a-125">Dies ist die GUID für den persistenten Handler.</span><span class="sxs-lookup"><span data-stu-id="f106a-125">This is the GUID for the persistent handler.</span></span>                                                              |
| <span data-ttu-id="f106a-126">**{Filterhandlerclsid}**</span><span class="sxs-lookup"><span data-stu-id="f106a-126">**{FilterHandlerCLSID}**</span></span>                 | <span data-ttu-id="f106a-127">Benutzer</span><span class="sxs-lookup"><span data-stu-id="f106a-127">User</span></span>                        | <span data-ttu-id="f106a-128">Dies ist der Klassen Bezeichner (CLSID) für den Filter Handler.</span><span class="sxs-lookup"><span data-stu-id="f106a-128">This is the class identifier (CLSID) for the filter handler.</span></span>                                              |
| <span data-ttu-id="f106a-129">**{Applicationguid}**</span><span class="sxs-lookup"><span data-stu-id="f106a-129">**{ApplicationGUID}**</span></span>                    | <span data-ttu-id="f106a-130">Benutzer</span><span class="sxs-lookup"><span data-stu-id="f106a-130">User</span></span>                        | <span data-ttu-id="f106a-131">Dies ist eine zwischen (aggregierte) GUID.</span><span class="sxs-lookup"><span data-stu-id="f106a-131">This is an intermediate (aggregated) GUID.</span></span>                                                                |

<span data-ttu-id="f106a-132">Filter Handler müssen auf dem lokalen HKEY-Computer registriert werden, \_ \_ da SearchFilterHost.exe unter dem System Konto ausgeführt wird und daher nicht auf die Registrierungsschlüssel für den aktuellen HKEY- \_ \_ Benutzer für den angemeldeten Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="f106a-132">Filter handlers must be registered in HKEY\_LOCAL\_MACHINE because SearchFilterHost.exe is running under the SYSTEM account and therefore cannot access registry keys for HKEY\_CURRENT\_USER for the logged-on user.</span></span> <span data-ttu-id="f106a-133">Außerdem muss die Gruppe "Benutzer" über Lese-und Ausführungs Berechtigungen für die Datei "Filter Handler. dll" verfügen, da SearchFilterHost.exe alle Administratorrechte entfernt und nur nicht Administratorrechte zulässt.</span><span class="sxs-lookup"><span data-stu-id="f106a-133">In addition, the Users group must have read-and-execute access to the filter handler .dll itself because SearchFilterHost.exe removes all administrator rights and permits only non-administrator rights.</span></span> <span data-ttu-id="f106a-134">Da sich der Standard Speicherort von Visual Studio im Verzeichnis des aktuellen Benutzers befindet und keine Leseberechtigungen für die Benutzergruppe erteilt, müssen Sie entweder die DLL-Datei verschieben oder die ACLs ändern, um SearchFilterHost.exe Zugriff zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="f106a-134">Because the default Visual Studio project location is in the current user's directory, and so does not give read permissions to the Users group, you must either move the .dll or change the ACLs to allow SearchFilterHost.exe access.</span></span>

<span data-ttu-id="f106a-135">Wenn Sie einen neuen Filter Handler registrieren, empfiehlt es sich, einen beschreibenden Namen zu verwenden, z. b. html-IFilter.</span><span class="sxs-lookup"><span data-stu-id="f106a-135">When you register a new filter handler, we recommend that you use a descriptive name, for example, HTML IFilter.</span></span>

<span data-ttu-id="f106a-136">**So registrieren Sie den neuen Filter Handler:**</span><span class="sxs-lookup"><span data-stu-id="f106a-136">**To register your new filter handler:**</span></span>

1. <span data-ttu-id="f106a-137">Geben Sie die Erweiterung und die persistente handlerguid an, von der der Filter Handler verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="f106a-137">Specify the extension and persistent handler GUID that will use the filter handler:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                PersistentHandler
                   (Default) = {PersistentHandlerGUID}
```

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {PersistentHandlerGUID}
                      PersistentAddinsRegistered
                         {89BCB740-6119-101A-BCB7-00DD010655AF}l
                            (Default) = {FilterHandlerCLSID}
```

2. <span data-ttu-id="f106a-138">Registrieren Sie den Filter Handler mit den folgenden Schlüsseln und Werten:</span><span class="sxs-lookup"><span data-stu-id="f106a-138">Register your filter handler with the following keys and values:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {FilterHandlerCLSID}
                      (Default) = {DescriptiveFilterHandlerName}
                      InprocServer32
                         (Default) = DLL Install Path
                         ThreadingModel = Both
```

### <a name="obsolete-approach-for-registering-filters-handlers"></a><span data-ttu-id="f106a-139">Veralteter Ansatz zum Registrieren von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="f106a-139">Obsolete Approach for Registering Filters Handlers</span></span>

<span data-ttu-id="f106a-140">Diese Vorgehensweise wird nicht für die Verwendung empfohlen.</span><span class="sxs-lookup"><span data-stu-id="f106a-140">This approach is not recommended for use.</span></span> <span data-ttu-id="f106a-141">Filter können für eine CLSID registriert werden, die eine Component Object Model (com)-Klasse und/oder für eine Dateinamenerweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="f106a-141">Filters can be registered for a CLSID that represents a Component Object Model (COM) class, and/or for a file name extension.</span></span> <span data-ttu-id="f106a-142">Sie können beide Filter registrieren, wenn Sie einen Filter Handler für eine Klasse registrieren müssen, und einen anderen Filter Handler für eine Dateinamenerweiterung innerhalb der Klasse.</span><span class="sxs-lookup"><span data-stu-id="f106a-142">You could register both filters if you need to register a filter handler for a class, and a different filter handler for a file name extension within the class.</span></span> <span data-ttu-id="f106a-143">Beachten Sie, dass ein für eine Dateinamenerweiterung registrierter Filter Handler Vorrang vor einem Filter Handler für eine CLSID hat.</span><span class="sxs-lookup"><span data-stu-id="f106a-143">Note that a filter handler registered for a file name extension takes precedence over a filter handler for a CLSID.</span></span>

<span data-ttu-id="f106a-144">Diese Einträge sind OLE-Standard Registrierungseinträge bis einschließlich des Eintrags für die Klassen- **CLSID \\ {applicationguid}**.</span><span class="sxs-lookup"><span data-stu-id="f106a-144">These entries are standard OLE registry entries up to and including the entry for the class **CLSID\\{ApplicationGUID}**.</span></span> <span data-ttu-id="f106a-145">Die dll-sample.dll implementiert das Verhalten für das Ausführen von Objekten für die txt-Klasse.</span><span class="sxs-lookup"><span data-stu-id="f106a-145">The DLL sample.dll implements running object behavior for the .txt class.</span></span> <span data-ttu-id="f106a-146">Beachten Sie den zusätzlichen Eintrag PersistentHandler.</span><span class="sxs-lookup"><span data-stu-id="f106a-146">Note the extra entry, PersistentHandler.</span></span> <span data-ttu-id="f106a-147">Dieser Eintrag gibt die Klasse an, die für das Broker von Anforderungen an die persistenten Objekte der Beispiel Klasse zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="f106a-147">This entry specifies the class that is responsible for brokering requests to the persistent objects of the sample class.</span></span> <span data-ttu-id="f106a-148">Der Eintrag unter **persistentaddinsregistered** identifiziert die für die Schnittstelle mit dem Namen **89bcb740-6119-101A-bcb7-00dd010655af**(IID \_ IFilter) Verantwortliche Implementierung.</span><span class="sxs-lookup"><span data-stu-id="f106a-148">The entry under **PersistentAddinsRegistered** identifies the implementation responsible for the interface named **89BCB740-6119-101A-BCB7-00DD010655AF**(IID\_IFilter).</span></span> <span data-ttu-id="f106a-149">Die Klasse, die **IID \_ IFilter** implementiert, verfügt über Standard-OLE-Registrierungseinträge.</span><span class="sxs-lookup"><span data-stu-id="f106a-149">The class implementing **IID\_IFilter** has standard OLE registry entries.</span></span> <span data-ttu-id="f106a-150">Die InprocServer32-dll wird über den OLE-Standardmechanismus geladen.</span><span class="sxs-lookup"><span data-stu-id="f106a-150">The InprocServer32 DLL is loaded through the standard OLE mechanism.</span></span>

<span data-ttu-id="f106a-151">Windows Search beobachtet das Thread Modell, das für den Filter Handler angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f106a-151">Windows Search observes the threading model specified for the filter handler.</span></span> <span data-ttu-id="f106a-152">Wenn das Threading Modell auf **beide** festgelegt ist, muss der Filter Handler Thread sicher sein. Wenn Sie andernfalls nicht Thread sicher ist, geben Sie **Apartment** an.</span><span class="sxs-lookup"><span data-stu-id="f106a-152">When the threading model is set to **Both**, the filter handler must be thread safe; otherwise, if it is not thread safe, specify **Apartment**.</span></span> <span data-ttu-id="f106a-153">Beachten Sie, dass Filter Handler immer Thread sicher sein sollten.</span><span class="sxs-lookup"><span data-stu-id="f106a-153">Note that filter handlers should always be thread safe.</span></span>

<span data-ttu-id="f106a-154">Die folgenden Beispiel Registrierungseinträge gelten für einen Filter Handler, der für eine Klassen-und Dateinamenerweiterung registriert ist.</span><span class="sxs-lookup"><span data-stu-id="f106a-154">The following example registry entries are for a filter handler registered for a class and file name extension.</span></span> <span data-ttu-id="f106a-155">**{Persistenthandlerguid}** und **{filterhandlerclsid}** werden als Variablen zum Angeben von Werten verwendet, die vom Ersteller des Filter Handlers angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f106a-155">**{PersistentHandlerGUID}** and **{FilterHandlerCLSID}** are used as variables indicating values that need to be specified by the creator of the filter handler.</span></span> <span data-ttu-id="f106a-156">Die Werte sind vom Typ reg \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="f106a-156">The values are of type REG\_SZ.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Classes
         .txt
            (Default) = SampleFile
         SampleFile
            (Default) = Class for Sample Files
            CLSID
               (Default) = {ApplicationGUID}
         CLSID
            {ApplicationGUID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sample.dll
               PersistentHandler
                  (Default) = {PersistentHandlerGUID}
            {PersistentHandlerGUID}
               (Default) = Sample file persistent handler
               PersistentAddinsRegistered
                  {89BCB740-6119-101A-BCB7-00DD010655AF}l
                     (Default) = {FilterHandlerCLSID}
            {FilterHandlerCLSID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sampfilt.dll
                  ThreadingModel = Both
```

## <a name="replacing-existing-filter-handlers"></a><span data-ttu-id="f106a-157">Ersetzen von vorhandenen Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="f106a-157">Replacing Existing Filter Handlers</span></span>

<span data-ttu-id="f106a-158">Es wird empfohlen, die integrierten Filter Handler nicht für allgemeine Dateitypen wie txt, doc, HTML,. URL usw. zu ersetzen, da dies unerwünschte Auswirkungen auf andere Systemkomponenten haben kann.</span><span class="sxs-lookup"><span data-stu-id="f106a-158">We recommend that you do not replace the built-in filter handlers for common file types such as .txt, .doc, .html, .url, and so forth, because doing so can have undesired effects on other system components.</span></span> <span data-ttu-id="f106a-159">Das Indizieren von e-Mail-Nachrichtentext hängt z. b. von den Filter Handlern. txt,. html und RTF ab.</span><span class="sxs-lookup"><span data-stu-id="f106a-159">Indexing email message bodies depends on the .txt, .html, and .rtf filter handlers, for example.</span></span>

<span data-ttu-id="f106a-160">Wenn ein neuer Filter Handler für einen Dateityp als Ersatz für eine vorhandene Filter Registrierung installiert wird, sollte der Installer die aktuelle Registrierung speichern und wiederherstellen, wenn der neue Filter Handler deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="f106a-160">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="f106a-161">Es gibt keinen Mechanismus zum Verketten von Filtern.</span><span class="sxs-lookup"><span data-stu-id="f106a-161">There is no mechanism to chain filters.</span></span> <span data-ttu-id="f106a-162">Daher ist der neue Filter Handler für die Replikation aller notwendigen Funktionen des alten Filters verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="f106a-162">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a><span data-ttu-id="f106a-163">Suchen eines Filter Handlers für eine bestimmte Dateierweiterung</span><span class="sxs-lookup"><span data-stu-id="f106a-163">Finding a Filter Handler for a Given File Extension</span></span>

<span data-ttu-id="f106a-164">Sie können die [**iloadfilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) -Schnittstelle verwenden, um einen Filter Handler für eine angegebene Dateinamenerweiterung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f106a-164">You can use the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface to find a filter handler for a given file name extension.</span></span> <span data-ttu-id="f106a-165">Die folgenden Beispiel Registrierungseinträge veranschaulichen, wie dies für HTML-Dateien durchzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="f106a-165">The following example registry entries illustrate how to do so for HTML files.</span></span> <span data-ttu-id="f106a-166">In diesem Beispiel wird der Filter Handler für HTML-Dokumente nlhtml.dll.</span><span class="sxs-lookup"><span data-stu-id="f106a-166">In this example, the filter handler for HTML documents is nlhtml.dll.</span></span> <span data-ttu-id="f106a-167">Die Werte sind vom Typ reg \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="f106a-167">The values are of type REG\_SZ.</span></span>

<span data-ttu-id="f106a-168">**So finden Sie den Filter Handler für eine bestimmte Dateinamenerweiterung:**</span><span class="sxs-lookup"><span data-stu-id="f106a-168">**To find the filter handler for a given file name extension:**</span></span>

1. <span data-ttu-id="f106a-169">Überprüfen Sie, ob die Erweiterung für den Typ der gefilterten Dateien über einen permanenten Handler verfügt, der im Registrierungs Eintrag \\ HKEY \_ local \_ Machine \\ \\ Classes Software Classes. Extension registriert ist.</span><span class="sxs-lookup"><span data-stu-id="f106a-169">Check whether the extension for the type of files that are filtered has a persistent handler registered under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.extension.</span></span> <span data-ttu-id="f106a-170">Wenn dies der Fall ist, lassen Sie diesen Schlüssel {persistenthandlerguid}.</span><span class="sxs-lookup"><span data-stu-id="f106a-170">If so, let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. <span data-ttu-id="f106a-171">Wenn kein persistenter Handler für die Erweiterung registriert ist, suchen Sie nach der CLSID, die dem Dokumenttyp im Registrierungs Eintrag \\ HKEY \_ local \_ Machine- \\ Software \\ Klassen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f106a-171">If there is not a persistent handler registered for the extension, find the CLSID associated with the document type under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.</span></span> <span data-ttu-id="f106a-172">Übernehmen Sie diesen Schlüssel {applicationguid}.</span><span class="sxs-lookup"><span data-stu-id="f106a-172">Let this key be {ApplicationGUID}.</span></span> <span data-ttu-id="f106a-173">Legen Sie dann fest, ob ein permanenter Handler für die CLSID registriert ist: Suchen Sie mithilfe von {applicationguid} den permanenten Handler für den \\ \_ Eintrag " \_ \\ \\ \\ CLSID \\ {applicationguid}" der HKEY Local Machine Classes.</span><span class="sxs-lookup"><span data-stu-id="f106a-173">Then determine whether a persistent handler is registered for the CLSID: using {ApplicationGUID} locate the persistent handler for the \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{ApplicationGUID} entry.</span></span> <span data-ttu-id="f106a-174">Lassen Sie diesen Schlüssel {persistenthandlerguid}.</span><span class="sxs-lookup"><span data-stu-id="f106a-174">Let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                (Default) = Class for WWW HTML files
                CLSID
                   (Default) = {25336920-03F9-11CF-8FD0-00AA00686F13}
             CLSID
                {25336920-03F9-11CF-8FD0-00AA00686F13}
                   PersistentHandler
                      (Default) = {PersistentHandlerGUID}
```

3. <span data-ttu-id="f106a-175">Bestimmen Sie die GUID des permanenten Handlers: Verwenden Sie {persistenthandlerguid}, um die persistente handlerguid für den Dokumenttyp zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f106a-175">Determine the GUID of the persistent handler: using {PersistentHandlerGUID} find the persistent handler GUID for the document type.</span></span> <span data-ttu-id="f106a-176">Der Wert unter dem Registrierungs Eintrag HKEY \_ local \_ Machine \\ \\ Classes \\ CLSID \\ {persistenthandlerguid} \\ persistentaddinsregistered \\ 89bcb740-6119-101A-bcb7-00dd010655af ergibt die persistente handlerguid für diesen Dokumenttyp.</span><span class="sxs-lookup"><span data-stu-id="f106a-176">The value under the registry entry HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{PersistentHandlerGUID}\\PersistentAddinsRegistered\\ 89BCB740-6119-101A-BCB7-00DD010655AF yields the persistent handler GUID for this document type.</span></span> <span data-ttu-id="f106a-177">Lassen Sie den Schlüssel {filterhandlerclsid}.</span><span class="sxs-lookup"><span data-stu-id="f106a-177">Let this key be {FilterHandlerCLSID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. <span data-ttu-id="f106a-178">Bestimmen des Filter Handlers: mithilfe von {filterhandlerclsid}, der im vorherigen Schritt ermittelt wurde, finden Sie den Filter Handler unter dem Eintrag \\ HKEY \_ local \_ Machine \\ \\ Classes \\ CLSID \\ {filterhandlerclsid} \\ InProcServer32.</span><span class="sxs-lookup"><span data-stu-id="f106a-178">Determine the filter handler: using {FilterHandlerCLSID} that was determined in the previous step locate the filter handler under the entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{FilterHandlerCLSID}\\InprocServer32.</span></span> <span data-ttu-id="f106a-179">In diesem Beispiel ist der Name des beschreibenden Filter Handlers der HTML-IFilter.</span><span class="sxs-lookup"><span data-stu-id="f106a-179">In this example the descriptive filter handler name used is HTML IFilter.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             CLSID
                {EEC97550-47A9-11CF-B952-00AA0051FE20}
                   (Default) = HTML IFilter
                    Data type  REG_SZ
                    InprocServer32
                    nlhtml.dll
```

## <a name="additional-resources"></a><span data-ttu-id="f106a-180">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f106a-180">Additional Resources</span></span>

- <span data-ttu-id="f106a-181">Das in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbare [ifiltersample](-search-sample-ifiltersample.md) -Codebeispiel veranschaulicht, wie eine [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Basisklasse für die Implementierung der **IFilter** -Schnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f106a-181">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) base class for implementing the **IFilter** interface.</span></span>
- <span data-ttu-id="f106a-182">Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f106a-182">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="f106a-183">Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f106a-183">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="f106a-184">Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".</span><span class="sxs-lookup"><span data-stu-id="f106a-184">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f106a-185">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f106a-185">Related topics</span></span>

[<span data-ttu-id="f106a-186">Entwickeln von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="f106a-186">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="f106a-187">Informationen zu Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="f106a-187">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="f106a-188">Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="f106a-188">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="f106a-189">Zurückgeben von Eigenschaften aus einem Filter Handler</span><span class="sxs-lookup"><span data-stu-id="f106a-189">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="f106a-190">Filtern von Handlern, die mit Windows ausgeliefert werden</span><span class="sxs-lookup"><span data-stu-id="f106a-190">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="f106a-191">Implementieren von Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="f106a-191">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="f106a-192">Testen von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="f106a-192">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
