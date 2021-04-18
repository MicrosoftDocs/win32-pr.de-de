---
title: Easy of Access-hilfstechnologieregistrierung
description: In diesem Artikel wird erläutert, wie Sie eine Barrierefreiheits Anwendung mit dem Easy Access Center registrieren. Außerdem wird erläutert, wie Sie Ihre Barrierefreiheits Anwendung so anpassen, dass Sie gut mit dem sicheren Desktop funktioniert.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 66901cd899fc578b032f86e3752fcdcac0788ba1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339287"
---
# <a name="ease-of-access---assistive-technology-registration"></a><span data-ttu-id="cf937-104">Easy of Access-hilfstechnologieregistrierung</span><span class="sxs-lookup"><span data-stu-id="cf937-104">Ease of Access   Assistive Technology Registration</span></span>

<span data-ttu-id="cf937-105">In diesem Artikel wird erläutert, wie Sie eine Barrierefreiheits Anwendung mit dem Easy Access Center registrieren.</span><span class="sxs-lookup"><span data-stu-id="cf937-105">This article explains how to register an accessibility application with the Ease of Access Center.</span></span> <span data-ttu-id="cf937-106">Außerdem wird erläutert, wie Sie Ihre Barrierefreiheits Anwendung so anpassen, dass Sie gut mit dem sicheren Desktop funktioniert.</span><span class="sxs-lookup"><span data-stu-id="cf937-106">It also explains how to tailor your accessibility application so it works well with the secure desktop.</span></span>

<span data-ttu-id="cf937-107">Das Easy of Access Center ist eine System Steuerungsanwendung für Microsoft Windows, die Funktionen für Barrierefreiheit und Benutzerfreundlichkeit vereint.</span><span class="sxs-lookup"><span data-stu-id="cf937-107">The Ease of Access Center is a Control Panel application for Microsoft Windows brings together functionality for accessibility and ease of use.</span></span> <span data-ttu-id="cf937-108">Mithilfe des Easy Access Centers können Benutzer ihre Computer so konfigurieren, dass Sie Ihren physischen und kognitiven Anforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cf937-108">By using the Ease of Access Center, users can configure their computers to suit their physical and cognitive needs.</span></span>

<span data-ttu-id="cf937-109">Eine Funktion des Easy Access Centers besteht darin, Benutzern das Starten von Barrierefreiheits Anwendungen zu erleichtern, einschließlich Sprachausgabe, Bildschirmtastatur und Bildschirmlupe.</span><span class="sxs-lookup"><span data-stu-id="cf937-109">One function of the Ease of Access Center is to help users launch accessibility applications, including Narrator, On-Screen Keyboard, and Magnifier.</span></span> <span data-ttu-id="cf937-110">Registrierte Anwendungen von Drittanbietern werden auch im Easy Access Center angezeigt und können direkt von dort aus gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="cf937-110">Registered third-party applications also appear in the Ease of Access Center and can be launched directly from there.</span></span>

<span data-ttu-id="cf937-111">Barrierefreiheits Anwendungen müssen problemlos mit dem sicheren Desktop arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cf937-111">Accessibility applications need to work smoothly with the secure desktop.</span></span> <span data-ttu-id="cf937-112">Der sichere Desktop ist die Benutzeroberfläche, die angezeigt wird, wenn der Computer gesperrt ist (bei der Anmeldung oder wenn der Benutzer den Desktop gesperrt hat), und wenn der Benutzer aufgefordert wird, eine potenziell unsichere Aktion zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="cf937-112">The secure desktop is the user interface that appears when the computer is locked (at log-on or when the user has locked the desktop), and when the user is prompted to allow a potentially unsafe action.</span></span> <span data-ttu-id="cf937-113">Aus Sicherheitsgründen werden von Windows Grenzwerte für Software von Drittanbietern auf dem sicheren Desktop platziert.</span><span class="sxs-lookup"><span data-stu-id="cf937-113">For security reasons, Windows places limits on third-party software running on the secure desktop.</span></span> <span data-ttu-id="cf937-114">Wenn Sie möchten, dass Ihre Barrierefreiheits Anwendung auf dem sicheren Desktop ausgeführt wird, müssen Sie die Anwendung mit dem Easy Access Center registrieren.</span><span class="sxs-lookup"><span data-stu-id="cf937-114">If you want your accessibility application to run on the secure desktop, you need to register the application with the Ease of Access Center.</span></span>

## <a name="registering-with-the-ease-of-access-center"></a><span data-ttu-id="cf937-115">Registrierung mit dem Easy Access Center</span><span class="sxs-lookup"><span data-stu-id="cf937-115">Registering with the Ease of Access Center</span></span>

<span data-ttu-id="cf937-116">Barrierefreiheits Anwendungen registrieren sich mit dem Easy of Access Center, indem bei der Installation der Anwendung mindestens ein Registrierungsschlüssel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-116">Accessibility applications register with the Ease of Access Center by creating one or more registry keys when the application is installed.</span></span> <span data-ttu-id="cf937-117">In der folgenden Tabelle sind die Informationen aufgeführt, die in den Registrierungs Schlüsseln enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cf937-117">The following table lists the information contained in the registry keys.</span></span>



| <span data-ttu-id="cf937-118">Name</span><span class="sxs-lookup"><span data-stu-id="cf937-118">Name</span></span>                        | <span data-ttu-id="cf937-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf937-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="cf937-120">Obligatorisch/Optional</span><span class="sxs-lookup"><span data-stu-id="cf937-120">Mandatory/Optional</span></span> | <span data-ttu-id="cf937-121">Sprache</span><span class="sxs-lookup"><span data-stu-id="cf937-121">Language</span></span>      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| <span data-ttu-id="cf937-122">Anwendungsname</span><span class="sxs-lookup"><span data-stu-id="cf937-122">Application Name</span></span>            | <span data-ttu-id="cf937-123">Der Name der Anwendung in einer Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="cf937-123">The name of the application, which is in a resource file.</span></span> <span data-ttu-id="cf937-124">Dieser Registrierungs Wert enthält eine Zeichenfolge in einem angegebenen Format.</span><span class="sxs-lookup"><span data-stu-id="cf937-124">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="cf937-125">Dies könnte eine lokalisierte Version des Anwendungs namens sein, wenn die Anwendung in anderen Sprachen als Englisch lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-125">This could be a localized version of the application name, if the application is localized in languages other than English.</span></span> <span data-ttu-id="cf937-126">Der Name wird im Easy Access Center angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf937-126">The name appears in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="cf937-127">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cf937-127">Mandatory</span></span>          | <span data-ttu-id="cf937-128">Ertem</span><span class="sxs-lookup"><span data-stu-id="cf937-128">Localized</span></span>     |
| <span data-ttu-id="cf937-129">ATEXE</span><span class="sxs-lookup"><span data-stu-id="cf937-129">ATExe</span></span>                       | <span data-ttu-id="cf937-130">Der Name der ausführbaren Datei der Anwendung oder des Images.</span><span class="sxs-lookup"><span data-stu-id="cf937-130">The name of the application executable file or image.</span></span> <span data-ttu-id="cf937-131">Windows verwendet diesen Wert, um zu bestimmen, ob die Barrierefreiheits Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-131">Windows uses this value to determine whether the accessibility application is running.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="cf937-132">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cf937-132">Mandatory</span></span>          | <span data-ttu-id="cf937-133">Nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="cf937-133">Not localized</span></span> |
| <span data-ttu-id="cf937-134">Copysettingstolockeddesktop</span><span class="sxs-lookup"><span data-stu-id="cf937-134">CopySettingsToLockedDesktop</span></span> | <span data-ttu-id="cf937-135">Ein **DWORD** -Wert, der angibt, ob die Einstellungen der Barrierefreiheits Anwendung auf den gesperrten Desktop kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cf937-135">A **DWORD** value that indicates whether to copy the accessibility application's settings to the locked desktop.</span></span><br/> <span data-ttu-id="cf937-136">Wenn dieser Wert 1 ist, kann die Anwendung Einstellungen in einen Speicherort in der Benutzerregistrierung schreiben, und Windows kopiert die Einstellungen an denselben Speicherort in der Benutzerregistrierung für den gesperrten Desktop.</span><span class="sxs-lookup"><span data-stu-id="cf937-136">If this value is 1, the application can write settings to a location in the user registry, and Windows copies the settings to the same location in the user registry for the locked desktop.</span></span> <span data-ttu-id="cf937-137">Dadurch kann die Anwendung ihren Zustand vom "normalen" Desktop auf den gesperrten Desktop persistent speichern.</span><span class="sxs-lookup"><span data-stu-id="cf937-137">This enables the application to persist its state from the "normal" desktop to the locked desktop.</span></span><br/>                                                                                                                                                             | <span data-ttu-id="cf937-138">Optional</span><span class="sxs-lookup"><span data-stu-id="cf937-138">Optional</span></span>           | <span data-ttu-id="cf937-139">Nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="cf937-139">Not localized</span></span> |
| <span data-ttu-id="cf937-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf937-140">Description</span></span>                 | <span data-ttu-id="cf937-141">Eine kurze Beschreibung der Anwendung aus einer Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="cf937-141">A brief description of the application, from a resource file.</span></span> <span data-ttu-id="cf937-142">Dieser Registrierungs Wert enthält eine Zeichenfolge in einem angegebenen Format.</span><span class="sxs-lookup"><span data-stu-id="cf937-142">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="cf937-143">Dies könnte eine lokalisierte Version der Beschreibung sein, wenn die Anwendung in anderen Sprachen als Englisch lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-143">This could be a localized version of the description, if the application is localized in languages other than English.</span></span> <span data-ttu-id="cf937-144">Die Länge dieser Zeichenfolge muss weniger als 512 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="cf937-144">The length of this string must be less than 512 characters.</span></span><br/> <span data-ttu-id="cf937-145">Die Beschreibung wird im Easy Access Center angezeigt, um dem Benutzer zusätzliche Informationen zur Barrierefreiheits Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cf937-145">The description appears in the Ease of Access Center to provide additional information about the accessibility application to the user.</span></span><br/> <span data-ttu-id="cf937-146">Dieser Wert kann auch verwendet werden, um den Benutzer darüber zu benachrichtigen, dass die Anwendung nicht auf dem sicheren Desktop verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-146">This value can also be used to notify the user that the application is not used on the secure desktop.</span></span><br/>      | <span data-ttu-id="cf937-147">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cf937-147">Mandatory</span></span>          | <span data-ttu-id="cf937-148">Ertem</span><span class="sxs-lookup"><span data-stu-id="cf937-148">Localized</span></span>     |
| <span data-ttu-id="cf937-149">Profil</span><span class="sxs-lookup"><span data-stu-id="cf937-149">Profile</span></span>                     | <span data-ttu-id="cf937-150">Ein kurzes XML-Element, das die von der Anwendung bereitgestellten Unterbringung angibt.</span><span class="sxs-lookup"><span data-stu-id="cf937-150">A short piece of XML that specifies the accommodations that the application provides.</span></span> <span data-ttu-id="cf937-151">Dadurch wird sichergestellt, dass die Anwendung im Easy of Access Center unter der richtigen Kategorie angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-151">It ensures that the application appears under the correct category in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="cf937-152">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cf937-152">Mandatory</span></span>          | <span data-ttu-id="cf937-153">Nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="cf937-153">Not localized</span></span> |
| <span data-ttu-id="cf937-154">Passiveautostartbehavior</span><span class="sxs-lookup"><span data-stu-id="cf937-154">PassiveAutoStartBehavior</span></span>    | <p><span data-ttu-id="cf937-155">Ein **DWORD** -Wert, der angibt, ob das automatische Startverhalten aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cf937-155">A **DWORD** value that indicates whether legacy auto-start behavior is enabled.</span></span></p><p><span data-ttu-id="cf937-156">Der Standardwert ist 0 (null). Dies bedeutet, dass ein-Wert ein älteres Automatisches Startverhalten erfordert.</span><span class="sxs-lookup"><span data-stu-id="cf937-156">The default value is 0, which indicates that an AT requires legacy auto-start behavior.</span></span> <span data-ttu-id="cf937-157">Dies bewirkt, dass die Einstellung "nach der Anmeldung starten" für diese Option in der Out-of-Box-Umgebung (OOBE) und in der Systemsteuerung aktiviert wird (siehe **Systemsteuerung-> Easy of Access-> Easy of Access Center-> Change Sign-in Settings**) und startet automatisch auf der UAC und dem Sperrbildschirm.</span><span class="sxs-lookup"><span data-stu-id="cf937-157">This  causes the “Start after sign-in” setting for that AT to be checked in the Out Of Box Experience (OOBE) and Control Panel (see **Control Panel -> Ease of Access -> Ease of Access Center -> Change sign-in settings**), and automatically starts the AT after UAC and lock-screen.</span></span></p><p><span data-ttu-id="cf937-158">Der Wert 1 gibt an, dass der at das neue Auto Startverhalten verwenden soll, bei dem die Einstellung "nach der Anmeldung starten" für diese Option nicht im Feld "Out-of-Box-Umgebung" (OOBE) und in der Systemsteuerung aktiviert ist und der at-Vorgang automatisch einmal pro Benutzersitzung (bei der Anmeldung) gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-158">A value of 1 indicates that the AT should use the new auto-start behavior where the “Start after sign-in” setting for that AT is not checked in the Out Of Box Experience (OOBE) and Control Panel, and the AT is automatically started once per user session (at login) only if the “start after sign-in” setting is checked.</span></span></p>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="cf937-159">Optional</span><span class="sxs-lookup"><span data-stu-id="cf937-159">Optional</span></span>          | <span data-ttu-id="cf937-160">Nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="cf937-160">Not localized</span></span> |
| <span data-ttu-id="cf937-161">Securedesktopaccommodation</span><span class="sxs-lookup"><span data-stu-id="cf937-161">SecureDesktopAccommodation</span></span>  | <span data-ttu-id="cf937-162">Der Name einer alternativen Barrierefreiheits Anwendung, die auf dem sicheren Desktop anstelle dieser Anwendung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf937-162">The name of an alternate accessibility application to run on the secure desktop in the place of this application.</span></span> <span data-ttu-id="cf937-163">Die Alternative kann eine andere Anwendung, eine andere Version derselben Anwendung, eine der in Windows enthaltenen Barrierefreiheits Anwendungen oder "None" sein, wenn Sie keine Barrierefreiheits Anwendung auf dem sicheren Desktop ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="cf937-163">The alternate can be a different application, a different version of the same application, one of the accessibility applications that is included in Windows, or "none" if you do not want to run any accessibility application on the secure desktop.</span></span> <br/>                                                                                                                                                                                                               | <span data-ttu-id="cf937-164">Optional</span><span class="sxs-lookup"><span data-stu-id="cf937-164">Optional</span></span>           | <span data-ttu-id="cf937-165">Nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="cf937-165">Not localized</span></span> |
| <span data-ttu-id="cf937-166">Einfaches Profil</span><span class="sxs-lookup"><span data-stu-id="cf937-166">Simple Profile</span></span>              | <span data-ttu-id="cf937-167">Ein Wert, der beschreibt, wie die Anwendung in einem Wort oder zwei klassifiziert wird, z. b. Bildschirmleser, Bildschirmlupe oder Bildschirmtastatur.</span><span class="sxs-lookup"><span data-stu-id="cf937-167">A value that describes how to classify the application in a word or two: Screen reader, Magnifier, or On-screen keyboard, for example.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="cf937-168">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cf937-168">Mandatory</span></span>          | <span data-ttu-id="cf937-169">Nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="cf937-169">Not localized</span></span> |
| <span data-ttu-id="cf937-170">StartExe</span><span class="sxs-lookup"><span data-stu-id="cf937-170">StartExe</span></span>                    | <span data-ttu-id="cf937-171">Der vollständige Pfad der ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="cf937-171">The full path of the executable.</span></span> <span data-ttu-id="cf937-172">Dieser Wert wird verwendet, um die Barrierefreiheits Anwendung zu starten.</span><span class="sxs-lookup"><span data-stu-id="cf937-172">This value is used to launch the accessibility application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="cf937-173">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cf937-173">Mandatory</span></span>          | <span data-ttu-id="cf937-174">Nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="cf937-174">Not localized</span></span> |
| <span data-ttu-id="cf937-175">Startpara</span><span class="sxs-lookup"><span data-stu-id="cf937-175">StartParams</span></span>                 | <span data-ttu-id="cf937-176">Befehlszeilenargumenten</span><span class="sxs-lookup"><span data-stu-id="cf937-176">Command-line arguments.</span></span> <span data-ttu-id="cf937-177">Diese Werte werden zusammen mit startexe verwendet, um die Anwendung zu starten.</span><span class="sxs-lookup"><span data-stu-id="cf937-177">These values are used along with StartExe to start the application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="cf937-178">Optional</span><span class="sxs-lookup"><span data-stu-id="cf937-178">Optional</span></span>           | <span data-ttu-id="cf937-179">Nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="cf937-179">Not localized</span></span> |
| <span data-ttu-id="cf937-180">Terminateondesktopswitch</span><span class="sxs-lookup"><span data-stu-id="cf937-180">TerminateOnDesktopSwitch</span></span>    | <span data-ttu-id="cf937-181">Ein **DWORD** -Wert, der angibt, wie die Barrierefreiheits Anwendung auf den Übergang zum oder vom sicheren Desktop antwortet.</span><span class="sxs-lookup"><span data-stu-id="cf937-181">A **DWORD** value that specifies how the accessibility application responds to transitions to or from the secure desktop.</span></span><br/> <span data-ttu-id="cf937-182">Wenn dieser Wert nicht vorhanden ist oder 1 ist, wird die Anwendung von Windows bei jedem Übergang zum oder vom sicheren Desktop beendet und neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="cf937-182">If this value does not exist or is 1, Windows terminates and restarts the application on each transition to or from the secure desktop.</span></span> <span data-ttu-id="cf937-183">Dies ist das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="cf937-183">This is the default behavior.</span></span><br/> <span data-ttu-id="cf937-184">Wenn dieser Wert 0 ist, wird die Barrierefreiheits Anwendung bei einem Desktop Übergang von Windows nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="cf937-184">If this value is 0, Windows does not terminate the accessibility application on a desktop transition.</span></span> <span data-ttu-id="cf937-185">Die Anwendung wird weiterhin auf dem vorherigen Desktop ausgeführt, und Windows startet eine neue Instanz auf dem neuen Desktop, wenn eine Instanz nicht bereits ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-185">The application continues to run on the previous desktop, and Windows starts a new instance on the new desktop if an instance is not already running there.</span></span><br/> | <span data-ttu-id="cf937-186">Optional</span><span class="sxs-lookup"><span data-stu-id="cf937-186">Optional</span></span>           | <span data-ttu-id="cf937-187">Nicht lokalisiert</span><span class="sxs-lookup"><span data-stu-id="cf937-187">Not localized</span></span> |


 

### <a name="localization"></a><span data-ttu-id="cf937-188">Lokalisierung</span><span class="sxs-lookup"><span data-stu-id="cf937-188">Localization</span></span>

<span data-ttu-id="cf937-189">Die Registrierungs Werte für den Anwendungsnamen und die Beschreibung müssen lokalisiert werden können, um die mehrsprachige Benutzeroberfläche (MUI) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cf937-189">The registry values of Application Name and Description need to be localizable to support Multilingual User Interface (MUI).</span></span>

<span data-ttu-id="cf937-190">Diese Zeichen folgen weisen das folgende Format auf, wobei Spitze Klammern erforderliche Elemente und eckige Klammern ein optionales Element angeben.</span><span class="sxs-lookup"><span data-stu-id="cf937-190">These strings are in the following format, where angle brackets signify required elements and square brackets signify an optional element.</span></span>

<span data-ttu-id="cf937-191">*@ <resdllpath \\ resdllfilename>,- <resID> \[ ;<comment>\]*</span><span class="sxs-lookup"><span data-stu-id="cf937-191">*@<ResDllPath\\ResDLLFilename>,-<resID>\[;<comment>\]*</span></span>

<span data-ttu-id="cf937-192">*<resdllpath \\ Resdllfilename>* ist der Pfad zur Ressourcen-DLL.</span><span class="sxs-lookup"><span data-stu-id="cf937-192">*<ResDllPath\\ResDLLFilename>* is the path to the resource DLL.</span></span> <span data-ttu-id="cf937-193">Der Pfad kann Umgebungsvariablen enthalten.</span><span class="sxs-lookup"><span data-stu-id="cf937-193">The path can contain environmental variables.</span></span>

<span data-ttu-id="cf937-194">*<resID>* die Ressourcen-ID für die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cf937-194">*<resID>* is the resource ID for the string.</span></span>

<span data-ttu-id="cf937-195">der *\[ Kommentar \]* enthält optionale Kommentare.</span><span class="sxs-lookup"><span data-stu-id="cf937-195">*\[comment\]* contains any optional comments.</span></span>

<span data-ttu-id="cf937-196">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cf937-196">Here is an example:</span></span>


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



<span data-ttu-id="cf937-197">Weitere Informationen zu MUI finden Sie unter [Windows MUI Knowledge Center](../intl/about-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="cf937-197">For more information about MUI, see [Windows MUI Knowledge Center](../intl/about-multilingual-user-interface.md).</span></span>

### <a name="hci-profile"></a><span data-ttu-id="cf937-198">HCI-Profil</span><span class="sxs-lookup"><span data-stu-id="cf937-198">HCI Profile</span></span>

<span data-ttu-id="cf937-199">Mit dem HCI-Profil (Human Computer Interaktion) können Sie feststellen, welche Unterkünfte basierend auf den Anforderungen des Benutzers bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cf937-199">The Human Computer Interaction (HCI) profile is a way to determine what accommodations to provide based on the needs of the user.</span></span> <span data-ttu-id="cf937-200">Barrierefreiheits Anwendungen sollten Informationen über die Art der Behinderung registrieren, die die Anwendung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cf937-200">Accessibility applications should register information about the kind of disability the application helps to accommodate.</span></span>

<span data-ttu-id="cf937-201">Der Wert für die Profil Registrierung enthält XML-Code, der die Art der für die Barrierefreiheits Anwendung vorgesehenen Behinderung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cf937-201">The Profile registry value contains XML that describes the kind of disability targeted by the accessibility application.</span></span> <span data-ttu-id="cf937-202">Dieser XML-Code weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="cf937-202">This XML has the following format:</span></span>


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



<span data-ttu-id="cf937-203">Die gültigen Werte für das-Attribut des- **Lizenztyps** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cf937-203">The valid values for the **Accommodation type** attribute are as follows:</span></span>

-   <span data-ttu-id="cf937-204">milde Vision</span><span class="sxs-lookup"><span data-stu-id="cf937-204">mild vision</span></span>
-   <span data-ttu-id="cf937-205">schwerwiegende Vision</span><span class="sxs-lookup"><span data-stu-id="cf937-205">severe vision</span></span>
-   <span data-ttu-id="cf937-206">milde Cognitive</span><span class="sxs-lookup"><span data-stu-id="cf937-206">mild cognitive</span></span>
-   <span data-ttu-id="cf937-207">Schwerwiegender Cognitive</span><span class="sxs-lookup"><span data-stu-id="cf937-207">severe cognitive</span></span>
-   <span data-ttu-id="cf937-208">milde Dexterität</span><span class="sxs-lookup"><span data-stu-id="cf937-208">mild dexterity</span></span>
-   <span data-ttu-id="cf937-209">schwerwiegende Dexterität</span><span class="sxs-lookup"><span data-stu-id="cf937-209">severe dexterity</span></span>
-   <span data-ttu-id="cf937-210">mildes hören</span><span class="sxs-lookup"><span data-stu-id="cf937-210">mild hearing</span></span>
-   <span data-ttu-id="cf937-211">schwerwiegendes hören</span><span class="sxs-lookup"><span data-stu-id="cf937-211">severe hearing</span></span>
-   <span data-ttu-id="cf937-212">milde Sprache</span><span class="sxs-lookup"><span data-stu-id="cf937-212">mild speech</span></span>
-   <span data-ttu-id="cf937-213">harte Sprache</span><span class="sxs-lookup"><span data-stu-id="cf937-213">severe speech</span></span>

> [!Note]  
> <span data-ttu-id="cf937-214">Bei diesen Werten wird zwischen Groß-/Kleinschreibung unterschieden.</span><span class="sxs-lookup"><span data-stu-id="cf937-214">These values are case sensitive.</span></span>

 

<span data-ttu-id="cf937-215">Wenn eine Barrierefreiheits Anwendung mehrere-Unternehmen unterstützt, sollte der Wert für die Profil Registrierung für jede-Unterkunft ein **Attributtyp** Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="cf937-215">If an accessibility application supports multiple accommodations, the Profile registry value should include an **Accommodation type** attribute for each accommodation.</span></span>

### <a name="ease-of-access-registry-details"></a><span data-ttu-id="cf937-216">Details zur einfachen Zugriffs Registrierung</span><span class="sxs-lookup"><span data-stu-id="cf937-216">Ease of Access registry details</span></span>

<span data-ttu-id="cf937-217">Zum Registrieren Ihrer Barrierefreiheits Anwendung müssen Sie einen Schlüssel für Ihre Anwendung am folgenden Registrierungs Speicherort erstellen und mit Name-Wert-Paaren auffüllen.</span><span class="sxs-lookup"><span data-stu-id="cf937-217">To register your accessibility application, you need to create a key for your application at the following registry location and populate it with name-value pairs.</span></span>

<span data-ttu-id="cf937-218">**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Barrierefreiheit \\\\**</span><span class="sxs-lookup"><span data-stu-id="cf937-218">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\**</span></span>

<span data-ttu-id="cf937-219">Benennen Sie den Registrierungsschlüssel Ihrer Anwendung im folgenden Format:</span><span class="sxs-lookup"><span data-stu-id="cf937-219">Name your application's registry key using the following format:</span></span>

<span data-ttu-id="cf937-220">*"CompanyName \_ ProductName \_ v \# "*</span><span class="sxs-lookup"><span data-stu-id="cf937-220">*"CompanyName\_ProductName\_v\#"*</span></span>

<span data-ttu-id="cf937-221">Beispiel: "Configuration Manager \_ \_ v 2.0".</span><span class="sxs-lookup"><span data-stu-id="cf937-221">For example, "Contoso\_Magnifier\_v2.0".</span></span>

<span data-ttu-id="cf937-222">Zum Hinzufügen von Registrierungs Werten muss das Installationsprogramm mit erhöhten Rechten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cf937-222">To add registry values, your installation program must be running with elevated privileges.</span></span>

### <a name="secure-desktop-accommodation"></a><span data-ttu-id="cf937-223">Sichere Desktop-Unterbringung</span><span class="sxs-lookup"><span data-stu-id="cf937-223">Secure desktop accommodation</span></span>

<span data-ttu-id="cf937-224">Mit dem Registrierungsschlüssel **securedesktopaccommodation** können Sie angeben, wie Ihre Barrierefreiheits Anwendung auf den sicheren Desktop antwortet.</span><span class="sxs-lookup"><span data-stu-id="cf937-224">The **SecureDesktopAccommodation** registry key lets you specify how your accessibility application responds to the secure desktop.</span></span> <span data-ttu-id="cf937-225">Standardmäßig wird Ihre Anwendung von der Easy Access Center-Anwendung auf dem sicheren Desktop gestartet, wenn Sie bereits auf dem normalen Desktop ausgeführt wurde, oder wenn Sie für die Ausführung auf dem Anmelde Desktop konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="cf937-225">By default, the Ease of Access Center launches your application on the secure desktop if it was already running on the normal desktop, or if it is configured to run on the logon desktop.</span></span> <span data-ttu-id="cf937-226">Mit dem Schlüssel **securedesktopaccommodation** können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="cf937-226">By using the **SecureDesktopAccommodation** key, you can:</span></span>

-   <span data-ttu-id="cf937-227">Geben Sie eine Alternative Version der Anwendung an, die auf dem sicheren Desktop verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf937-227">Specify an alternate version of your application for use on the secure desktop.</span></span> <span data-ttu-id="cf937-228">Beispielsweise können Sie über eine Alternative Version verfügen, die nicht gesicherte Features deaktiviert, oder Sie ist für die Verwendung von weniger Arbeitsspeicher und schnellere Starts optimiert.</span><span class="sxs-lookup"><span data-stu-id="cf937-228">For example, you might have an alternate version that disables unsecured features, or is optimized to use less memory and launch faster.</span></span>

    <span data-ttu-id="cf937-229">Zum Angeben der alternativen Version legen Sie den **securedesktopaccommodation** -Schlüssel auf den Namen der alternativen Version fest.</span><span class="sxs-lookup"><span data-stu-id="cf937-229">To specify the alternate version, set the **SecureDesktopAccommodation** key to the name of the alternate version.</span></span> <span data-ttu-id="cf937-230">Wenn Sie Ihre Anwendung z. b. auf dem Schlüssel für den Schlüssel von "TSO \_ Screen Reader \_ v 1.0" registriert haben, können Sie die Alternative Version auf dem \_ Bildschirm readersecure \_ v 1.0 registrieren.</span><span class="sxs-lookup"><span data-stu-id="cf937-230">For example, if you registered your application at the Contoso\_Screen Reader\_v1.0 key, you could register the alternate version at Contoso\_Screen ReaderSecure\_v1.0.</span></span> <span data-ttu-id="cf937-231">Legen Sie dann den **securedesktopaccommodation** -Schlüssel von "Configuration Manager" von "Configuration Manager" \_ \_ für "mso" auf "" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cf937-231">Then, set the **SecureDesktopAccommodation** key of Contoso\_Screen Reader\_v1.0 to "Contoso\_Screen ReaderSecure\_v1.0".</span></span>

-   <span data-ttu-id="cf937-232">Geben Sie eine Microsoft-Barrierefreiheits Anwendung an, die auf dem sicheren Desktop anstelle der Anwendung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf937-232">Specify a Microsoft accessibility application to use on the secure desktop in place of your application.</span></span> <span data-ttu-id="cf937-233">Legen Sie für diese Option **securedesktopaccommodation** auf den Namen der bestimmten Microsoft-Eingabe Hilfen-Anwendung fest: "OSK", "Bildschirmlupe" oder "Sprachausgabe".</span><span class="sxs-lookup"><span data-stu-id="cf937-233">For this option, set **SecureDesktopAccommodation** to the name of the particular Microsoft accessibility application: "osk", "magnifierpane", or "Narrator".</span></span>
-   <span data-ttu-id="cf937-234">Geben Sie an, dass die Anwendung nicht auf dem sicheren Desktop ausgeführt werden soll und keine Alternative Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cf937-234">Specify that your application should not run on the secure desktop, and neither should any alternate application.</span></span> <span data-ttu-id="cf937-235">Legen Sie für diese Option **securedesktopaccommodation** auf "None" (empfohlen) oder den Namen einer nicht vorhandenen Anwendung fest.</span><span class="sxs-lookup"><span data-stu-id="cf937-235">For this option, set **SecureDesktopAccommodation** to "none" (recommend) or the name of a nonexistent application.</span></span>

<span data-ttu-id="cf937-236">Wenn der **securedesktopaccommodation** -Registrierungsschlüssel für Ihre Barrierefreiheits Anwendung eine Microsoft-Barrierefreiheits Anwendung angibt, die auf dem sicheren Desktop anstelle der Anwendung ausgeführt werden soll, wird der Benutzer von Windows benachrichtigt, wenn der Übergang zum sicheren Desktop erfolgt.</span><span class="sxs-lookup"><span data-stu-id="cf937-236">If the **SecureDesktopAccommodation** registry key for your accessibility application specifies a Microsoft accessibility application to run on the secure desktop in place of your application, Windows notifies the user of this when making the transition to the secure desktop.</span></span> <span data-ttu-id="cf937-237">Um den Benutzer zu benachrichtigen, zeigt Windows die Zeichenfolge an, die im Registrierungsschlüssel "Description" für Ihre Anwendung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cf937-237">To notify the user, Windows displays the string specified in the Description registry key for your application.</span></span> <span data-ttu-id="cf937-238">Wenn z. b. die Anwendung Screenreader Deluxe 1,0 die Microsoft-Sprachausgabe auf dem sicheren Desktop verwendet, enthält Sie eine Beschreibungs Zeichenfolge, z. b. "Microsoft-Sprachausgabe wird in den gesperrten, Anmelde-und anderen sicheren Desktops anstelle von Screenreader Deluxe 1,0 verwendet."</span><span class="sxs-lookup"><span data-stu-id="cf937-238">For example, if the ScreenReader Deluxe 1.0 application uses Microsoft Narrator on the secure desktop, it would include a Description string such as, "Microsoft Narrator will be used in the locked, logon, and other secure desktops in place of ScreenReader Deluxe 1.0."</span></span>

<span data-ttu-id="cf937-239">Wenn der **securedesktopaccommodation** -Schlüssel Ihrer Anwendung auf "None" festgelegt ist, verwenden Sie den **Beschreibungs** Schlüssel, um dem Benutzer mitzuteilen, dass Ihre Anwendung auf dem sicheren Desktop nicht verfügbar ist und keine Alternative bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-239">If your application's **SecureDesktopAccommodation** key is set to "none", use the **Description** key to tell the user your application is not available on the secure desktop and no alternative is provided.</span></span>

<span data-ttu-id="cf937-240">Windows zeigt den Beschreibungstext an den entsprechenden Speicherorten im Easy of Access Center an.</span><span class="sxs-lookup"><span data-stu-id="cf937-240">Windows displays the Description text in the relevant locations in the Ease of Access Center.</span></span>

### <a name="running-at-installation-and-on-the-logon-desktop"></a><span data-ttu-id="cf937-241">Ausführung bei der Installation und auf dem Anmelde Desktop</span><span class="sxs-lookup"><span data-stu-id="cf937-241">Running at installation and on the logon desktop</span></span>

<span data-ttu-id="cf937-242">Wenn Sie den registrierten Schlüsselnamen ihrer Barrierefreiheits Anwendung an die Zeichenfolge am folgenden Registrierungs Speicherort anfügen, wird die Anwendung sofort nach der Installation von Windows gestartet.</span><span class="sxs-lookup"><span data-stu-id="cf937-242">If you append your accessibility application's registered key name to the string at the following registry location, Windows will launch your application immediately after it is installed.</span></span> <span data-ttu-id="cf937-243">Außerdem wird die Anwendung automatisch von Windows ausgeführt, wenn der Anmelde Desktop aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="cf937-243">Also, Windows will automatically run your application whenever the logon desktop is active.</span></span>

<span data-ttu-id="cf937-244">**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion ( \\ Barrierefreiheits \\ Konfiguration)**</span><span class="sxs-lookup"><span data-stu-id="cf937-244">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\Configuration**</span></span>

<span data-ttu-id="cf937-245">Der Konfigurationsschlüssel ist eine durch Trennzeichen getrennte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cf937-245">The Configuration key is a comma-delimited string.</span></span> <span data-ttu-id="cf937-246">Um Ihre Anwendung hinzuzufügen, fügen Sie eine Zeichenfolge an, die dem Registrierungsschlüssel Ihrer Anwendung unter HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Barrierefreiheit \\ ATS entspricht \\ .</span><span class="sxs-lookup"><span data-stu-id="cf937-246">To add your application, append a string that is the same as your application's registry key at HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\.</span></span>

### <a name="running-in-a-job"></a><span data-ttu-id="cf937-247">Ausführen in einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="cf937-247">Running in a job</span></span>

<span data-ttu-id="cf937-248">Wenn der Registrierungsschlüssel **terminateondesktopswitch** nicht vorhanden ist oder auf einen Wert ungleich 0 (null) festgelegt ist, führt Windows die Anwendung im Kontext eines Auftrags aus und beendet die Anwendung mit jedem Desktop Übergang und startet Sie neu.</span><span class="sxs-lookup"><span data-stu-id="cf937-248">If the **TerminateOnDesktopSwitch** registry key is not present or is set to non-zero, Windows runs the application in the context of a job, terminating and restarting the application with each desktop transition.</span></span> <span data-ttu-id="cf937-249">Wenn Sie in einem Auftrag ausführen, wird sichergestellt, dass nur eine einzelne Instanz der Anwendung zu einem bestimmten Zeitpunkt ausgeführt wird, und die Anwendung muss den Desktop Status nicht überwachen.</span><span class="sxs-lookup"><span data-stu-id="cf937-249">Running in a job ensures that only a single instance of the application is running at a particular time, and frees the application from having to monitor the desktop state.</span></span> <span data-ttu-id="cf937-250">Zu den Nachteilen der Ausführung von in einem Auftrag gehören:</span><span class="sxs-lookup"><span data-stu-id="cf937-250">The disadvantages of running in a job include:</span></span>

-   <span data-ttu-id="cf937-251">Die Anwendung verursacht einen Startkosten bei jedem Desktop Übergang.</span><span class="sxs-lookup"><span data-stu-id="cf937-251">The application incurs a startup cost with each desktop transition.</span></span>
-   <span data-ttu-id="cf937-252">Die Anwendung kann nur über das Easy of Access Center gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="cf937-252">The application can be started only through the Ease of Access Center.</span></span>
-   <span data-ttu-id="cf937-253">Die Anwendung muss Ihre Einstellungen ständig speichern, da Sie jederzeit durch einen Desktop Übergang beendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cf937-253">The application must continually save its settings because it can be terminated at any time by a desktop transition.</span></span>

<span data-ttu-id="cf937-254">Wenn der **terminateondesktopswitch** -Schlüssel vorhanden und auf 0 festgelegt ist, führt Windows die Barrierefreiheits Anwendung nicht in einem Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="cf937-254">If the **TerminateOnDesktopSwitch** key exists and is set to 0, Windows doesn't run the accessibility application in a job.</span></span> <span data-ttu-id="cf937-255">Dies bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="cf937-255">This has the following advantages:</span></span>

-   <span data-ttu-id="cf937-256">Den Desktop Übergängen sind keine Startkosten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cf937-256">No startup costs are associated with desktop transitions.</span></span>
-   <span data-ttu-id="cf937-257">Die Anwendung kann außerhalb der Easy of Access Center gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="cf937-257">The application can be started outside of the Ease of Access Center.</span></span>

<span data-ttu-id="cf937-258">Zu den Nachteilen, die nicht in einem Auftrag ausgeführt werden, gehören:</span><span class="sxs-lookup"><span data-stu-id="cf937-258">The disadvantages of not running in a job include:</span></span>

-   <span data-ttu-id="cf937-259">Da die Anwendung auf Desktop Übergängen nicht neu gestartet wurde, muss Sie erkennen, wenn der aktuelle Desktop inaktiv ist und entsprechend antwortet.</span><span class="sxs-lookup"><span data-stu-id="cf937-259">Because the application isn t restarted on desktop transitions, it must detect when the current desktop is inactive and respond appropriately.</span></span> <span data-ttu-id="cf937-260">Beispielsweise muss die Anwendung die Steuerung der Hardware aufgeben, damit Sie von der sicheren Desktop Version der Anwendung verwendet werden kann, und die Anwendung sollte in den Energiesparmodus wechseln, um die Verwendung von Prozessorressourcen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="cf937-260">For example, the application must relinquish control of hardware so the secure desktop version of the application can use it, and the application should enter sleep mode to avoid using processor resources.</span></span>
-   <span data-ttu-id="cf937-261">Wenn die Anwendung über das Startmenü, den Windows-Explorer oder die Befehlszeile gestartet werden kann, muss das Easy Access Center informiert werden.</span><span class="sxs-lookup"><span data-stu-id="cf937-261">If the application can be started through the Start menu, Windows Explorer, or the command line, the Ease of Access Center needs to be informed.</span></span> <span data-ttu-id="cf937-262">Weitere Informationen finden Sie unter **Windows-Logo-Taste + U**.</span><span class="sxs-lookup"><span data-stu-id="cf937-262">For more information, see **Windows Logo key + U**.</span></span>
-   <span data-ttu-id="cf937-263">Da mehrere Kopien der Anwendung gleichzeitig auf unterschiedlichen Desktops ausgeführt werden können, muss die Anwendung so geschrieben werden, dass mehrere laufende Kopien unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cf937-263">Because multiple copies of the application can run simultaneously on different desktops, the application must be written to support multiple running copies.</span></span>

### <a name="windows-logo-key--u"></a><span data-ttu-id="cf937-264">Windows-Taste + U</span><span class="sxs-lookup"><span data-stu-id="cf937-264">Windows Logo key + U</span></span>

<span data-ttu-id="cf937-265">Wenn Ihre Barrierefreiheits Anwendung so konfiguriert ist, dass Sie in einem Auftrag ausgeführt wird, sollte der Startcode Ihrer Anwendung einen Aufrufen der [**isprocessinjob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) -Funktion enthalten, um zu bestimmen, ob die Anwendung in einem Auftrag gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-265">If your accessibility application is configured to run in a job, your application's startup code should include a call to the [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) function to determine whether the application is starting in a job.</span></span> <span data-ttu-id="cf937-266">Wenn dies der Fall ist, sollte die Anwendung das Easy of Access Center starten und dann beenden.</span><span class="sxs-lookup"><span data-stu-id="cf937-266">If it is, the application should start the Ease of Access Center and then exit.</span></span> <span data-ttu-id="cf937-267">Im folgenden Beispiel wird gezeigt, wie **isprocessinjob** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-267">The following example shows how to call **IsProcessInJob**.</span></span>


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



<span data-ttu-id="cf937-268">Wenn die Barrierefreiheits Anwendung so konfiguriert ist, dass Sie außerhalb eines Auftrags ausgeführt wird, sollte Sie die Erleichterung des Zugriffs Centers Benachrichtigen, dass die Anwendung gestartet wird und wie üblich fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-268">If the accessibility application is configured to run outside of a job, it should notify the Ease of Access Center that the application is starting and continue as normal.</span></span>

<span data-ttu-id="cf937-269">Unabhängig davon, wie die Anwendung konfiguriert ist, muss die Anwendung, wenn Sie eine Möglichkeit zum Beenden innerhalb der Anwendung bietet (z. b. eine Schaltfläche zum Schließen), die Benutzerfreundlichkeit des Zugriffs Centers Benachrichtigen, dass Sie beendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-269">Regardless of how the application is configured, if it provides a way to exit from within the application, such as a Close button, the application must notify the Ease of Access Center that it is exiting.</span></span>

<span data-ttu-id="cf937-270">Eine Anwendung benachrichtigt das Easy of Access Center durch Festlegen eines temporären Registrierungsschlüssels und Einfügen der Tastenkombination Windows-Taste + U in den Eingabestream.</span><span class="sxs-lookup"><span data-stu-id="cf937-270">An application notifies the Ease of Access Center by setting a temporary registry key and then injecting the Windows Logo key + U key combination into the input stream.</span></span>

<span data-ttu-id="cf937-271">Die Anwendung sollte den temporären Schlüssel an folgendem Speicherort erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf937-271">The application should create the temporary key at the following location.</span></span>

<span data-ttu-id="cf937-272">**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ accessibilitytemp**</span><span class="sxs-lookup"><span data-stu-id="cf937-272">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\AccessibilityTemp**</span></span>

<span data-ttu-id="cf937-273">Der temporäre Schlüssel muss den gleichen Namen wie der registrierte Anwendungsname aufweisen, z. b. "kontoso \_ Screen Reader \_ v 1.0".</span><span class="sxs-lookup"><span data-stu-id="cf937-273">The temporary key should have the same name as the registered application name, such as "Contoso\_Screen Reader\_v1.0".</span></span> <span data-ttu-id="cf937-274">Der Wert des Schlüssels ist ein **DWORD** -Wert, der beim Starten auf 0x0003 erfordert festgelegt ist, oder 0x0002, wenn die Anwendung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-274">The value of the key is a **DWORD** set to 0x0003 when it is starting, or 0x0002 when the application is exiting.</span></span>


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a><span data-ttu-id="cf937-275">Windows-Taste + Lautstärke</span><span class="sxs-lookup"><span data-stu-id="cf937-275">Windows Logo key + Volume Up</span></span>

<span data-ttu-id="cf937-276">Wenn der Benutzer die Barrierefreiheits Anwendung durch Drücken der Tastenkombination Windows-Taste + aufgerundet (z. b. auf einem Tablet-Gerät) startet, übergibt das Easy of Access Center das folgende Befehlszeilenargument an die Anwendung:</span><span class="sxs-lookup"><span data-stu-id="cf937-276">When the user starts your accessibility application by pressing the Windows Logo key + Volume Up key combination (such as on a tablet device), the Ease of Access Center passes the following command-line argument to the application:</span></span>

<span data-ttu-id="cf937-277">**/hardwarebuttonlaunch**</span><span class="sxs-lookup"><span data-stu-id="cf937-277">**/hardwarebuttonlaunch**</span></span>

<span data-ttu-id="cf937-278">Die Anwendung kann dieses Argument verwenden, um zu bestimmen, ob normal gestartet werden soll, oder um das Verhalten entsprechend anzupassen.</span><span class="sxs-lookup"><span data-stu-id="cf937-278">Your application can use this argument to determine whether to start normally, or to adjust behavior accordingly.</span></span>

### <a name="transferring-secure-desktop-settings"></a><span data-ttu-id="cf937-279">Übertragen sicherer Desktop Einstellungen</span><span class="sxs-lookup"><span data-stu-id="cf937-279">Transferring secure desktop settings</span></span>

<span data-ttu-id="cf937-280">Wenn Ihre Barrierefreiheits Anwendung den sicheren Desktop unterstützt, können Sie die-Registrierung verwenden, um Einstellungen zu kopieren, wenn die Anwendung auf den sicheren Desktop übergeht.</span><span class="sxs-lookup"><span data-stu-id="cf937-280">If your accessibility application supports the secure desktop, you can use the registry to copy settings when the application transitions to the secure desktop.</span></span> <span data-ttu-id="cf937-281">Durch das Kopieren von Einstellungen wird der Übergang zum sicheren Desktop für den Benutzer nahtlos.</span><span class="sxs-lookup"><span data-stu-id="cf937-281">Copying settings helps makes the transition to the secure desktop more seamless for the user.</span></span>

<span data-ttu-id="cf937-282">Legen Sie zum Kopieren von Einstellungen den Registrierungsschlüssel copysettingstolockeddesktop der Anwendung auf 1 fest, und speichern Sie die Einstellungen im folgenden Registrierungs Speicherort.</span><span class="sxs-lookup"><span data-stu-id="cf937-282">To copy settings, set the application's CopySettingsToLockedDesktop registry key to 1, and store the settings in the following registry location.</span></span>

<span data-ttu-id="cf937-283">**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Barrierefreiheit \\ atconfig\\<AT Key Name>**</span><span class="sxs-lookup"><span data-stu-id="cf937-283">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATConfig\\<AT Key Name>**</span></span>

<span data-ttu-id="cf937-284">Das Easy Access Center überwacht diesen Registrierungs Speicherort, während die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-284">The Ease of Access Center monitors this registry location while the application is running.</span></span> <span data-ttu-id="cf937-285">Wenn eine Umstellung auf den sicheren Desktop stattfindet, werden die Einstellungen durch das Easy Access Center an denselben Speicherort in der HKCU-Hive-Struktur des sicheren Desktops kopiert.</span><span class="sxs-lookup"><span data-stu-id="cf937-285">When a transition to the secure desktop occurs, the Ease of Access Center copies the settings to the same location in the secure desktop s HKCU hive.</span></span> <span data-ttu-id="cf937-286">Die Anwendung kann dann die Einstellungen lesen und ihren Status fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="cf937-286">The application can then read the settings and resume its state.</span></span>

<span data-ttu-id="cf937-287">Ihre Barrierefreiheits Anwendung sollte Ihre Einstellungen in regelmäßigen Abständen oder immer dann schreiben, wenn sich die Werte ändern.</span><span class="sxs-lookup"><span data-stu-id="cf937-287">Your accessibility application should write its settings at regular intervals or whenever the values change.</span></span> <span data-ttu-id="cf937-288">Das Schreiben von Einstellungen beim Beenden der Anwendung funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="cf937-288">Writing settings on application exit will not work.</span></span> <span data-ttu-id="cf937-289">Wenn die Anwendung in einem Auftrag ausgeführt wird, wird Sie bei der Umstellung vom sicheren Desktop beendet, bevor der Exitcode ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cf937-289">If the application is running in a job, it is terminated on the transition away from the secure desktop, before the exit code has a chance to run.</span></span> <span data-ttu-id="cf937-290">Wenn die Anwendung nicht in einem Auftrag ausgeführt wird, wird die Anwendung bei der Umstellung vom sicheren Desktop nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="cf937-290">If the application is not running in a job, the application is not terminated on the transition away from the secure desktop.</span></span>

### <a name="caution"></a><span data-ttu-id="cf937-291">Achtung</span><span class="sxs-lookup"><span data-stu-id="cf937-291">Caution</span></span>

<span data-ttu-id="cf937-292">Da die hier beschriebenen Registrierungsschlüssel im Benutzermodus geschrieben werden, sind Sie nicht sicher.</span><span class="sxs-lookup"><span data-stu-id="cf937-292">Because the registry keys described here are written in user mode, they are not secure.</span></span> <span data-ttu-id="cf937-293">Wenn Ihre Barrierefreiheits Anwendung den Inhalt dieser Schlüssel liest, sollte die Daten sorgfältig überprüft und mit Bedacht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf937-293">If your accessibility application reads the contents of these keys, it should carefully check the data and use it with caution.</span></span> <span data-ttu-id="cf937-294">Insbesondere sollte Ihre Anwendung eine Überprüfung auf **DWORD** -Werte durchführen, bei Zeichen folgen Längen Vorsicht walten lassen, keine Plug-in-DLL-Namen lesen und keine Befehle ausführen, die in Zeichen folgen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="cf937-294">Specifically, your application should do a bounds check on **DWORD** values, be careful with string lengths, should not read plug-in DLL names, and should not execute any commands found in strings.</span></span>

## <a name="registry-examples"></a><span data-ttu-id="cf937-295">Registrierungs Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf937-295">Registry Examples</span></span>

<span data-ttu-id="cf937-296">Das folgende Beispiel zeigt die möglichen Registrierungs Werte für ein fiktives Produkt mit dem Namen "CSO Screenreader Version 2,0", dessen lokalisierter Name als Ressource gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="cf937-296">The following example shows the possible registry values for a fictitious product called Contoso ScreenReader version 2.0, whose localized name is stored as a resource.</span></span>

<span data-ttu-id="cf937-297">Die Werte in der Tabelle liegen unter folgendem Schlüssel:</span><span class="sxs-lookup"><span data-stu-id="cf937-297">The values in the table are under the following key:</span></span>

<span data-ttu-id="cf937-298">**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Barrierefreiheit \\ ist \\ Conin so \_ Screen Reader \_ v 2.0**</span><span class="sxs-lookup"><span data-stu-id="cf937-298">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\Contoso\_Screen Reader\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf937-299">Name</span><span class="sxs-lookup"><span data-stu-id="cf937-299">Name</span></span></th>
<th><span data-ttu-id="cf937-300">Typ</span><span class="sxs-lookup"><span data-stu-id="cf937-300">Type</span></span></th>
<th><span data-ttu-id="cf937-301">Daten</span><span class="sxs-lookup"><span data-stu-id="cf937-301">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf937-302">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="cf937-302">ApplicationName</span></span></td>
<td><span data-ttu-id="cf937-303">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-303">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-304">@% Systemroot% \system32\ContosoRes.dll,-5020</span><span class="sxs-lookup"><span data-stu-id="cf937-304">@%SystemRoot%\system32\ContosoRes.dll,-5020</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf937-305">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf937-305">Description</span></span></td>
<td><span data-ttu-id="cf937-306">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-306">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-307">@% Systemroot% \system32\ContosoRes.dll,-5040</span><span class="sxs-lookup"><span data-stu-id="cf937-307">@%SystemRoot%\system32\ContosoRes.dll,-5040</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf937-308">Profil</span><span class="sxs-lookup"><span data-stu-id="cf937-308">Profile</span></span></td>
<td><span data-ttu-id="cf937-309">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-309">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf937-310">XML</span><span class="sxs-lookup"><span data-stu-id="cf937-310">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf937-311">Simpleprofile</span><span class="sxs-lookup"><span data-stu-id="cf937-311">SimpleProfile</span></span></td>
<td><span data-ttu-id="cf937-312">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-312">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-313">Screenreader</span><span class="sxs-lookup"><span data-stu-id="cf937-313">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf937-314">StartExe</span><span class="sxs-lookup"><span data-stu-id="cf937-314">StartExe</span></span></td>
<td><span data-ttu-id="cf937-315">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-315">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-316">C:\ContosoTools\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="cf937-316">C:\ContosoTools\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf937-317">Startpara</span><span class="sxs-lookup"><span data-stu-id="cf937-317">StartParams</span></span></td>
<td><span data-ttu-id="cf937-318">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-318">REG_SZ</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="cf937-319">Securedesktopaccommodation</span><span class="sxs-lookup"><span data-stu-id="cf937-319">SecureDesktopAccommodation</span></span></td>
<td><span data-ttu-id="cf937-320">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-320">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-321">Narrator</span><span class="sxs-lookup"><span data-stu-id="cf937-321">Narrator</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cf937-322">Wenn die Anwendung eine Sprachausgabe und eine Bildschirmlupe in einer einzelnen ausführbaren Datei bereitstellt, können die Werte für die Bildschirm Lese Komponente wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="cf937-322">If the application provides both a screen reader and a screen magnifier in a single executable, the values for the screen reader component might look like this:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf937-323">Name</span><span class="sxs-lookup"><span data-stu-id="cf937-323">Name</span></span></th>
<th><span data-ttu-id="cf937-324">Typ</span><span class="sxs-lookup"><span data-stu-id="cf937-324">Type</span></span></th>
<th><span data-ttu-id="cf937-325">Daten</span><span class="sxs-lookup"><span data-stu-id="cf937-325">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf937-326">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="cf937-326">ApplicationName</span></span></td>
<td><span data-ttu-id="cf937-327">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-327">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-328">@C:\Program Files\Contoso\Contosores.dll,-30</span><span class="sxs-lookup"><span data-stu-id="cf937-328">@C:\Program Files\Contoso\Contosores.dll,-30</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf937-329">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf937-329">Description</span></span></td>
<td><span data-ttu-id="cf937-330">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-330">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-331">@C:\Program Files\Contoso\Contosores.dll,-32</span><span class="sxs-lookup"><span data-stu-id="cf937-331">@C:\Program Files\Contoso\Contosores.dll,-32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf937-332">Profil</span><span class="sxs-lookup"><span data-stu-id="cf937-332">Profile</span></span></td>
<td><span data-ttu-id="cf937-333">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-333">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf937-334">XML</span><span class="sxs-lookup"><span data-stu-id="cf937-334">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf937-335">Simpleprofile</span><span class="sxs-lookup"><span data-stu-id="cf937-335">SimpleProfile</span></span></td>
<td><span data-ttu-id="cf937-336">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-336">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-337">Screenreader</span><span class="sxs-lookup"><span data-stu-id="cf937-337">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf937-338">StartExe</span><span class="sxs-lookup"><span data-stu-id="cf937-338">StartExe</span></span></td>
<td><span data-ttu-id="cf937-339">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-339">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-340">C:\ProgrammeFiles\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="cf937-340">C:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf937-341">Startpara</span><span class="sxs-lookup"><span data-stu-id="cf937-341">StartParams</span></span></td>
<td><span data-ttu-id="cf937-342">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-342">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-343">/r</span><span class="sxs-lookup"><span data-stu-id="cf937-343">/r</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cf937-344">Die Werte für die Bildschirm Vergrößerungs Komponente befinden sich im folgenden Schlüssel:</span><span class="sxs-lookup"><span data-stu-id="cf937-344">The values for the magnifier component would be in the following key:</span></span>

<span data-ttu-id="cf937-345">**HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ condesoibility \\ ATS \\ Conto so \_ Lupe \_ v 2.0**</span><span class="sxs-lookup"><span data-stu-id="cf937-345">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Contosoibility\\ATs\\Contoso\_Magnifier\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf937-346">Name</span><span class="sxs-lookup"><span data-stu-id="cf937-346">Name</span></span></th>
<th><span data-ttu-id="cf937-347">Typ</span><span class="sxs-lookup"><span data-stu-id="cf937-347">Type</span></span></th>
<th><span data-ttu-id="cf937-348">Daten</span><span class="sxs-lookup"><span data-stu-id="cf937-348">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf937-349">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="cf937-349">ApplicationName</span></span></td>
<td><span data-ttu-id="cf937-350">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-350">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-351">@c:\Program Files\Contoso\Contosores.dll,-31</span><span class="sxs-lookup"><span data-stu-id="cf937-351">@c:\Program Files\Contoso\Contosores.dll,-31</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf937-352">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf937-352">Description</span></span></td>
<td><span data-ttu-id="cf937-353">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-353">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-354">@c:\Program Files\Contoso\Contosores.dll,-42</span><span class="sxs-lookup"><span data-stu-id="cf937-354">@c:\Program Files\Contoso\Contosores.dll,-42</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf937-355">Profil</span><span class="sxs-lookup"><span data-stu-id="cf937-355">Profile</span></span></td>
<td><span data-ttu-id="cf937-356">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-356">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf937-357">XML</span><span class="sxs-lookup"><span data-stu-id="cf937-357">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf937-358">Simpleprofile</span><span class="sxs-lookup"><span data-stu-id="cf937-358">SimpleProfile</span></span></td>
<td><span data-ttu-id="cf937-359">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-359">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-360">Vergrößern</span><span class="sxs-lookup"><span data-stu-id="cf937-360">Magnification</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf937-361">StartExe</span><span class="sxs-lookup"><span data-stu-id="cf937-361">StartExe</span></span></td>
<td><span data-ttu-id="cf937-362">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-362">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-363">c:\ProgrammeFiles\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="cf937-363">c:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf937-364">Startpara</span><span class="sxs-lookup"><span data-stu-id="cf937-364">StartParams</span></span></td>
<td><span data-ttu-id="cf937-365">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cf937-365">REG_SZ</span></span></td>
<td><span data-ttu-id="cf937-366">/m</span><span class="sxs-lookup"><span data-stu-id="cf937-366">/m</span></span></td>
</tr>
</tbody>
</table>



 

 

