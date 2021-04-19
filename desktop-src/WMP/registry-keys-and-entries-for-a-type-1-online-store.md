---
title: Registrierungsschlüssel und-Einträge für einen Typ-1-Online Speicher
description: Registrierungsschlüssel und-Einträge für einen Typ-1-Online Speicher
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Windows Media Player Online Stores, Registrierung
- Online Stores, Registrierung
- Typ 1 Online Stores, Registrierung
- Registrierung, Typ 1 Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339868"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a><span data-ttu-id="aba77-107">Registrierungsschlüssel und-Einträge für einen Typ-1-Online Speicher</span><span class="sxs-lookup"><span data-stu-id="aba77-107">Registry Keys and Entries for a Type 1 Online Store</span></span>

<span data-ttu-id="aba77-108">Um einen Onlinespeicher vom Typ 1 in Windows Media Player verfügbar zu machen, muss der Onlinespeicher Anbieter die folgenden Registrierungs Unterschlüssel und Einträge auf dem Computer des Benutzers erstellen.</span><span class="sxs-lookup"><span data-stu-id="aba77-108">To make a type 1 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> <span data-ttu-id="aba77-109">Das Festlegen des Werts von dllersatz auf die leere Zeichenfolge gibt an, dass die com-Laufzeit das Plug-in des Online Stores in das standardmäßige DLL-Ersatz Zeichen (dllhost.exe) lädt.</span><span class="sxs-lookup"><span data-stu-id="aba77-109">Setting the value of DllSurrogate to the empty string indicates that the COM runtime will load the online store's plug-in into the default DLL surrogate, dllhost.exe.</span></span>

 

<span data-ttu-id="aba77-110">In der vorangehenden Registrierungs Syntax sind die Symbole in kursiv Platzhalter für Namen und Global Unique Identifier (GUIDs), die für den Online Store spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="aba77-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="aba77-111">In der folgenden Tabelle werden diese Platzhalter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aba77-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="aba77-112">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="aba77-112">Placeholder</span></span>    | <span data-ttu-id="aba77-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aba77-113">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aba77-114">*keyName*</span><span class="sxs-lookup"><span data-stu-id="aba77-114">*keyName*</span></span>      | <span data-ttu-id="aba77-115">Eine Zeichenfolge, die zwischen Microsoft und dem Online Store vereinbart wurde.</span><span class="sxs-lookup"><span data-stu-id="aba77-115">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="aba77-116">Diese Zeichenfolge identifiziert den Online Store eindeutig. Beispiel: "Proseware"</span><span class="sxs-lookup"><span data-stu-id="aba77-116">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="aba77-117">*flags*</span><span class="sxs-lookup"><span data-stu-id="aba77-117">*flags*</span></span>        | <span data-ttu-id="aba77-118">Eine bitweise **or** -Funktion von mindestens einem Plug-in-funktionsflags diese Flags geben an, ob Windows Media Player bestimmte Methoden von [iwmpcontentpartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)aufruft.</span><span class="sxs-lookup"><span data-stu-id="aba77-118">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span></span> <span data-ttu-id="aba77-119">Weitere Informationen zu unterstützten Flags finden Sie in der Tabelle mit den Plug-in-funktionsflags, die dieser Tabelle folgt. Beispiel: 00000058</span><span class="sxs-lookup"><span data-stu-id="aba77-119">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000058</span></span><br/> |
| <span data-ttu-id="aba77-120">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="aba77-120">*clsid*</span></span>        | <span data-ttu-id="aba77-121">Eine GUID, bei der es sich um den Klassen Bezeichner (CLSID) für die Klasse handelt, die **iwmpcontentpartner** im Online Store-Plug-in implementiert.</span><span class="sxs-lookup"><span data-stu-id="aba77-121">A GUID that is the class identifier (CLSID) for the class that implements **IWMPContentPartner** in the online store's plug-in.</span></span> <span data-ttu-id="aba77-122">Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden. Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="aba77-122">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                  |
| <span data-ttu-id="aba77-123">*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="aba77-123">*friendlyname*</span></span> | <span data-ttu-id="aba77-124">Ein Anzeige Name für den Online Shop. Beispiel: "Proseware Music Service"</span><span class="sxs-lookup"><span data-stu-id="aba77-124">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="aba77-125">*appid*</span><span class="sxs-lookup"><span data-stu-id="aba77-125">*appid*</span></span>        | <span data-ttu-id="aba77-126">Eine GUID, bei der es sich um den Anwendungs Bezeichner (AppID) für das Plug-in des Online Stores handelt.</span><span class="sxs-lookup"><span data-stu-id="aba77-126">A GUID that is the application identifier (AppID) for the online store's plug-in.</span></span> <span data-ttu-id="aba77-127">Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden. Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="aba77-127">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                |
| <span data-ttu-id="aba77-128">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="aba77-128">*pluginName*</span></span>   | <span data-ttu-id="aba77-129">Ein Name für das Plug-in des Online Stores. Beispiel: "Proseware Content Partner Plug-in"</span><span class="sxs-lookup"><span data-stu-id="aba77-129">A name for the online store's plug-in.Example: "Proseware Content Partner Plug-in"</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="aba77-130">*className*</span><span class="sxs-lookup"><span data-stu-id="aba77-130">*className*</span></span>    | <span data-ttu-id="aba77-131">Der Name der Klasse, die **iwmpcontentpartner** im Plug-in des Online Stores implementiert. Beispiel: "cprosewarepartner"</span><span class="sxs-lookup"><span data-stu-id="aba77-131">The name of the class that implements **IWMPContentpartner** in the online store's plug-in.Example: "CProsewarePartner"</span></span><br/>                                                                                                                                                                                              |
| <span data-ttu-id="aba77-132">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="aba77-132">*moduleName*</span></span>   | <span data-ttu-id="aba77-133">Der voll qualifizierte Pfad zu der dll, die das Plug-in des Online Stores implementiert. Beispiel: "C: \\ Program Files \\ proseware \\ProsewarePartner.dll"</span><span class="sxs-lookup"><span data-stu-id="aba77-133">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewarePartner.dll"</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="aba77-134">*Threading*</span><span class="sxs-lookup"><span data-stu-id="aba77-134">*threading*</span></span>    | <span data-ttu-id="aba77-135">Der Typ des Apartment, in dem das Plug-in ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aba77-135">The type of apartment the plug-in runs in.</span></span> <span data-ttu-id="aba77-136">"ThreadingModel" = "Apartment" gibt an, dass das Plug-in in einem Single Thread-Apartment (STA) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aba77-136">"ThreadingModel"="Apartment" indicates that the plug-in runs in a single-threaded apartment (STA).</span></span> <span data-ttu-id="aba77-137">"ThreadingModel" = "Free" gibt an, dass das Plug-in im Multithread-Apartment (MTA) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aba77-137">"ThreadingModel"="Free" indicates that the plug-in runs in the multithreaded apartment (MTA).</span></span>                                                                                     |



 

<span data-ttu-id="aba77-138">In der folgenden Tabelle werden die Plug-in-funktionsflags beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aba77-138">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="aba77-139">Flag</span><span class="sxs-lookup"><span data-stu-id="aba77-139">Flag</span></span>                                    | <span data-ttu-id="aba77-140">Wert</span><span class="sxs-lookup"><span data-stu-id="aba77-140">Value</span></span> | <span data-ttu-id="aba77-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aba77-141">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aba77-142">\_ \_ backgroundprocessing für Abonnement Abdeckung</span><span class="sxs-lookup"><span data-stu-id="aba77-142">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="aba77-143">0x8</span><span class="sxs-lookup"><span data-stu-id="aba77-143">0x8</span></span>   | <span data-ttu-id="aba77-144">Windows Media Player sollte [iwmpcontentpartner:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) anrufen, um das Plug-in zu informieren, wenn die Hintergrundverarbeitung gestartet und beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aba77-144">Windows Media Player should call [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) to inform the plug-in when it should start and stop background processing.</span></span>                                                                                                     |
| <span data-ttu-id="aba77-145">Abonnement \_ Abdeckung \_ deviceavailable</span><span class="sxs-lookup"><span data-stu-id="aba77-145">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="aba77-146">0x10</span><span class="sxs-lookup"><span data-stu-id="aba77-146">0x10</span></span>  | <span data-ttu-id="aba77-147">Windows Media Player sollte [iwmpcontentpartner:: updatedevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aba77-147">Windows Media Player should call [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span></span>                                                                                                                                                                   |
| <span data-ttu-id="aba77-148">Abonnement \_ Grenze \_ ist \_ Contentpartner</span><span class="sxs-lookup"><span data-stu-id="aba77-148">SUBSCRIPTION\_CAP\_IS\_CONTENTPARTNER</span></span>   | <span data-ttu-id="aba77-149">0x40</span><span class="sxs-lookup"><span data-stu-id="aba77-149">0x40</span></span>  | <span data-ttu-id="aba77-150">Informiert Windows Media Player, dass das Plug-in die **iwmpcontentpartner** -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="aba77-150">Informs Windows Media Player that the plug-in implements the **IWMPContentPartner** interface.</span></span> <span data-ttu-id="aba77-151">Dieses Flag muss von allen Online Store-Plug-ins vom Typ 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aba77-151">All type 1 online store plug-ins must set this flag.</span></span>                                                                                                                         |
| <span data-ttu-id="aba77-152">Abonnement- \_ Cap- \_ altanmeldung</span><span class="sxs-lookup"><span data-stu-id="aba77-152">SUBSCRIPTION\_CAP\_ALTLOGIN</span></span>             | <span data-ttu-id="aba77-153">0x80</span><span class="sxs-lookup"><span data-stu-id="aba77-153">0x80</span></span>  | <span data-ttu-id="aba77-154">Informiert Windows Media Player, dass das Plug-in eine Alternative Anmeldung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aba77-154">Informs Windows Media Player that the plug-in supports an alternate login.</span></span> <span data-ttu-id="aba77-155">Wenn das Plug-in eine Alternative Anmeldung unterstützt, ruft Windows Media Player die Alternative Anmelde-URL und Beschriftung durch Aufrufen von [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)ab.</span><span class="sxs-lookup"><span data-stu-id="aba77-155">If the plug-in supports an alternate login, Windows Media Player retrieves the alternate login URL and caption by calling [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span></span> |



 

<span data-ttu-id="aba77-156">**Registrierungseinträge für Entwicklung und Tests**</span><span class="sxs-lookup"><span data-stu-id="aba77-156">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="aba77-157">Wenn Sie mit der Entwicklung Ihres Online Stores beginnen, bietet Microsoft Ihnen zwei Schlüssel: einen Testschlüssel und einen Produktions Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="aba77-157">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="aba77-158">Während der Entwicklungs-und Testphase wird der Online Shop in Windows Media Player nur angezeigt, wenn sich der Testschlüssel oder Ihr Produktions Schlüssel in der Registrierung auf dem Computer des Benutzers befindet.</span><span class="sxs-lookup"><span data-stu-id="aba77-158">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="aba77-159">Weitere Informationen zu Test-und Produktions Schlüsseln finden Sie unter [Test-und Produktions Schlüssel für einen Online Store vom Typ 1](test-and-production-keys-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="aba77-159">For more information about the test and production keys, see [Test and Production Keys for a Type 1 Online Store](test-and-production-keys-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="aba77-160">Platzieren Sie den Test-oder Produktions Schlüssel an folgendem Speicherort in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="aba77-160">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="aba77-161">Beachten Sie, dass der Wert des Registrierungs Eintrags Testparameter mehrere Test-oder Produktions Schlüssel angeben kann.</span><span class="sxs-lookup"><span data-stu-id="aba77-161">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="aba77-162">Nehmen wir beispielsweise an, dass Proseware einen Testschlüssel mit dem Wert "1234" hat und dass die Datei "" den Testschlüssel "2345" hat.</span><span class="sxs-lookup"><span data-stu-id="aba77-162">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="aba77-163">Der folgende Registrierungs Eintrag gibt an, dass die Test Speicher für Proseware und Microsoft Configuration Manager in der Windows-Media Player angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="aba77-163">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="aba77-164">**ActiveService-Registrierungs Eintrag**</span><span class="sxs-lookup"><span data-stu-id="aba77-164">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="aba77-165">Wenn der Benutzer einen Online Shop aktiviert, schreibt Windows Media Player Informationen in die Registrierung, die den aktiven Online Store identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aba77-165">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="aba77-166">In Windows Media Player werden die Informationen an folgendem Speicherort in der Registrierung auf dem Computer des Benutzers abgelegt.</span><span class="sxs-lookup"><span data-stu-id="aba77-166">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="aba77-167">In der vorangehenden Registrierungs Syntax ist *serviceInfo* ein Platzhalter für eine Zeichenfolge, die beschreibende Informationen zum aktiven Online Store enthält.</span><span class="sxs-lookup"><span data-stu-id="aba77-167">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aba77-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aba77-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aba77-169">**Referenz für Typ 1-Onlineshops**</span><span class="sxs-lookup"><span data-stu-id="aba77-169">**Reference for Type 1 Online Stores**</span></span>](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





