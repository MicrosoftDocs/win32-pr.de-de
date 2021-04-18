---
description: Führt einen Vorgang für eine angegebene Datei aus.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: Wowshellexecute-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: ae50ad570211303cdfb7aa8e86908593ab48537d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106368281"
---
# <a name="wowshellexecute-function"></a><span data-ttu-id="7f6ed-103">Wowshellexecute-Funktion</span><span class="sxs-lookup"><span data-stu-id="7f6ed-103">WOWShellExecute function</span></span>

<span data-ttu-id="7f6ed-104">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="7f6ed-105">Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="7f6ed-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7f6ed-106">Führt einen Vorgang für eine angegebene Datei aus.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-106">Performs an operation on a specified file.</span></span> <span data-ttu-id="7f6ed-107">**Wowshellexecute** ist nur für die Verwendung mit dem Microsoft Windows NT Virtual DOS Machine (Ntvdm.exe) vorhanden, mit dem Betriebssystem-und 16-Bit-Software auf einem Windows-System ausgeführt werden kann und von keinem anderen Benutzer verwendet werden darf.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-107">**WOWShellExecute** exists only for use with the Microsoft Windows NT Virtual DOS Machine (Ntvdm.exe), which allows disk operating system (DOS) and 16-bit software to run on a Windows system, and should not be used by anyone else.</span></span> <span data-ttu-id="7f6ed-108">Verwenden Sie stattdessen [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="7f6ed-108">Use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6ed-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f6ed-109">Syntax</span></span>


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a><span data-ttu-id="7f6ed-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f6ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f6ed-111">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f6ed-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f6ed-112">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-112">Type: **HWND**</span></span>

<span data-ttu-id="7f6ed-113">Ein Handle für das Besitzer Fenster, das für die Anzeige einer Benutzeroberfläche oder von Fehlermeldungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-113">A handle to the owner window used for displaying a UI or error messages.</span></span> <span data-ttu-id="7f6ed-114">Dieser Wert kann **null** sein, wenn der Vorgang keinem Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-114">This value can be **NULL** if the operation is not associated with a window.</span></span>

</dd> <dt>

<span data-ttu-id="7f6ed-115">*lpoperation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f6ed-115">*lpOperation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f6ed-116">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-116">Type: **LPCTSTR**</span></span>

<span data-ttu-id="7f6ed-117">Ein Zeiger auf eine mit **null** endende Zeichenfolge, die in diesem Fall als *Verb* bezeichnet wird und die auszuführende Aktion angibt.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-117">A pointer to a **null**-terminated string, referred to in this case as a *verb*, that specifies the action to be performed.</span></span> <span data-ttu-id="7f6ed-118">Der Satz der verfügbaren Verben hängt von der jeweiligen Datei bzw. dem Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-118">The set of available verbs depends on the particular file or folder.</span></span> <span data-ttu-id="7f6ed-119">Im Allgemeinen sind die im Kontextmenü eines Objekts verfügbaren Aktionen verfügbare Verben.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-119">Generally, the actions available from an object's shortcut menu are available verbs.</span></span> <span data-ttu-id="7f6ed-120">Weitere Informationen zu Verben und deren Verfügbarkeit finden Sie im Abschnitt *Objekt Verben* unter [Starten von Anwendungen](launch.md).</span><span class="sxs-lookup"><span data-stu-id="7f6ed-120">For more information about verbs and their availability, see the *Object Verbs* section of [Launching Applications](launch.md).</span></span> <span data-ttu-id="7f6ed-121">Weitere Erörterung von Kontextmenüs finden Sie unter Erweitern von Kontext [Menüs](context.md) .</span><span class="sxs-lookup"><span data-stu-id="7f6ed-121">See [Extending Shortcut Menus](context.md) for further discussion of shortcut menus.</span></span> <span data-ttu-id="7f6ed-122">Die folgenden Verben werden häufig verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-122">The following verbs are commonly used.</span></span>

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span data-ttu-id="7f6ed-123"><span id="edit"></span><span id="EDIT"></span>**Bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-123"><span id="edit"></span><span id="EDIT"></span>**edit**</span></span>


</dt> <dd>

<span data-ttu-id="7f6ed-124">Öffnet einen Editor und öffnet das Dokument zum Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-124">Launches an editor and opens the document for editing.</span></span> <span data-ttu-id="7f6ed-125">Wenn *lpfile* keine Dokument Datei ist, tritt bei der Funktion ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-125">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span data-ttu-id="7f6ed-126"><span id="explore"></span><span id="EXPLORE"></span>**Entdecken**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-126"><span id="explore"></span><span id="EXPLORE"></span>**explore**</span></span>


</dt> <dd>

<span data-ttu-id="7f6ed-127">Untersucht den von *lpfile* angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-127">Explores the folder specified by *lpFile*.</span></span>

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span data-ttu-id="7f6ed-128"><span id="find"></span><span id="FIND"></span>**sich**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-128"><span id="find"></span><span id="FIND"></span>**find**</span></span>


</dt> <dd>

<span data-ttu-id="7f6ed-129">Initiiert eine Suche beginnend mit dem angegebenen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-129">Initiates a search starting from the specified directory.</span></span>

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span data-ttu-id="7f6ed-130"><span id="open"></span><span id="OPEN"></span>**eren**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-130"><span id="open"></span><span id="OPEN"></span>**open**</span></span>


</dt> <dd>

<span data-ttu-id="7f6ed-131">Öffnet die Datei, die durch den *lpfile* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-131">Opens the file specified by the *lpFile* parameter.</span></span> <span data-ttu-id="7f6ed-132">Bei der Datei kann es sich um eine ausführbare Datei, eine Dokument Datei oder einen Ordner handeln.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-132">The file can be an executable file, a document file, or a folder.</span></span>

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="7f6ed-133"><span id="print"></span><span id="PRINT"></span>**gedruck**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-133"><span id="print"></span><span id="PRINT"></span>**print**</span></span>


</dt> <dd>

<span data-ttu-id="7f6ed-134">Druckt die von *lpfile* angegebene Dokument Datei.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-134">Prints the document file specified by *lpFile*.</span></span> <span data-ttu-id="7f6ed-135">Wenn *lpfile* keine Dokument Datei ist, tritt bei der Funktion ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-135">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span data-ttu-id="7f6ed-136"><span id="NULL"></span><span id="null"></span>**Normal**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-136"><span id="NULL"></span><span id="null"></span>**NULL**</span></span>


</dt> <dd>

<span data-ttu-id="7f6ed-137">Für Systeme vor Windows 2000 wird das Standardverb verwendet, wenn es gültig und in der Registrierung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-137">For systems prior to Windows 2000, the default verb is used if it is valid and available in the registry.</span></span> <span data-ttu-id="7f6ed-138">Wenn dies nicht der Wert ist, wird das Verb "Öffnen" verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-138">If not, the "open" verb is used.</span></span>

<span data-ttu-id="7f6ed-139">Für Windows 2000-Systeme und spätere Systeme wird das Standardverb verwendet, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-139">For Windows 2000 and later systems, the default verb is used if available.</span></span> <span data-ttu-id="7f6ed-140">Wenn dies nicht der Wert ist, wird das Verb "Öffnen" verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-140">If not, the "open" verb is used.</span></span> <span data-ttu-id="7f6ed-141">Wenn keines der beiden Verb verfügbar ist, verwendet das System das erste Verb, das in der Registrierung aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-141">If neither verb is available, the system uses the first verb listed in the registry.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7f6ed-142">*lpfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f6ed-142">*lpFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f6ed-143">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-143">Type: **LPCTSTR**</span></span>

<span data-ttu-id="7f6ed-144">Ein Zeiger auf eine **null**-terminierte Zeichenfolge, die die Datei oder das Objekt angibt, für das das angegebene Verb ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-144">A pointer to a **null**-terminated string that specifies the file or object on which to execute the specified verb.</span></span> <span data-ttu-id="7f6ed-145">Übergeben Sie zum Angeben eines Shell-Namespace Objekts den voll qualifizierten Namen der Analyse.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-145">To specify a Shell namespace object, pass the fully qualified parse name.</span></span> <span data-ttu-id="7f6ed-146">Beachten Sie, dass nicht alle Verben für alle Objekte unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-146">Note that not all verbs are supported on all objects.</span></span> <span data-ttu-id="7f6ed-147">Beispielsweise unterstützen nicht alle Dokumenttypen das Verb "Drucken".</span><span class="sxs-lookup"><span data-stu-id="7f6ed-147">For example, not all document types support the "print" verb.</span></span>

</dd> <dt>

<span data-ttu-id="7f6ed-148">*lpparameters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f6ed-148">*lpParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f6ed-149">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-149">Type: **LPCTSTR**</span></span>

<span data-ttu-id="7f6ed-150">Wenn der *lpfile* -Parameter eine ausführbare Datei angibt, ist *lpparameters* ein Zeiger auf eine auf **null** endende Zeichenfolge, die die Parameter angibt, die an die Anwendung übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-150">If the *lpFile* parameter specifies an executable file, *lpParameters* is a pointer to a **null**-terminated string that specifies the parameters to be passed to the application.</span></span> <span data-ttu-id="7f6ed-151">Das Format dieser Zeichenfolge wird durch das Verb bestimmt, das aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-151">The format of this string is determined by the verb that is to be invoked.</span></span> <span data-ttu-id="7f6ed-152">Wenn die *lpfile-Datei* eine Dokument Datei angibt, sollten *lpparameters* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-152">If *lpFile* specifies a document file, *lpParameters* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7f6ed-153">*lpdirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f6ed-153">*lpDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f6ed-154">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-154">Type: **LPCTSTR**</span></span>

<span data-ttu-id="7f6ed-155">Ein Zeiger auf eine **null**-terminierte Zeichenfolge, die das Standardverzeichnis angibt.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-155">A pointer to a **null**-terminated string that specifies the default directory.</span></span>

</dd> <dt>

<span data-ttu-id="7f6ed-156">*nshowcmd* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f6ed-156">*nShowCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f6ed-157">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-157">Type: **INT**</span></span>

<span data-ttu-id="7f6ed-158">Die Flags, die angeben, wie eine Anwendung beim Öffnen angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-158">The flags that specify how an application is to be displayed when it is opened.</span></span> <span data-ttu-id="7f6ed-159">Wenn *lpfile* eine Dokument Datei angibt, wird das Flag einfach an die zugehörige Anwendung übergeben.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-159">If *lpFile* specifies a document file, the flag is simply passed to the associated application.</span></span> <span data-ttu-id="7f6ed-160">Es liegt an der Anwendung, zu entscheiden, wie Sie behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-160">It is up to the application to decide how to handle it.</span></span> <span data-ttu-id="7f6ed-161">Dabei kann es sich um einen beliebigen Wert handeln, der im *nCmdShow* -Parameter für die [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-161">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="7f6ed-162">*lpfncbwinexec*</span><span class="sxs-lookup"><span data-stu-id="7f6ed-162">*lpfnCBWinExec*</span></span> 
</dt> <dd>

<span data-ttu-id="7f6ed-163">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="7f6ed-163">Type: **void\***</span></span>

<span data-ttu-id="7f6ed-164">Rückruffunktion, die verwendet wird, um " [**deateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " im 16-Bit-Kernel aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-164">Callback function used to call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) in the 16-bit kernel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f6ed-165">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f6ed-165">Return value</span></span>

<span data-ttu-id="7f6ed-166">Typ: **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-166">Type: **HINSTANCE**</span></span>

<span data-ttu-id="7f6ed-167">Gibt einen Wert zurück, der größer als 32 ist, wenn erfolgreich, oder einen Fehlerwert, der kleiner oder gleich 32 ist, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-167">Returns a value greater than 32 if successful, or an error value that is less than or equal to 32 otherwise.</span></span> <span data-ttu-id="7f6ed-168">In der folgenden Tabelle sind die Fehler Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-168">The following table lists the error values.</span></span> <span data-ttu-id="7f6ed-169">Der Rückgabewert wird als HINSTANCE für die Abwärtskompatibilität mit 16-Bit-Windows-Anwendungen umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-169">The return value is cast as an HINSTANCE for backward compatibility with 16-bit Windows applications.</span></span> <span data-ttu-id="7f6ed-170">Es handelt sich jedoch nicht um eine echte HINSTANCE.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-170">It is not a true HINSTANCE, however.</span></span> <span data-ttu-id="7f6ed-171">Das einzige, was mit der zurückgegebenen HINSTANCE erreicht werden kann, ist die Umwandlung in einen **int** -Wert und das Vergleichen mit dem Wert 32 oder einem der unten angegebenen Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-171">The only thing that can be done with the returned HINSTANCE is to cast it to an **int** and compare it with the value 32 or one of the error codes below.</span></span>



| <span data-ttu-id="7f6ed-172">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7f6ed-172">Return code</span></span>                                                                                             | <span data-ttu-id="7f6ed-173">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f6ed-173">Description</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f6ed-174"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-174"><dt>**0**</dt></span></span> </dl>                        | <span data-ttu-id="7f6ed-175">Das Betriebssystem verfügt nicht über genügend Arbeitsspeicher oder Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-175">The operating system is out of memory or resources.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="7f6ed-176"><dt>**Fehler \_ Datei \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-176"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="7f6ed-177">Die angegebene Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-177">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="7f6ed-178"><dt>**der Fehler \_ Pfad wurde \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-178"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="7f6ed-179">Der angegebene Pfad wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-179">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="7f6ed-180"><dt>**fehlerhaftes \_ \_ Format**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-180"><dt>**ERROR\_BAD\_FORMAT**</dt></span></span> </dl>       | <span data-ttu-id="7f6ed-181">Die exe-Datei ist ungültig (keine Win32. exe-Datei oder Fehler im exe-Image).</span><span class="sxs-lookup"><span data-stu-id="7f6ed-181">The .exe file is invalid (non-Win32 .exe or error in .exe image).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="7f6ed-182"><dt>**SE \_ Err \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-182"><dt>**SE\_ERR\_ACCESSDENIED**</dt></span></span> </dl>    | <span data-ttu-id="7f6ed-183">Das Betriebssystem hat den Zugriff auf die angegebene Datei verweigert.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-183">The operating system denied access to the specified file.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="7f6ed-184"><dt>**SE \_ Err \_ associncomplete**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-184"><dt>**SE\_ERR\_ASSOCINCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="7f6ed-185">Die Dateinamen Zuordnung ist unvollständig oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-185">The file name association is incomplete or invalid.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="7f6ed-186"><dt>**SE \_ Err \_ DDE ausgelastet**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-186"><dt>**SE\_ERR\_DDEBUSY**</dt></span></span> </dl>         | <span data-ttu-id="7f6ed-187">Die DDE-Transaktion konnte nicht abgeschlossen werden, da andere DDE-Transaktionen verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-187">The DDE transaction could not be completed because other DDE transactions were being processed.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="7f6ed-188"><dt>**SE \_ Err \_ dmissfail**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-188"><dt>**SE\_ERR\_DDEFAIL**</dt></span></span> </dl>         | <span data-ttu-id="7f6ed-189">Fehler bei DDE-Transaktion.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-189">The DDE transaction failed.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="7f6ed-190"><dt>**SE \_ Err \_ ddetimeout**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-190"><dt>**SE\_ERR\_DDETIMEOUT**</dt></span></span> </dl>      | <span data-ttu-id="7f6ed-191">Die DDE-Transaktion konnte nicht abgeschlossen werden, da die Anforderung abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-191">The DDE transaction could not be completed because the request timed out.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="7f6ed-192"><dt>**SE \_ Err \_ dllnotfound**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-192"><dt>**SE\_ERR\_DLLNOTFOUND**</dt></span></span> </dl>     | <span data-ttu-id="7f6ed-193">Die angegebene DLL wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-193">The specified DLL was not found.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="7f6ed-194"><dt>**SE \_ Err \_ FNF**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-194"><dt>**SE\_ERR\_FNF**</dt></span></span> </dl>             | <span data-ttu-id="7f6ed-195">Die angegebene Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-195">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="7f6ed-196"><dt>**SE \_ Err \_ noassoc**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-196"><dt>**SE\_ERR\_NOASSOC**</dt></span></span> </dl>         | <span data-ttu-id="7f6ed-197">Der angegebenen Dateinamenerweiterung ist keine Anwendung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-197">There is no application associated with the given file name extension.</span></span> <span data-ttu-id="7f6ed-198">Dieser Fehler wird auch zurückgegeben, wenn Sie versuchen, eine nicht druckbare Datei zu drucken.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-198">This error will also be returned if you attempt to print a file that is not printable.</span></span><br/> |
| <dl> <span data-ttu-id="7f6ed-199"><dt>**SE \_ Err \_ OOM**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-199"><dt>**SE\_ERR\_OOM**</dt></span></span> </dl>             | <span data-ttu-id="7f6ed-200">Es war nicht genügend Arbeitsspeicher vorhanden, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-200">There was not enough memory to complete the operation.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="7f6ed-201"><dt>**SE \_ Err \_ PNF**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-201"><dt>**SE\_ERR\_PNF**</dt></span></span> </dl>             | <span data-ttu-id="7f6ed-202">Der angegebene Pfad wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-202">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="7f6ed-203"><dt>**SE \_ Err- \_ Freigabe**</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-203"><dt>**SE\_ERR\_SHARE**</dt></span></span> </dl>           | <span data-ttu-id="7f6ed-204">Eine Freigabe Verletzung ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-204">A sharing violation occurred.</span></span><br/>                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="7f6ed-205">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f6ed-205">Remarks</span></span>

<span data-ttu-id="7f6ed-206">**Wowshellexecute** ist nicht in einer Header-oder LIB-Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-206">**WOWShellExecute** is not included in a header or .lib file.</span></span> <span data-ttu-id="7f6ed-207">Sie wird aus Shell32.dll nach Namen exportiert.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-207">It is exported from Shell32.dll by name.</span></span>

<span data-ttu-id="7f6ed-208">Mit dieser Methode können Sie beliebige Befehle im Kontextmenü eines Ordners ausführen oder in der Registrierung speichern.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-208">This method allows you to execute any commands in a folder's shortcut menu or stored in the registry.</span></span>

<span data-ttu-id="7f6ed-209">Wenn *lpoperation* den Wert **null** hat, öffnet die Funktion die von *lpfile* angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-209">If *lpOperation* is **NULL**, the function opens the file specified by *lpFile*.</span></span> <span data-ttu-id="7f6ed-210">Wenn *lpoperation* "Open" oder "Explore" ist, versucht die Funktion, den Ordner zu öffnen oder zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-210">If *lpOperation* is "open" or "explore", the function attempts to open or explore the folder.</span></span>

<span data-ttu-id="7f6ed-211">Zum Abrufen von Informationen über die Anwendung, die als Ergebnis des Aufrufs von **wowshellexecute** gestartet wird, verwenden Sie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="7f6ed-211">To obtain information about the application that is launched as a result of calling **WOWShellExecute**, use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

> [!Note]  
> <span data-ttu-id="7f6ed-212">Die Einstellung **Ordner Fenster in einem separaten Prozess** in Ordneroptionen starten wirkt sich auf **wowshellexecute** aus.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-212">The **Launch folder windows in a separate process** setting in Folder Options affects **WOWShellExecute**.</span></span> <span data-ttu-id="7f6ed-213">Wenn diese Option deaktiviert ist (Standardeinstellung), verwendet **wowshellexecute** ein geöffnetes Explorer-Fenster, anstatt ein neues zu starten.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-213">If that option is disabled (the default setting), **WOWShellExecute** uses an open Explorer window rather than launch a new one.</span></span> <span data-ttu-id="7f6ed-214">Wenn kein Explorer-Fenster geöffnet ist, wird von **wowshellexecute** ein neues gestartet.</span><span class="sxs-lookup"><span data-stu-id="7f6ed-214">If no Explorer window is open, **WOWShellExecute** launches a new one.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7f6ed-215">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f6ed-215">Requirements</span></span>



| <span data-ttu-id="7f6ed-216">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f6ed-216">Requirement</span></span> | <span data-ttu-id="7f6ed-217">Wert</span><span class="sxs-lookup"><span data-stu-id="7f6ed-217">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6ed-218">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f6ed-218">Minimum supported client</span></span><br/> | <span data-ttu-id="7f6ed-219">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f6ed-219">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7f6ed-220">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f6ed-220">Minimum supported server</span></span><br/> | <span data-ttu-id="7f6ed-221">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f6ed-221">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7f6ed-222">DLL</span><span class="sxs-lookup"><span data-stu-id="7f6ed-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f6ed-223"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f6ed-223"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f6ed-224">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f6ed-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f6ed-225">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="7f6ed-225">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
