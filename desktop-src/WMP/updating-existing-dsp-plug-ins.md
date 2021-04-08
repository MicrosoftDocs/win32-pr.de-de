---
title: Aktualisieren vorhandener DSP-Plug-ins
description: Aktualisieren vorhandener DSP-Plug-ins
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Windows Media Player-Plug-ins, digitale Signalverarbeitung (DSP)
- Plug-ins, digitale Signalverarbeitung (DSP)
- Plug-Ins für die digitale Signalverarbeitung, aktualisieren
- DSP-Plug-ins, aktualisieren
- Versionen von Windows Media Player, DSP-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393cde356e0d86bb920825e731bb12ee0b7c2818
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723472"
---
# <a name="updating-existing-dsp-plug-ins"></a><span data-ttu-id="18bb7-108">Aktualisieren vorhandener DSP-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="18bb7-108">Updating Existing DSP Plug-ins</span></span>

<span data-ttu-id="18bb7-109">DSP-Plug-ins, die vor der Veröffentlichung des Windows Media Player 11 SDK erstellt wurden, funktionieren möglicherweise nicht erwartungsgemäß, wenn Windows Media Player 11 unter Windows Vista ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18bb7-109">DSP plug-ins created before the release of the Windows Media Player 11 SDK might not work as expected with Windows Media Player 11 running on Windows Vista.</span></span> <span data-ttu-id="18bb7-110">Um sicherzustellen, dass Kunden, die Windows Media Player 11 unter Windows Vista ausführen, die Plug-Ins verwenden können, müssen Sie einige Änderungen an Ihrem DSP-Plug-in-Code vornehmen, das Projekt neu kompilieren und das aktualisierte Plug-in an Ihre Kunden verteilen.</span><span class="sxs-lookup"><span data-stu-id="18bb7-110">To ensure that customers who run Windows Media Player 11 on Windows Vista can use your plug-ins, you must make some changes to your DSP plug-in code, recompile your project, and distribute the updated plug-in to your customers.</span></span>

<span data-ttu-id="18bb7-111">Projekte, die mit der neuesten Version des Assistenten für Windows Media Player-Plug-Ins erstellt werden, enthalten die erforderlichen Updates.</span><span class="sxs-lookup"><span data-stu-id="18bb7-111">Projects created using the latest version of the Windows Media Player plug-in wizard will contain the required updates.</span></span> <span data-ttu-id="18bb7-112">Weitere [Informationen finden Sie unter Updates für den DSP-Plug-in-Assistenten für Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="18bb7-112">See [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span> <span data-ttu-id="18bb7-113">(Es empfiehlt sich, den Assistenten auszuführen, um ein neues Beispiel Projekt zu erstellen und dann ein Tool wie Windiff.exe zu verwenden, das in Visual Studio zur Verfügung steht, um die Unterschiede zwischen dem Beispielcode und dem Produktionscode zu untersuchen.)</span><span class="sxs-lookup"><span data-stu-id="18bb7-113">(It is a good idea to run the wizard to create a new sample project and then use a tool like Windiff.exe, which comes with Visual Studio, to inspect the differences between the sample code and your production code.)</span></span>

<span data-ttu-id="18bb7-114">An allen vorhandenen DSP-Plug-Ins müssen Sie drei wesentliche Änderungen vornehmen:</span><span class="sxs-lookup"><span data-stu-id="18bb7-114">There are three main changes you will need to make to any existing DSP plug-ins:</span></span>

-   <span data-ttu-id="18bb7-115">Ändern der Art und Weise, wie das Plug-in registriert wird.</span><span class="sxs-lookup"><span data-stu-id="18bb7-115">Change the way the plug-in registers.</span></span> <span data-ttu-id="18bb7-116">Ihr vorhandenes Plug-in registriert das Threading Modell wahrscheinlich als "Apartment".</span><span class="sxs-lookup"><span data-stu-id="18bb7-116">Your existing plug-in probably registers the threading model as "Apartment".</span></span> <span data-ttu-id="18bb7-117">Windows Media Player 11 unter Windows Vista erfordert, dass DSP-Plug-ins das Threading Modell als "beides" registrieren.</span><span class="sxs-lookup"><span data-stu-id="18bb7-117">Windows Media Player 11 running on Windows Vista requires that DSP plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="18bb7-118">Sie können dieses Problem beheben, indem Sie den Threading Modell Wert in der Datei " *ProjectName*. RGS" wie folgt ändern:</span><span class="sxs-lookup"><span data-stu-id="18bb7-118">You can fix this by changing the threading model value in your *projectname*.rgs file, as follows:</span></span>

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > <span data-ttu-id="18bb7-119">Durch Angeben des Threading Modells als "both" wird jede Serialisierung entfernt, die com für Aufrufe von benutzerdefinierten Schnittstellen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="18bb7-119">Specifying the threading model as "Both" removes any serialization that COM provides for calls to custom interfaces.</span></span> <span data-ttu-id="18bb7-120">Wenn Sie benutzerdefinierte Schnittstellen aus mehreren Threads aufrufen, müssen Sie diese Serialisierung selbst bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="18bb7-120">If you make calls to your custom interfaces from multiple threads, you must provide this serialization yourself.</span></span>

     

    <span data-ttu-id="18bb7-121">Windows Media Player 11 stellt sicher, dass Aufrufe der DMO-Schnittstellen ordnungsgemäß serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="18bb7-121">Windows Media Player 11 ensures that calls to DMO interfaces are properly serialized.</span></span>

    1.  <span data-ttu-id="18bb7-122">Fügen Sie die folgenden Befehle hinzu [: wmpregisterplayerplayerplayerplayerplayerplayerplayerplayerplayerplayerplug](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) -in mit einem neuen Plug-in-Typ: [](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) WMP \_ PlugInType \_ DSP \_ oudeberproc in DllRegisterServer und DllUnregisterServer in der Datei *projectnamedll*. cpp.</span><span class="sxs-lookup"><span data-stu-id="18bb7-122">Add calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC in DllRegisterServer and DllUnregisterServer in your *projectnamedll*.cpp file.</span></span> <span data-ttu-id="18bb7-123">Weitere Informationen finden Sie auf den Referenzseiten für diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="18bb7-123">See the reference pages for these methods for details.</span></span>
    2.  <span data-ttu-id="18bb7-124">Erstellen und verteilen Sie eine Proxy-/Stub-DLL, um das COM-Marshalling einer beliebigen benutzerdefinierten Schnittstelle zu ermöglichen, die von der Plug-in-Klasse implementiert oder erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="18bb7-124">Create and distribute a proxy/stub DLL to enable COM marshaling of any custom interface implemented on or created by the plug-in class.</span></span> <span data-ttu-id="18bb7-125">Eine benutzerdefinierte Schnittstelle ist eine beliebige proprietäre Schnittstelle, die Sie für die Verwendung durch das Plug-in-Objekt definieren und implementieren.</span><span class="sxs-lookup"><span data-stu-id="18bb7-125">A custom interface is any proprietary interface that you define and implement for use by the plug-in object.</span></span> <span data-ttu-id="18bb7-126">Dies schließt die benutzerdefinierte Schnittstelle ein, die von der Eigenschaften Seite verwendet wird, wenn Sie eine solche bereitgestellt haben, kann jedoch auch Schnittstellen enthalten, die eine Verbindung mit Benutzeroberflächen-Plug-ins herstellen</span><span class="sxs-lookup"><span data-stu-id="18bb7-126">This includes the custom interface used by your property page, if you provided one, but might also include interfaces that connect to UI plug-ins, for example.</span></span> <span data-ttu-id="18bb7-127">Ein Beispiel für eine benutzerdefinierte Schnittstelle, die vom Plug-in-Assistenten erstellt wurde, ist *iprojectname*.</span><span class="sxs-lookup"><span data-stu-id="18bb7-127">An example of a custom interface created by the plug-in wizard is *Iprojectname*.</span></span> <span data-ttu-id="18bb7-128">Beispiele für Schnittstellen, die keine benutzerdefinierten Schnittstellen sind, sind **imediaobject** und **iwmppluginenable**.</span><span class="sxs-lookup"><span data-stu-id="18bb7-128">Examples of interfaces that are not custom interfaces include **IMediaObject** and **IWMPPluginEnable**.</span></span>

<span data-ttu-id="18bb7-129">Wenn Ihr DSP-Plug-in Audioprozesse verarbeitet, müssen Sie auch Unterstützung für die folgenden neuen Audioformate hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="18bb7-129">If your DSP plug-in processes audio, you must also add support for the following new audio formats:</span></span>

-   <span data-ttu-id="18bb7-130">"Wave \_ Format \_ IEEE \_ float"</span><span class="sxs-lookup"><span data-stu-id="18bb7-130">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
-   <span data-ttu-id="18bb7-131">Das Wave- \_ Format ist \_ erweiterbar mit dem unter Format "ksdataformat"- \_ Untertyp \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="18bb7-131">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

<span data-ttu-id="18bb7-132">Wenn Ihr DSP-Plug-in Video verarbeitet, müssen Sie Unterstützung für das NV12-Videoformat hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="18bb7-132">If your DSP plug-in processes video, you must add support for the NV12 video format.</span></span>

<span data-ttu-id="18bb7-133">Ein Beispiel für die Verarbeitung dieser Format Typen finden Sie im Beispiel für das Audio-oder Video DSP-Plug-in, das vom Assistenten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="18bb7-133">See the sample audio or video DSP plug-in that the wizard creates for an example of how to process these format types.</span></span>

## <a name="about-the-proxystub-project"></a><span data-ttu-id="18bb7-134">Informationen zum Proxy-/Stubprojekt</span><span class="sxs-lookup"><span data-stu-id="18bb7-134">About the Proxy/Stub Project</span></span>

<span data-ttu-id="18bb7-135">Möglicherweise ist die einfachste Möglichkeit, ein Proxy-/Stub-DLL-Projekt für Ihr DSP-Plug-in zu erstellen, den DSP-Plug-in-Assistenten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="18bb7-135">Perhaps the simplest way to create a proxy/stub DLL project for your DSP plug-in is to run the DSP plug-in wizard.</span></span> <span data-ttu-id="18bb7-136">Dadurch wird ein Beispiel für ein Proxy-/Stubprojekt erstellt, das Sie ändern können, um mit vorhandenem Code zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="18bb7-136">This will create a sample proxy/stub project that you can modify to work with your existing code.</span></span> <span data-ttu-id="18bb7-137">Sie müssen die folgenden Änderungen vornehmen:</span><span class="sxs-lookup"><span data-stu-id="18bb7-137">You will need to make the following changes:</span></span>

1.  <span data-ttu-id="18bb7-138">Entfernen Sie alle vorhandenen Definitionen für Ihre benutzerdefinierten Schnittstellen aus Ihrem Code.</span><span class="sxs-lookup"><span data-stu-id="18bb7-138">Remove any existing definitions for your custom interfaces from your code.</span></span> <span data-ttu-id="18bb7-139">Der DSP-Plug-in-Assistent aus dem Windows Media Player 10 SDK hat z. b. die *iprojectname* -Schnittstellen Definition in der Datei " *ProjectName*. h" mithilfe des Schlüssel Worts " **Interface** " erstellt.</span><span class="sxs-lookup"><span data-stu-id="18bb7-139">For example, the DSP plug-in wizard from the Windows Media Player 10 SDK created the *Iprojectname* interface definition in the *projectname*.h file by using the **interface** keyword.</span></span>
2.  <span data-ttu-id="18bb7-140">Definieren Sie die benutzerdefinierten Schnittstellen in der IDL-Datei des Proxy-/stubprojekts.</span><span class="sxs-lookup"><span data-stu-id="18bb7-140">Define your custom interfaces in the proxy/stub project's IDL file.</span></span>
3.  <span data-ttu-id="18bb7-141">Erstellen Sie das Proxy-/Stubprojekt vor dem Hauptprojekt.</span><span class="sxs-lookup"><span data-stu-id="18bb7-141">Build the proxy/stub project before your main project.</span></span> <span data-ttu-id="18bb7-142">Sie können Visual Studio so konfigurieren, dass dies automatisch geschieht, wenn beide Projekte Teil derselben Projekt Mappe sind.</span><span class="sxs-lookup"><span data-stu-id="18bb7-142">You can configure Visual Studio to do this automatically if both projects are part of the same solution.</span></span>
4.  <span data-ttu-id="18bb7-143">Der mittlerer l-Compiler erstellt eine neue Header Datei mit einem Namen im Format *ProjectName* \_ h.h.</span><span class="sxs-lookup"><span data-stu-id="18bb7-143">The MIDL compiler will create a new header file having a name in the format *projectname*\_h.h.</span></span> <span data-ttu-id="18bb7-144">Sie müssen diesen Header in das Hauptprojekt (in *ProjectName*. h) einschließen.</span><span class="sxs-lookup"><span data-stu-id="18bb7-144">You must include this header in your main project (in *projectname*.h).</span></span> <span data-ttu-id="18bb7-145">Sie enthält die Definitionen für Ihre benutzerdefinierten Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="18bb7-145">It contains the definitions for your custom interfaces.</span></span>

## <a name="distributing-the-updated-plug-in"></a><span data-ttu-id="18bb7-146">Das aktualisierte Plug-in wird verteilt.</span><span class="sxs-lookup"><span data-stu-id="18bb7-146">Distributing the Updated Plug-in</span></span>

<span data-ttu-id="18bb7-147">Sie können das aktualisierte Plug-in genau so wie in der Vergangenheit auf den Computern Ihrer Benutzer installieren.</span><span class="sxs-lookup"><span data-stu-id="18bb7-147">You can install the updated plug-in on your users' computers exactly as you have in the past.</span></span> <span data-ttu-id="18bb7-148">Sie müssen jetzt jedoch auch die Proxy-/Stub-DLL verteilen und registrieren.</span><span class="sxs-lookup"><span data-stu-id="18bb7-148">However, you must now also distribute and register the proxy/stub DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18bb7-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18bb7-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18bb7-150">**Übersicht über den DSP-Plug-in-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="18bb7-150">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




