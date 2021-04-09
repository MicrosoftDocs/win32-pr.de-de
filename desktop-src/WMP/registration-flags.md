---
title: Registrierungsflags
description: Registrierungsflags
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Windows Media Player-Plug-ins, Registrierungsflags
- Plug-ins, Registrierungsflags
- Benutzerschnittstellen-Plug-ins, Registrierungsflags
- UI-Plug-ins, Registrierungsflags
- Flags, Benutzerschnittstellen-Plug-ins
- Registrierung, UI-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac609b45866cd5f18edf61dffc2d3b7ac3c397ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038567"
---
# <a name="registration-flags"></a><span data-ttu-id="0e783-109">Registrierungsflags</span><span class="sxs-lookup"><span data-stu-id="0e783-109">Registration Flags</span></span>

<span data-ttu-id="0e783-110">Wenn der Assistent für den Windows Media Player-Plug-in ein neues Plug-in-Projekt für die Benutzeroberfläche erstellt, erstellt er einen Schlüssel in der Registrierung, der Informationen zum Plug-in enthält.</span><span class="sxs-lookup"><span data-stu-id="0e783-110">When the Windows Media Player Plug-in Wizard creates a new UI plug-in project, it creates a key in the registry that contains information about the plug-in.</span></span> <span data-ttu-id="0e783-111">Dieser Schlüssel wird am folgenden Speicherort erstellt:</span><span class="sxs-lookup"><span data-stu-id="0e783-111">This key is created in the following location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



<span data-ttu-id="0e783-112">*ClassID* ist die Klassen-ID des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="0e783-112">*ClassId* is the class id of the plug-in.</span></span>

<span data-ttu-id="0e783-113">Dieser Schlüssel umfasst die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="0e783-113">This key includes the following values.</span></span>



| <span data-ttu-id="0e783-114">Name</span><span class="sxs-lookup"><span data-stu-id="0e783-114">Name</span></span>                     | <span data-ttu-id="0e783-115">type</span><span class="sxs-lookup"><span data-stu-id="0e783-115">Type</span></span>       | <span data-ttu-id="0e783-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e783-116">Description</span></span>                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e783-117">Funktionen</span><span class="sxs-lookup"><span data-stu-id="0e783-117">Capabilities</span></span>             | <span data-ttu-id="0e783-118">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="0e783-118">REG\_DWORD</span></span> | <span data-ttu-id="0e783-119">Ein DWORD-Wert, der aus mindestens einem Plug-in-Typflag besteht, das mit einem oder mehreren Plug-in-Funktionen-Flags mithilfe von binären-oder-Vorgängen kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0e783-119">A DWORD value that consists of at least one plug-in type flag that may be combined with one or more plug-in capabilities flags by using binary OR operations.</span></span>                             |
| <span data-ttu-id="0e783-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e783-120">Description</span></span>              | <span data-ttu-id="0e783-121">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="0e783-121">REG\_SZ</span></span>    | <span data-ttu-id="0e783-122">Eine Zeichenfolge, die die Beschreibung des Plug-Ins enthält.</span><span class="sxs-lookup"><span data-stu-id="0e783-122">A string that contains the description of the plug-in.</span></span> <span data-ttu-id="0e783-123">Der Plug-in-Assistent erstellt eine Zeichen folgen Ressource und stellt die URL der Ressource (mit dem res-Protokoll) für diesen Wert bereit.</span><span class="sxs-lookup"><span data-stu-id="0e783-123">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span>         |
| <span data-ttu-id="0e783-124">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0e783-124">FriendlyName</span></span>             | <span data-ttu-id="0e783-125">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="0e783-125">REG\_SZ</span></span>    | <span data-ttu-id="0e783-126">Eine Zeichenfolge, die den vom Benutzer lesbaren Namen für das Plug-in enthält.</span><span class="sxs-lookup"><span data-stu-id="0e783-126">A string that contains the user-readable name for the plug-in.</span></span> <span data-ttu-id="0e783-127">Der Plug-in-Assistent erstellt eine Zeichen folgen Ressource und stellt die URL der Ressource (mit dem res-Protokoll) für diesen Wert bereit.</span><span class="sxs-lookup"><span data-stu-id="0e783-127">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span> |
| <span data-ttu-id="0e783-128">Uninstallpath (optional)</span><span class="sxs-lookup"><span data-stu-id="0e783-128">UninstallPath (optional)</span></span> | <span data-ttu-id="0e783-129">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="0e783-129">REG\_SZ</span></span>    | <span data-ttu-id="0e783-130">Eine Zeichenfolge, die den Pfad zu einer ausführbaren Datei enthält, die das Plug-in deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="0e783-130">A string that contains the path to an executable file that uninstalls the plug-in.</span></span>                                                                                                        |



 

<span data-ttu-id="0e783-131">Weitere Informationen zum res-Protokoll finden Sie unter Internet Development SDK.</span><span class="sxs-lookup"><span data-stu-id="0e783-131">For more information about the res protocol, see the Internet Development SDK.</span></span>

<span data-ttu-id="0e783-132">In der folgenden Tabelle werden die Plug-in-typanflags ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="0e783-132">The following table details the plug-in type flags.</span></span>



| <span data-ttu-id="0e783-133">Plug-in-Typ-Flag</span><span class="sxs-lookup"><span data-stu-id="0e783-133">Plug-in Type Flag</span></span>                | <span data-ttu-id="0e783-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0e783-134">Value</span></span> | <span data-ttu-id="0e783-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e783-135">Description</span></span>                                       |
|----------------------------------|-------|---------------------------------------------------|
| <span data-ttu-id="0e783-136">**Hintergrund des Plug-Ins \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0e783-136">**PLUGIN\_TYPE\_BACKGROUND**</span></span>     | <span data-ttu-id="0e783-137">0x1</span><span class="sxs-lookup"><span data-stu-id="0e783-137">0x1</span></span>   | <span data-ttu-id="0e783-138">Im UI-Plug-in wird keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e783-138">The UI plug-in does not display a user interface.</span></span> |
| <span data-ttu-id="0e783-139">**Plug-in- \_ Typ \_ trennfenster**</span><span class="sxs-lookup"><span data-stu-id="0e783-139">**PLUGIN\_TYPE\_SEPARATEWINDOW**</span></span> | <span data-ttu-id="0e783-140">0x2</span><span class="sxs-lookup"><span data-stu-id="0e783-140">0x2</span></span>   | <span data-ttu-id="0e783-141">Das UI-Plug-in ist ein separates Fenster-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="0e783-141">The UI plug-in is a separate window plug-in.</span></span>      |
| <span data-ttu-id="0e783-142">**Anzeigebereich des Plug-Ins \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0e783-142">**PLUGIN\_TYPE\_DISPLAYAREA**</span></span>    | <span data-ttu-id="0e783-143">0x3</span><span class="sxs-lookup"><span data-stu-id="0e783-143">0x3</span></span>   | <span data-ttu-id="0e783-144">Das UI-Plug-in ist ein Anzeige Bereichs-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="0e783-144">The UI plug-in is a display area plug-in.</span></span>         |
| <span data-ttu-id="0e783-145">**Einstellungsart des Plug-Ins \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0e783-145">**PLUGIN\_TYPE\_SETTINGSAREA**</span></span>   | <span data-ttu-id="0e783-146">0x4</span><span class="sxs-lookup"><span data-stu-id="0e783-146">0x4</span></span>   | <span data-ttu-id="0e783-147">Das UI-Plug-in ist ein Einstellungsbereich-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="0e783-147">The UI plug-in is a settings area plug-in.</span></span>        |
| <span data-ttu-id="0e783-148">**Plug-in- \_ \_ METADATAAREA**</span><span class="sxs-lookup"><span data-stu-id="0e783-148">**PLUGIN\_TYPE\_METADATAAREA**</span></span>   | <span data-ttu-id="0e783-149">0x5</span><span class="sxs-lookup"><span data-stu-id="0e783-149">0x5</span></span>   | <span data-ttu-id="0e783-150">Das UI-Plug-in ist ein Metadatenbereich-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="0e783-150">The UI plug-in is a metadata area plug-in.</span></span>        |



 

<span data-ttu-id="0e783-151">In der folgenden Tabelle werden die Flags für Plug-in-Funktionen erläutert.</span><span class="sxs-lookup"><span data-stu-id="0e783-151">The following table details the plug-in capabilities flags.</span></span>



| <span data-ttu-id="0e783-152">Flag für Plug-in-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0e783-152">Plug-in Capabilities Flag</span></span>             | <span data-ttu-id="0e783-153">Wert</span><span class="sxs-lookup"><span data-stu-id="0e783-153">Value</span></span>      | <span data-ttu-id="0e783-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e783-154">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e783-155">**Plug-in- \_ Flags- \_ Annahmen**</span><span class="sxs-lookup"><span data-stu-id="0e783-155">**PLUGIN\_FLAGS\_ACCEPTSMEDIA**</span></span>       | <span data-ttu-id="0e783-156">0x10000000</span><span class="sxs-lookup"><span data-stu-id="0e783-156">0x10000000</span></span> | <span data-ttu-id="0e783-157">Das UI-Plug-in kann **Medien** Objekt-Zeiger Arrays akzeptieren, wenn Windows Media Player " [**iwmppluginui:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) " aufruft.</span><span class="sxs-lookup"><span data-stu-id="0e783-157">The UI plug-in can accept **Media** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="0e783-158">**Plug-in- \_ Flags " \_ akzeptsplaylists"**</span><span class="sxs-lookup"><span data-stu-id="0e783-158">**PLUGIN\_FLAGS\_ACCEPTSPLAYLISTS**</span></span>   | <span data-ttu-id="0e783-159">0x8000000</span><span class="sxs-lookup"><span data-stu-id="0e783-159">0x8000000</span></span>  | <span data-ttu-id="0e783-160">Das UI-Plug-in kann **Listen Objekt-** Zeiger Arrays akzeptieren, wenn Windows Media Player " [**iwmppluginui:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) " aufruft.</span><span class="sxs-lookup"><span data-stu-id="0e783-160">The UI plug-in can accept **Playlist** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="0e783-161">**Plug-Ins für Plug-Ins \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0e783-161">**PLUGIN\_FLAGS\_HASPRESETS**</span></span>         | <span data-ttu-id="0e783-162">0x4000000</span><span class="sxs-lookup"><span data-stu-id="0e783-162">0x4000000</span></span>  | <span data-ttu-id="0e783-163">Das UI-Plug-in verwendet Voreinstellungen.</span><span class="sxs-lookup"><span data-stu-id="0e783-163">The UI plug-in uses presets.</span></span> <span data-ttu-id="0e783-164">Wenn das Plug-in dieses Flag angibt, fragt Windows Media Player das Plug-in nach voreingestellten Informationen ab, indem [**iwmppluginui:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0e783-164">If the plug-in specifies this flag, Windows Media Player will query the plug-in for preset information by calling [**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="0e783-165">**Plug-in- \_ Flags \_ haspropertypage**</span><span class="sxs-lookup"><span data-stu-id="0e783-165">**PLUGIN\_FLAGS\_HASPROPERTYPAGE**</span></span>    | <span data-ttu-id="0e783-166">0x80000000</span><span class="sxs-lookup"><span data-stu-id="0e783-166">0x80000000</span></span> | <span data-ttu-id="0e783-167">Das UI-Plug-in enthält ein Dialogfeld für eine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="0e783-167">The UI plug-in provides a property page dialog.</span></span> <span data-ttu-id="0e783-168">Windows Media Player ruft [**iwmppluginui::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) auf, wenn dieses Flag festgelegt wird, wenn die Eigenschaften Seite aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0e783-168">Windows Media Player will call [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) if this flag is set when the property page is invoked.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="0e783-169">**\_ \_ ausgeblendet**</span><span class="sxs-lookup"><span data-stu-id="0e783-169">**PLUGIN\_FLAGS\_HIDDEN**</span></span>             | <span data-ttu-id="0e783-170">0x02000000</span><span class="sxs-lookup"><span data-stu-id="0e783-170">0x02000000</span></span> | <span data-ttu-id="0e783-171">Das Plug-in für die Benutzeroberfläche für die Benutzeroberfläche wird nicht im Menü **Plug-ins** angezeigt, auf das Sie über die Menüs **Ansicht** oder **Tools** oder die Schaltfläche **jetzt Wiedergabe Optionen auswählen** in der Wiedergabeliste zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0e783-171">The background UI plug-in does not appear on the **Plug-ins** menu that is accessed from the **View** or **Tools** menus or the **Select Now Playing options** button in Now Playing.</span></span> <span data-ttu-id="0e783-172">Er wird im Dialogfeld Optionen auf der Registerkarte **Plug-ins** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e783-172">It does appear on the **Plug-ins** tab of the Options dialog.</span></span> <span data-ttu-id="0e783-173">Dies bewirkt, dass das Plug-in für die Hintergrund Ausführung in der Statusleiste angezeigt wird. Dieses Flag hat keine Auswirkung auf Plug-ins, die keine background-UI-Plug-ins sind.</span><span class="sxs-lookup"><span data-stu-id="0e783-173">It does cause the Background Plug-in Running icon to appear in the status bar.This flag has no effect on plug-ins other than background UI plug-ins.</span></span><br/> |
| <span data-ttu-id="0e783-174">**Plug \_ \_ -in-Flags installautorun**</span><span class="sxs-lookup"><span data-stu-id="0e783-174">**PLUGIN\_FLAGS\_INSTALLAUTORUN**</span></span>     | <span data-ttu-id="0e783-175">0x40000000</span><span class="sxs-lookup"><span data-stu-id="0e783-175">0x40000000</span></span> | <span data-ttu-id="0e783-176">Windows Media Player führt das UI-Plug-in automatisch aus, wenn das Plug-in installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0e783-176">Windows Media Player runs the UI plug-in automatically when the plug-in is installed.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="0e783-177">**Plug-in- \_ Flags \_ launchpropertypage**</span><span class="sxs-lookup"><span data-stu-id="0e783-177">**PLUGIN\_FLAGS\_LAUNCHPROPERTYPAGE**</span></span> | <span data-ttu-id="0e783-178">0x20000000</span><span class="sxs-lookup"><span data-stu-id="0e783-178">0x20000000</span></span> | <span data-ttu-id="0e783-179">Windows Media Player ruft [**iwmppluginui::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) auf, wenn das UI-Plug-in zum ersten Mal ausgeführt wird. Wenn dieses Flag angegeben ist, sollten die Plug-in- **\_ Flags \_ haspropertypage** ebenfalls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e783-179">Windows Media Player calls [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) when the UI plug-in runs for the first time.If this flag is specified, **PLUGIN\_FLAGS\_HASPROPERTYPAGE** should be specified also.</span></span><br/>                                                                                                                                                             |



 

<span data-ttu-id="0e783-180">Die folgenden Konstanten sind in wmpplug. h definiert.</span><span class="sxs-lookup"><span data-stu-id="0e783-180">The following constants are defined in wmpplug.h.</span></span> <span data-ttu-id="0e783-181">Ändern Sie nicht die Werte, die diesen Konstanten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0e783-181">Do not change the values associated with these constants.</span></span>



| <span data-ttu-id="0e783-182">Name</span><span class="sxs-lookup"><span data-stu-id="0e783-182">Name</span></span>                                    | <span data-ttu-id="0e783-183">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e783-183">Description</span></span>                               |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="0e783-184">**Plug-in- \_ installregkey**</span><span class="sxs-lookup"><span data-stu-id="0e783-184">**PLUGIN\_INSTALLREGKEY**</span></span>               | <span data-ttu-id="0e783-185">Der Speicherort des Plug-in-Registrierungsschlüssels.</span><span class="sxs-lookup"><span data-stu-id="0e783-185">The location of the plug-in registry key.</span></span> |
| <span data-ttu-id="0e783-186">**Plug-in \_ installregkey \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="0e783-186">**PLUGIN\_INSTALLREGKEY\_FRIENDLYNAME**</span></span> | <span data-ttu-id="0e783-187">Der Name des benutzerfreundlichen namens Werts.</span><span class="sxs-lookup"><span data-stu-id="0e783-187">The name of the friendly name value.</span></span>      |
| <span data-ttu-id="0e783-188">**Plug-in- \_ installregkey \_**</span><span class="sxs-lookup"><span data-stu-id="0e783-188">**PLUGIN\_INSTALLREGKEY\_DESCRIPTION**</span></span>  | <span data-ttu-id="0e783-189">Der Name des Beschreibungs Werts.</span><span class="sxs-lookup"><span data-stu-id="0e783-189">The name of the description value.</span></span>        |
| <span data-ttu-id="0e783-190">**installregkey-Plug-in \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0e783-190">**PLUGIN\_INSTALLREGKEY\_CAPABILITIES**</span></span> | <span data-ttu-id="0e783-191">Der Name des Funktions Werts.</span><span class="sxs-lookup"><span data-stu-id="0e783-191">The name of the capabilities value.</span></span>       |
| <span data-ttu-id="0e783-192">**Plug-in \_ installregkey \_ deinstallieren**</span><span class="sxs-lookup"><span data-stu-id="0e783-192">**PLUGIN\_INSTALLREGKEY\_UNINSTALL**</span></span>    | <span data-ttu-id="0e783-193">Der Name des Deinstallations Pfad Werts.</span><span class="sxs-lookup"><span data-stu-id="0e783-193">The name of the uninstall path value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="0e783-194">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e783-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e783-195">**Iwmppluginui::D isplaypropertypage**</span><span class="sxs-lookup"><span data-stu-id="0e783-195">**IWMPPluginUI::DisplayPropertyPage**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[<span data-ttu-id="0e783-196">**Iwmppluginui:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="0e783-196">**IWMPPluginUI::GetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[<span data-ttu-id="0e783-197">**Iwmppluginui:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="0e783-197">**IWMPPluginUI::SetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[<span data-ttu-id="0e783-198">**Programmier Referenz zu Benutzeroberflächen-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="0e783-198">**User Interface Plug-ins Programming Reference**</span></span>](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





