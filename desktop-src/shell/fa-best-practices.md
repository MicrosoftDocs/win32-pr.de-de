---
description: Die folgende Liste wird empfohlen, wenn Sie mit Dateizuordnungen arbeiten.
title: Bewährte Methoden für Dateizuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f49c1df6d145c32b8fcbdf70462b30f14f51b3d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525796"
---
# <a name="best-practices-for-file-associations"></a><span data-ttu-id="35ffe-103">Bewährte Methoden für Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="35ffe-103">Best Practices for File Associations</span></span>

<span data-ttu-id="35ffe-104">Die folgende Liste wird empfohlen, wenn Sie mit Dateizuordnungen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="35ffe-104">The following list are recommended best practices you should use when working with file associations.</span></span>

-   [<span data-ttu-id="35ffe-105">Dateizuordnungen nicht aus der Registrierung kopieren</span><span class="sxs-lookup"><span data-stu-id="35ffe-105">Do Not Copy File Associations from the Registry</span></span>](#do-not-copy-file-associations-from-the-registry)
-   [<span data-ttu-id="35ffe-106">Vermeiden Sie, wenn möglich, Hard-Coding Pfade in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="35ffe-106">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [<span data-ttu-id="35ffe-107">Erweitern Sie immer erweiternde Zeichen folgen in Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="35ffe-107">Always Wrap Expanding Strings in Quotation Marks</span></span>](#always-wrap-expanding-strings-in-quotation-marks)
-   [<span data-ttu-id="35ffe-108">"AutoPlay/AutoRun" nicht mit Dateizuordnungen verwechseln</span><span class="sxs-lookup"><span data-stu-id="35ffe-108">Do Not Confuse Autoplay/Autorun with File Associations</span></span>](#do-not-confuse-autoplayautorun-with-file-associations)
-   [<span data-ttu-id="35ffe-109">Verwechseln Sie die Internet Explorer-MIME-Datenbank nicht mit Dateizuordnungen.</span><span class="sxs-lookup"><span data-stu-id="35ffe-109">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [<span data-ttu-id="35ffe-110">Ordnungsgemäß formatierte und versionierte ProgIDs verwenden</span><span class="sxs-lookup"><span data-stu-id="35ffe-110">Use Properly Formed and Versioned ProgIDs</span></span>](#use-properly-formed-and-versioned-progids)
-   [<span data-ttu-id="35ffe-111">Verwenden Sie keine kurzen Dateinamen Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="35ffe-111">Do Not Use Short File Name Extensions</span></span>](#do-not-use-short-file-name-extensions)
-   [<span data-ttu-id="35ffe-112">Registrieren neuer Dateitypen in der IANA-MIME-Datenbank</span><span class="sxs-lookup"><span data-stu-id="35ffe-112">Register New File Types in the IANA MIME Database</span></span>](#register-new-file-types-in-the-iana-mime-database)
-   [<span data-ttu-id="35ffe-113">Registrieren beim Windows-Webdienst für Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="35ffe-113">Sign Up with the Windows Web Service for File Associations</span></span>](#sign-up-with-the-windows-web-service-for-file-associations)
-   [<span data-ttu-id="35ffe-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35ffe-114">Related topics</span></span>](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a><span data-ttu-id="35ffe-115">Dateizuordnungen nicht aus der Registrierung kopieren</span><span class="sxs-lookup"><span data-stu-id="35ffe-115">Do Not Copy File Associations from the Registry</span></span>

<span data-ttu-id="35ffe-116">Es wird empfohlen, dass Sie keine vorhandenen Dateizuordnungen aus der Registrierung kopieren.</span><span class="sxs-lookup"><span data-stu-id="35ffe-116">We recommended that you do not copy existing file associations from the registry.</span></span> <span data-ttu-id="35ffe-117">Dies führt häufig zu der Propagierung von unzureichend formatierten Dateizuordnungen.</span><span class="sxs-lookup"><span data-stu-id="35ffe-117">This often leads to the propagation of poorly formed file associations.</span></span> <span data-ttu-id="35ffe-118">Stattdessen sollten Sie die unter [Beispielszenario für Datei](fa-sample-scenarios.md)Zuordnungen beschriebenen Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="35ffe-118">Instead, you should follow the steps outlined in [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a><span data-ttu-id="35ffe-119">Vermeiden Sie, wenn möglich, Hard-Coding Pfade in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="35ffe-119">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>

<span data-ttu-id="35ffe-120">Ebenso wie hart codierte Pfade in Programmen Probleme verursachen können, können hart Codierungs Pfade in der Registrierung zu Problemen führen.</span><span class="sxs-lookup"><span data-stu-id="35ffe-120">Just as hard-coding paths into programs can cause problems, hard-coding paths into the registry can also lead to problems.</span></span> <span data-ttu-id="35ffe-121">Stattdessen sollten Sie Registrierungs Erweiterungs Zeichenfolgen (reg \_ Expand \_ SZ) verwenden, um ggf. Pfad Unabhängigkeit bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="35ffe-121">Instead, you should use registry expansion strings (REG\_EXPAND\_SZ) to provide path independence where applicable.</span></span> <span data-ttu-id="35ffe-122">Anstatt diese Methode zu verwenden, verwenden Sie z. b. Folgendes:</span><span class="sxs-lookup"><span data-stu-id="35ffe-122">For example, instead of using this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

<span data-ttu-id="35ffe-123">Verwenden Sie diese Methode:</span><span class="sxs-lookup"><span data-stu-id="35ffe-123">You should use this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a><span data-ttu-id="35ffe-124">Erweitern Sie immer erweiternde Zeichen folgen in Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="35ffe-124">Always Wrap Expanding Strings in Quotation Marks</span></span>

<span data-ttu-id="35ffe-125">Erweiterungs Zeichenfolgen können Leerzeichen enthalten, wenn Sie erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="35ffe-125">Expanding strings can contain spaces when they expand.</span></span> <span data-ttu-id="35ffe-126">Da Leerzeichen häufig als Argument Trennzeichen interpretiert werden, werden unter bestimmten Umständen Probleme verursacht.</span><span class="sxs-lookup"><span data-stu-id="35ffe-126">Because spaces are often interpreted as argument delimiters, they cause problems under certain circumstances.</span></span> <span data-ttu-id="35ffe-127">Beispielsweise kann ein Befehl zum Aufrufen von myprogram wie folgt in der Registrierung gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="35ffe-127">For example, a command to invoke MyProgram can be stored in the registry as:</span></span>

`%SYSTEMROOT%\MyProgram %1 %2`

<span data-ttu-id="35ffe-128">"Myprogram" erwartet, dass "%1" der vollständige Pfad zu einem Dateinamen und "%2" ein Schalter ist, um eine Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="35ffe-128">MyProgram expects that %1 is the full path to a file name, and %2 is a switch to indicate some action.</span></span> <span data-ttu-id="35ffe-129">Wenn dieser Befehl mit **den Argumenten c: \\ Program Files \\ My Documents \\document.txt** und **"/Print** ausgeführt wird und ein systemroot von C: \\ Winnt annimmt, wird er zu folgenden Zwecken erweitert:</span><span class="sxs-lookup"><span data-stu-id="35ffe-129">If this command is executed with arguments **C:\\Program Files\\My Documents\\document.txt** and **/print**, and assuming a SYSTEMROOT of C:\\WINNT, it expands to:</span></span>

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

<span data-ttu-id="35ffe-130">In diesem Fall interpretiert myprogram, dass das erste Argument C: \\ Program ist, und das zweite Argument ist Files \\ My, das nicht das beabsichtigte Verhalten ist.</span><span class="sxs-lookup"><span data-stu-id="35ffe-130">In this case, MyProgram interprets that the first argument is C:\\Program, and the second argument is Files\\My, which is not the intended behavior.</span></span> <span data-ttu-id="35ffe-131">Die Argumente werden jedoch unabhängig davon, ob Sie Leerzeichen enthalten, ordnungsgemäß interpretiert, wenn die erweiterbaren Zeichen folgen wie folgt in Anführungszeichen gesetzt werden:</span><span class="sxs-lookup"><span data-stu-id="35ffe-131">The arguments are interpreted correctly, however, regardless of whether they contain spaces, if the expanding strings are wrapped in quotation marks as follows:</span></span>

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a><span data-ttu-id="35ffe-132">"AutoPlay/AutoRun" nicht mit Dateizuordnungen verwechseln</span><span class="sxs-lookup"><span data-stu-id="35ffe-132">Do Not Confuse Autoplay/Autorun with File Associations</span></span>

<span data-ttu-id="35ffe-133">Dateizuordnungen ähneln in gewisser Weise AutoPlay/AutoRun.</span><span class="sxs-lookup"><span data-stu-id="35ffe-133">File Associations are similar to Autoplay/Autorun in some ways.</span></span> <span data-ttu-id="35ffe-134">Allerdings bietet AutoPlay/AutoRun separate und unterschiedliche Funktionen, die von den Dateizuordnungen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="35ffe-134">However, Autoplay/Autorun offers separate and distinct facilities from those provided by file associations.</span></span> <span data-ttu-id="35ffe-135">Weitere Informationen finden Sie unter [Erstellen einer Autorun-aktivierten CD-ROM-Anwendung](autoplay.md).</span><span class="sxs-lookup"><span data-stu-id="35ffe-135">For more information see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md).</span></span>

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a><span data-ttu-id="35ffe-136">Verwechseln Sie die Internet Explorer-MIME-Datenbank nicht mit Dateizuordnungen.</span><span class="sxs-lookup"><span data-stu-id="35ffe-136">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>

<span data-ttu-id="35ffe-137">Dateizuordnungen ähneln der Windows Internet Explorer-MIME-Datenbank, da Dateitypen eine MIME-Typdefinition enthalten können (und sollten sollte).</span><span class="sxs-lookup"><span data-stu-id="35ffe-137">File Associations are similar to the Windows Internet Explorer MIME database, in that file types can (and should) include a MIME type definition.</span></span> <span data-ttu-id="35ffe-138">Die Internet Explorer-MIME-Datenbank ist jedoch getrennt und unterscheidet sich von Dateizuordnungen.</span><span class="sxs-lookup"><span data-stu-id="35ffe-138">However, the Internet Explorer MIME database is separate and distinct from file associations.</span></span>

## <a name="use-properly-formed-and-versioned-progids"></a><span data-ttu-id="35ffe-139">Ordnungsgemäß formatierte und versionierte ProgIDs verwenden</span><span class="sxs-lookup"><span data-stu-id="35ffe-139">Use Properly Formed and Versioned ProgIDs</span></span>

<span data-ttu-id="35ffe-140">Verwenden Sie immer [versionierte ProgIDs](fa-progids.md), auch wenn nur eine Version der ProgID vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="35ffe-140">Always use [versioned ProgIDs](fa-progids.md), even if there is only one version of the ProgID.</span></span> <span data-ttu-id="35ffe-141">ProgIDs mit Versions Angabe helfen, ProgID-Konflikte und über schreibungen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="35ffe-141">Versioned ProgIDs help to avoid ProgID conflicts and overwrites.</span></span> <span data-ttu-id="35ffe-142">Außerdem ermöglichen Sie, dass unterschiedliche Versionen einer Anwendung nebeneinander vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="35ffe-142">They also enable different versions of an application to co-exist.</span></span>

## <a name="do-not-use-short-file-name-extensions"></a><span data-ttu-id="35ffe-143">Verwenden Sie keine kurzen Dateinamen Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="35ffe-143">Do Not Use Short File Name Extensions</span></span>

<span data-ttu-id="35ffe-144">Lange Dateinamen Erweiterungen bieten folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="35ffe-144">Long file name extensions offer the following advantages:</span></span>

-   <span data-ttu-id="35ffe-145">Die begrenzte Länge der kurzen Erweiterungen macht Sie anfällig für *Erweiterungs Kollisionen.*</span><span class="sxs-lookup"><span data-stu-id="35ffe-145">The limited length of short extensions make them prone to *extension collisions.*</span></span> <span data-ttu-id="35ffe-146">Ein Erweiterungs Konflikt tritt auf, wenn die gleiche Erweiterung verwendet wird, um mehrere Dateitypen zu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="35ffe-146">An extension collision occurs when the same extension is used to classify multiple file types.</span></span> <span data-ttu-id="35ffe-147">Die Verwendung von langen Erweiterungen verringert die Wahrscheinlichkeit einer Kollision erheblich.</span><span class="sxs-lookup"><span data-stu-id="35ffe-147">Using long extensions significantly decreases the chances of a collision.</span></span>
-   <span data-ttu-id="35ffe-148">Kurze Dateinamen sind tendenziell etwas kryptisch.</span><span class="sxs-lookup"><span data-stu-id="35ffe-148">Short file names tend to be somewhat cryptic.</span></span> <span data-ttu-id="35ffe-149">Lange Erweiterungen sind tendenziell aussagekräftiger, da zusätzliche Informationen in die Erweiterung eingebettet werden können.</span><span class="sxs-lookup"><span data-stu-id="35ffe-149">Long extensions tend to be more meaningful because additional information can be embedded in the extension.</span></span>

<span data-ttu-id="35ffe-150">Weitere Informationen finden Sie unter [Dateinamen Erweiterungen](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="35ffe-150">For more information, see [file name extensions](fa-file-extensions.md).</span></span>

## <a name="register-new-file-types-in-the-iana-mime-database"></a><span data-ttu-id="35ffe-151">Registrieren neuer Dateitypen in der IANA-MIME-Datenbank</span><span class="sxs-lookup"><span data-stu-id="35ffe-151">Register New File Types in the IANA MIME Database</span></span>

<span data-ttu-id="35ffe-152">Die Internet Assigned Numbers Authority (IANA) bewahrt eine öffentliche Datenbank registrierter MIME-Typen auf.</span><span class="sxs-lookup"><span data-stu-id="35ffe-152">The Internet Assigned Numbers Authority (IANA) keeps a public database of registered MIME types.</span></span> <span data-ttu-id="35ffe-153">Wenn Sie einen neuen öffentlichen Dateityp definieren, wird empfohlen, dass Sie auch einen MIME-Typ für den Dateityp definieren und diesen Typ bei der IANA registrieren.</span><span class="sxs-lookup"><span data-stu-id="35ffe-153">When defining a new public file type, we recommended that you also define a MIME type for the file type and register this type with the IANA.</span></span> <span data-ttu-id="35ffe-154">Es fallen keine Kosten für die Registrierung an.</span><span class="sxs-lookup"><span data-stu-id="35ffe-154">There is no cost for registration.</span></span>

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a><span data-ttu-id="35ffe-155">Registrieren beim Windows-Webdienst für Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="35ffe-155">Sign Up with the Windows Web Service for File Associations</span></span>

<span data-ttu-id="35ffe-156">Anwendungsentwickler können sich mit dem Windows-Webdienst anmelden, den Benutzer für die Suche nach Anwendungen verwenden, die auf bestimmte Dateitypen angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="35ffe-156">Application developers can sign up with the Windows Web Service that users use to find applications that can operate on specific file types.</span></span> <span data-ttu-id="35ffe-157">Der Prozess für die Registrierung mit dem Webdienst wird im [Windows-Datei Zuordnungs System-Onboarding-Prozess](https://support.microsoft.com/kb/929149)ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="35ffe-157">The process for signing up with the web service is detailed in [Windows File Association System on-boarding process](https://support.microsoft.com/kb/929149).</span></span>

## <a name="related-topics"></a><span data-ttu-id="35ffe-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35ffe-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35ffe-159">Beispielszenario für Datei Zuordnung</span><span class="sxs-lookup"><span data-stu-id="35ffe-159">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="35ffe-160">Richtlinien für die Verwaltung von Standardanwendungen in Windows Vista und höher</span><span class="sxs-lookup"><span data-stu-id="35ffe-160">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="35ffe-161">Standardprogramme</span><span class="sxs-lookup"><span data-stu-id="35ffe-161">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="35ffe-162">Festlegen des Programm Zugriffs und der Computer Standardwerte (SPAD)</span><span class="sxs-lookup"><span data-stu-id="35ffe-162">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 



