---
description: Verwenden Sie Standardprogramme, um die Standardbenutzer Funktion festzulegen.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Standardprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cd741794189e47888f4daa1d4585b2d8942cf
ms.sourcegitcommit: 1a97e0e0f92d4dcc2fb68738b910ba3910508df3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2021
ms.locfileid: "103869292"
---
# <a name="default-programs"></a><span data-ttu-id="cd12d-103">Standardprogramme</span><span class="sxs-lookup"><span data-stu-id="cd12d-103">Default Programs</span></span>

<span data-ttu-id="cd12d-104">Verwenden Sie **Standardprogramme** , um die Standardbenutzer Funktion festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-104">Use **Default Programs** to set the default user experience.</span></span> <span data-ttu-id="cd12d-105">Benutzer können über die Systemsteuerung oder direkt über das **Startmenü** auf **Standardprogramme** zugreifen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-105">Users can access **Default Programs** from Control Panel or directly from the **Start** menu.</span></span> <span data-ttu-id="cd12d-106">Legen Sie das Tool [Programm Zugriffs-und Computer Standardwerte (SPAD) fest](cpl-setprogramaccess.md) , das primäre Standardbenutzer Oberflächen für Benutzer in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd12d-106">[Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) tool, the primary defaults experience for users in Windows XP, is now one part of **Default Programs**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd12d-107">Dieses Thema gilt nicht für Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cd12d-107">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="cd12d-108">Die Art und Weise, wie standardmäßige Dateizuordnungen in Windows 10 geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-108">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="cd12d-109">Weitere Informationen finden Sie im Abschnitt zu den **Änderungen in Windows 10** für die Behandlung von Standard-apps in [diesem Beitrag](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span><span class="sxs-lookup"><span data-stu-id="cd12d-109">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

<span data-ttu-id="cd12d-110">Wenn ein Benutzerprogramm Standardwerte mithilfe von **Standardprogrammen** festlegt, gilt die Standardeinstellung nur für diesen Benutzer und nicht für andere Benutzer, die den gleichen Computer verwenden können.</span><span class="sxs-lookup"><span data-stu-id="cd12d-110">When a user sets program defaults using **Default Programs**, the default setting applies only to that user and not to other users who might use the same computer.</span></span> <span data-ttu-id="cd12d-111">**Standardprogramme** bieten eine Reihe von APIs (in Windows 8 veraltet), mit denen unabhängige Softwarehersteller (ISVs) ihre Programme oder Anwendungen in das Standardsystem einbeziehen können.</span><span class="sxs-lookup"><span data-stu-id="cd12d-111">**Default Programs** provides a set of APIs (deprecated in Windows 8) that enable independent software vendors (ISVs) to include their programs or applications in the defaults system.</span></span> <span data-ttu-id="cd12d-112">Der API-Satz hilft ISVs bei der besseren Verwaltung Ihres Status als Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="cd12d-112">The API set also helps ISVs better manage their status as defaults.</span></span>

<span data-ttu-id="cd12d-113">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="cd12d-113">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="cd12d-114">Einführung in Standardprogramme und den zugehörigen API-Satz</span><span class="sxs-lookup"><span data-stu-id="cd12d-114">Introduction to Default Programs and Its Related API Set</span></span>](#introduction-to-default-programs-and-its-related-api-set)
-   [<span data-ttu-id="cd12d-115">Registrieren einer Anwendung für die Verwendung mit Standardprogrammen</span><span class="sxs-lookup"><span data-stu-id="cd12d-115">Registering an Application for Use with Default Programs</span></span>](#registering-an-application-for-use-with-default-programs)
    -   [<span data-ttu-id="cd12d-116">ProgIDs</span><span class="sxs-lookup"><span data-stu-id="cd12d-116">ProgIDs</span></span>](#progids)
    -   [<span data-ttu-id="cd12d-117">Registrierungs Unterschlüssel und Wert Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="cd12d-117">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
    -   [<span data-ttu-id="cd12d-118">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="cd12d-118">RegisteredApplications</span></span>](#registeredapplications)
    -   [<span data-ttu-id="cd12d-119">Beispiel für vollständige Registrierung</span><span class="sxs-lookup"><span data-stu-id="cd12d-119">Full Registration Example</span></span>](#full-registration-example)
-   [<span data-ttu-id="cd12d-120">Wird zum Standard Browser</span><span class="sxs-lookup"><span data-stu-id="cd12d-120">Becoming the Default Browser</span></span>](#becoming-the-default-browser)
-   [<span data-ttu-id="cd12d-121">Benutzeroberfläche von Standardprogrammen</span><span class="sxs-lookup"><span data-stu-id="cd12d-121">Default Programs UI</span></span>](#default-programs-ui)
-   [<span data-ttu-id="cd12d-122">Bewährte Methoden für die Verwendung von Standardprogrammen</span><span class="sxs-lookup"><span data-stu-id="cd12d-122">Best Practices for Using Default Programs</span></span>](#best-practices-for-using-default-programs)
    -   [<span data-ttu-id="cd12d-123">Während der Installation</span><span class="sxs-lookup"><span data-stu-id="cd12d-123">During Installation</span></span>](#during-installation)
    -   [<span data-ttu-id="cd12d-124">Nach der Installation</span><span class="sxs-lookup"><span data-stu-id="cd12d-124">After Installation</span></span>](#after-installation)
-   [<span data-ttu-id="cd12d-125">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cd12d-125">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="cd12d-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd12d-126">Related topics</span></span>](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a><span data-ttu-id="cd12d-127">Einführung in Standardprogramme und den zugehörigen API-Satz</span><span class="sxs-lookup"><span data-stu-id="cd12d-127">Introduction to Default Programs and Its Related API Set</span></span>

<span data-ttu-id="cd12d-128">**Standardprogramme** sind hauptsächlich für Anwendungen konzipiert, die Standard Dateitypen wie z. b. MP3-oder JPG-Dateien oder Standardprotokolle, wie z. b. http oder mailto, verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-128">**Default Programs** is primarily designed for applications that use standard file types such as .mp3 or .jpg files or standard protocols, such as HTTP or mailto.</span></span> <span data-ttu-id="cd12d-129">Anwendungen, die ihre eigenen proprietären Protokolle und Dateizuordnungen verwenden, verwenden in der Regel nicht die **Standard-Programm** Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="cd12d-129">Applications that use their own proprietary protocols and file associations do not typically use the **Default Programs** functionality.</span></span>

<span data-ttu-id="cd12d-130">Nachdem Sie eine Anwendung für die **Standardprogramm** Funktionalität registriert haben, sind die folgenden Optionen und Funktionen verfügbar, indem Sie den API-Satz verwenden:</span><span class="sxs-lookup"><span data-stu-id="cd12d-130">After you register an application for **Default Programs** functionality, the following options and functionality are available by using the API set:</span></span>

-   <span data-ttu-id="cd12d-131">Stellen Sie alle registrierten Standardwerte für eine Anwendung wieder her.</span><span class="sxs-lookup"><span data-stu-id="cd12d-131">Restore all registered defaults for an application.</span></span> <span data-ttu-id="cd12d-132">Veraltet für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cd12d-132">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="cd12d-133">Stellen Sie einen einzelnen registrierten Standardwert für eine Anwendung wieder her.</span><span class="sxs-lookup"><span data-stu-id="cd12d-133">Restore a single registered default for an application.</span></span> <span data-ttu-id="cd12d-134">Veraltet für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cd12d-134">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="cd12d-135">Fragen Sie den Besitzer eines bestimmten standardmäßig in einem einzelnen-Befehl ab, anstatt die Registrierung zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-135">Query for the owner of a specific default in a single call instead of searching the registry.</span></span> <span data-ttu-id="cd12d-136">Sie können den Standardwert einer Datei Zuordnung, eines Protokolls oder eines kanonischen Verbs im **Startmenü** Abfragen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-136">You can query for the default of a file association, protocol, or **Start** menu canonical verb.</span></span>
-   <span data-ttu-id="cd12d-137">Hiermit wird eine Benutzeroberfläche für eine bestimmte Anwendung gestartet, in der ein Benutzer individuelle Standardeinstellungen festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="cd12d-137">Launch a UI for a specific application where a user can set individual defaults.</span></span>
-   <span data-ttu-id="cd12d-138">Entfernen Sie alle Benutzer bezogenen Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-138">Remove all per-user associations.</span></span>

<span data-ttu-id="cd12d-139">**Standardprogramme** bieten außerdem eine Benutzeroberfläche, die Ihnen ermöglicht, eine Anwendung zu registrieren, um dem Benutzer zusätzliche Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-139">**Default Programs** also provides a UI that enables you to register an application in order to provide additional information to the user.</span></span> <span data-ttu-id="cd12d-140">Eine Digital signierte Anwendung kann z. b. eine URL zur Startseite des Herstellers enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd12d-140">For example, a digitally signed application can include a URL to the manufacturer's home page.</span></span>

<span data-ttu-id="cd12d-141">Die Verwendung des zugeordneten API-Satzes kann dazu beitragen, dass eine Anwendung unter der in Windows Vista eingeführten Benutzerkontensteuerung (User Account Control, UAC) ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="cd12d-141">Use of the associated API set can help an application function correctly under the user account control (UAC) feature introduced in Windows Vista.</span></span> <span data-ttu-id="cd12d-142">Unter UAC wird dem System ein Administrator als Standardbenutzer angezeigt, sodass der Administrator in der Regel nicht in die Unterstruktur des **\_ lokalen \_ HKEY** -Computers schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="cd12d-142">Under UAC, an administrator appears to the system as a standard user, so that administrator cannot typically write to the **HKEY\_LOCAL\_MACHINE** subtree.</span></span> <span data-ttu-id="cd12d-143">Diese Einschränkung ist ein Sicherheits Feature, das verhindert, dass ein Prozess als Administrator ohne das Wissen des Administrators fungiert.</span><span class="sxs-lookup"><span data-stu-id="cd12d-143">This restriction is a security feature that prevents a process from acting as an administrator without the administrator's knowledge.</span></span>

<span data-ttu-id="cd12d-144">Die Installation eines Programms durch einen Benutzer wird in der Regel als erhöhter Prozess ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-144">Installation of a program by a user is typically performed as an elevated process.</span></span> <span data-ttu-id="cd12d-145">Versuche einer Anwendung, das Standard Zuordnungs Verhalten auf Computer Ebene nach der Installation zu ändern, sind jedoch nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="cd12d-145">However, attempts by an application to modify default association behaviors at a machine level post-installation will be unsuccessful.</span></span> <span data-ttu-id="cd12d-146">Stattdessen müssen die Standardeinstellungen auf Benutzerebene registriert werden, wodurch verhindert wird, dass mehrere Benutzer die Standardwerte der anderen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="cd12d-146">Instead, defaults must be registered on a per-user level, which prevents multiple users from overwriting each other's defaults.</span></span>

<span data-ttu-id="cd12d-147">Die hierarchische Registrierungs Struktur für Datei-und Protokoll Zuordnungen hat Vorrang vor Standardeinstellungen auf Computer Ebene.</span><span class="sxs-lookup"><span data-stu-id="cd12d-147">The hierarchical registry structure for file and protocol associations gives precedence to per-user defaults over machine-level defaults.</span></span> <span data-ttu-id="cd12d-148">Einige Anwendungen enthalten Punkte in Ihrem Code, die ihre Rechte vorübergehend erhöhen, wenn Sie die Standardwerte für den **lokalen HKEY- \_ \_ Computer** beanspruchen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-148">Some applications include points in their code that temporarily elevate their rights when they claim defaults registered in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="cd12d-149">Diese Anwendungen können unerwartete Ergebnisse erleben, wenn eine andere Anwendung bereits als Standardbenutzer registriert ist.</span><span class="sxs-lookup"><span data-stu-id="cd12d-149">These applications might experience unexpected results if another application is already registered as the per-user default.</span></span> <span data-ttu-id="cd12d-150">Die Verwendung von **Standardprogrammen** verhindert diese Mehrdeutigkeit und garantiert die erwarteten Ergebnisse auf der Ebene pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="cd12d-150">Use of **Default Programs** prevents this ambiguity and guarantees expected results on a per-user level.</span></span>

## <a name="registering-an-application-for-use-with-default-programs"></a><span data-ttu-id="cd12d-151">Registrieren einer Anwendung für die Verwendung mit Standardprogrammen</span><span class="sxs-lookup"><span data-stu-id="cd12d-151">Registering an Application for Use with Default Programs</span></span>

<span data-ttu-id="cd12d-152">In diesem Abschnitt werden die Registrierungs Unterschlüssel und-Werte angezeigt, die zum Registrieren einer Anwendung mit **Standardprogrammen** benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-152">This section shows you the registry subkeys and values needed to register an application with **Default Programs**.</span></span> <span data-ttu-id="cd12d-153">Es enthält ein vollständiges Beispiel.</span><span class="sxs-lookup"><span data-stu-id="cd12d-153">It includes a full example.</span></span>

<span data-ttu-id="cd12d-154">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="cd12d-154">This section contains the following topics:</span></span>

-   [<span data-ttu-id="cd12d-155">ProgIDs</span><span class="sxs-lookup"><span data-stu-id="cd12d-155">ProgIDs</span></span>](#progids)
-   [<span data-ttu-id="cd12d-156">Registrierungs Unterschlüssel und Wert Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="cd12d-156">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
-   [<span data-ttu-id="cd12d-157">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="cd12d-157">RegisteredApplications</span></span>](#registeredapplications)
-   [<span data-ttu-id="cd12d-158">Beispiel für vollständige Registrierung</span><span class="sxs-lookup"><span data-stu-id="cd12d-158">Full Registration Example</span></span>](#full-registration-example)

<span data-ttu-id="cd12d-159">**Standardprogramme** erfordert, dass jede Anwendung explizit die Dateizuordnungen, MIME-Zuordnungen und Protokolle registriert, für die die Anwendung als möglicher Standard aufgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd12d-159">**Default Programs** requires each application to register explicitly the file associations, MIME associations, and protocols for which the application should be listed as a possible default.</span></span> <span data-ttu-id="cd12d-160">Sie registrieren die Zuordnungen mithilfe der folgenden Registrierungs Elemente, die später in diesem Thema unter [Registrierungs Unterschlüssel und Wert Beschreibungen](#registration-subkey-and-value-descriptions)ausführlich erläutert werden:</span><span class="sxs-lookup"><span data-stu-id="cd12d-160">You register the associations by using the following registry elements, which are explained in detail later in this topic under [Registration Subkey and Value Descriptions](#registration-subkey-and-value-descriptions):</span></span>

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

<span data-ttu-id="cd12d-161">Im folgenden Beispiel werden die Registrierungseinträge für einen fiktiven Ordner mit dem Namen Webbrowser angezeigt:</span><span class="sxs-lookup"><span data-stu-id="cd12d-161">The following example shows the registry entries for a fictional Contoso browser that is called WebBrowser:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a><span data-ttu-id="cd12d-162">ProgIDs</span><span class="sxs-lookup"><span data-stu-id="cd12d-162">ProgIDs</span></span>

<span data-ttu-id="cd12d-163">Eine Anwendung muss eine bestimmte [ProgID](fa-progids.md)bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-163">An application must provide a specific [ProgID](fa-progids.md).</span></span> <span data-ttu-id="cd12d-164">Stellen Sie sicher, dass Sie alle Informationen einschließen, die in der Regel in den generischen Standard Unterschlüssel für die Erweiterung geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-164">Be sure to include all the information that is typically written into the generic default subkey for the extension.</span></span> <span data-ttu-id="cd12d-165">Der fiktive Litware Media Player stellt z. b. die anwendungsspezifischen HKEY-Software Klassen für **\_ lokale \_ Computer** \\  \\  \\ **LitwarePlayer11.AssocFile.MP3** Unterschlüssel bereit.</span><span class="sxs-lookup"><span data-stu-id="cd12d-165">For example, the fictional Litware media player provides the application-specific **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**LitwarePlayer11.AssocFile.MP3** subkey.</span></span> <span data-ttu-id="cd12d-166">Dieser Unterschlüssel enthält alle Informationen im generischen Standard-Unterschlüssel **HKEY \_ local \_ Machine** \\ **Software** \\ **Classes** \\ **. MP3** sowie alle zusätzlichen Informationen, die von der Anwendung registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-166">That subkey includes all the information in the generic default subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\ **.mp3** plus any additional information that you want the application to register.</span></span> <span data-ttu-id="cd12d-167">Dadurch wird sichergestellt, dass die Informationen des Litware-Players, wenn der Benutzer die. MP3-Zuordnung wiederherstellt, intakt sind und nicht von einer anderen Anwendung überschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-167">This ensures that if the user restores the .mp3 association to the Litware player, the Litware player's information is intact and has not been overwritten by another application.</span></span> <span data-ttu-id="cd12d-168">(Überschreiben kann auftreten, wenn der Standard Unterschlüssel die einzige Quelle dieser Informationen ist.)</span><span class="sxs-lookup"><span data-stu-id="cd12d-168">(Overwriting might occur if the default subkey is the only source of that information.)</span></span>

<span data-ttu-id="cd12d-169">Wenn Sie eine ProgID einer Dateinamenerweiterung oder eines Protokolls zuordnen, kann eine Anwendung eins zu eins oder 1: n zuordnen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-169">When you map a ProgID to a file name extension or protocol, an application can map one-to-one or one-to-many.</span></span> <span data-ttu-id="cd12d-170">In CONSO Example zeigt condesohtml auf eine einzelne ProgID, die ShellExecute-Informationen für die Erweiterungen. htm,. html,. shtml,. xht und. XHTML bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-170">In the Contoso example, ContosoHTML points to a single ProgID that provides shellexecute information for the .htm, .html, .shtml, .xht, and .xhtml extensions.</span></span> <span data-ttu-id="cd12d-171">Da für jedes Protokoll eine andere ProgID vorhanden ist, aktivieren Sie bei Verwendung von Protokollen für jedes Protokoll eine eigene Ausführungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cd12d-171">Because a different ProgID exists for each protocol, when you use protocols you enable each protocol to have its own execution string.</span></span>

<span data-ttu-id="cd12d-172">Wenn Ihr MIME-Typ Inline in einem Browser angezeigt werden kann, muss die ProgID für den MIME-Typ den **CLSID** -Unterschlüssel enthalten, der den Klassen Bezeichner (CLSID) der entsprechenden Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd12d-172">When your MIME type can be viewed inline in a browser, the ProgID for the MIME type must contain the **CLSID** subkey that uses the class identifier (CLSID) of the corresponding application.</span></span> <span data-ttu-id="cd12d-173">Diese CLSID wird in einer Suche nach der CLSID in der MIME-Datenbank verwendet, die in **HKEY- \_ \_** \\ **Software** \\ **Klassen** der \\ **MIME**- \\ **Datenbank**- \\ **Inhaltstyp** gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="cd12d-173">This CLSID is used in a lookup against the CLSID in the MIME database that is stored in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**MIME**\\**Database**\\**Content Type**.</span></span> <span data-ttu-id="cd12d-174">Wenn Ihr MIME-Typ nicht als Inline in einem Browser angezeigt werden soll, kann dieser Schritt ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-174">If your MIME type is not intended to be viewed inline in a browser, this step can be omitted.</span></span>

### <a name="registration-subkey-and-value-descriptions"></a><span data-ttu-id="cd12d-175">Registrierungs Unterschlüssel und Wert Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="cd12d-175">Registration Subkey and Value Descriptions</span></span>

<span data-ttu-id="cd12d-176">In diesem Abschnitt werden die einzelnen Registrierungs Unterschlüssel und Werte beschrieben, die zum Registrieren einer Anwendung mit **Standardprogrammen** verwendet werden, wie zuvor veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="cd12d-176">This section describes the individual registry subkeys and values used in registering an application with **Default Programs**, as illustrated previously.</span></span>

### <a name="capabilities"></a><span data-ttu-id="cd12d-177">Funktionen</span><span class="sxs-lookup"><span data-stu-id="cd12d-177">Capabilities</span></span>

<span data-ttu-id="cd12d-178">Der Unterschlüssel **Funktionen** enthält alle **Standardprogramm** Informationen für eine bestimmte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cd12d-178">The **Capabilities** subkey contains all the **Default Programs** information for a specific application.</span></span> <span data-ttu-id="cd12d-179">Der Platzhalter "% applicationcapabilitypath%" bezieht sich auf den Registrierungs Pfad von **HKEY \_ Current \_ User** oder **HKEY \_ local \_ Machine** zum Unterschlüssel der Anwendungs **Funktionen** .</span><span class="sxs-lookup"><span data-stu-id="cd12d-179">The placeholder %ApplicationCapabilityPath% refers to the registry path from either **HKEY\_CURRENT\_USER** or **HKEY\_LOCAL\_MACHINE** to the application's **Capabilities** subkey.</span></span> <span data-ttu-id="cd12d-180">Dieser Unterschlüssel enthält die signifikanten Werte, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cd12d-180">This subkey contains the significant values shown in the following table.</span></span>



| <span data-ttu-id="cd12d-181">Wert</span><span class="sxs-lookup"><span data-stu-id="cd12d-181">Value</span></span>                  | <span data-ttu-id="cd12d-182">type</span><span class="sxs-lookup"><span data-stu-id="cd12d-182">Type</span></span>                       | <span data-ttu-id="cd12d-183">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cd12d-183">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd12d-184">ApplicationDescription</span><span class="sxs-lookup"><span data-stu-id="cd12d-184">ApplicationDescription</span></span> | <span data-ttu-id="cd12d-185">Reg \_ SZ oder reg \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="cd12d-185">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="cd12d-186">**Erforderlich**.</span><span class="sxs-lookup"><span data-stu-id="cd12d-186">**Required**.</span></span> <span data-ttu-id="cd12d-187">Damit ein Benutzer eine fundierte Standard Zuweisungs Auswahl treffen kann, muss eine Anwendung eine Zeichenfolge bereitstellen, die die Funktionen der Anwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-187">To enable a user to make an informed default assignment choice, an application must provide a string that describes the application's capabilities.</span></span> <span data-ttu-id="cd12d-188">Obwohl das vorherige Beispiel von "cationdescription" die Beschreibung direkt dem Wert "applicationdescription" zuweist, stellen Anwendungen die Beschreibung in der Regel als eine Ressource bereit, die in eine DLL-Datei eingebettet ist, um die Lokalisierung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-188">Although the previous Contoso example assigns the description directly to the ApplicationDescription value, applications typically provide the description as a resource that is embedded in a .dll file to facilitate localization.</span></span> <span data-ttu-id="cd12d-189">Wenn "applicationdescription" nicht angegeben wird, wird die Anwendung nicht in der Benutzeroberflächen Liste möglicher Standardprogramme angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-189">If ApplicationDescription is not provided, the application does not appear in UI lists of potential default programs.</span></span>                                                            |
| <span data-ttu-id="cd12d-190">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="cd12d-190">ApplicationName</span></span>        | <span data-ttu-id="cd12d-191">Reg \_ SZ oder reg \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="cd12d-191">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="cd12d-192">**Optional.**</span><span class="sxs-lookup"><span data-stu-id="cd12d-192">**Optional.**</span></span> <span data-ttu-id="cd12d-193">Der Name, mit dem das Programm in der Benutzeroberfläche der Standardprogramme angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cd12d-193">The name by which the program appears in the Default Programs UI.</span></span> <span data-ttu-id="cd12d-194">Wenn diese Daten nicht von der Anwendung bereitgestellt werden, wird der Name des ausführbaren Programms, das mit der ersten registrierten ProgID für die Anwendung verknüpft ist, in der Benutzeroberfläche verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd12d-194">If this data is not provided by the application, the name of the executable program that is associated with the first registered ProgID for the application is used in the UI.</span></span> <span data-ttu-id="cd12d-195">ApplicationName muss immer mit dem Namen identisch sein, der unter [RegisteredApplications](#registeredapplications)registriert ist.</span><span class="sxs-lookup"><span data-stu-id="cd12d-195">ApplicationName must always match the name that is registered under [RegisteredApplications](#registeredapplications).</span></span> <span data-ttu-id="cd12d-196">Sie können ApplicationName verwenden, wenn Sie möchten, dass verschiedene Anwendungs Typen, z. b. ein Browser und ein e-Mail-Client, auf dieselbe ausführbare Datei verweisen, während Sie als unterschiedliche Namen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-196">You can use ApplicationName if you want different application types, such as a browser and an email client, to point to the same executable file while they appear as different names.</span></span><br/> |
| <span data-ttu-id="cd12d-197">Ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="cd12d-197">Hidden</span></span>                 | <span data-ttu-id="cd12d-198">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="cd12d-198">REG\_DWORD</span></span>                 | <span data-ttu-id="cd12d-199">**Optional.**</span><span class="sxs-lookup"><span data-stu-id="cd12d-199">**Optional.**</span></span> <span data-ttu-id="cd12d-200">Legen Sie diesen Wert auf 1 fest, um die Anwendung aus der Liste der Programme im Dialogfeld " **Standardprogramme festlegen** " zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="cd12d-200">Set this value to 1 to suppress the application from the list of programs in the **Set your default programs** dialog.</span></span> <span data-ttu-id="cd12d-201">Wenn dieser Wert 0 oder nicht vorhanden ist, wird die Anwendung normal in der Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-201">If this value is 0 or not present, then the application appears in the list normally.</span></span>                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a><span data-ttu-id="cd12d-202">Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="cd12d-202">FileAssociations</span></span>

<span data-ttu-id="cd12d-203">Der Unterschlüssel **fileassociations** enthält bestimmte Dateizuordnungen, die von der Anwendung beansprucht werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-203">The **FileAssociations** subkey contains specific file associations that are claimed by the application.</span></span> <span data-ttu-id="cd12d-204">Diese Ansprüche werden als Werte mit einem Wert für jede Erweiterung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cd12d-204">These claims are stored as values, with one value for each extension.</span></span> <span data-ttu-id="cd12d-205">Zuordnungen zeigen auf eine anwendungsspezifische ProgID anstelle einer generischen ProgID.</span><span class="sxs-lookup"><span data-stu-id="cd12d-205">Associations point to an application-specific ProgID instead of a generic ProgID.</span></span> <span data-ttu-id="cd12d-206">Allerdings sind nicht alle Zuordnungen erforderlich, um auf dieselbe ProgID zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-206">However, all associations are not required to point to the same ProgID.</span></span>

### <a name="mimeassociations"></a><span data-ttu-id="cd12d-207">Fehlstellungen</span><span class="sxs-lookup"><span data-stu-id="cd12d-207">MIMEAssociations</span></span>

<span data-ttu-id="cd12d-208">Der Unterschlüssel **MIMEAssociations** enthält bestimmte MIME-Typen, die von der Anwendung beansprucht werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-208">The **MIMEAssociations** subkey contains specific MIME types that are claimed by the application.</span></span> <span data-ttu-id="cd12d-209">Diese Ansprüche werden als Werte mit einem Wert für jeden MIME-Typ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cd12d-209">These claims are stored as values, with one value for each MIME type.</span></span> <span data-ttu-id="cd12d-210">Der Wertname für jeden MIME-Typ muss exakt mit dem MIME-Namen übereinstimmen, der in der MIME-Datenbank gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="cd12d-210">The value name for each MIME type must exactly match the MIME name that is stored in the MIME database.</span></span> <span data-ttu-id="cd12d-211">Dem Wert muss außerdem eine anwendungsspezifische ProgID zugewiesen werden, die die entsprechende CLSID der Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="cd12d-211">The value must also be assigned an application-specific ProgID that contains the corresponding CLSID of the application.</span></span>

### <a name="startmenu"></a><span data-ttu-id="cd12d-212">Startmenü</span><span class="sxs-lookup"><span data-stu-id="cd12d-212">Startmenu</span></span>

<span data-ttu-id="cd12d-213">Der Unterschlüssel **Startmenu** ist den vom Benutzer zustellbaren **Internet** -und **e-Mail** -Einträgen im **Startmenü** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cd12d-213">The **Startmenu** subkey is associated with the user-assignable **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="cd12d-214">Eine Anwendung muss separat als Kandidat für diese Einträge registriert werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-214">An application must register separately as a contender for those entries.</span></span> <span data-ttu-id="cd12d-215">Weitere Informationen finden Sie unter [Registrieren von Programmen mit Client Typen](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="cd12d-215">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

> [!Note]  
> <span data-ttu-id="cd12d-216">Ab Windows 7 sind im **Startmenü** keine **Internet** -und **e-Mail-** Einträge mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-216">As of Windows 7, there are no longer **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="cd12d-217">Die dem **e-Mail-** Eintrag zugeordneten Registrierungsdaten werden weiterhin für den Standard-MAPI-Client verwendet, aber die mit dem **Internet** Eintrag verknüpften Registrierungsdaten werden von Windows überhaupt nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd12d-217">The registry data associated with the **E-mail** entry is still used for the default MAPI client, but the registry data associated with the **Internet** entry is not used by Windows at all.</span></span>

 

<span data-ttu-id="cd12d-218">Indem die Registrierung einer Anwendung im **Startmenü** mit der Registrierung der **Standardprogramme** verknüpft wird, wird die Anwendung als potenzieller Standardwert in der Benutzeroberfläche der **Set-Zuordnungen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-218">By associating the **Start** menu registration of an application with its **Default Programs** registration, the application appears as a potential default in the **Set associations** UI.</span></span> <span data-ttu-id="cd12d-219">Wenn der Benutzer die Anwendung als Standard ausgewählt hat und anschließend alle Anwendungs Standardwerte später wiederherstellen möchten, wird die Anwendung für diesen Benutzer an der **Start** Menü Position wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-219">If the user has chosen the application as the default and then chooses to restore all application defaults later, the application is restored to its **Start** menu position for that user.</span></span> <span data-ttu-id="cd12d-220">Weitere Informationen und eine Abbildung finden Sie im Abschnitt [default Programme UI](#default-programs-ui) weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="cd12d-220">For more information and an illustration, see the [Default Programs UI](#default-programs-ui) section later in this topic.</span></span>

<span data-ttu-id="cd12d-221">Der Unterschlüssel **Startmenu** hat zwei Einträge: StartMenuInternet und Mail, die den kanonischen **Internet** -und **e-Mail-** Positionen im **Startmenü** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-221">The **Startmenu** subkey has two entries: StartMenuInternet and Mail, which correspond to the canonical **Internet** and **E-mail** positions in the **Start** menu.</span></span> <span data-ttu-id="cd12d-222">Eine Anwendung weist entweder StartMenuInternet oder Mail einen Wert zu, der dem Namen des registrierten unter Schlüssels der Anwendung unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **StartMenuInternet** oder **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **Mail** entspricht (wie unter [Registrieren von Programmen mit Client Typen](reg-middleware-apps.md)beschrieben).</span><span class="sxs-lookup"><span data-stu-id="cd12d-222">An application assigns either StartMenuInternet or Mail a value equal to the name of the application's registered subkey under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** or **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** (as described in [Registering Programs with Client Types](reg-middleware-apps.md)).</span></span>

<span data-ttu-id="cd12d-223">Wenn die kanonische **e-Mail-** Position im **Startmenü** angezeigt wird, stellt Sie den Standard-MAPI-Client dar und wird daher als fähig angenommen, MAPI-Aufrufe zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="cd12d-223">In the case of the **E-mail** canonical position in the **Start** menu, it represents the default MAPI client and is therefore assumed capable of handing MAPI calls.</span></span> <span data-ttu-id="cd12d-224">Wenn im **Startmenü** unter Windows 7 keine kanonische **e-Mail-** Position mehr vorhanden ist, wird dieser Unterschlüssel weiterhin für den standardmäßigen MAPI-Client verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd12d-224">Under Windows 7, while there is no longer an **E-mail** canonical position in the **Start** menu, this subkey continues to be used for the default MAPI client.</span></span> <span data-ttu-id="cd12d-225">Eine Anwendung, die den Standardwert für die e-Mail beansprucht, sollte sich als MAPI-Handler unter dem folgenden Unterschlüssel registrieren:</span><span class="sxs-lookup"><span data-stu-id="cd12d-225">An application claiming the mail default should register as a MAPI handler under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

<span data-ttu-id="cd12d-226">Wenn ein e-Mail-Client MAPI nicht unterstützen kann, aber immer noch für die kanonische Position des **Startmenü** **-e-Mail-** Supports kämpfen möchte, kann er eine Befehlszeile unter folgendem Unterschlüssel registrieren</span><span class="sxs-lookup"><span data-stu-id="cd12d-226">If a mail client cannot support MAPI but still wants to contend for the **Start** menu **E-mail** canonical position, it can register a command line under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

<span data-ttu-id="cd12d-227">Fügen Sie außerdem unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Clients** \\ **Mail** \\ *CanonicalName* einen Standardwert mit dem Anwendungsnamen hinzu.</span><span class="sxs-lookup"><span data-stu-id="cd12d-227">Also, under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**\\*CanonicalName* add a default value with the application name.</span></span>

<span data-ttu-id="cd12d-228">Diese Einträge ermöglichen das Starten der Anwendung über die **e-Mail-** Position des **Start** Menüs.</span><span class="sxs-lookup"><span data-stu-id="cd12d-228">These entries allow the application to be launched from the **Start** menu's **E-mail** position.</span></span> <span data-ttu-id="cd12d-229">Beachten Sie, dass MAPI-Aufrufe weiterhin an der Anwendung vorgenommen werden und entweder auf den vorherigen MAPI-Handler zugreifen oder einen Fehler erzeugen, wenn kein MAPI-Handler festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="cd12d-229">Note that MAPI calls are still made to the application, and either fall through to the prior MAPI handler, or fail if no MAPI handler has been set.</span></span> <span data-ttu-id="cd12d-230">Weitere Informationen finden Sie unter [Registrieren von Programmen mit Client Typen](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="cd12d-230">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

### <a name="urlassociations"></a><span data-ttu-id="cd12d-231">Urlzuordnungen</span><span class="sxs-lookup"><span data-stu-id="cd12d-231">UrlAssociations</span></span>

<span data-ttu-id="cd12d-232">Der **UrlAssociations** -Unterschlüssel enthält die spezifischen URL-Protokolle, die von der Anwendung beansprucht werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-232">The **UrlAssociations** subkey contains the specific URL protocols that are claimed by the application.</span></span> <span data-ttu-id="cd12d-233">Diese Ansprüche werden als Werte mit einem Wert für jedes Protokoll gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cd12d-233">These claims are stored as values, with one value for each protocol.</span></span> <span data-ttu-id="cd12d-234">Jedes Protokoll muss auf eine anwendungsspezifische ProgID anstelle einer generischen ProgID zeigen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-234">Each protocol must point to an application-specific ProgID instead of to a generic ProgID.</span></span> <span data-ttu-id="cd12d-235">Wie im Beispiel "" von "" in "" von "", können Sie für jedes Protokoll eine andere ProgID verwenden, damit jede eine eigene Ausführungs Zeichenfolge hat.</span><span class="sxs-lookup"><span data-stu-id="cd12d-235">As mentioned in the Contoso example, you can use a different ProgID for each protocol in order for each to have its own execution string.</span></span>

### <a name="registeredapplications"></a><span data-ttu-id="cd12d-236">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="cd12d-236">RegisteredApplications</span></span>

<span data-ttu-id="cd12d-237">Der vollständige Unterschlüssel für **RegisteredApplications** lautet:</span><span class="sxs-lookup"><span data-stu-id="cd12d-237">The full subkey for **RegisteredApplications** is:</span></span>

<span data-ttu-id="cd12d-238">**HKEY \_ \_** \\ **Software**- \\ **RegisteredApplications** für lokale Computer</span><span class="sxs-lookup"><span data-stu-id="cd12d-238">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**RegisteredApplications**</span></span>

<span data-ttu-id="cd12d-239">Dieser Unterschlüssel stellt dem Betriebssystem den Registrierungs Speicherort der **Standardprogramm** Informationen für die Anwendung bereit.</span><span class="sxs-lookup"><span data-stu-id="cd12d-239">This subkey provides the operating system with the registry location of the **Default Programs** information for the application.</span></span> <span data-ttu-id="cd12d-240">Der Speicherort wird als Wert gespeichert, dessen Name dem Namen der Anwendung entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="cd12d-240">The location is stored as a value whose name must match the name of the application.</span></span>

### <a name="full-registration-example"></a><span data-ttu-id="cd12d-241">Beispiel für vollständige Registrierung</span><span class="sxs-lookup"><span data-stu-id="cd12d-241">Full Registration Example</span></span>

<span data-ttu-id="cd12d-242">Dieses Beispiel zeigt die Unterschlüssel und Werte, die beim Registrieren des fiktiven Litware Media Player verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-242">This example shows the subkeys and values that are used in registering the fictional Litware media player.</span></span> <span data-ttu-id="cd12d-243">Das Beispiel enthält die ProgID-Einträge, um zu zeigen, wie alles zueinander passt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-243">The example includes the ProgID entries in order to show how it all fits together.</span></span>

<span data-ttu-id="cd12d-244">Der folgende Unterschlüssel zeigt die anwendungsspezifische ProgID für den. MP3-MIME-Typ:</span><span class="sxs-lookup"><span data-stu-id="cd12d-244">The following subkey shows the application-specific ProgID for the .mp3 MIME type:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

<span data-ttu-id="cd12d-245">Als nächstes ist die anwendungsspezifische ProgID, die das Litware-Programm der Dateinamenerweiterung ". MP3" zuordnet.</span><span class="sxs-lookup"><span data-stu-id="cd12d-245">Next is the application-specific ProgID that associates the Litware program with the .mp3 file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="cd12d-246">In den nächsten Einträgen wird die kombinierte ProgID sowohl für den MIME-Typ (. MPEG) als auch für die Dateinamenerweiterung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-246">The next entries show the combined ProgID for both the .mpeg MIME type and file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="cd12d-247">Mit den nächsten Einträgen wird das Litware-Programm in **Standardprogrammen** registriert und die zuvor registrierten ProgIDs verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd12d-247">The next entries register the Litware program in **Default Programs** and use the previously registered ProgIDs</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

<span data-ttu-id="cd12d-248">Schließlich wird in diesem Beispiel der Speicherort der Litware- **Standardprogramm** Registrierung registriert.</span><span class="sxs-lookup"><span data-stu-id="cd12d-248">Lastly, this example registers the location of the Litware **Default Programs** registration.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a><span data-ttu-id="cd12d-249">Wird zum Standard Browser</span><span class="sxs-lookup"><span data-stu-id="cd12d-249">Becoming the Default Browser</span></span>

<span data-ttu-id="cd12d-250">Die Browser Registrierung muss den in diesem Thema beschriebenen bewährten Methoden entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-250">Browser registration must follow the best practices outlined in this topic.</span></span> <span data-ttu-id="cd12d-251">Wenn der Browser installiert ist, kann Windows dem Benutzer eine System Benachrichtigung präsentieren, über die der Benutzer den Browser als System Standard auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="cd12d-251">When the browser is installed, Windows can present the user with a system notification through which the user can select the browser as the system default.</span></span> <span data-ttu-id="cd12d-252">Diese Benachrichtigung wird angezeigt, wenn die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="cd12d-252">This notification is shown when these conditions are met:</span></span>

-   <span data-ttu-id="cd12d-253">Der Installer des Browsers ruft [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) mit dem Flag **shcne \_ assocchanged** auf, um Windows mitzuteilen, dass neue Protokollhandler registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-253">The browser's installer calls [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the **SHCNE\_ASSOCCHANGED** flag to tell Windows that new protocol handlers have been registered.</span></span>
-   <span data-ttu-id="cd12d-254">Windows erkennt, dass eine oder mehrere neue Anwendungen registriert wurden, um sowohl die http://-als auch die https://-Protokolle zu verarbeiten, und der Benutzer wurde noch nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-254">Windows detects that one or more new applications have registered to handle both http:// and https:// protocols, and the user has not yet been notified.</span></span> <span data-ttu-id="cd12d-255">Das heißt, dass dem Benutzer keine der folgenden Elemente angezeigt wird: eine System Benachrichtigung, die die Anwendung sendet, ein openWith Flyout, das die Anwendung enthält, oder die System Steuerungs Seite "Benutzer Standards festlegen (Sud)" für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cd12d-255">In other words, none of the following have been shown to the user: a system notification advertising the application, an OpenWith flyout that contains the application, or the Set User Defaults (SUD) Control Panel page for the application.</span></span>

<span data-ttu-id="cd12d-256">Das folgende Beispiel zeigt den empfohlenen Registrierungscode, den der Installer des Browsers ausführen muss, nachdem er seine Registrierungsschlüssel geschrieben hat.</span><span class="sxs-lookup"><span data-stu-id="cd12d-256">The following example shows the recommended registration code that the browser's installer should run after it writes its registry keys.</span></span>

<span data-ttu-id="cd12d-257">" [**Shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) " benachrichtigt das System zunächst, dass neue Zuordnungs Optionen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="cd12d-257">[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) first notifies the system that new association choices are available.</span></span> <span data-ttu-id="cd12d-258">Der **shchangenotify** -Befehl ist erforderlich, um die ordnungsgemäße Funktionsweise von System Standardwerten sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-258">The **SHChangeNotify** call is required to ensure the proper functioning of system defaults.</span></span>

<span data-ttu-id="cd12d-259">Eine [**Standby**](/windows/win32/api/synchapi/nf-synchapi-sleep) -Anweisung ermöglicht dann Zeit für System Prozesse, die Benachrichtigung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="cd12d-259">A [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) statement then allows time for system processes to handle the notification.</span></span>


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



<span data-ttu-id="cd12d-260">Wenn der Benutzer die sich ergebende Benachrichtigung oder das resultierende Flyout ignoriert oder ignoriert, ohne eine neue Standardbrowser Auswahl vorzunehmen, bleibt der Standardbrowser unverändert.</span><span class="sxs-lookup"><span data-stu-id="cd12d-260">If the user dismisses or ignores the resulting notification or flyout without making a new default browser selection, the default browser remains unchanged.</span></span> <span data-ttu-id="cd12d-261">Beachten Sie, dass der Benutzer den Standardbrowser jederzeit über andere Mechanismen ändern kann, einschließlich der Einstellung Benutzer Standardwerte in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="cd12d-261">Note that the user can also change the default browser at any time through other mechanisms, including Set User Defaults in the Control Panel.</span></span>

## <a name="default-programs-ui"></a><span data-ttu-id="cd12d-262">Benutzeroberfläche von Standardprogrammen</span><span class="sxs-lookup"><span data-stu-id="cd12d-262">Default Programs UI</span></span>

<span data-ttu-id="cd12d-263">Die Abbildungen in diesem Abschnitt zeigen die Benutzeroberfläche für **Standardprogramme** , wie Sie der Benutzer sehen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-263">The illustrations in this section show the UI for **Default Programs** as seen by the user.</span></span>

<span data-ttu-id="cd12d-264">Die folgende Abbildung zeigt das Hauptfenster " **Programme** " in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="cd12d-264">The following illustration shows the main **Default Programs** window in Control Panel.</span></span>

![Screenshot der Seite "Standardprogramme-Eintrag"](images/defaultprogramsmain.png)

<span data-ttu-id="cd12d-266">Wenn ein Benutzer die Option **Standardprogramme festlegen** auswählt, wird das folgende Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-266">When a user chooses the **Set your default programs** option, the following window appears.</span></span> <span data-ttu-id="cd12d-267">Benutzer können diese Seite verwenden, um ein Standardprogramm für alle Dateitypen und Protokolle zuzuweisen, für die das Programm eine mögliche Standardeinstellung ist.</span><span class="sxs-lookup"><span data-stu-id="cd12d-267">Users can use this page to assign a default program for all file types and protocols for which the program is a possible default.</span></span> <span data-ttu-id="cd12d-268">Wie in der folgenden Abbildung gezeigt, werden alle [registrierten](#registering-an-application-for-use-with-default-programs) Programme und das Programmsymbol auf der linken Seite im Feld **Programme** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-268">As shown in the following illustration, all [registered](#registering-an-application-for-use-with-default-programs) programs and the program icon appear in the **Programs** box on the left.</span></span>

![Screenshot der Seite "Festlegen der Standardprogramme"](images/setyourdefaultprograms.png)

<span data-ttu-id="cd12d-270">Wenn der Benutzer ein Programm aus der Liste auswählt, werden das Programmsymbol und der Anbieter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-270">When the user selects a program from the list, the program icon and provider are displayed.</span></span> <span data-ttu-id="cd12d-271">Wenn die URL in das Digital signierte Zertifikat des Programms eingebettet ist, kann das Programm auch eine URL anzeigen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-271">If the URL is embedded in the program's digitally signed certificate, the program can also display a URL.</span></span> <span data-ttu-id="cd12d-272">Programme, die nicht digital signiert sind, können keine URL anzeigen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-272">Programs that are not digitally signed cannot display a URL.</span></span>

<span data-ttu-id="cd12d-273">Ein beschreibender Text, der vom Programm während der Registrierung bereitgestellt wird, wird ebenfalls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-273">Descriptive text, which is supplied by the program during registration, is also displayed.</span></span> <span data-ttu-id="cd12d-274">Dieser Text ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cd12d-274">This text is required.</span></span> <span data-ttu-id="cd12d-275">Unter dem Feld Beschreibung finden Sie einen Hinweis darauf, wie viele Standardwerte dem Programm derzeit von der vollständigen Nummer zugewiesen werden, die für die Verarbeitung registriert ist.</span><span class="sxs-lookup"><span data-stu-id="cd12d-275">Beneath the description box is an indication of how many defaults the program is currently assigned out of the full number it is registered to handle.</span></span>

<span data-ttu-id="cd12d-276">Wenn Sie ein Programm als Standard für alle Dateien und Protokolle zuweisen oder wiederherstellen möchten, für die es registriert ist, klickt der Benutzer auf die Option **dieses Programm als Standard festlegen** .</span><span class="sxs-lookup"><span data-stu-id="cd12d-276">To assign or restore a program as the default for all files and protocols for which it is registered, the user clicks the **Set this program as default** option.</span></span>

<span data-ttu-id="cd12d-277">Um einzelne Dateitypen und Protokolle einem Programm zuzuweisen, klickt der Benutzer auf die Option **Standardwerte für dieses Programm auswählen** , die eine **Gruppe von Zuordnungen für ein Programm** Fenster anzeigt, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-277">To assign individual file types and protocols to a program, the user clicks the **Choose defaults for this program** option, which displays a **Set associations for a program** window like the one in the following illustration.</span></span>

> [!Note]  
> <span data-ttu-id="cd12d-278">Es wird empfohlen, dass Sie die **Set-Zuordnungen für ein Programm** mithilfe von [**iapplicationassociationregistrationui:: launchadvancedassociationui**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-278">We recommend you call the **Set associations for a program** by using [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span></span>

 

![Screenshot der Seite "Sätze für ein Programm festlegen"](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a><span data-ttu-id="cd12d-280">Bewährte Methoden für die Verwendung von Standardprogrammen</span><span class="sxs-lookup"><span data-stu-id="cd12d-280">Best Practices for Using Default Programs</span></span>

<span data-ttu-id="cd12d-281">Dieser Abschnitt enthält bewährte Methoden für die Verwendung von **Standardprogrammen** beim Registrieren von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-281">This section provides best practice guidelines for using **Default Programs** when you register applications.</span></span> <span data-ttu-id="cd12d-282">Außerdem bietet es Entwurfsvorschläge zum Erstellen einer Anwendung, die den Benutzern optimale **Standardprogramm** Funktionen bietet.</span><span class="sxs-lookup"><span data-stu-id="cd12d-282">It also offers design suggestions for creating an application that provides users with optimal **Default Programs** functionality.</span></span>

### <a name="during-installation"></a><span data-ttu-id="cd12d-283">Während der Installation</span><span class="sxs-lookup"><span data-stu-id="cd12d-283">During Installation</span></span>

<span data-ttu-id="cd12d-284">Zusätzlich zu den Installations Prozeduren, die normalerweise unter Windows XP ausgeführt werden, muss eine auf Windows Vista oder höher basierende Anwendung mit der **Standardprogramm** Funktion registriert werden, um von den Funktionen zu profitieren.</span><span class="sxs-lookup"><span data-stu-id="cd12d-284">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista or later based application must register with the **Default Programs** feature to take advantage of its functionality.</span></span>

<span data-ttu-id="cd12d-285">Führen Sie die folgenden Schritte während der Installation aus.</span><span class="sxs-lookup"><span data-stu-id="cd12d-285">Perform the following sequence of steps during installation.</span></span> <span data-ttu-id="cd12d-286">Die Schritte 1-3 entsprechen den Schritten, die in Windows XP verwendet wurden. Schritt 4 war neu in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cd12d-286">Steps 1-3 match the steps that were used in Windows XP; step 4 was new in Windows Vista.</span></span>

1.  <span data-ttu-id="cd12d-287">Installieren Sie die erforderlichen Binärdateien.</span><span class="sxs-lookup"><span data-stu-id="cd12d-287">Install the necessary binary files.</span></span>
2.  <span data-ttu-id="cd12d-288">Schreiben Sie ProgIDs auf den lokalen HKEY- \_ \_ Computer.</span><span class="sxs-lookup"><span data-stu-id="cd12d-288">Write ProgIDs to HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="cd12d-289">Beachten Sie, dass Anwendungen anwendungsspezifische ProgIDs für Ihre Zuordnungen erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-289">Note that applications must create application-specific ProgIDs for their associations.</span></span>
3.  <span data-ttu-id="cd12d-290">Registrieren Sie die Anwendung mit **Standardprogrammen** , wie zuvor in [Registrieren einer Anwendung für die Verwendung mit Standardprogrammen](#registering-an-application-for-use-with-default-programs)erläutert.</span><span class="sxs-lookup"><span data-stu-id="cd12d-290">Register the application with **Default Programs** as previously explained in [Registering an Application for Use with Default Programs](#registering-an-application-for-use-with-default-programs).</span></span>

### <a name="after-installation"></a><span data-ttu-id="cd12d-291">Nach der Installation</span><span class="sxs-lookup"><span data-stu-id="cd12d-291">After Installation</span></span>

<span data-ttu-id="cd12d-292">In diesem Abschnitt wird erläutert, wie die Anwendungs Aufforderung den einzelnen Benutzern zuerst die Standardoptionen präsentieren sollte.</span><span class="sxs-lookup"><span data-stu-id="cd12d-292">This section discusses how the application prompt should first present its default options to each user.</span></span> <span data-ttu-id="cd12d-293">Außerdem wird erläutert, wie eine Anwendung ihren Status als Standardwert für die möglichen Zuordnungen und Protokolle überwachen kann.</span><span class="sxs-lookup"><span data-stu-id="cd12d-293">It also discusses how an application can monitor its status as the default for its possible associations and protocols.</span></span>

### <a name="first-run-experiences"></a><span data-ttu-id="cd12d-294">Erfahrung beim ersten Ausführen</span><span class="sxs-lookup"><span data-stu-id="cd12d-294">First Run Experiences</span></span>

<span data-ttu-id="cd12d-295">Wenn die Anwendung zum ersten Mal von einem Benutzer ausgeführt wird, wird empfohlen, dass die Anwendung die Benutzeroberfläche für den Benutzer anzeigt, der normalerweise diese beiden Optionen umfasst:</span><span class="sxs-lookup"><span data-stu-id="cd12d-295">When the application is run by a user for the first time, it is recommended that the application display UI to the user that typically includes these two choices:</span></span>

-   <span data-ttu-id="cd12d-296">Akzeptieren Sie die Standard Anwendungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-296">Accept the default application settings.</span></span> <span data-ttu-id="cd12d-297">Diese Option ist standardmäßig ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-297">This option is selected by default.</span></span>
-   <span data-ttu-id="cd12d-298">Passen Sie die Standard Anwendungseinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="cd12d-298">Customize the default application settings.</span></span>

<span data-ttu-id="cd12d-299">Wenn der Benutzer vor Windows 8 die Standardeinstellungen annimmt, ruft die Anwendung [**iapplicationassociationregistration:: setappasdefaultall**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall)auf, bei der alle während der Installation deklarierten Zuordnungen auf Computer Ebene für diesen Benutzer in benutzerspezifische Einstellungen konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-299">Prior to Windows 8, if the user accepts the default settings, your application calls [**IApplicationAssociationRegistration::SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), which converts all machine-level associations that are declared during installation to per-user settings for that user.</span></span>

<span data-ttu-id="cd12d-300">Wenn sich der Benutzer entscheidet, die Einstellungen anzupassen, ruft die Anwendung [**iapplicationassociationregistrationui:: launchadvancedassociationui**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) auf, um die Benutzeroberfläche der Datei Zuordnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-300">If the user decides to customize the settings, your application calls [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) to display the file association UI.</span></span> <span data-ttu-id="cd12d-301">Die folgende Abbildung zeigt dieses Fenster für den fiktiven Litware Media Player.</span><span class="sxs-lookup"><span data-stu-id="cd12d-301">The following illustration shows this window for the fictional Litware media player.</span></span>

![Screenshot der Seite "Zuordnungen für ein Programm festlegen" für Litware](images/setassociationsforaprogramforlitware.png)

<span data-ttu-id="cd12d-303">Das Fenster Datei Zuordnung zeigt die Standardwerte an, die die Anwendung registriert hat, und zeigt außerdem den aktuellen Standardwert für andere Erweiterungen und Protokolle an.</span><span class="sxs-lookup"><span data-stu-id="cd12d-303">The file association window shows the defaults that the application registered and also shows the current default for other extensions and protocols.</span></span> <span data-ttu-id="cd12d-304">Nachdem der Benutzer seine Standardeinstellungen angepasst hat, klicken Sie auf die Schaltfläche **Speichern** , um die Änderungen zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-304">After the user finishes customizing their defaults, they click the **Save** button to commit the changes.</span></span> <span data-ttu-id="cd12d-305">Wenn der Benutzer auf **Abbrechen** klickt, wird das Fenster geschlossen, ohne die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="cd12d-305">If the user clicks **Cancel**, the window closes without saving changes.</span></span>

<span data-ttu-id="cd12d-306">Sie sollten diese Benutzeroberfläche für Ihre Anwendungen verwenden, anstatt ihre eigenen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-306">You should use this UI for your applications instead of creating your own.</span></span> <span data-ttu-id="cd12d-307">Auf diese Weise können Sie die Ressourcen speichern, die zuvor zum Entwickeln der Benutzeroberfläche für die Datei Zuordnung benötigt wurden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-307">By doing so, you save the resources that were previously required to develop file association UI.</span></span> <span data-ttu-id="cd12d-308">Außerdem gewährleisten Sie, dass Zuordnungen ordnungsgemäß gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-308">You also guarantee that associations are saved correctly.</span></span>

### <a name="set-an-application-to-check-whether-it-is-the-default"></a><span data-ttu-id="cd12d-309">Festlegen einer Anwendung, um zu überprüfen, ob Sie die Standardeinstellung ist</span><span class="sxs-lookup"><span data-stu-id="cd12d-309">Set an Application to Check Whether It Is the Default</span></span>

> [!Note]  
> <span data-ttu-id="cd12d-310">Dies wird ab Windows 8 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd12d-310">This is no longer supported as of Windows 8.</span></span>

 

<span data-ttu-id="cd12d-311">Anwendungen überprüfen in der Regel, ob Sie als Standard festgelegt werden, wenn Sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-311">Applications typically check whether they are set as the default when they are run.</span></span> <span data-ttu-id="cd12d-312">Legen Sie Ihre Anwendungen so fest, dass diese Überprüfung durch Aufrufen von " [**iapplicationassociationregistration:: queryappisdefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) " oder " [**iapplicationassociationregistration:: queryappisdefaultall**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall)" durchführen wird.</span><span class="sxs-lookup"><span data-stu-id="cd12d-312">Set your applications to make this check by calling [**IApplicationAssociationRegistration::QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) or [**IApplicationAssociationRegistration::QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span></span>

<span data-ttu-id="cd12d-313">Wenn die Anwendung feststellt, dass es sich nicht um die Standardeinstellung handelt, kann Sie die Benutzeroberfläche zur Verfügung stellen, die den Benutzer auffordert, ob Sie die aktuelle Situation akzeptieren oder die Anwendung als Standard festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="cd12d-313">If the application determines that it is not the default, it can present UI that asks the user whether to accept the current situation or to make the application the default.</span></span> <span data-ttu-id="cd12d-314">Fügen Sie in dieser Benutzeroberfläche immer ein Kontrollkästchen ein, das standardmäßig ausgewählt ist und die Option anzeigt, dass die Option nicht erneut angefordert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd12d-314">Always include a check box in this UI that is selected by default and that presents the option not to be asked again.</span></span>

> [!Note]  
> <span data-ttu-id="cd12d-315">Der Standardwert sollte vom Benutzer gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="cd12d-315">The choice of default should be user driven.</span></span> <span data-ttu-id="cd12d-316">Eine Anwendung sollte niemals einen Standardwert freigeben, ohne den Benutzer zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="cd12d-316">An application should never reclaim a default without asking the user.</span></span>

 

<span data-ttu-id="cd12d-317">Die folgende Abbildung zeigt ein Beispiel Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="cd12d-317">The following illustration shows an example dialog box.</span></span>

![Screenshot eines Beispiel Dialogfelds](images/notthedefaultui.png)

## <a name="additional-resources"></a><span data-ttu-id="cd12d-319">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cd12d-319">Additional Resources</span></span>

-   [<span data-ttu-id="cd12d-320">**Iapplicationassociationregistration**</span><span class="sxs-lookup"><span data-stu-id="cd12d-320">**IApplicationAssociationRegistration**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [<span data-ttu-id="cd12d-321">**Iapplicationassociationregistrationui**</span><span class="sxs-lookup"><span data-stu-id="cd12d-321">**IApplicationAssociationRegistrationUI**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a><span data-ttu-id="cd12d-322">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd12d-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd12d-323">Bewährte Methoden für Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="cd12d-323">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="cd12d-324">Beispielszenario für Datei Zuordnung</span><span class="sxs-lookup"><span data-stu-id="cd12d-324">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="cd12d-325">Richtlinien für die Verwaltung von Standardanwendungen in Windows Vista und höher</span><span class="sxs-lookup"><span data-stu-id="cd12d-325">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="cd12d-326">Festlegen des Programm Zugriffs und der Computer Standardwerte (SPAD)</span><span class="sxs-lookup"><span data-stu-id="cd12d-326">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
