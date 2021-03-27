---
description: Das Startmenü in Windows XP und Windows Vista enthält reservierte Slots für die Standard Clients für Internet (Browser) und e-Mail (Mail), die häufig als Startmenü-Internetanwendungen bezeichnet werden.
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Registrieren eines Internet Browsers oder e-Mail-Clients über das Windows-Startmenü
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219050"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a><span data-ttu-id="c8f2a-103">Registrieren eines Internet Browsers oder e-Mail-Clients über das Windows-Startmenü</span><span class="sxs-lookup"><span data-stu-id="c8f2a-103">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>

> [!Note]  
> <span data-ttu-id="c8f2a-104">Dieses Thema gilt für Windows XP, Windows Vista und Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-104">This topic applies to Windows XP, Windows Vista, and Windows 7.</span></span>

 

<span data-ttu-id="c8f2a-105">Das Startmenü in Windows XP und Windows Vista enthält reservierte Slots für die Standard Clients für **Internet** (Browser) und **e-Mail** (Mail), die häufig als *Startmenü-Internetanwendungen* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-105">The Start menu in Windows XP and Windows Vista contains reserved slots for the default **Internet** (browser) and **E-mail** (mail) clients, together commonly known as *Start Menu Internet Applications*.</span></span> <span data-ttu-id="c8f2a-106">Anwendungen, die als Startmenü-Internet Anwendungen registriert sind, über das gesamte System (pro Computer).</span><span class="sxs-lookup"><span data-stu-id="c8f2a-106">Applications which register as Start Menu Internet Applications do so across the entire system (per-machine).</span></span> <span data-ttu-id="c8f2a-107">In Windows Vista kann der Benutzer das **Standardprogramm "Programme** " verwenden, um eine Standardeinstellung für Benutzer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-107">In Windows Vista, the user may use the **Default Programs** feature to set a per-user default.</span></span>

<span data-ttu-id="c8f2a-108">Wenn Anwendungen als Startmenü-Internet Anwendungen registriert werden, erstellen Windows XP und Windows Vista **Internet** -und **e-Mail-** Symbole im Startmenü.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-108">When applications register as Start Menu Internet Applications, Windows XP and Windows Vista create **Internet** and **E-mail** icons on the Start menu.</span></span> <span data-ttu-id="c8f2a-109">Wenn Sie auf diese Symbole klicken, wird das Startmenü zum Überprüfen der Registrierungs Teilstruktur pro Benutzer (**HKEY \_ Current \_ User**) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-109">Clicking these icons causes the Start menu to check the per-user registry subtree (**HKEY\_CURRENT\_USER**).</span></span> <span data-ttu-id="c8f2a-110">Wenn keine benutzerspezifische Standardeinstellung gefunden wird, sucht das Startmenü in der Unterstruktur des **lokalen HKEY-Computers nach \_ \_** dem Standard Unterschlüssel pro Computer.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-110">If no per-user default setting is found, the Start menu looks for the per-machine default subkey in the **HKEY\_LOCAL\_MACHINE** subtree.</span></span>

> [!Note]  
> <span data-ttu-id="c8f2a-111">Die Standardinstallation von Windows registriert nicht ein standardmäßiges Internet oder e-Mail-Programm pro Benutzer, sondern nur eine systemweite Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-111">The default installation of Windows does not register a per-user default Internet or email program, only a system-wide default.</span></span> <span data-ttu-id="c8f2a-112">Dies bietet einen reibungslosen Upgradepfad von früheren Versionen des Betriebssystems, in dem nur die HKEY- \_ \_ Unterstruktur lokaler Computer für Client Registrierungen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-112">This provides a smooth upgrade path from previous versions of the operating system, in which only the HKEY\_LOCAL\_MACHINE subtree is supported for client registrations.</span></span>

 

<span data-ttu-id="c8f2a-113">In diesem Thema werden die folgenden Elemente erläutert:</span><span class="sxs-lookup"><span data-stu-id="c8f2a-113">This topic discusses the following items:</span></span>

-   [<span data-ttu-id="c8f2a-114">Registrieren für den Startmenü-Internet Link</span><span class="sxs-lookup"><span data-stu-id="c8f2a-114">Registering for the Start Menu Internet Link</span></span>](#registering-for-the-start-menu-internet-link)
    -   [<span data-ttu-id="c8f2a-115">Registrieren als standardmäßiger Internet Client</span><span class="sxs-lookup"><span data-stu-id="c8f2a-115">How to Register as the Default Internet Client</span></span>](#how-to-register-as-the-default-internet-client)
-   [<span data-ttu-id="c8f2a-116">Registrieren für den Link "Startmenü-e-Mail"</span><span class="sxs-lookup"><span data-stu-id="c8f2a-116">Registering for the Start Menu Email Link</span></span>](#registering-for-the-start-menu-email-link)
    -   [<span data-ttu-id="c8f2a-117">Anzeigen des Standard-e-Mail-Clients im Startmenü</span><span class="sxs-lookup"><span data-stu-id="c8f2a-117">How the Start Menu Displays the Default Email Client</span></span>](#how-the-start-menu-displays-the-default-email-client)
    -   [<span data-ttu-id="c8f2a-118">Registrieren als Standard-e-Mail-Client</span><span class="sxs-lookup"><span data-stu-id="c8f2a-118">How to Register as the Default EMail Client</span></span>](#how-to-register-as-the-default-email-client)
-   [<span data-ttu-id="c8f2a-119">Anpassen des Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="c8f2a-119">Customizing the Context Menu</span></span>](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a><span data-ttu-id="c8f2a-120">Registrieren für den Startmenü-Internet Link</span><span class="sxs-lookup"><span data-stu-id="c8f2a-120">Registering for the Start Menu Internet Link</span></span>

> [!Note]  
> <span data-ttu-id="c8f2a-121">Diese Registrierung ist ab Windows 7 veraltet, wodurch kein Startmenü-Internet Link mehr zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-121">This registration is deprecated as of Windows 7, which no longer provides a Start menu Internet link.</span></span> <span data-ttu-id="c8f2a-122">Vorhandene Registrierungen werden in Windows 7 und höher ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-122">Existing registrations are ignored in Windows 7 and later.</span></span> <span data-ttu-id="c8f2a-123">Die Registrierung als standardmäßige Startmenü-Internet Anwendung ist nicht identisch mit der Registrierung als Standard Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-123">Being registered as the default Start menu Internet application is not the same as being registered as the default web browser.</span></span> <span data-ttu-id="c8f2a-124">Der Standard Webbrowser wird verwendet, um beliebige URLs von einer beliebigen Stelle im System aus zu starten.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-124">The default web browser is used for launching arbitrary URLs from anywhere in the system.</span></span> <span data-ttu-id="c8f2a-125">Das Startmenü "Internetanwendung" steuert nur das Programm, das gestartet wird, wenn der Benutzer im Startmenü auf das Internet-Symbol klickt.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-125">The Start menu Internet application merely controls the program that is started when the user clicks the Internet icon on the Start menu.</span></span>

 

<span data-ttu-id="c8f2a-126">Alle Webbrowser Anwendungen können sich registrieren, damit Sie im Startmenü als Internet Client angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-126">Any web browser application can register to appear as an Internet client on the Start menu.</span></span> <span data-ttu-id="c8f2a-127">Diese Sichtbarkeit, gekoppelt mit der ordnungsgemäßen Registrierung für die [Datei](fa-intro.md) -und [Protokoll](/previous-versions//aa767743(v=vs.85)) Typen einer Anwendung, gibt dem Standardbrowser Status der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-127">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default browser status.</span></span>

<span data-ttu-id="c8f2a-128">Registrierungen, die in der **HKEY \_ Current \_ User** -Teilstruktur vorgenommen wurden, haben Vorrang vor den entsprechenden Registrierungen, die auf dem **lokalen HKEY- \_ \_ Computer** durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-128">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="c8f2a-129">Für neue Benutzer im System werden die auf dem **lokalen HKEY- \_ \_ Computer** gespeicherten Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-129">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="c8f2a-130">Ab Windows XP werden die Internet Einstellungen für das Startmenü in den Standardeinträgen für zwei Registrierungs Speicherorte gespeichert:</span><span class="sxs-lookup"><span data-stu-id="c8f2a-130">As of Windows XP, Start menu Internet settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="c8f2a-131">**HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Clients** \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="c8f2a-131">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>
-   <span data-ttu-id="c8f2a-132">**HKEY \_ Software Clients für lokale \_ Computer** \\  \\  \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="c8f2a-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>

<span data-ttu-id="c8f2a-133">Der Unterschlüssel **HKEY \_ Current \_ User** \\ **Software** \\ **Clients** \\ **StartMenuInternet** beschreibt den Internetbrowser, der gestartet wird, wenn der Benutzer im Startmenü auf das **Internet** -Symbol klickt.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-133">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** describes the Internet browser that is started when the user clicks the **Internet** icon on the Start menu.</span></span> <span data-ttu-id="c8f2a-134">Wenn der Unterschlüssel leer ist oder nicht vorhanden ist, wird das **Internet** -Symbol im Startmenü auf den Standardwert des Systems festgelegt, das am zweiten Speicherort auf **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **StartMenuInternet** gespeichert ist, in dem alle auf dem System installierten Internet Browser Anwendungen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-134">If that subkey is blank or missing, then the **Internet** icon on the Start menu is set to the system default stored in the second location at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** , which describes all Internet browser applications that are installed on the system.</span></span>

<span data-ttu-id="c8f2a-135">Wenn ein neuer Benutzer sich beim System anmeldet, verwendet das Startmenü den Standardwert im Unterschlüssel auf **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **StartMenuInternet** , um den standardmäßigen Internet Client anzuzeigen und die registrierte Anwendung zu starten, wenn auf das Symbol geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-135">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** to display the default Internet client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-internet-client"></a><span data-ttu-id="c8f2a-136">Registrieren als standardmäßiger Internet Client</span><span class="sxs-lookup"><span data-stu-id="c8f2a-136">How to Register as the Default Internet Client</span></span>

<span data-ttu-id="c8f2a-137">Unterhalb des unter Schlüssels **HKEY \_ lokale \_ Computer** \\ **Software** \\ **Clients** \\ **StartMenuInternet** können NULL oder mehr Unterschlüssel vorhanden sein, eine für jede registrierte Internet Browser Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-137">Below the subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** there can be zero or more subkeys, one for each registered Internet browser application.</span></span> <span data-ttu-id="c8f2a-138">Ein hypothetisches System könnte z. b. folgende Anordnung aufweisen:</span><span class="sxs-lookup"><span data-stu-id="c8f2a-138">For example, a hypothetical system might have this arrangement:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

<span data-ttu-id="c8f2a-139">Wir veranschaulichen Registrierungseinträge mit einem hypothetischen Browser namens "Lit View" aus einem fiktiven Unternehmen namens Litware Inc. angenommen, der Name der ausführbaren Datei ist Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-139">We will demonstrate registry entries with a hypothetical browser called "Lit View" from a fictional company called Litware Inc. Suppose that the executable name for Lit View is Litview.exe.</span></span> <span data-ttu-id="c8f2a-140">Die Registrierung der beleuchteten Ansicht erfolgt wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="c8f2a-140">The registration of Lit View occurs as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="c8f2a-141">Die LocalizedString-Daten sind vom Typ reg \_ SZ, oder reg \_ Expand SZ, \_ Wenn Pfad Variablen wie `%programfiles%` verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-141">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="c8f2a-142">LocalizedString stellt den Pfad zu einer ausführbaren Datei (. exe) oder einer Bibliotheksdatei (DLL-Datei) bereit.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-142">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="c8f2a-143">Beachten Sie, dass die Pfad Zeichenfolge mit einem "at"-Zeichen (@) beginnt und dass für den Pfad keine Anführungszeichen erforderlich sind, unabhängig davon, ob darin Leerzeichen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-143">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="c8f2a-144">Die ganzzahlige Ganzzahl ist die ID einer Zeichen folgen Ressource, die in der angegebenen dll enthalten ist, deren Wert dem Benutzer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-144">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="c8f2a-145">Dadurch kann dieselbe Registrierung für mehrere Sprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-145">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="c8f2a-146">Jede Sprache stellt eine andere ResourceDLL.dll bereit.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-146">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="c8f2a-147">Dadurch kann das System die richtige Zeichenfolge auf der Grundlage der aktuell ausgewählten Sprache anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-147">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="c8f2a-148">Mit dem folgenden reg \_ SZ-oder reg \_ Expand-Wert wird \_ das Startmenü des Standard Symbols angezeigt, das angezeigt wird, wenn der Benutzer die Beleuchtung als Startmenü im Internet Browser auswählt.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-148">The following REG\_SZ or REG\_EXPAND\_SZ value informs the Start menu of the default icon to display when the user selects Lit View as the Start menu Internet browser.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

<span data-ttu-id="c8f2a-149">Der folgende Registrierungs Unterschlüssel gibt eine Befehlszeile an, die ausgeführt werden soll, wenn der Benutzer im Startmenü auf den Menübefehl Internet klickt</span><span class="sxs-lookup"><span data-stu-id="c8f2a-149">The following registry subkey specifies a command line to run when the user clicks the Internet menu command on the Start menu, assuming that Lit View is the selected Start menu Internet browser.</span></span> <span data-ttu-id="c8f2a-150">Der Befehl könnte z. b. den Browser mit der Startseite des Benutzers öffnen, oder der Befehl könnte eine einführende Benutzeroberfläche starten, die der unabhängige Softwarehersteller (ISV) geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-150">For example, the command might open the browser with the user's home page or the command could launch an introductory user interface that the independent software vendor (ISV) feels is appropriate.</span></span> <span data-ttu-id="c8f2a-151">Die Daten sind vom Typ reg \_ SZ oder reg \_ Expand \_ SZ. Beachten Sie jedoch, dass der Pfad der ausführbaren Datei in Anführungszeichen eingeschlossen ist, weil der Befehlszeilen Pfad leer ist.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-151">The data is of type REG\_SZ or REG\_EXPAND\_SZ, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

<span data-ttu-id="c8f2a-152">Wenn der Benutzer über [Set Program Access and Computer defaults (SPAD)](cpl-setprogramaccess.md) angibt, dass die beleuchtete Ansicht als Standard Webbrowser auf Computer Ebene verwendet werden soll, sollte die Anwendung den folgenden reg \_ SZ-Eintrag festlegen.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-152">When the user specifies through [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) that Lit View should be used as the computer-level default web browser, the application should set the following REG\_SZ entry.</span></span> <span data-ttu-id="c8f2a-153">Beachten Sie, dass der Zugriff auf diesen Unterschlüssel zulässig ist, da SPAD mit Administrator Rechten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-153">Note that because SPAD runs with Administrator privileges, access to this subkey is allowed.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> <span data-ttu-id="c8f2a-154">In Windows Vista sollte der Standard Webbrowser auf Benutzerebene mit dem Tool " **Standardprogramme** " und nicht mit " [SPAD](cpl-setprogramaccess.md)" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-154">In Windows Vista, the user-level default web browser should be set using the **Default Programs** tool, not [SPAD](cpl-setprogramaccess.md).</span></span>
> 
> <span data-ttu-id="c8f2a-155">**Die folgenden Informationen gelten nur für Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="c8f2a-155">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="c8f2a-156">Wenn die Registrierung des Standard Webbrowser auf Computer Ebene unter HKEY \_ local \_ Machine, wie oben gezeigt, erfolgreich ist, sollte die Anwendung den Standardeintrag unter dem folgenden Unterschlüssel löschen:</span><span class="sxs-lookup"><span data-stu-id="c8f2a-156">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> <span data-ttu-id="c8f2a-157">Wenn die Registrierung des Standard Webbrowser auf Computer Ebene unter HKEY \_ local \_ Machine fehlschlägt, sollte die Anwendung die REG SZ- \_ Daten wie im folgenden Beispiel für die Anwendung lit View festlegen:</span><span class="sxs-lookup"><span data-stu-id="c8f2a-157">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE fails, the application should set the REG\_SZ data as shown in this example for the Lit View application:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

<span data-ttu-id="c8f2a-158">Nach dem Aktualisieren der entsprechenden Unterschlüssel überträgt die Anwendung die [**WM- \_ settingchange**](../winmsg/wm-settingchange.md) -Nachricht, wobei der *wParam* -Parameter auf 0 festgelegt ist und der zugehörige *LPARAM* -Parameter auf die auf NULL endenden Zeichenfolge verweist `"Software\Clients\StartMenuInternet"` .</span><span class="sxs-lookup"><span data-stu-id="c8f2a-158">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\StartMenuInternet"`.</span></span> <span data-ttu-id="c8f2a-159">Dadurch wird das Betriebssystem benachrichtigt, dass sich der Standard Client geändert hat.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-159">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="c8f2a-160">Das Festlegen dieser Unterschlüssel für das standardmäßige Startmenü Internet Browser ist erforderlich, um die Abwärtskompatibilität mit alten Webbrowsern beizubehalten, die keine benutzerspezifischen Registrierungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-160">Setting these subkeys for the default Start menu Internet browser is necessary to preserve backward compatibility with old web browsers that do not support per-user registrations.</span></span>

## <a name="registering-for-the-start-menu-email-link"></a><span data-ttu-id="c8f2a-161">Registrieren für den Link "Startmenü-e-Mail"</span><span class="sxs-lookup"><span data-stu-id="c8f2a-161">Registering for the Start Menu Email Link</span></span>

> [!Note]  
> <span data-ttu-id="c8f2a-162">Der Link für den Startmenü-e-Mail-Link wurde ab Windows 7 entfernt.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-162">The Start menu Email link has been removed as of Windows 7.</span></span> <span data-ttu-id="c8f2a-163">Diese in diesem Abschnitt erörterte Registrierung sollte jedoch weiterhin durchgeführt werden, um den standardmäßigen MAPI-Client zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-163">However, this registration discussed in this section should still be performed for its effect in assigning the default MAPI client.</span></span>

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a><span data-ttu-id="c8f2a-164">Anzeigen des Standard-e-Mail-Clients im Startmenü</span><span class="sxs-lookup"><span data-stu-id="c8f2a-164">How the Start Menu Displays the Default Email Client</span></span>

<span data-ttu-id="c8f2a-165">Eine beliebige e-Mail-Anwendung kann als e-Mail-Client im Startmenü angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-165">Any email application can register to appear as an email client on the Start menu.</span></span> <span data-ttu-id="c8f2a-166">Diese Sichtbarkeit, gekoppelt mit der ordnungsgemäßen Registrierung für die [Datei](fa-intro.md) -und [Protokoll](/previous-versions//aa767743(v=vs.85)) Typen einer Anwendung, gibt dem Standard-e-Mail-Status der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-166">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default mail status.</span></span>

<span data-ttu-id="c8f2a-167">Registrierungen, die in der **HKEY \_ Current \_ User** -Teilstruktur vorgenommen wurden, haben Vorrang vor den entsprechenden Registrierungen, die auf dem **lokalen HKEY- \_ \_ Computer** durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-167">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="c8f2a-168">Für neue Benutzer im System werden die auf dem **lokalen HKEY- \_ \_ Computer** gespeicherten Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-168">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="c8f2a-169">Ab Windows XP werden die e-Mail-Einstellungen für das Startmenü in den Standardeinträgen für zwei Registrierungs Speicherorte gespeichert:</span><span class="sxs-lookup"><span data-stu-id="c8f2a-169">As of Windows XP, Start menu Email settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="c8f2a-170">**HKEY \_ \_** \\ **Software** \\ **Clients** \\  aktueller Benutzer</span><span class="sxs-lookup"><span data-stu-id="c8f2a-170">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>
-   <span data-ttu-id="c8f2a-171">**HKEY \_ E \_**- \\  \\  \\ **Mail** -Clients für lokale Computer</span><span class="sxs-lookup"><span data-stu-id="c8f2a-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>

<span data-ttu-id="c8f2a-172">Der Unterschlüssel **HKEY \_ Current \_ User** \\ **Software** \\ **Clients** \\ **Mail** beschreibt den e-Mail-Client, der gestartet wird, wenn der Benutzer im Startmenü auf das **e-Mail-** Symbol klickt.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-172">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email client that is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="c8f2a-173">Der Unterschlüssel **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **Mail** beschreibt die e-Mail-Anwendungen, die auf dem System installiert sind, sowie die Standard-e-Mail-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-173">The subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email applications that are installed on the system, as well as the default email application.</span></span>

<span data-ttu-id="c8f2a-174">Wenn die e-Mail-Clients des **aktuellen HKEY- \_ \_ Benutzers** \\  \\  \\  leer sind oder nicht vorhanden sind, wird der Standardwert, der in **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **Mail** definiert ist, verwendet, um die im Startmenü angezeigte e-Mail-Anwendung auszuwählen</span><span class="sxs-lookup"><span data-stu-id="c8f2a-174">If the **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** is blank or missing, the default value defined in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** is used to select the email application that appears on the Start menu.</span></span>

<span data-ttu-id="c8f2a-175">Wenn ein neuer Benutzer sich beim System anmeldet, verwendet das Startmenü den Standardwert im Unterschlüssel unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **Mail** , um den Standard-e-Mail-Client anzuzeigen, und startet die registrierte Anwendung, wenn auf das Symbol geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-175">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** to display the default email client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-email-client"></a><span data-ttu-id="c8f2a-176">Registrieren als Standard-e-Mail-Client</span><span class="sxs-lookup"><span data-stu-id="c8f2a-176">How to Register as the Default EMail Client</span></span>

<span data-ttu-id="c8f2a-177">**HKEY \_ E \_** \\  \\  \\ -**Mail** -Clients für lokale Computer können keine oder mehrere Unterschlüssel enthalten, eine für jede registrierte e-Mail-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-177">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** can contain zero or more subkeys, one for each registered email application.</span></span> <span data-ttu-id="c8f2a-178">Ein hypothetisches System könnte z. b. die folgenden Unterschlüssel definieren:</span><span class="sxs-lookup"><span data-stu-id="c8f2a-178">For example, a hypothetical system might define the following subkeys:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

<span data-ttu-id="c8f2a-179">Wir veranschaulichen Registrierungseinträge mit einem hypothetischen e-Mail-Client namens "Lit Mail" aus dem fiktiven Unternehmen namens Litware Inc. Litware Inc. beschließt, diesen e-Mail-Client unter dem internen Namen "LitMail" zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-179">We will demonstrate registry entries with a hypothetical email client called "Lit Mail" from the fictional company called Litware Inc. Litware Inc. decides to register this email client under the internal name "LitMail".</span></span> <span data-ttu-id="c8f2a-180">Wie bei einem Browser ist der interne Name eine eindeutige Zeichenfolge, die als Unterschlüssel Name verwendet wird, der aber nie dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-180">As with a browser, the internal name is a unique string used as the subkey name, but it is never shown to the user.</span></span>

<span data-ttu-id="c8f2a-181">Um den e-Mail-Client für die Beleuchtung als Standard zu installieren, verwenden Sie den folgenden Unterschlüssel und die zugehörigen Einträge:</span><span class="sxs-lookup"><span data-stu-id="c8f2a-181">To install the Lit Mail email client as the default, they use the following subkey and its entries:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

<span data-ttu-id="c8f2a-182">Die LocalizedString-Daten sind vom Typ reg \_ SZ, oder reg \_ Expand SZ, \_ Wenn Pfad Variablen wie `%programfiles%` verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-182">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="c8f2a-183">LocalizedString stellt den Pfad zu einer ausführbaren Datei (. exe) oder einer Bibliotheksdatei (DLL-Datei) bereit.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-183">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="c8f2a-184">Beachten Sie, dass die Pfad Zeichenfolge mit einem "at"-Zeichen (@) beginnt und dass für den Pfad keine Anführungszeichen erforderlich sind, unabhängig davon, ob darin Leerzeichen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-184">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="c8f2a-185">Die ganzzahlige Ganzzahl ist die ID einer Zeichen folgen Ressource, die in der angegebenen dll enthalten ist, deren Wert dem Benutzer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-185">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="c8f2a-186">Dadurch kann dieselbe Registrierung für mehrere Sprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-186">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="c8f2a-187">Jede Sprache stellt eine andere ResourceDLL.dll bereit.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-187">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="c8f2a-188">Dadurch kann das System die richtige Zeichenfolge auf der Grundlage der aktuell ausgewählten Sprache anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-188">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="c8f2a-189">Nach dem Aktualisieren der entsprechenden Unterschlüssel überträgt die Anwendung die [**WM- \_ settingchange**](../winmsg/wm-settingchange.md) -Nachricht, wobei der *wParam* -Parameter auf 0 festgelegt ist und der zugehörige *LPARAM* -Parameter auf die auf NULL endenden Zeichenfolge verweist `"Software\Clients\Mail"` .</span><span class="sxs-lookup"><span data-stu-id="c8f2a-189">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\Mail"`.</span></span> <span data-ttu-id="c8f2a-190">Dadurch wird das Betriebssystem benachrichtigt, dass sich der Standard Client geändert hat.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-190">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="c8f2a-191">Aus Gründen der Abwärtskompatibilität mit Anwendungen, die keine lokalisierten Zeichen folgen unterstützen, sollte der Name der Anwendung in der installierten Sprache auch als Standardwert für den Unterschlüssel festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-191">For backward compatibility with applications that do not support localized strings, the name of the application in the installed language should also be set as the default value for the subkey.</span></span>

<span data-ttu-id="c8f2a-192">Mit dem folgenden **reg \_ SZ** -oder reg-Erweiterungs Wert wird das Startmenü des Standard Symbols angezeigt, das angezeigt wird, wenn der Benutzer "Lit Mail" als Start Menü-e-Mail-Programm auswählt: **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="c8f2a-192">The following **REG\_SZ** or **REG\_EXPAND\_SZ** value informs the Start menu of the default icon to display when the user selects Lit Mail as the Start menu mail program:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

<span data-ttu-id="c8f2a-193">Der folgende Eintrag gibt eine Befehlszeile an, die ausgeführt werden soll, wenn der Benutzer im Startmenü auf das Menü Element **e-Mail** klickt, vorausgesetzt, dass Lit Mail das ausgewählte e-Mail-Programm für das Startmenü ist</span><span class="sxs-lookup"><span data-stu-id="c8f2a-193">The following entry specifies a command line to run when the user clicks the **E-mail** menu item on the Start menu, assuming that Lit Mail is the selected Start menu email program.</span></span> <span data-ttu-id="c8f2a-194">Diese Befehlszeile wird auch ausgeführt, wenn der Benutzer im Menü Extras von Windows **Internet Explorer die** Option **e-Mail lesen auswählt** .</span><span class="sxs-lookup"><span data-stu-id="c8f2a-194">This command line is also run if the user selects **Read email** from the Windows Internet Explorer **Tools** menu.</span></span> <span data-ttu-id="c8f2a-195">Die Daten sind vom Typ **reg \_ SZ** oder **reg \_ Expand \_ SZ**. Beachten Sie jedoch, dass der Pfad der ausführbaren Datei in Anführungszeichen eingeschlossen ist, weil der Befehlszeilen Pfad leer ist.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-195">The data is of type **REG\_SZ** or **REG\_EXPAND\_SZ**, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

<span data-ttu-id="c8f2a-196">Wenn (und nur wenn) *der Benutzer die* Beleuchtung als standardmäßige Startmenü-e-Mail-Anwendung angibt, kann die Anwendung "Lit Mail" den internen Namen in den folgenden **reg- \_ SZ** -Wert schreiben:</span><span class="sxs-lookup"><span data-stu-id="c8f2a-196">If (and only if) *the user* specifies Lit Mail to be the default Start menu email application, the Lit Mail application may write its internal name to the following **REG\_SZ** value:</span></span>

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="c8f2a-197">Wenn (und nur wenn) *der Benutzer die* Beleuchtung als systemweite Standard-e-Mail-Anwendung angibt, kann die Anwendung "Lit Mail" den internen Namen in den unten angegebenen **reg \_ SZ** -Wert schreiben.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-197">If (and only if) *the user* specifies Lit Mail to be the system-wide default email application, the Lit Mail application may write its internal name to the **REG\_SZ** value specified below.</span></span> <span data-ttu-id="c8f2a-198">Beachten Sie, dass der Zugriff auf diesen Unterschlüssel möglicherweise eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-198">Note that access to this subkey might be restricted.</span></span> <span data-ttu-id="c8f2a-199">Anwendungen sollten nicht davon ausgehen, dass alle Benutzer über die Berechtigung zum Ändern der systemweiten Standard-e-Mail-Anwendung verfügen.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-199">Applications should not assume that all users have permission to change the system-wide default email application.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="c8f2a-200">Die Registrierung als standardmäßige Startmenü-e-Mail-Anwendung entspricht nicht der Registrierung als Standard-e-Mail-Client des Systems oder dem registrierten *mailto* -Handler.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-200">Registration as the default Start menu email application is not equivalent to registration as the system default email client or the registered *mailto* handler.</span></span>

-   <span data-ttu-id="c8f2a-201">Der Standard-e-Mail-Client des Systems wird gestartet, wenn der Benutzer im **Internet Explorer** -Menü Extras auf **e-Mail lesen** klickt.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-201">The system default email client is started when the user clicks **Read email** from the Internet Explorer **Tools** menu.</span></span>
-   <span data-ttu-id="c8f2a-202">Der registrierte *mailto* -Handler wird gestartet, wenn der Benutzer auf eine URL des Formulars klickt `mailto:someone@example.com` .</span><span class="sxs-lookup"><span data-stu-id="c8f2a-202">The registered *mailto* handler is started when the user clicks a URL of the form `mailto:someone@example.com`.</span></span>
-   <span data-ttu-id="c8f2a-203">Die Start Menü-e-Mail-Anwendung wird gestartet, wenn der Benutzer im Startmenü auf das **e-Mail-** Symbol klickt.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-203">The Start menu email application is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="c8f2a-204">Wenn keine standardmäßige Start Menü-e-Mail-Anwendung angegeben ist, wird das e-Mail-Symbol im Startmenü den standardmäßigen e-Mail-Client</span><span class="sxs-lookup"><span data-stu-id="c8f2a-204">If no default Start menu email application is specified, the Email icon on the Start menu launches the system default email client.</span></span>

<span data-ttu-id="c8f2a-205">In diesem Thema wird die Registrierung der Anwendung nicht als Standard- *mailto* -Protokollhandler behandelt.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-205">This topic does not cover registration of the application as the default *mailto* protocol handler.</span></span> <span data-ttu-id="c8f2a-206">Anwendungen, die sich auf diese Weise registrieren möchten, sollten weiterhin den vorhandenen Spezifikationen für diesen Betreff entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-206">Applications that want to register in such a manner should continue to follow existing specifications on this subject.</span></span>

## <a name="customizing-the-context-menu"></a><span data-ttu-id="c8f2a-207">Anpassen des Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="c8f2a-207">Customizing the Context Menu</span></span>

<span data-ttu-id="c8f2a-208">Eine Anwendung kann die Eigenschaften Seiten anpassen, die angezeigt werden, wenn der Benutzer im Kontextmenü des **e-Mail-** Symbols (oder des **Internet** Symbols) **Eigenschaften** auswählt.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-208">An application can customize the property pages that are displayed when the user selects **Properties** from the **E-mail** (or **Internet**) icon's shortcut menu.</span></span> <span data-ttu-id="c8f2a-209">Die Litware-e-Mail-Anwendung fügt z. b. die folgenden **reg \_ SZ** -oder **reg \_ Expand \_** -Daten hinzu, um ein benutzerdefiniertes Eigenschaften Blatt für das **e-Mail-** Symbol anstelle seines Standardeigenschaften Blatts anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="c8f2a-209">For example, the Litware email application adds the following **REG\_SZ** or **REG\_EXPAND\_SZ** data to display a custom property sheet for the **E-mail** icon rather than its default property sheet.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

<span data-ttu-id="c8f2a-210">Das MUIVerb-Datenelement wird beginnend mit einem "at"-Zeichen (@), gefolgt vom vollständigen Pfad zur Ressourcen-DLL, einem Komma, einem Minuszeichen (-) und dann dem anzuzeigenden Dezimalzeichen folgen Ressourcen Bezeichner erstellt.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-210">The MUIVerb data item is constructed beginning with an "at" sign (@), followed by the full path to the resource DLL, a comma, a minus sign (-), and then the decimal string resource identifier to display.</span></span> <span data-ttu-id="c8f2a-211">Beachten Sie, dass der Pfad zum LitMail.exe Programm Leerzeichen enthält, sodass die Pfad Zeichenfolge in Anführungszeichen gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-211">Note that the path to the LitMail.exe program contains spaces, so the path string is placed inside quotation marks.</span></span>

<span data-ttu-id="c8f2a-212">Eine Anwendung kann dem Kontextmenü auch weitere Befehle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-212">An application can also add additional commands to the context menu.</span></span> <span data-ttu-id="c8f2a-213">Beispielsweise fügt die Litware-e-Mail-Anwendung einen **Find** -Befehl mit den folgenden **reg \_ SZ** -Daten hinzu:</span><span class="sxs-lookup"><span data-stu-id="c8f2a-213">For example, the Litware email application adds a **find** command with the following **REG\_SZ** data:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

<span data-ttu-id="c8f2a-214">Der Unterschlüssel Name unterhalb der **Shell** (in diesem Fall "Find") ist ein beliebiger, nicht lokalisierter Name.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-214">The subkey name below **shell** (in this case, "find") is an arbitrary, nonlocalized name.</span></span> <span data-ttu-id="c8f2a-215">Erneut enthalten die MUIVerb-Daten ein "at"-Zeichen (@) als erstes Element, gefolgt vom Pfad zu einer Ressourcen-DLL, einem Komma Trennzeichen und einem Minuszeichen, das dem Dezimalzeichen folgen Ressourcen Bezeichner vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-215">Once again the MUIVerb data contains an "at" sign (@) as the first element, followed by the path to a resource DLL, a comma separator, and then a minus sign preceding the decimal string resource identifier.</span></span> <span data-ttu-id="c8f2a-216">Beispielsweise könnte diese Zeichen folgen Ressource "Open Address Book" lauten.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-216">For example, that string resource might be "Open Address Book".</span></span> <span data-ttu-id="c8f2a-217">Beachten Sie schließlich, dass die Befehlszeilen Zeichenfolge Leerzeichen enthält, sodass Sie in Anführungszeichen eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c8f2a-217">Finally, note that the command-line string contains spaces, so it is enclosed in quotation marks.</span></span>

 

 
