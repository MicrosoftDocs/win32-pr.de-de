---
description: In diesem Thema wird erläutert, wie Anwendungen Informationen über sich selbst verfügbar machen können, um bestimmte Szenarien zu ermöglichen.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Anwendungs Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857e96893d2fe717f1a4939d06c77af043ead318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958777"
---
# <a name="application-registration"></a><span data-ttu-id="e516b-103">Anwendungs Registrierung</span><span class="sxs-lookup"><span data-stu-id="e516b-103">Application Registration</span></span>

<span data-ttu-id="e516b-104">In diesem Thema wird erläutert, wie Anwendungen Informationen über sich selbst verfügbar machen können, um bestimmte Szenarien zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e516b-104">This topic discusses how applications can expose information about themselves necessary to enable certain scenarios.</span></span> <span data-ttu-id="e516b-105">Dies umfasst Informationen, die erforderlich sind, um die Anwendung zu finden, die von der Anwendung unterstützten Verben und die Dateitypen, die von einer Anwendung verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="e516b-105">This includes information needed to locate the application, the verbs that the application supports and the types of files that an application can handle.</span></span>

<span data-ttu-id="e516b-106">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="e516b-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e516b-107">Suchen einer ausführbaren Datei der Anwendung</span><span class="sxs-lookup"><span data-stu-id="e516b-107">Finding an Application Executable</span></span>](#finding-an-application-executable)
-   [<span data-ttu-id="e516b-108">Anwendungen werden registriert</span><span class="sxs-lookup"><span data-stu-id="e516b-108">Registering Applications</span></span>](#registering-applications)
    -   [<span data-ttu-id="e516b-109">Verwenden des unter Schlüssels für App-Pfade</span><span class="sxs-lookup"><span data-stu-id="e516b-109">Using the App Paths Subkey</span></span>](#using-the-app-paths-subkey)
    -   [<span data-ttu-id="e516b-110">Verwenden des unter Schlüssels "Anwendungen"</span><span class="sxs-lookup"><span data-stu-id="e516b-110">Using the Applications Subkey</span></span>](#using-the-applications-subkey)
-   [<span data-ttu-id="e516b-111">Registrieren von Verben und anderen Datei Zuordnungs Informationen</span><span class="sxs-lookup"><span data-stu-id="e516b-111">Registering Verbs and Other File Association Information</span></span>](#registering-verbs-and-other-file-association-information)
-   [<span data-ttu-id="e516b-112">Registrieren eines erkannten Typs</span><span class="sxs-lookup"><span data-stu-id="e516b-112">Registering a Perceived Type</span></span>](#registering-a-perceived-type)
-   [<span data-ttu-id="e516b-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e516b-113">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="e516b-114">Anwendungen können auch in den Einstellungen "Programm Zugriff und Computer Standards festlegen" (SPAD) registriert und die System Steuerungsanwendungen für die Standardprogramme (SYDP) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e516b-114">Applications can also be registered in the Set Program Access and Computer Defaults (SPAD) and Set Your Default Programs (SYDP) control panel applications.</span></span> <span data-ttu-id="e516b-115">Informationen zur Registrierung von SPAD-und SYDP-Anwendungen finden Sie unter [Richtlinien für Dateizuordnungen und Standardprogramme](appguide-fa-defpro.md)und [Festlegen des Programm Zugriffs und der Computer Standards (SPAD)](cpl-setprogramaccess.md).</span><span class="sxs-lookup"><span data-stu-id="e516b-115">For information about SPAD and SYDP application registration, see [Guidelines for File Associations and Default Programs](appguide-fa-defpro.md), and [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md).</span></span>

 

## <a name="finding-an-application-executable"></a><span data-ttu-id="e516b-116">Suchen einer ausführbaren Datei der Anwendung</span><span class="sxs-lookup"><span data-stu-id="e516b-116">Finding an Application Executable</span></span>

<span data-ttu-id="e516b-117">Wenn die [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) -Funktion mit dem Namen einer ausführbaren Datei im *lpfile* -Parameter aufgerufen wird, gibt es mehrere Stellen, an denen die Funktion nach der Datei sucht.</span><span class="sxs-lookup"><span data-stu-id="e516b-117">When the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called with the name of an executable file in its *lpFile* parameter, there are several places where the function looks for the file.</span></span> <span data-ttu-id="e516b-118">Es wird empfohlen, die Anwendung im Registrierungs Unterschlüssel **App-Pfade** zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e516b-118">We recommend registering your application in the **App Paths** registry subkey.</span></span> <span data-ttu-id="e516b-119">Dadurch entfällt die Notwendigkeit, dass Anwendungen die Systempfad-Umgebungsvariable ändern.</span><span class="sxs-lookup"><span data-stu-id="e516b-119">Doing so avoids the need for applications to modify the system PATH environment variable.</span></span>

<span data-ttu-id="e516b-120">Die Datei wird an den folgenden Speicherorten gesucht:</span><span class="sxs-lookup"><span data-stu-id="e516b-120">The file is sought in the following locations:</span></span>

-   <span data-ttu-id="e516b-121">Das aktuelle Arbeitsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="e516b-121">The current working directory.</span></span>
-   <span data-ttu-id="e516b-122">Nur das **Windows** -Verzeichnis (es werden keine Unterverzeichnisse durchsucht).</span><span class="sxs-lookup"><span data-stu-id="e516b-122">The **Windows** directory only (no subdirectories are searched).</span></span>
-   <span data-ttu-id="e516b-123">Das **Windows \\ system32** -Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e516b-123">The **Windows\\System32** directory.</span></span>
-   <span data-ttu-id="e516b-124">Verzeichnisse, die in der PATH-Umgebungsvariablen aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e516b-124">Directories listed in the PATH environment variable.</span></span>
-   <span data-ttu-id="e516b-125">Empfohlen: **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion**- \\ **App-Pfade**</span><span class="sxs-lookup"><span data-stu-id="e516b-125">Recommended: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**</span></span>

## <a name="registering-applications"></a><span data-ttu-id="e516b-126">Anwendungen werden registriert</span><span class="sxs-lookup"><span data-stu-id="e516b-126">Registering Applications</span></span>

<span data-ttu-id="e516b-127">Die Registrierungs Unterschlüssel **App-Pfade** und **Anwendungen** werden verwendet, um das Verhalten des Systems im Auftrag von Anwendungen zu registrieren und zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e516b-127">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="e516b-128">Der Unterschlüssel für **App-Pfade** ist der bevorzugte Speicherort.</span><span class="sxs-lookup"><span data-stu-id="e516b-128">The **App Paths** subkey is the preferred location.</span></span>

### <a name="using-the-app-paths-subkey"></a><span data-ttu-id="e516b-129">Verwenden des unter Schlüssels für App-Pfade</span><span class="sxs-lookup"><span data-stu-id="e516b-129">Using the App Paths Subkey</span></span>

<span data-ttu-id="e516b-130">In Windows 7 und höher wird dringend empfohlen, Anwendungen pro Benutzer anstatt pro Computer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="e516b-130">In Windows 7 and later, we strongly recommend you install applications per user rather than per machine.</span></span> <span data-ttu-id="e516b-131">Eine Anwendung, die für pro Benutzer installiert wird, kann unter **HKEY \_ Current \_ User** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app path** registriert werden.</span><span class="sxs-lookup"><span data-stu-id="e516b-131">An application that is installed for per user can be registered under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span> <span data-ttu-id="e516b-132">Eine Anwendung, die für alle Benutzer des Computers installiert ist, kann unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app path** registriert werden.</span><span class="sxs-lookup"><span data-stu-id="e516b-132">An application that is installed for all users of the computer can be registered under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span>

<span data-ttu-id="e516b-133">Die unter APP- **Pfade** gefundenen Einträge werden hauptsächlich für folgende Zwecke verwendet:</span><span class="sxs-lookup"><span data-stu-id="e516b-133">The entries found under **App Paths** are used primarily for the following purposes:</span></span>

-   <span data-ttu-id="e516b-134">, Um den Namen der ausführbaren Datei einer Anwendung dem voll qualifizierten Pfad der Datei zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e516b-134">To map an application's executable file name to that file's fully qualified path.</span></span>
-   <span data-ttu-id="e516b-135">, Um der Umgebungsvariablen "Path" pro Anwendung, pro Prozess, Informationen vorab hinzufügen zu können.</span><span class="sxs-lookup"><span data-stu-id="e516b-135">To pre-pend information to the PATH environment variable on a per-application, per-process basis.</span></span>

<span data-ttu-id="e516b-136">Wenn der Name eines unter Schlüssels von **App-Pfaden** mit dem Dateinamen übereinstimmt, führt die Shell zwei Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="e516b-136">If the name of a subkey of **App Paths** matches the file name, the Shell performs two actions:</span></span>

-   <span data-ttu-id="e516b-137">Der (standardmäßige) Eintrag wird als voll qualifizierter Pfad der Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="e516b-137">The (Default) entry is used as the file's fully qualified path.</span></span>
-   <span data-ttu-id="e516b-138">Der Pfad Eintrag für diesen Unterschlüssel wird der PATH-Umgebungsvariablen dieses Prozesses vorausgeht.</span><span class="sxs-lookup"><span data-stu-id="e516b-138">The Path entry for that subkey is pre-pended to the PATH environment variable of that process.</span></span> <span data-ttu-id="e516b-139">Wenn dies nicht erforderlich ist, kann der Pfadwert weggelassen werden.</span><span class="sxs-lookup"><span data-stu-id="e516b-139">If this is not required, the Path value can be omitted.</span></span>

<span data-ttu-id="e516b-140">Folgende mögliche Probleme sind zu beachten:</span><span class="sxs-lookup"><span data-stu-id="e516b-140">Potential issues to be aware of include:</span></span>

-   <span data-ttu-id="e516b-141">Die Shell schränkt die Länge einer Befehlszeile auf Max \_ . Pfad \* 2 Zeichen ein.</span><span class="sxs-lookup"><span data-stu-id="e516b-141">The Shell limits the length of a command line to MAX\_PATH \* 2 characters.</span></span> <span data-ttu-id="e516b-142">Wenn viele Dateien als Registrierungseinträge aufgeführt sind oder die Pfade lang sind, können die Dateinamen später in der Liste verloren gehen, wenn die Befehlszeile abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="e516b-142">If there are many files listed as registry entries or their paths are long, file names later in the list could be lost as the command line is truncated.</span></span>
-   <span data-ttu-id="e516b-143">Einige Anwendungen akzeptieren nicht mehrere Dateinamen in einer Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="e516b-143">Some applications do not accept multiple file names in a command line.</span></span>
-   <span data-ttu-id="e516b-144">Einige Anwendungen, die mehrere Dateinamen akzeptieren, erkennen nicht das Format, in dem Sie von der Shell bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e516b-144">Some applications that accept multiple file names do not recognize the format in which the Shell provides them.</span></span> <span data-ttu-id="e516b-145">Die Shell stellt die Parameterliste als Zeichenfolge in Anführungszeichen bereit, aber einige Anwendungen erfordern möglicherweise Zeichen folgen ohne Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="e516b-145">The Shell provides the parameter list as a quoted string, but some applications might require strings without quotes.</span></span>
-   <span data-ttu-id="e516b-146">Nicht alle Elemente, die gezogen werden können, sind Teil des Dateisystems. beispielsweise Drucker.</span><span class="sxs-lookup"><span data-stu-id="e516b-146">Not all items that can be dragged are part of the file system; for example, printers.</span></span> <span data-ttu-id="e516b-147">Diese Elemente verfügen über keinen standardmäßigen Win32-Pfad. Daher gibt es keine Möglichkeit, für [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)einen sinnvollen *lpparameter* -Wert bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e516b-147">These items do not have a standard Win32 path, so there is no way to provide a meaningful *lpParameters* value to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="e516b-148">Die Verwendung des DropTarget-Eintrags vermeidet diese potenziellen Probleme durch die Bereitstellung des Zugriffs auf alle Zwischenablage Formate, einschließlich [cfstr \_ shellidlist](clipboard.md) (für lange Dateilisten) und [cfstr \_ File Content](clipboard.md) (für nicht-Dateisystem Objekte).</span><span class="sxs-lookup"><span data-stu-id="e516b-148">Using the DropTarget entry avoids these potential issues by providing access to all of the clipboard formats, including [CFSTR\_SHELLIDLIST](clipboard.md) (for long file lists) and [CFSTR\_FILECONTENTS](clipboard.md) (for non-file-system objects).</span></span>

<span data-ttu-id="e516b-149">So **registrieren und Steuern Sie das Verhalten Ihrer Anwendungen mit dem Unterschlüssel für App-Pfade**:</span><span class="sxs-lookup"><span data-stu-id="e516b-149">**To register and control the behavior of your applications with the App Paths subkey**:</span></span>

1.  <span data-ttu-id="e516b-150">Fügen Sie dem Unterschlüssel für **App-Pfade** einen Unterschlüssel mit dem gleichen Namen wie die ausführbare Datei hinzu, wie im folgenden Registrierungs Eintrag gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e516b-150">Add a subkey with the same name as your executable file to the **App Paths** subkey, as shown in the following registry entry.</span></span>

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  <span data-ttu-id="e516b-151">In der folgenden Tabelle finden Sie Details zu den Unterschlüssel Einträgen für **App-Pfade** .</span><span class="sxs-lookup"><span data-stu-id="e516b-151">See the following table for details of the **App Paths** subkey entries.</span></span> 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="e516b-152">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="e516b-152">Registry entry</span></span></th>
    <th><span data-ttu-id="e516b-153">Details</span><span class="sxs-lookup"><span data-stu-id="e516b-153">Details</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="e516b-154">(Standardwert)</span><span class="sxs-lookup"><span data-stu-id="e516b-154">(Default)</span></span></td>
    <td><span data-ttu-id="e516b-155">Der voll qualifizierte Pfad der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e516b-155">Is the fully qualified path to the application.</span></span> <span data-ttu-id="e516b-156">Der im (Standard-) Eintrag angegebene Anwendungsname kann mit oder ohne Erweiterung. exe angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e516b-156">The application name provided in the (Default) entry can be stated with or without its .exe extension.</span></span> <span data-ttu-id="e516b-157">Bei Bedarf fügt die <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> -Funktion beim Durchsuchen des unter Schlüssels der <strong>App-Pfade</strong> die Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="e516b-157">If necessary, the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function adds the extension when searching <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="e516b-158">Der Eintrag ist vom <strong>REG_SZ</strong> Typ.</span><span class="sxs-lookup"><span data-stu-id="e516b-158">The entry is of the <strong>REG_SZ</strong> type.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e516b-159">Dontusedesktopchangerouter</span><span class="sxs-lookup"><span data-stu-id="e516b-159">DontUseDesktopChangeRouter</span></span></td>
    <td><span data-ttu-id="e516b-160">Ist für Debugger-Anwendungen obligatorisch, um beim Debuggen des Windows-Explorer-Prozesses Datei Dialogfelder zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="e516b-160">Is mandatory for debugger applications to avoid file dialog deadlocks when debugging the Windows Explorer process.</span></span> <span data-ttu-id="e516b-161">Das Festlegen des "dontusedesktopchangerouter"-Eintrags führt jedoch zu einer etwas weniger effizienten Behandlung der Änderungs Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="e516b-161">Setting the DontUseDesktopChangeRouter entry produces a slightly less efficient handling of the change notifications, however.</span></span> <span data-ttu-id="e516b-162">Der Eintrag ist vom <strong>REG_DWORD</strong> Typ, und der Wert ist 0x1.</span><span class="sxs-lookup"><span data-stu-id="e516b-162">The entry is of the <strong>REG_DWORD</strong> type and the value is 0x1.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="e516b-163">DropTarget</span><span class="sxs-lookup"><span data-stu-id="e516b-163">DropTarget</span></span></td>
    <td><span data-ttu-id="e516b-164">Ist ein Klassen Bezeichner (CLSID).</span><span class="sxs-lookup"><span data-stu-id="e516b-164">Is a class identifier (CLSID).</span></span> <span data-ttu-id="e516b-165">Der DropTarget-Eintrag enthält die CLSID eines Objekts (in der Regel ein lokaler Server anstelle eines in-Process-Servers), der <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>implementiert.</span><span class="sxs-lookup"><span data-stu-id="e516b-165">The DropTarget entry contains the CLSID of an object (usually a local server rather than an in-process server) that implements <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>.</span></span> <span data-ttu-id="e516b-166">Wenn das Ablage Ziel eine ausführbare Datei ist und kein DropTarget-Wert bereitgestellt wird, konvertiert die Shell standardmäßig die Liste der gelöschten Dateien in einen Befehlszeilenparameter und übergibt Sie mithilfe von <em>lpparameters</em>an <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e516b-166">By default, when the drop target is an executable file, and no DropTarget value is provided, the Shell converts the list of dropped files into a command-line parameter and passes it to <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> through <em>lpParameters</em>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e516b-167">`Path`</span><span class="sxs-lookup"><span data-stu-id="e516b-167">Path</span></span></td>
    <td><span data-ttu-id="e516b-168">Stellt eine Zeichenfolge (in Form einer durch Semikolons getrennten Liste von Verzeichnissen) bereit, die an die PATH-Umgebungsvariable angehängt werden soll, wenn eine Anwendung durch den Aufruf von <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e516b-168">Supplies a string (in the form of a semicolon-separated list of directories) to append to the PATH environment variable when an application is launched by calling <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span></span> <span data-ttu-id="e516b-169">Dabei handelt es sich um den voll qualifizierten Pfad der exe-Datei.</span><span class="sxs-lookup"><span data-stu-id="e516b-169">It is the fully qualified path to the .exe.</span></span> <span data-ttu-id="e516b-170">Es ist <strong>REG_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="e516b-170">It is of <strong>REG_SZ</strong>.</span></span> <span data-ttu-id="e516b-171">In <strong>Windows 7 und</strong>höher kann der Typ <strong>REG_EXPAND_SZ</strong>werden und ist häufig <strong>REG_EXPAND_SZ</strong> % Program Files%.</span><span class="sxs-lookup"><span data-stu-id="e516b-171">In <strong>Windows 7 and later</strong>, the type can be <strong>REG_EXPAND_SZ</strong>, and is commonly <strong>REG_EXPAND_SZ</strong> %ProgramFiles%.</span></span>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="e516b-172">Zusätzlich zu den (Standard), Pfad-und DropTarget-Einträgen, die von der Shell erkannt werden, kann eine Anwendung auch benutzerdefinierte Werte dem <strong>App-Pfad</strong> -Unterschlüssel der ausführbaren Datei hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e516b-172">In addition to the (Default), Path, and DropTarget entries recognized by the Shell, an application can also add custom values to its executable file's <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="e516b-173">Wir empfehlen Anwendungsentwicklern, den <strong>App</strong> -Pfad-Unterschlüssel zu verwenden, um einen anwendungsspezifischen Pfad bereitzustellen, anstatt Erweiterungen zum globalen Systempfad zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e516b-173">We encourage application developers to use the <strong>App Paths</strong> subkey to provide an application-specific path instead of making additions to the global system path.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="e516b-174">SupportedProtocols</span><span class="sxs-lookup"><span data-stu-id="e516b-174">SupportedProtocols</span></span></td>
    <td><span data-ttu-id="e516b-175">Erstellt eine Zeichenfolge, die die URL-Protokoll Schemas für einen angegebenen Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="e516b-175">Creates a string that contains the URL protocol schemes for a given key.</span></span> <span data-ttu-id="e516b-176">Dies kann mehrere Registrierungs Werte enthalten, um anzugeben, welche Schemas unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e516b-176">This can contain multiple registry values to indicate which schemes are supported.</span></span> <span data-ttu-id="e516b-177">Diese Zeichenfolge folgt dem Format von <strong>scheme1: scheme2</strong>.</span><span class="sxs-lookup"><span data-stu-id="e516b-177">This string follows the format of <strong>scheme1:scheme2</strong>.</span></span> <span data-ttu-id="e516b-178">Wenn diese Liste nicht leer ist, wird die <strong>Datei:</strong> der Zeichenfolge hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e516b-178">If this list is not empty, <strong>file:</strong> will be added to the string.</span></span> <span data-ttu-id="e516b-179">Dieses Protokoll wird implizit unterstützt, wenn " <em>supportedprotokolls</em> " definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e516b-179">This protocol is implicitly supported when <em>SupportedProtocols</em> is defined.</span></span> <br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e516b-180">UseUrl</span><span class="sxs-lookup"><span data-stu-id="e516b-180">UseUrl</span></span></td>
    <td><span data-ttu-id="e516b-181">Gibt an, dass die Anwendung eine URL (anstelle eines Datei namens) in der Befehlszeile annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="e516b-181">Indicates that your application can accept a URL (instead of a file name) on the command line.</span></span> <span data-ttu-id="e516b-182">Anwendungen, die Dokumente direkt aus dem Internet öffnen können, wie Webbrowser und Medien Player, sollten diesen Eintrag festlegen.</span><span class="sxs-lookup"><span data-stu-id="e516b-182">Applications that can open documents directly from the internet, like web browsers and media players, should set this entry.</span></span> <br/> <span data-ttu-id="e516b-183">Wenn die <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> -Funktion eine Anwendung startet und der Wert useurl = 1 nicht festgelegt ist, lädt <strong>ShellExecuteEx</strong> das Dokument in eine lokale Datei herunter und ruft den Handler für die lokale Kopie auf.</span><span class="sxs-lookup"><span data-stu-id="e516b-183">When the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function starts an application and the UseUrl=1 value is not set, <strong>ShellExecuteEx</strong> downloads the document to a local file and invokes the handler on the local copy.</span></span><br/> <span data-ttu-id="e516b-184">Wenn für die Anwendung z. b. dieser Eintrag festgelegt ist und ein Benutzer mit der rechten Maustaste auf eine auf einem Webserver gespeicherte Datei klickt, wird das geöffnete Verb verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="e516b-184">For example, if the application has this entry set and a user right-clicks on a file stored on a web server, the Open verb will be made available.</span></span> <span data-ttu-id="e516b-185">Wenn dies nicht der Fall ist, muss der Benutzer die Datei herunterladen und die lokale Kopie öffnen.</span><span class="sxs-lookup"><span data-stu-id="e516b-185">If not, the user will have to download the file and open the local copy.</span></span> <br/> <span data-ttu-id="e516b-186">Der useurl-Eintrag hat <strong>REG_DWORD</strong> Typ, und der Wert ist 0x1.</span><span class="sxs-lookup"><span data-stu-id="e516b-186">The UseUrl entry is of <strong>REG_DWORD</strong> type, and the value is 0x1.</span></span><br/> <span data-ttu-id="e516b-187">In Windows Vista und früheren Versionen hat dieser Eintrag angegeben, dass die URL zusammen mit einem lokalen Dateinamen an die Anwendung weitergegeben werden soll, wenn Sie über ShellExecuteEx aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e516b-187">In Windows Vista and earlier, this entry indicated that the URL should be passed to the application along with a local file name, when called via ShellExecuteEx.</span></span> <span data-ttu-id="e516b-188">In Windows 7 deutet dies darauf hin, dass die Anwendung jede HTTP-oder HTTPS-URL, die an Sie übergeben wird, verstehen kann, ohne auch den Cache Dateinamen angeben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="e516b-188">In Windows 7, it indicates that the application can understand any http or https url that is passed to it, without having to supply the cache file name as well.</span></span> <span data-ttu-id="e516b-189">Dieser Registrierungsschlüssel ist mit dem <em>supportedprotokolls</em> -Schlüssel verknüpft.</span><span class="sxs-lookup"><span data-stu-id="e516b-189">This registry key is associated with the <em>SupportedProtocols</em> key.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a><span data-ttu-id="e516b-190">Verwenden des unter Schlüssels "Anwendungen"</span><span class="sxs-lookup"><span data-stu-id="e516b-190">Using the Applications Subkey</span></span>

<span data-ttu-id="e516b-191">Durch die Einbindung von Registrierungs Einträgen unter den **HKEY \_ - \_ Klassen** Stamm \\ **Anwendungen** \\ *ApplicationName.exe* Unterschlüssel können Anwendungen die anwendungsspezifischen Informationen bereitstellen, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e516b-191">Through the inclusion of registry entries under the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey, applications can provide the application-specific information shown in the following table.</span></span>



| <span data-ttu-id="e516b-192">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="e516b-192">Registry entry</span></span>                   | <span data-ttu-id="e516b-193">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e516b-193">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e516b-194">\\shellverb</span><span class="sxs-lookup"><span data-stu-id="e516b-194">shell\\verb</span></span>                      | <span data-ttu-id="e516b-195">Stellt die Verb Methode zum Aufrufen der Anwendung aus openWith bereit.</span><span class="sxs-lookup"><span data-stu-id="e516b-195">Provides the verb method for calling the application from OpenWith.</span></span> <span data-ttu-id="e516b-196">Ohne eine hier angegebene Verb Definition geht das System davon aus, dass die Anwendung "up [**Process**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)" unterstützt, und übergibt den Dateinamen in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="e516b-196">Without a verb definition specified here, the system assumes that the application supports [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), and passes the file name on the command line.</span></span> <span data-ttu-id="e516b-197">Diese Funktion gilt für alle Verb-Methoden, einschließlich DropTarget, ExecuteCommand und dynamischer Datenaustausch (DDE).</span><span class="sxs-lookup"><span data-stu-id="e516b-197">This functionality applies to all the verb methods, including DropTarget, ExecuteCommand, and Dynamic Data Exchange (DDE).</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e516b-198">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="e516b-198">DefaultIcon</span></span>                      | <span data-ttu-id="e516b-199">Ermöglicht es einer Anwendung, ein bestimmtes Symbol zur Darstellung der Anwendung bereitzustellen, anstatt das erste Symbol, das in der exe-Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="e516b-199">Enables an application to provide a specific icon to represent the application instead of the first icon stored in the .exe file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="e516b-200">Friendlyappname</span><span class="sxs-lookup"><span data-stu-id="e516b-200">FriendlyAppName</span></span>                  | <span data-ttu-id="e516b-201">Bietet eine Möglichkeit, einen lokalisierbaren Namen für eine Anwendung zu erhalten, anstatt nur die angezeigten Versionsinformationen anzuzeigen, die möglicherweise nicht lokalisierbar sind.</span><span class="sxs-lookup"><span data-stu-id="e516b-201">Provides a way to get a localizable name to display for an application instead of just the version information appearing, which may not be localizable.</span></span> <span data-ttu-id="e516b-202">Die Association-Abfrage [**assocstr**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) liest diesen Registrierungs Eintrags Wert und greift auf den FileDescription-Namen in den Versionsinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="e516b-202">The association query [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) reads this registry entry value and falls back to use the FileDescription name in the version information.</span></span> <span data-ttu-id="e516b-203">Wenn dieser Name fehlt, wird für die Zuordnungs Abfrage standardmäßig der Anzeige Name der Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="e516b-203">If that name is missing, the association query defaults to the display name of the file.</span></span> <span data-ttu-id="e516b-204">Anwendungen sollten mithilfe von **assocstr \_ friendlyappname** diese Informationen abrufen, um das richtige Verhalten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e516b-204">Applications should use **ASSOCSTR\_FRIENDLYAPPNAME** to retrieve this information to obtain the proper behavior.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="e516b-205">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="e516b-205">SupportedTypes</span></span>                   | <span data-ttu-id="e516b-206">Listet die Dateitypen auf, die von der Anwendung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e516b-206">Lists the file types that the application supports.</span></span> <span data-ttu-id="e516b-207">Dadurch kann die Anwendung im Dialogfeld **Öffnen mit** im Menü Cascade aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e516b-207">Doing so enables the application to be listed in the cascade menu of the **Open with** dialog box.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e516b-208">Noopenwith</span><span class="sxs-lookup"><span data-stu-id="e516b-208">NoOpenWith</span></span>                       | <span data-ttu-id="e516b-209">Gibt an, dass keine Anwendung zum Öffnen dieses Dateityps angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e516b-209">Indicates that no application is specified for opening this file type.</span></span> <span data-ttu-id="e516b-210">Beachten Sie, dass, wenn ein OpenWithProgIds-Unterschlüssel für eine Anwendung nach Dateityp festgelegt wurde und der ProgID-Unterschlüssel selbst nicht auch über einen noopenwith-Eintrag verfügt, diese Anwendung in der Liste der empfohlenen oder verfügbaren Anwendungen angezeigt wird, auch wenn Sie den Eintrag noopenwith angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="e516b-210">Be aware that if an OpenWithProgIDs subkey has been set for an application by file type, and the ProgID subkey itself does not also have a NoOpenWith entry, that application will appear in the list of recommended or available applications even if it has specified the NoOpenWith entry.</span></span> <span data-ttu-id="e516b-211">Weitere Informationen finden Sie unter Gewusst wie: [Einschließen einer Anwendung im Dialogfeld "Öffnen mit](how-to-include-an-application-on-the-open-with-dialog-box.md) " und [ausschließen einer Anwendung aus dem Dialogfeld Öffnen mit](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="e516b-211">For more information, see [How to How to Include an Application in the Open With Dialog Box](how-to-include-an-application-on-the-open-with-dialog-box.md) and [How to exclude an Application from the Open with Dialog Box](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span></span><br/> |
| <span data-ttu-id="e516b-212">Ishostapp</span><span class="sxs-lookup"><span data-stu-id="e516b-212">IsHostApp</span></span>                        | <span data-ttu-id="e516b-213">Gibt an, dass es sich bei dem Prozess um einen Host Prozess handelt, z. b. Rundll32.exe oder Dllhost.exe, und sollte nicht für das **anheten des Start** Menüs oder das einschließen in die Liste der am häufigsten verwendeten (MFU-) Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e516b-213">Indicates that the process is a host process, such as Rundll32.exe or Dllhost.exe, and should not be considered for **Start** menu pinning or inclusion in the Most Frequently Used (MFU) list.</span></span> <span data-ttu-id="e516b-214">Beim Start mit einer Verknüpfung, die eine Argumentliste ungleich NULL oder eine explizite [Anwendungs Benutzer Modell-ID (appusermudelids)](appids.md)enthält, kann der Prozess fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="e516b-214">When launched with a shortcut that contains a non-null argument list or an explicit [Application User Model IDs (AppUserModelIDs)](appids.md), the process can be pinned (as that shortcut).</span></span> <span data-ttu-id="e516b-215">Solche Verknüpfungen sind Kandidaten für die Einbindung in die MFU-Liste.</span><span class="sxs-lookup"><span data-stu-id="e516b-215">Such shortcuts are candidates for inclusion in the MFU list.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="e516b-216">NoStartPage</span><span class="sxs-lookup"><span data-stu-id="e516b-216">NoStartPage</span></span>                      | <span data-ttu-id="e516b-217">Gibt an, dass die ausführbare Datei der Anwendung und Verknüpfungen aus dem **Startmenü** ausgeschlossen und in der MFU-Liste fixiert oder eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e516b-217">Indicates that the application executable and shortcuts should be excluded from the **Start** menu and from pinning or inclusion in the MFU list.</span></span> <span data-ttu-id="e516b-218">Dieser Eintrag wird normalerweise verwendet, um System Tools, Installationsprogramme und Uninstaller sowie Info Dateien auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="e516b-218">This entry is typically used to exclude system tools, installers and uninstallers, and readme files.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e516b-219">Useexecutablefortaskbargroupicon</span><span class="sxs-lookup"><span data-stu-id="e516b-219">UseExecutableForTaskbarGroupIcon</span></span> | <span data-ttu-id="e516b-220">Bewirkt, dass die Taskleiste das Standard Symbol dieser ausführbaren Datei verwendet, wenn für diese Anwendung keine Einfügbare Verknüpfung vorhanden ist, und nicht das Symbol des Fensters, das zuerst gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="e516b-220">Causes the taskbar to use the default icon of this executable if there is no pinnable shortcut for this application, and instead of the icon of the window that was first encountered.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e516b-221">Taskbargroupicon</span><span class="sxs-lookup"><span data-stu-id="e516b-221">TaskbarGroupIcon</span></span>                 | <span data-ttu-id="e516b-222">Gibt das Symbol an, das zum Überschreiben des Task leisten Symbols verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e516b-222">Specifies the icon used to override the taskbar icon.</span></span> <span data-ttu-id="e516b-223">Das Fenster Symbol wird normalerweise für die Taskleiste verwendet.</span><span class="sxs-lookup"><span data-stu-id="e516b-223">The window icon is normally used for the taskbar.</span></span> <span data-ttu-id="e516b-224">Wenn Sie den Eintrag taskbargroupicon festlegen, verwendet das System stattdessen das Symbol aus der exe-Anwendung für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e516b-224">Setting the TaskbarGroupIcon entry causes the system to use the icon from the .exe for the application instead.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="e516b-225">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e516b-225">Examples</span></span>

<span data-ttu-id="e516b-226">Einige Beispiele für Anwendungs Registrierungen über die **HKEY- \_ Klassen \_** Stamm \\ **Anwendungen** \\ *ApplicationName.exe* Unterschlüssel lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="e516b-226">Some examples of application registrations through the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey are as follows.</span></span> <span data-ttu-id="e516b-227">Alle Registrierungs Eintrags Werte sind vom Typ " **reg \_ SZ** ", mit Ausnahme von " **DefaultIcon** " mit dem Typ " **reg \_ Expand \_ SZ** ".</span><span class="sxs-lookup"><span data-stu-id="e516b-227">All registry entry values are of **REG\_SZ** type, with the exception of **DefaultIcon** which is of **REG\_EXPAND\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a><span data-ttu-id="e516b-228">Registrieren von Verben und anderen Datei Zuordnungs Informationen</span><span class="sxs-lookup"><span data-stu-id="e516b-228">Registering Verbs and Other File Association Information</span></span>

<span data-ttu-id="e516b-229">Unterschlüssel, die unter den **HKEY- \_ Klassen " \_ root** \\ **systemfilezuordnungen** " registriert sind, ermöglichen der Shell, das Standardverhalten von Attributen für Dateitypen zu definieren und freigegebene Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="e516b-229">Subkeys registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** enable the Shell to define the default behavior of attributes for file types and enable shared file associations.</span></span> <span data-ttu-id="e516b-230">Wenn Benutzer die Standardanwendung für einen Dateityp ändern, hat die ProgID der neuen Standardanwendung eine Priorität bei der Bereitstellung von Verben und anderen Zuordnungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="e516b-230">When users change the default application for a file type, the ProgID of the new default application has priority in providing verbs and other association information.</span></span> <span data-ttu-id="e516b-231">Diese Priorität ist darauf zurückzuführen, dass es sich um den ersten Eintrag im Association-Array handelt.</span><span class="sxs-lookup"><span data-stu-id="e516b-231">This priority is due to it being the first entry in the association array.</span></span> <span data-ttu-id="e516b-232">Wenn das Standardprogramm geändert wird, sind die Informationen unter der vorherigen ProgID nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e516b-232">If the default program is changed, the information under the previous ProgID is no longer available.</span></span>

<span data-ttu-id="e516b-233">Wenn Sie proaktiv mit den Folgen einer Änderung an Standardprogrammen umgehen möchten, können Sie die **HKEY- \_ Klassen " \_ root** \\ **systemfileassociation** " verwenden, um Verben und andere Zuordnungs Informationen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e516b-233">To deal proactively with the consequences of a change to default programs, you can use **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** to register verbs and other association information.</span></span> <span data-ttu-id="e516b-234">Aufgrund ihrer Position nach der ProgID im Association-Array haben diese Registrierungen eine niedrigere Priorität.</span><span class="sxs-lookup"><span data-stu-id="e516b-234">Due to their location after the ProgID in the association array, these registrations are lower priority.</span></span> <span data-ttu-id="e516b-235">Diese systemfileassociationsregistrierungen sind auch dann stabil, wenn Benutzer die Standardprogramme ändern, und geben einen Speicherort zum Registrieren sekundärer Verben an, die für einen bestimmten Dateityp immer verfügbar sein werden.</span><span class="sxs-lookup"><span data-stu-id="e516b-235">These SystemFileAssociationsregistrations are stable even when users change the default programs, and provide a location to register secondary verbs that will always be available for a particular file type.</span></span> <span data-ttu-id="e516b-236">Ein Beispiel für die Registrierung finden Sie unter [Registrieren eines erkannten Typs](#registering-a-perceived-type) weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="e516b-236">For a registry example, see [Registering a Perceived Type](#registering-a-perceived-type) later in this topic.</span></span>

<span data-ttu-id="e516b-237">Das folgende Registrierungs Beispiel zeigt, was geschieht, wenn der Benutzer das Element " **Standardprogramme** " in der Systemsteuerung ausführt, um die Standardeinstellung für. MP3-Dateien in App2ProgID zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e516b-237">The following registry example shows what happens when the user runs the **Default Programs** item in Control Panel to change the default for .mp3 files to App2ProgID.</span></span> <span data-ttu-id="e516b-238">Nach dem Ändern der Standardeinstellung ist Verb1 nicht mehr verfügbar, und Verb2 wird zum Standard.</span><span class="sxs-lookup"><span data-stu-id="e516b-238">After changing the default, Verb1 is no longer available, and Verb2 becomes the default.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a><span data-ttu-id="e516b-239">Registrieren eines erkannten Typs</span><span class="sxs-lookup"><span data-stu-id="e516b-239">Registering a Perceived Type</span></span>

<span data-ttu-id="e516b-240">Registrierungs Werte für wahrgenommene Typen werden als Unterschlüssel des Stamm **\_ \_** \\ **systemfileassociations** -Registrierungs unter Schlüssels der HKEY-Klassen definiert.</span><span class="sxs-lookup"><span data-stu-id="e516b-240">Registry values for perceived types are defined as subkeys of the **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey.</span></span> <span data-ttu-id="e516b-241">Beispielsweise wird der erkannte **Typtext** wie folgt registriert:</span><span class="sxs-lookup"><span data-stu-id="e516b-241">For example, the perceived type **text** is registered as follows:</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

<span data-ttu-id="e516b-242">Der wahrgenommene Typ eines Dateityps wird durch Einschließen eines "wahrnehmvedtype"-Werts in den Unterschlüssel des Dateityps angegeben.</span><span class="sxs-lookup"><span data-stu-id="e516b-242">A file type's perceived type is indicated by including a PerceivedType value in the file type's subkey.</span></span> <span data-ttu-id="e516b-243">Der Wert "wahrnehmvedtype" wird auf den Namen des erkannten Typs festgelegt, der unter **HKEY \_ Classes \_ root** \\ **systemfileassociations** -Registrierungs Unterschlüssel registriert ist, wie im vorherigen Registrierungs Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e516b-243">The PerceivedType value is set to the name of the perceived type registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey, as shown in the previous registry example.</span></span> <span data-ttu-id="e516b-244">Fügen Sie beispielsweise den folgenden Registrierungs Eintrag hinzu, um cpp-Dateien als den wahrgenommenen Typ "Text" zu deklarieren:</span><span class="sxs-lookup"><span data-stu-id="e516b-244">To declare .cpp files as being of perceived type "text", for example, add the following registry entry:</span></span>

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a><span data-ttu-id="e516b-245">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e516b-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e516b-246">Dateitypen</span><span class="sxs-lookup"><span data-stu-id="e516b-246">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="e516b-247">Funktionsweise von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="e516b-247">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="e516b-248">Inhaltsansicht nach Dateityp oder-Art</span><span class="sxs-lookup"><span data-stu-id="e516b-248">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="e516b-249">Dateityp Überprüfung</span><span class="sxs-lookup"><span data-stu-id="e516b-249">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="e516b-250">Dateityp Handler</span><span class="sxs-lookup"><span data-stu-id="e516b-250">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="e516b-251">Programmgesteuerte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e516b-251">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="e516b-252">Wahrgenommene Typen</span><span class="sxs-lookup"><span data-stu-id="e516b-252">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="e516b-253">Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="e516b-253">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

