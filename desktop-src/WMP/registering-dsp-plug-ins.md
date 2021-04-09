---
title: Registrieren von DSP-Plug-ins
description: Registrieren von DSP-Plug-ins
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Windows Media Player-Plug-ins, Registrierungseinträge
- Plug-ins, Registrierungseinträge
- Plug-Ins für die digitale Signalverarbeitung, Registrierungseinträge
- DSP-Plug-ins, Registrierungseinträge
- Registrierung, DSP-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948439"
---
# <a name="registering-dsp-plug-ins"></a><span data-ttu-id="e6267-108">Registrieren von DSP-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="e6267-108">Registering DSP Plug-ins</span></span>

<span data-ttu-id="e6267-109">Um Ihr DSP-Plug-in in Media Player Windows verfügbar zu machen, müssen Sie auf dem Computer des Benutzers die folgenden Registrierungs Unterschlüssel und Einträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="e6267-109">To make your DSP plug-in available in Windows Media Player you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



<span data-ttu-id="e6267-110">In der vorangehenden Registrierungs Syntax sind die Symbole in kursiv Platzhalter für Namen und Global Unique Identifier (GUIDs), die für das DSP-Plug-in spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="e6267-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="e6267-111">In der folgenden Tabelle werden diese Platzhalter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e6267-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="e6267-112">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="e6267-112">Placeholder</span></span>               | <span data-ttu-id="e6267-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6267-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6267-114">*Pluginclsid*</span><span class="sxs-lookup"><span data-stu-id="e6267-114">*PluginClsid*</span></span>             | <span data-ttu-id="e6267-115">Eine GUID, die der Klassen Bezeichner für die primäre Klasse des DSP-Plug-ins ist.</span><span class="sxs-lookup"><span data-stu-id="e6267-115">A GUID that is the class identifier for the DSP plug-in's primary class.</span></span> <span data-ttu-id="e6267-116">Dies ist die Klasse, die **imediaobject**, **ipluginenable** und möglicherweise **ISpecifyPropertyPages** implementiert.</span><span class="sxs-lookup"><span data-stu-id="e6267-116">This is the class that implements **IMediaObject**, **IPluginEnable**, and possibly **ISpecifyPropertyPages**.</span></span> <span data-ttu-id="e6267-117">In einem Dual-Mode-Plug-in implementiert diese Klasse auch **IMF Transform** und **IMF GetService**. Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden.</span><span class="sxs-lookup"><span data-stu-id="e6267-117">In a dual-mode plug-in, this class also implements **IMFTransform** and **IMFGetService**.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="e6267-118">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="e6267-118">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="e6267-119">*Pluginclassfriendlyname*</span><span class="sxs-lookup"><span data-stu-id="e6267-119">*PluginClassFriendlyName*</span></span> | <span data-ttu-id="e6267-120">Ein Anzeige Name für die primäre Klasse des DSP-Plug-ins. Beispiel: "prosewaredsp Class"</span><span class="sxs-lookup"><span data-stu-id="e6267-120">A friendly name for the DSP plug-in's primary class.Example: "ProsewareDSP Class"</span></span><br/>                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e6267-121">*Pluginmodulename*</span><span class="sxs-lookup"><span data-stu-id="e6267-121">*PluginModuleName*</span></span>        | <span data-ttu-id="e6267-122">Der voll qualifizierte Pfad zu der dll, die das DSP-Plug-in implementiert. Beispiel: "C: \\ Program Files \\ proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="e6267-122">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="e6267-123">*Threading*</span><span class="sxs-lookup"><span data-stu-id="e6267-123">*Threading*</span></span>               | <span data-ttu-id="e6267-124">Eine Zeichenfolge, die das Threading Modell für das Plug-in angibt.</span><span class="sxs-lookup"><span data-stu-id="e6267-124">A string that specifies the threading model for the plug-in.</span></span> <span data-ttu-id="e6267-125">Wenn das Plug-in mit Windows Media Player 11 unter Windows Vista ausgeführt wird, muss dieser Registrierungs Eintrag gleich "beide" sein.</span><span class="sxs-lookup"><span data-stu-id="e6267-125">If the plug-in is going to run with Windows Media Player 11 on Windows Vista, this registry entry must be equal to "Both".</span></span> <span data-ttu-id="e6267-126">Wenn das Plug-in unter Windows XP oder älteren Betriebssystemen ausgeführt werden soll, kann dieser Registrierungs Eintrag entweder "Apartment" oder "both" lauten.</span><span class="sxs-lookup"><span data-stu-id="e6267-126">If the plug-in is going to run on Windows XP or older operating systems, this registry entry can be equal to either "Apartment" or "Both".</span></span>                                                                                           |



 

<span data-ttu-id="e6267-127">Wenn Ihr DSP-Plug-in eine benutzerdefinierte Schnittstelle implementiert und das Plug-in unter Windows Media Player 11 unter Windows Vista ausgeführt wird, müssen Sie auf dem Computer des Benutzers die folgenden Registrierungs Unterschlüssel und-Einträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="e6267-127">If your DSP plug-in implements a custom interface and if your plug-in is going to run in Windows Media Player 11 on Windows Vista, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



<span data-ttu-id="e6267-128">In der vorangehenden Registrierungs Syntax sind die Symbole in kursiv Platzhalter für Namen, numerische Werte und global eindeutige Bezeichner (GUIDs), die für das DSP-Plug-in spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="e6267-128">In the preceding registry syntax, the symbols in italic are placeholders for names, numeric values, and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="e6267-129">In der folgenden Tabelle werden diese Platzhalter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e6267-129">The following table describes those placeholders.</span></span>



| <span data-ttu-id="e6267-130">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="e6267-130">Placeholder</span></span>           | <span data-ttu-id="e6267-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6267-131">Description</span></span>                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6267-132">*Proxystubclsid*</span><span class="sxs-lookup"><span data-stu-id="e6267-132">*ProxyStubClsid*</span></span>      | <span data-ttu-id="e6267-133">Eine GUID, die der Klassen Bezeichner für die Klasse ist, die die Proxys und stubwerte für die benutzerdefinierten Schnittstellen des DSP-Plug-Ins implementiert. Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden.</span><span class="sxs-lookup"><span data-stu-id="e6267-133">A GUID that is the class identifier for the class that implements the proxies and stubs for the DSP plug-in's custom interfaces.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="e6267-134">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="e6267-134">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="e6267-135">*Proxystubmodulename*</span><span class="sxs-lookup"><span data-stu-id="e6267-135">*ProxyStubModuleName*</span></span> | <span data-ttu-id="e6267-136">Der voll qualifizierte Pfad zu der dll, die die Proxy-und Stub-Schnittstellen für das DSP-Plug-in implementiert. Beispiel: "C: \\ Program Files \\ proseware \\ProsewareDspPS.dll"</span><span class="sxs-lookup"><span data-stu-id="e6267-136">The fully qualified path to the DLL that implements the proxy and stub interfaces for the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDspPS.dll"</span></span><br/>                                                                                               |
| <span data-ttu-id="e6267-137">*Custominterfakeid*</span><span class="sxs-lookup"><span data-stu-id="e6267-137">*CustomInterfaceId*</span></span>   | <span data-ttu-id="e6267-138">Eine GUID, die der Schnittstellen Bezeichner für eine benutzerdefinierte Schnittstelle ist, die durch das DSP-Plug-in implementiert wird. Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden.</span><span class="sxs-lookup"><span data-stu-id="e6267-138">A GUID that is the interface identifier for a custom interface that is implemented by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="e6267-139">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="e6267-139">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                           |
| <span data-ttu-id="e6267-140">*Custominterfakename*</span><span class="sxs-lookup"><span data-stu-id="e6267-140">*CustomInterfaceName*</span></span> | <span data-ttu-id="e6267-141">Der Name einer benutzerdefinierten Schnittstelle, die vom DSP-Plug-in implementiert wird. Beispiel: "iprosewaredsp"</span><span class="sxs-lookup"><span data-stu-id="e6267-141">The name of a custom interface that is implemented by the DSP plug-in.Example: "IProsewareDsp"</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="e6267-142">*Anzahlungsmethoden*</span><span class="sxs-lookup"><span data-stu-id="e6267-142">*NumberOfMethods*</span></span>     | <span data-ttu-id="e6267-143">Die Anzahl der Methoden, einschließlich der geerbten Methoden, die durch eine benutzerdefinierte Schnittstelle definiert werden. Beispiel: "5"</span><span class="sxs-lookup"><span data-stu-id="e6267-143">The number of methods, including inherited methods, defined by a custom interface.Example: "5"</span></span><br/>                                                                                                                                                                  |



 

<span data-ttu-id="e6267-144">Wenn Ihr DSP-Plug-in eine Eigenschaften Seite bereitstellt, müssen Sie auf dem Computer des Benutzers die folgenden Registrierungs Unterschlüssel und Einträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="e6267-144">If your DSP plug-in provides a property page, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="e6267-145">In der vorangehenden Registrierungs Syntax sind die Symbole in kursiv Platzhalter für Namen und Global Unique Identifier (GUIDs), die für das DSP-Plug-in spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="e6267-145">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="e6267-146">In der folgenden Tabelle werden diese Platzhalter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e6267-146">The following table describes those placeholders.</span></span>



| <span data-ttu-id="e6267-147">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="e6267-147">Placeholder</span></span>                 | <span data-ttu-id="e6267-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6267-148">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6267-149">*Proppageclsid*</span><span class="sxs-lookup"><span data-stu-id="e6267-149">*PropPageClsid*</span></span>             | <span data-ttu-id="e6267-150">Eine GUID, die der Klassen Bezeichner für die Eigenschaften Seiten Klasse ist, die vom DSP-Plug-in bereitgestellt wird. Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden.</span><span class="sxs-lookup"><span data-stu-id="e6267-150">A GUID that is the class identifier for the property page class provided by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="e6267-151">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="e6267-151">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="e6267-152">*Proppageclassfriendlyname*</span><span class="sxs-lookup"><span data-stu-id="e6267-152">*PropPageClassFriendlyName*</span></span> | <span data-ttu-id="e6267-153">Ein Anzeige Name für die Eigenschaften Seiten Klasse. Beispiel: "prosewaredsp Property Page Class"</span><span class="sxs-lookup"><span data-stu-id="e6267-153">A friendly name for the property page class.Example: "ProsewareDSP Property Page Class"</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="e6267-154">*Pluginmodulename*</span><span class="sxs-lookup"><span data-stu-id="e6267-154">*PluginModuleName*</span></span>          | <span data-ttu-id="e6267-155">Der voll qualifizierte Pfad zu der dll, die das DSP-Plug-in implementiert. Beispiel: "C: \\ Program Files \\ proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="e6267-155">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                               |



 

<span data-ttu-id="e6267-156">**Iwmppluginregistrar wird aufgerufen**</span><span class="sxs-lookup"><span data-stu-id="e6267-156">**Calling IWMPPluginRegistrar**</span></span>

<span data-ttu-id="e6267-157">Zusätzlich zu den in den vorangehenden Listen und Tabellen beschriebenen Registrierungs unter Schlüsseln und Einträgen müssen Sie einige Registrierungsschlüssel und-Einträge erstellen, indem Sie [iwmpmediapluginregistrar:: wmpregisterplayerplugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e6267-157">In addition to the registry subkeys and entries described in the preceding lists and tables, you must create some registry keys and entries by calling [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span></span> <span data-ttu-id="e6267-158">Diese Methode führt die erforderliche Registrierung aus, damit Windows Media Player Ihr Plug-in erkennen und als Option für den Benutzer präsentieren kann.</span><span class="sxs-lookup"><span data-stu-id="e6267-158">This method performs the necessary registration to enable Windows Media Player to recognize your plug-in and present it as an option to the user.</span></span>

<span data-ttu-id="e6267-159">Rufen Sie in der **DllRegisterServer** -Funktion des Plug-ins den Befehl **iwmpmediapluginregistrar:: wmpregisterplayerplugin** auf, und rufen Sie in der **DllUnregisterServer** -Funktion des Plug-ins den Befehl [iwmpmediapluginregistername](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) auf.</span><span class="sxs-lookup"><span data-stu-id="e6267-159">Call **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** in your plug-in's **DllRegisterServer** function, and call [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) in your plug-in's **DllUnregisterServer** function.</span></span> <span data-ttu-id="e6267-160">Um einen Zeiger auf eine **iwmpmediapluginregistrar** -Schnittstelle zu erhalten, müssen Sie **cokreateinstance** aufrufen und CLSID \_ wmpmediapluginregistrar als Klassen-ID übergeben.</span><span class="sxs-lookup"><span data-stu-id="e6267-160">To get a pointer to an **IWMPMediaPluginRegistrar** interface, call **CoCreateInstance**, passing CLSID\_WMPMediaPluginRegistrar as the Class ID.</span></span> <span data-ttu-id="e6267-161">Die Konstante CLSID \_ wmpmediapluginregistrar ist in wmpservices. h definiert.</span><span class="sxs-lookup"><span data-stu-id="e6267-161">The constant CLSID\_WMPMediaPluginRegistrar is defined in wmpservices.h.</span></span>

<span data-ttu-id="e6267-162">**Registrierung im DSP-Plug-in-Assistenten**</span><span class="sxs-lookup"><span data-stu-id="e6267-162">**Registration in the DSP Plug-in Wizard**</span></span>

<span data-ttu-id="e6267-163">Der DSP-Plug-in-Assistent, der in der Windows SDK enthalten ist, generiert Beispielcode, der auf Active Template Library (ATL) basiert.</span><span class="sxs-lookup"><span data-stu-id="e6267-163">The DSP plug-in wizard, which is included in the Windows SDK, generates sample code that is based on Active Template Library (ATL).</span></span> <span data-ttu-id="e6267-164">Die **DllRegisterServer** -Funktion des Plug-Ins für das Beispiel ruft die **RegisterServer** -Funktion von ATL auf, mit der Registrierungs Unterschlüssel und Einträge gemäß zwei Registrierungs Skriptdateien im Visual Studio-Projekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e6267-164">The sample plug-in's **DllRegisterServer** function calls ATL's **RegisterServer** function, which creates registry subkeys and entries according to two registry script files in the Visual Studio project.</span></span> <span data-ttu-id="e6267-165">Die Datei " *ProjectName*. RGS" enthält das Skript zum Registrieren der Hauptklasse des Plug-ins, und die Datei " *ProjectName* PropPage. RGS" enthält das Skript zum Registrieren der Eigenschaften Seiten Klasse des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="e6267-165">The file *ProjectName*.rgs contains the script for registering the plug-in's main class, and the file *ProjectName* PropPage.rgs contains the script for registering the plug-in's property page class.</span></span> <span data-ttu-id="e6267-166">Die **DllRegisterServer** -Funktion des Plug-Ins für das Beispiel ruft auch **iwmppluginregistrar:: wmpregisterplayerplugin** auf.</span><span class="sxs-lookup"><span data-stu-id="e6267-166">The sample plug-in's **DllRegisterServer** function also calls **IWMPPluginRegistrar::WMPRegisterPlayerPlugin**.</span></span>

<span data-ttu-id="e6267-167">Der DSP-Plug-in-Assistent generiert auch Code für eine ProxyStub-Komponente, bei der es sich um eine selbst registrierte DLL-Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="e6267-167">The DSP plug-in wizard also generates code for a proxy-stub component that is a self-registering .dll file.</span></span> <span data-ttu-id="e6267-168">Der Registrierungscode für diese Datei befindet sich in "dlldata. cpp".</span><span class="sxs-lookup"><span data-stu-id="e6267-168">The registration code for that file is in dlldata.cpp.</span></span> <span data-ttu-id="e6267-169">Die Makro- **dlldata- \_ Routinen** werden so erweitert, dass Sie eine Implementierung von **DllRegisterServer** enthalten.</span><span class="sxs-lookup"><span data-stu-id="e6267-169">The macro **DLLDATA\_ROUTINES** expands to include an implementation of **DllRegisterServer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6267-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6267-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6267-171">**Übersicht über den DSP-Plug-in-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="e6267-171">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="e6267-172">**Iwmpmediapluginregistrar**</span><span class="sxs-lookup"><span data-stu-id="e6267-172">**IWMPMediaPluginRegistrar**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





