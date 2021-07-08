---
description: Sobald Ihre Anwendung ein Dateiobjekt gefunden hat, besteht der nächste Schritt häufig in einer bestimmten Weise darauf.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Starten von Anwendungen (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ae5640acdbf4d959b97607cc66a4fd8fe8ac24
ms.sourcegitcommit: 89aa14b1f685f8d65d56ecbdb8bef12246c33cf9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "113508611"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="5dc1d-103">Starten von Anwendungen (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span><span class="sxs-lookup"><span data-stu-id="5dc1d-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="5dc1d-104">Sobald Ihre Anwendung ein Dateiobjekt gefunden hat, besteht der nächste Schritt häufig in einer bestimmten Weise darauf.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="5dc1d-105">Beispielsweise könnte Ihre Anwendung eine andere Anwendung starten, die es dem Benutzer ermöglicht, eine Datendatei zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="5dc1d-106">Wenn es sich bei der datei von Interesse um eine ausführbare Datei handelt, möchte Ihre Anwendung sie möglicherweise einfach starten.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="5dc1d-107">In diesem Dokument wird erläutert, wie [**ShellExecute oder**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) [**ShellExecuteEx zum**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) Ausführen dieser Aufgaben verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="5dc1d-108">Verwenden von ShellExecute und ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="5dc1d-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="5dc1d-109">Objektverben</span><span class="sxs-lookup"><span data-stu-id="5dc1d-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="5dc1d-110">Verwenden von ShellExecuteEx zum Bereitstellen von Aktivierungsdiensten von einem Standort</span><span class="sxs-lookup"><span data-stu-id="5dc1d-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [<span data-ttu-id="5dc1d-111">Verwenden von ShellExecute zum Starten des Suchdialogfelds</span><span class="sxs-lookup"><span data-stu-id="5dc1d-111">Using ShellExecute to Launch the Search Dialog Box</span></span>](#using-shellexecute-to-launch-the-search-dialog-box)
-   [<span data-ttu-id="5dc1d-112">Ein einfaches Beispiel für die Verwendung von ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="5dc1d-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="5dc1d-113">Verwenden von ShellExecute und ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="5dc1d-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="5dc1d-114">Um [**ShellExecute oder**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)zu verwenden, muss Ihre Anwendung das Datei-  oder Ordnerobjekt angeben, für das bzw. das die Aktion ausgeführt werden soll, sowie ein Verb, das den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="5dc1d-115">Weisen **Sie für ShellExecute** diese Werte den entsprechenden Parametern zu.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="5dc1d-116">Geben **Sie für ShellExecuteEx** die entsprechenden Member einer [**SHELLEXECUTEINFO-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) ein.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="5dc1d-117">Es gibt auch mehrere andere Member oder Parameter, die verwendet werden können, um das Verhalten der beiden Funktionen zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="5dc1d-118">Datei- und Ordnerobjekte können Teil des Dateisystems oder virtueller Objekte sein und entweder durch Pfade oder Zeiger auf Elementbezeichnerlisten (PIDLs) identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="5dc1d-119">Objektverben</span><span class="sxs-lookup"><span data-stu-id="5dc1d-119">Object Verbs</span></span>

<span data-ttu-id="5dc1d-120">Die für ein Objekt verfügbaren Verben sind im Wesentlichen die Elemente, die Sie im Kontextmenü eines Objekts finden.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="5dc1d-121">Um herauszufinden, welche Verben verfügbar sind, suchen Sie in der Registrierung unter .</span><span class="sxs-lookup"><span data-stu-id="5dc1d-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="5dc1d-122">**HKEY \_ CLASSES \_ ROOT** \\ **CLSID** \\ *{object \_ clsid}* \\  \\ *Shellverb*</span><span class="sxs-lookup"><span data-stu-id="5dc1d-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="5dc1d-123">Wobei *object \_ clsid* der Klassenbezeichner (CLSID) des Objekts und *verb* der Name des verfügbaren Verbs ist.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="5dc1d-124">Der  \\ **Unterschlüssel des Verbbefehls** enthält die Daten, die angeben, was geschieht, wenn dieses Verb aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="5dc1d-125">Um herauszufinden, welche Verben für vordefinierte [Shellobjekte verfügbar](handlers.md)sind, suchen Sie in der Registrierung unter .</span><span class="sxs-lookup"><span data-stu-id="5dc1d-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="5dc1d-126">**HKEY \_ CLASSES \_ ROOT-Objektnamen-Shellverb** \\ *\_* \\  \\ </span><span class="sxs-lookup"><span data-stu-id="5dc1d-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="5dc1d-127">Wobei *\_ Objektname* der Name des vordefinierten Shell-Objekts ist.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="5dc1d-128">Auch hier enthält *der Unterschlüssel* des Verbbefehls die Daten, die angeben, was \\  geschieht, wenn dieses Verb aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="5dc1d-129">Zu den häufig verfügbaren Verben gehören:</span><span class="sxs-lookup"><span data-stu-id="5dc1d-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="5dc1d-130">Verb</span><span class="sxs-lookup"><span data-stu-id="5dc1d-130">Verb</span></span>       | <span data-ttu-id="5dc1d-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5dc1d-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dc1d-132">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="5dc1d-132">edit</span></span>       | <span data-ttu-id="5dc1d-133">Startet einen Editor und öffnet das Dokument zur Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="5dc1d-134">Suchen</span><span class="sxs-lookup"><span data-stu-id="5dc1d-134">find</span></span>       | <span data-ttu-id="5dc1d-135">Initiiert eine Suche ab dem angegebenen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="5dc1d-136">öffnen</span><span class="sxs-lookup"><span data-stu-id="5dc1d-136">open</span></span>       | <span data-ttu-id="5dc1d-137">Startet eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-137">Launches an application.</span></span> <span data-ttu-id="5dc1d-138">Wenn es sich bei dieser Datei nicht um eine ausführbare Datei handelt, wird die zugehörige Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="5dc1d-139">print</span><span class="sxs-lookup"><span data-stu-id="5dc1d-139">print</span></span>      | <span data-ttu-id="5dc1d-140">Druckt die Dokumentdatei.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="5dc1d-141">properties</span><span class="sxs-lookup"><span data-stu-id="5dc1d-141">properties</span></span> | <span data-ttu-id="5dc1d-142">Zeigt die Eigenschaften des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="5dc1d-143">RunAs</span><span class="sxs-lookup"><span data-stu-id="5dc1d-143">runas</span></span>      | <span data-ttu-id="5dc1d-144">Startet eine Anwendung als Administrator.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-144">Launches an application as Administrator.</span></span> <span data-ttu-id="5dc1d-145">Die Benutzerkontensteuerung (User Account Control, UAC) fordert den Benutzer zur Zustimmung auf, die Anwendung mit erhöhten Rechten ausführen zu können, oder gibt die Anmeldeinformationen eines Administratorkontos ein, das zum Ausführen der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-145">User Account Control (UAC) will prompt the user for consent to run the application elevated or enter the credentials of an administrator account used to run the application.</span></span> |



<span data-ttu-id="5dc1d-146">Jedes Verb entspricht dem Befehl, der zum Starten der Anwendung über ein Konsolenfenster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-146">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="5dc1d-147">Das **offene** Verb ist ein gutes Beispiel, da es häufig unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-147">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="5dc1d-148">Öffnen .exe, um dateien **zu öffnen,** startet einfach die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-148">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="5dc1d-149">Es wird jedoch häufiger verwendet, um eine Anwendung zu starten, die für eine bestimmte Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-149">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="5dc1d-150">Beispielsweise können .txt von Microsoft WordPad geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-150">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="5dc1d-151">Das **geöffnete** Verb für eine .txt entspricht daher etwa dem folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="5dc1d-151">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="5dc1d-152">Wenn Sie [**ShellExecute oder**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) verwenden, um eine .txt zu öffnen, wird Wordpad.exe mit der angegebenen Datei als Argument gestartet.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-152">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="5dc1d-153">Einige Befehle können zusätzliche Argumente wie Flags enthalten, die nach Bedarf hinzugefügt werden können, um die Anwendung ordnungsgemäß zu starten.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-153">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="5dc1d-154">Weitere Informationen zu Kontextmenüs und Verben finden Sie unter [Erweitern von Kontextmenüs](context.md).</span><span class="sxs-lookup"><span data-stu-id="5dc1d-154">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="5dc1d-155">Im Allgemeinen ist der Versuch, die Liste der verfügbaren Verben für eine bestimmte Datei zu bestimmen, etwas kompliziert.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-155">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="5dc1d-156">In vielen Fällen können Sie einfach den *lpVerb-Parameter* auf **NULL** festlegen, wodurch der Standardbefehl für den Dateityp aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-156">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="5dc1d-157">Dieses Verfahren entspricht in der Regel dem Festlegen *von lpVerb* auf "open", aber einige Dateitypen verfügen möglicherweise über einen anderen Standardbefehl.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-157">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="5dc1d-158">Weitere Informationen finden Sie unter [Erweitern von Kontextmenüs](context.md) und in der [**Referenzdokumentation zu ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)</span><span class="sxs-lookup"><span data-stu-id="5dc1d-158">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="5dc1d-159">Verwenden von ShellExecuteEx zum Bereitstellen von Aktivierungsdiensten von einem Standort</span><span class="sxs-lookup"><span data-stu-id="5dc1d-159">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="5dc1d-160">Die Dienste einer Standortkette können viele Verhaltensweisen der Elementaktivierung steuern.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-160">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="5dc1d-161">Ab Windows 8 können Sie einen Zeiger auf die Standortkette auf [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) bereitstellen, um diese Verhaltensweisen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-161">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="5dc1d-162">So stellen Sie den Standort für **ShellExecuteEx zur Verfügung:**</span><span class="sxs-lookup"><span data-stu-id="5dc1d-162">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="5dc1d-163">Geben Sie das FLAG SEE \_ MASK \_ \_ HINST \_ IS SITE im \_ **fMask-Member** von [**SHELLEXECUTEINFO an.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)</span><span class="sxs-lookup"><span data-stu-id="5dc1d-163">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="5dc1d-164">Geben Sie [**IUnknown im**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **hInstApp-Member** von [**SHELLEXECUTEINFO an.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)</span><span class="sxs-lookup"><span data-stu-id="5dc1d-164">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="5dc1d-165">Verwenden von ShellExecute zum Starten des Suchdialogfelds</span><span class="sxs-lookup"><span data-stu-id="5dc1d-165">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="5dc1d-166">Wenn ein Benutzer im Explorer mit der rechten Maustaste auf ein Ordnersymbol Windows, ist eines der Menüelemente "Suchen".</span><span class="sxs-lookup"><span data-stu-id="5dc1d-166">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="5dc1d-167">Wenn sie dieses Element auswählen, startet die Shell ihr Suchprogramm.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-167">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="5dc1d-168">Dieses Hilfsprogramm zeigt ein Dialogfeld an, in dem Dateien nach einer angegebenen Textzeichenfolge durchsucht werden können.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-168">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="5dc1d-169">Eine Anwendung kann programmgesteuert das Suchprogramm für ein Verzeichnis starten, indem [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)mit "find" als *lpVerb-Parameter* und dem Verzeichnispfad als *lpFile-Parameter aufruft.*</span><span class="sxs-lookup"><span data-stu-id="5dc1d-169">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="5dc1d-170">Mit der folgenden Codezeile wird beispielsweise das Hilfsprogramm Suche für das Verzeichnis c: \\ MyPrograms gestartet.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-170">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="5dc1d-171">Ein einfaches Beispiel für die Verwendung von ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="5dc1d-171">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="5dc1d-172">Die folgende Beispielkonsolenanwendung veranschaulicht die Verwendung von [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="5dc1d-172">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="5dc1d-173">Die meisten Fehlerüberprüfungscodes wurden aus Gründen der Übersichtlichkeit ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-173">Most error checking code has been omitted for clarity.</span></span>


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



<span data-ttu-id="5dc1d-174">Die Anwendung ruft zuerst die PIDL des Windows-Verzeichnisses ab und listet ihren Inhalt auf, bis sie die erste .bmp findet.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-174">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="5dc1d-175">Im Gegensatz zum früheren Beispiel wird [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) verwendet, um den Analysenamen der Datei anstelle des Anzeigenamens abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-175">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="5dc1d-176">Da es sich um einen Dateisystemordner handelt, ist der Analysename ein vollqualifizierter Pfad, der für [**ShellExecuteEx erforderlich ist.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)</span><span class="sxs-lookup"><span data-stu-id="5dc1d-176">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="5dc1d-177">Nachdem die erste .bmp gefunden wurde, werden den Membern einer [**SHELLEXECUTEINFO-Struktur entsprechende Werte**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-177">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="5dc1d-178">Der **lpFile-Member** wird auf den Analysenamen der Datei und der **lpVerb-Member** auf **NULL** festgelegt, um den Standardvorgang zu starten.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-178">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="5dc1d-179">In diesem Fall ist der Standardvorgang "open".</span><span class="sxs-lookup"><span data-stu-id="5dc1d-179">In this case, the default operation is "open".</span></span> <span data-ttu-id="5dc1d-180">Die -Struktur wird dann an [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)übergeben, die den Standardhandler für Bitmapdateien startet, in der Regel MSPaint.exe, um die Datei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-180">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="5dc1d-181">Nachdem die Funktion zurückgegeben wurde, werden die PIDLs freigegeben, und Windows [**IShellFolder-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) des Ordners wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-181">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 
