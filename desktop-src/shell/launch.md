---
description: Nachdem die Anwendung ein Datei Objekt gefunden hat, besteht der nächste Schritt häufig darin, auf irgendeine Weise darauf zu reagieren.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Starten von Anwendungen (ShellExecute, ShellExecuteEx, shellexecuteinfo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e528e6c816040a83d57864999fbb2d683f9fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864127"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="d3120-103">Starten von Anwendungen (ShellExecute, ShellExecuteEx, shellexecuteinfo)</span><span class="sxs-lookup"><span data-stu-id="d3120-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="d3120-104">Nachdem die Anwendung ein Datei Objekt gefunden hat, besteht der nächste Schritt häufig darin, auf irgendeine Weise darauf zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="d3120-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="d3120-105">Beispielsweise kann Ihre Anwendung eine andere Anwendung starten, die es dem Benutzer ermöglicht, eine Datendatei zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d3120-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="d3120-106">Wenn es sich bei der gewünschten Datei um eine ausführbare Datei handelt, kann Sie von Ihrer Anwendung einfach gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="d3120-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="d3120-107">In diesem Dokument wird erläutert, wie [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) zum Ausführen dieser Aufgaben verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3120-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="d3120-108">Verwenden von ShellExecute und ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="d3120-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="d3120-109">Objekt Verben</span><span class="sxs-lookup"><span data-stu-id="d3120-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="d3120-110">Verwenden von ShellExecuteEx zum Bereitstellen von Aktivierungs Diensten von einem Standort</span><span class="sxs-lookup"><span data-stu-id="d3120-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [<span data-ttu-id="d3120-111">Verwenden von ShellExecute zum Starten des Dialog Felds "suchen"</span><span class="sxs-lookup"><span data-stu-id="d3120-111">Using ShellExecute to Launch the Search Dialog Box</span></span>](#using-shellexecute-to-launch-the-search-dialog-box)
-   [<span data-ttu-id="d3120-112">Ein einfaches Beispiel für die Verwendung von ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="d3120-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="d3120-113">Verwenden von ShellExecute und ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="d3120-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="d3120-114">Um [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)verwenden zu können, muss Ihre Anwendung das Datei-oder Ordner Objekt angeben, für das die Aktion durchgeführt werden soll, und ein *Verb* , das den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="d3120-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="d3120-115">Weisen Sie diese Werte für **ShellExecute** den entsprechenden Parametern zu.</span><span class="sxs-lookup"><span data-stu-id="d3120-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="d3120-116">Füllen Sie für **ShellExecuteEx** die entsprechenden Member einer [**shellexecuteinfo**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) -Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="d3120-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="d3120-117">Es gibt auch mehrere andere Member oder Parameter, die verwendet werden können, um das Verhalten der beiden Funktionen zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="d3120-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="d3120-118">Datei-und Ordner Objekte können Teil des Dateisystems oder der virtuellen Objekte sein. Sie können entweder durch Pfade oder Zeiger auf elementbezeichnerlisten (pidls) identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d3120-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="d3120-119">Objekt Verben</span><span class="sxs-lookup"><span data-stu-id="d3120-119">Object Verbs</span></span>

<span data-ttu-id="d3120-120">Die für ein Objekt verfügbaren Verben sind im Wesentlichen die Elemente, die im Kontextmenü eines Objekts gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d3120-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="d3120-121">Um zu ermitteln, welche Verben verfügbar sind, suchen Sie in der Registrierung unter</span><span class="sxs-lookup"><span data-stu-id="d3120-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="d3120-122">**HKEY \_ Klassen \_** Stamm- \\ **CLSID** \\ *{Object \_ CLSID}* \\  \\ *shellverb*</span><span class="sxs-lookup"><span data-stu-id="d3120-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="d3120-123">Dabei ist die *Objekt- \_ CLSID* der Klassen Bezeichner (CLSID) des Objekts, und das *Verb* ist der Name des verfügbaren Verbs.</span><span class="sxs-lookup"><span data-stu-id="d3120-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="d3120-124">Der Unterschlüssel des *Verbs*- \\ **Befehls** enthält die Daten, die angeben, was geschieht, wenn das Verb aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d3120-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="d3120-125">Wenn Sie herausfinden möchten, welche Verben für [vordefinierte Shellobjekte](handlers.md)verfügbar sind, suchen Sie in der Registrierung unter</span><span class="sxs-lookup"><span data-stu-id="d3120-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="d3120-126">**HKEY \_ Klassen \_** Stamm \\ *Objekt \_ Name* \\  \\ *shellverb*</span><span class="sxs-lookup"><span data-stu-id="d3120-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="d3120-127">Where *Object \_ Name* ist der Name des vordefinierten shellobjekts.</span><span class="sxs-lookup"><span data-stu-id="d3120-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="d3120-128">Der Unterschlüssel des *Verbs*- \\ **Befehls** enthält die Daten, die angeben, was geschieht, wenn das Verb aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d3120-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="d3120-129">Häufig verfügbare Verben sind:</span><span class="sxs-lookup"><span data-stu-id="d3120-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="d3120-130">Verb</span><span class="sxs-lookup"><span data-stu-id="d3120-130">Verb</span></span>       | <span data-ttu-id="d3120-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3120-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3120-132">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="d3120-132">edit</span></span>       | <span data-ttu-id="d3120-133">Öffnet einen Editor und öffnet das Dokument zum Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d3120-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="d3120-134">Suchen</span><span class="sxs-lookup"><span data-stu-id="d3120-134">find</span></span>       | <span data-ttu-id="d3120-135">Initiiert eine Suche beginnend mit dem angegebenen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d3120-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="d3120-136">open</span><span class="sxs-lookup"><span data-stu-id="d3120-136">open</span></span>       | <span data-ttu-id="d3120-137">Hiermit wird eine Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="d3120-137">Launches an application.</span></span> <span data-ttu-id="d3120-138">Wenn es sich bei dieser Datei nicht um eine ausführbare Datei handelt, wird die zugehörige Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="d3120-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="d3120-139">print</span><span class="sxs-lookup"><span data-stu-id="d3120-139">print</span></span>      | <span data-ttu-id="d3120-140">Druckt die Dokument Datei.</span><span class="sxs-lookup"><span data-stu-id="d3120-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="d3120-141">properties</span><span class="sxs-lookup"><span data-stu-id="d3120-141">properties</span></span> | <span data-ttu-id="d3120-142">Zeigt die Eigenschaften des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d3120-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="d3120-143">RunAs</span><span class="sxs-lookup"><span data-stu-id="d3120-143">runas</span></span>      | <span data-ttu-id="d3120-144">Hiermit wird eine Anwendung als Administrator gestartet.</span><span class="sxs-lookup"><span data-stu-id="d3120-144">Launches an application as Administrator.</span></span> <span data-ttu-id="d3120-145">Benutzerkontensteuerung (User Account Control, UAC) fordert den Benutzer zur Zustimmung zu</span><span class="sxs-lookup"><span data-stu-id="d3120-145">User Account Control (UAC) will prompt the user for consent to</span></span> |
|            | <span data-ttu-id="d3120-146">Ausführen der Anwendung mit erhöhten Rechten oder eingeben der Anmelde Informationen eines Administrator Kontos, das zum Ausführen des</span><span class="sxs-lookup"><span data-stu-id="d3120-146">run the application elevated or enter the credentials of an administrator account used to run the</span></span>        |
|            | <span data-ttu-id="d3120-147">Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d3120-147">application.</span></span>                                                                                             |

 

<span data-ttu-id="d3120-148">Jedes Verb entspricht dem Befehl, der zum Starten der Anwendung aus einem Konsolenfenster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3120-148">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="d3120-149">Das **offene** Verb ist ein gutes Beispiel, da es häufig unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d3120-149">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="d3120-150">**Öffnen** Sie für exe-Dateien einfach die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d3120-150">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="d3120-151">Es wird jedoch häufiger verwendet, um eine Anwendung zu starten, die für eine bestimmte Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3120-151">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="d3120-152">Beispielsweise können txt-Dateien von Microsoft WordPad geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="d3120-152">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="d3120-153">Das **geöffnete** Verb für eine txt-Datei entspricht daher etwa dem folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="d3120-153">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="d3120-154">Wenn Sie [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) zum Öffnen einer txt-Datei verwenden, wird Wordpad.exe mit der angegebenen Datei als Argument gestartet.</span><span class="sxs-lookup"><span data-stu-id="d3120-154">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="d3120-155">Einige Befehle können über zusätzliche Argumente verfügen, z. b. Flags, die nach Bedarf hinzugefügt werden können, um die Anwendung ordnungsgemäß zu starten.</span><span class="sxs-lookup"><span data-stu-id="d3120-155">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="d3120-156">Weitere Informationen zu Kontextmenüs und Verben finden Sie unter Erweitern von Kontext [Menüs](context.md).</span><span class="sxs-lookup"><span data-stu-id="d3120-156">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="d3120-157">Im Allgemeinen ist der Versuch, die Liste der verfügbaren Verben für eine bestimmte Datei zu ermitteln, etwas kompliziert.</span><span class="sxs-lookup"><span data-stu-id="d3120-157">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="d3120-158">In vielen Fällen können Sie einfach den *lpverb* -Parameter auf **null** festlegen, wodurch der Standardbefehl für den Dateityp aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d3120-158">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="d3120-159">Diese Prozedur entspricht in der Regel dem Festlegen von *lpverb* auf "Open", aber einige Dateitypen verfügen möglicherweise über einen anderen Standardbefehl.</span><span class="sxs-lookup"><span data-stu-id="d3120-159">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="d3120-160">Weitere Informationen finden Sie unter [erweitern](context.md) von Kontextmenüs und der Referenz Dokumentation zu [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="d3120-160">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="d3120-161">Verwenden von ShellExecuteEx zum Bereitstellen von Aktivierungs Diensten von einem Standort</span><span class="sxs-lookup"><span data-stu-id="d3120-161">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="d3120-162">Die Dienste einer Website Kette können viele Verhaltensweisen der Element Aktivierung steuern.</span><span class="sxs-lookup"><span data-stu-id="d3120-162">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="d3120-163">Ab Windows 8 können Sie einen Zeiger auf die Site Kette auf [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) bereitstellen, um diese Verhaltensweisen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3120-163">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="d3120-164">So geben Sie **ShellExecuteEx** den Standort an:</span><span class="sxs-lookup"><span data-stu-id="d3120-164">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="d3120-165">Geben Sie \_ \_ \_ \_ \_ im **fmask** -Member von [**shellexecuteingefo**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)das Flag hInst is-Flag für das Masken Kennzeichen anzeigen an.</span><span class="sxs-lookup"><span data-stu-id="d3120-165">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="d3120-166">Stellen Sie das [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Element im **hinstapp** -Mitglied von [**shellexecuteingefo**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)bereit.</span><span class="sxs-lookup"><span data-stu-id="d3120-166">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="d3120-167">Verwenden von ShellExecute zum Starten des Dialog Felds "suchen"</span><span class="sxs-lookup"><span data-stu-id="d3120-167">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="d3120-168">Wenn ein Benutzer mit der rechten Maustaste auf ein Ordnersymbol in Windows-Explorer klickt, ist eines der Menü Elemente "suchen".</span><span class="sxs-lookup"><span data-stu-id="d3120-168">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="d3120-169">Wenn Sie dieses Element auswählen, wird das Such Dienstprogramm der Shell gestartet.</span><span class="sxs-lookup"><span data-stu-id="d3120-169">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="d3120-170">Dieses Hilfsprogramm zeigt ein Dialogfeld an, das zum Durchsuchen von Dateien nach einer angegebenen Text Zeichenfolge verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d3120-170">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="d3120-171">Eine Anwendung kann das Such Dienstprogramm für ein Verzeichnis Programm gesteuert starten, indem [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)aufgerufen wird, wobei "Find" als *lpverb* -Parameter und der Verzeichnispfad als *lpder* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3120-171">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="d3120-172">Beispielsweise wird mit der folgenden Codezeile das Such Dienstprogramm für das Verzeichnis "c: \\ myprograms" gestartet.</span><span class="sxs-lookup"><span data-stu-id="d3120-172">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="d3120-173">Ein einfaches Beispiel für die Verwendung von ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="d3120-173">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="d3120-174">Die folgende Beispiel Konsolenanwendung veranschaulicht die Verwendung von [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="d3120-174">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="d3120-175">Der größte Fehler Überprüfungs Code wurde aus Gründen der Übersichtlichkeit ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="d3120-175">Most error checking code has been omitted for clarity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



<span data-ttu-id="d3120-176">Die Anwendung ruft zunächst die PIDL des Windows-Verzeichnisses ab und listet ihren Inhalt auf, bis die erste BMP-Datei gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="d3120-176">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="d3120-177">Im Gegensatz zum vorherigen Beispiel wird [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) verwendet, um den Namen der Datei statt des anzeigen Amens abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d3120-177">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="d3120-178">Da es sich hierbei um einen Dateisystem Ordner handelt, ist der namens Name ein voll qualifizierter Pfad, der für [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d3120-178">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="d3120-179">Nachdem die erste BMP-Datei gefunden wurde, werden die entsprechenden Werte den Elementen einer [**shellexecuteinfo**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) -Struktur zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d3120-179">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="d3120-180">Das **lpfile** -Element wird auf den Namen der Datei und den **lpverb** -Member auf **null** festgelegt, um den Standard Vorgang zu starten.</span><span class="sxs-lookup"><span data-stu-id="d3120-180">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="d3120-181">In diesem Fall ist der Standard Vorgang "Open".</span><span class="sxs-lookup"><span data-stu-id="d3120-181">In this case, the default operation is "open".</span></span> <span data-ttu-id="d3120-182">Die Struktur wird dann an [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)übergeben, wodurch der Standard Handler für Bitmapdateien gestartet wird, in der Regel MSPaint.exe, um die Datei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d3120-182">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="d3120-183">Nachdem die Funktion zurückgegeben wurde, werden die pidls freigegeben, und die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle des Windows-Ordners wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="d3120-183">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 
