---
description: Zeigt ein Hilfefenster an, das der aktuellen UI-Spracheinstellung entspricht.
title: Mlhtmlhelp-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: a477ef549b3b8437ba891259c7fecea4730f759e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993799"
---
# <a name="mlhtmlhelp-function"></a><span data-ttu-id="08ab2-103">Mlhtmlhelp-Funktion</span><span class="sxs-lookup"><span data-stu-id="08ab2-103">MLHtmlHelp function</span></span>

<span data-ttu-id="08ab2-104">\[Diese Funktion ist über Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="08ab2-104">\[This function is available through Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="08ab2-105">Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="08ab2-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="08ab2-106">Zeigt ein Hilfefenster an, das der aktuellen UI-Spracheinstellung entspricht.</span><span class="sxs-lookup"><span data-stu-id="08ab2-106">Displays a help window that corresponds to the current UI language setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="08ab2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="08ab2-107">Syntax</span></span>


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a><span data-ttu-id="08ab2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="08ab2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08ab2-109">*hwndcaller* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08ab2-109">*hwndCaller* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab2-110">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="08ab2-110">Type: **HWND**</span></span>

<span data-ttu-id="08ab2-111">Ein Handle für das übergeordnete Fenster, das diese Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="08ab2-111">A handle to the parent window that calls this function.</span></span>

</dd> <dt>

<span data-ttu-id="08ab2-112">*pszFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08ab2-112">*pszFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab2-113">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="08ab2-113">Type: **LPCTSTR**</span></span>

<span data-ttu-id="08ab2-114">Ein Zeiger auf einen Puffer, der den voll qualifizierten Pfad einer kompilierten Hilfedatei (. chm) oder eine themendatei in einer angegebenen Hilfedatei enthält.</span><span class="sxs-lookup"><span data-stu-id="08ab2-114">A pointer to a buffer that contains the fully qualified path of a compiled help (.chm) file, or a topic file within a specified help file.</span></span>

</dd> <dt>

<span data-ttu-id="08ab2-115">*ucommand* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08ab2-115">*uCommand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab2-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="08ab2-116">Type: **UINT**</span></span>

<span data-ttu-id="08ab2-117">Der Befehl, der ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08ab2-117">The command to complete.</span></span> <span data-ttu-id="08ab2-118">Diese Funktion unterstützt direkt nur das [HH- \_ Anzeige \_ Thema](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) und das [HH- \_ Anzeige \_ \_ TextPopup](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span><span class="sxs-lookup"><span data-stu-id="08ab2-118">This function directly supports only [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) and [HH\_DISPLAY\_TEXT\_POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span></span> <span data-ttu-id="08ab2-119">Bei einem beliebigen anderen Befehl wird der-Befehl ohne den *dwcrosscodepage* -Wert an [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api)weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="08ab2-119">In the case of any other command, the call is forwarded without the *dwCrossCodePage* value to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span></span>

</dd> <dt>

<span data-ttu-id="08ab2-120">*dwdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08ab2-120">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab2-121">Typ: **DWORD \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="08ab2-121">Type: **DWORD\_PTR**</span></span>

<span data-ttu-id="08ab2-122">Alle Daten, die möglicherweise erforderlich sind, basierend auf dem Wert des *ucommand* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="08ab2-122">Any data that may be required, based on the value of the *uCommand* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="08ab2-123">*dwcrosscodepage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08ab2-123">*dwCrossCodePage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab2-124">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="08ab2-124">Type: **DWORD**</span></span>

<span data-ttu-id="08ab2-125">Der **DWORD** -Wert, der die Codepage der aktuellen UI-Spracheinstellung angibt, z \_ . b. CP ACP.</span><span class="sxs-lookup"><span data-stu-id="08ab2-125">The **DWORD** value indicating the code page of the current UI language setting, such as CP\_ACP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08ab2-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08ab2-126">Return value</span></span>

<span data-ttu-id="08ab2-127">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="08ab2-127">Type: **HWND**</span></span>

<span data-ttu-id="08ab2-128">Abhängig vom angegebenen *ucommand* und dem Ergebnis gibt **mlhtmlhelp** einen oder beide der folgenden zurück:</span><span class="sxs-lookup"><span data-stu-id="08ab2-128">Depending on the specified *uCommand* and the result, **MLHtmlHelp** returns one or both of the following:</span></span>

-   <span data-ttu-id="08ab2-129">Das Handle (HWND) des Hilfe Fensters.</span><span class="sxs-lookup"><span data-stu-id="08ab2-129">The handle (hwnd) of the help window.</span></span>
-   <span data-ttu-id="08ab2-130">**Null**.</span><span class="sxs-lookup"><span data-stu-id="08ab2-130">**NULL**.</span></span> <span data-ttu-id="08ab2-131">In einigen Fällen weist **null** auf einen Fehler hin. in anderen Fällen gibt **null** an, dass das Hilfefenster noch nicht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="08ab2-131">In some cases, **NULL** indicates failure; in other cases, **NULL** indicates that the help window has not yet been created.</span></span>

## <a name="remarks"></a><span data-ttu-id="08ab2-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08ab2-132">Remarks</span></span>

<span data-ttu-id="08ab2-133">Wenn ein Problem mit dem Pfad der Hilfedatei für die aktuelle Sprache auftritt, wird der-Befehl zur Standardbehandlung an [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="08ab2-133">If a problem arises with the path of the help file for the current language, the call is forwarded to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) for standard handling.</span></span>

<span data-ttu-id="08ab2-134">Wenn das Hilfefenster geschlossen wird, wird der Fokus an den Besitzer zurückgegeben, es sei denn, der Besitzer ist der Desktop.</span><span class="sxs-lookup"><span data-stu-id="08ab2-134">When the help window is closed, focus returns to the owner unless the owner is the desktop.</span></span> <span data-ttu-id="08ab2-135">Wenn *hwndcaller* der Desktop ist, bestimmt das Betriebssystem, wohin der Fokus zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="08ab2-135">If *hwndCaller* is the desktop, then the operating system determines where focus is returned.</span></span>

<span data-ttu-id="08ab2-136">Wenn **mlhtmlhelp** Benachrichtigungs Meldungen aus dem Hilfefenster sendet, werden die Nachrichten außerdem an *hwndcaller* gesendet, solange Sie die Nachverfolgung von [Benachrichtigungs](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) Meldungen in der Hilfefenster Definition aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="08ab2-136">In addition, if **MLHtmlHelp** sends any notification messages from the help window, the messages are sent to *hwndCaller* as long as you have enabled [notification message](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) tracking in the help window definition.</span></span>

## <a name="examples"></a><span data-ttu-id="08ab2-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08ab2-137">Examples</span></span>

<span data-ttu-id="08ab2-138">Im folgenden Beispiel wird der Befehl [HH \_ Display \_ Topic](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) aufgerufen, um die Hilfedatei mit dem Namen Help. chm zu öffnen und das Standardthema im Hilfefenster mit dem Namen anzuzeigen `Mainwin` .</span><span class="sxs-lookup"><span data-stu-id="08ab2-138">The following example calls the [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) command to open the help file named Help.chm and display its default topic in the help window named `Mainwin`.</span></span> <span data-ttu-id="08ab2-139">Im Allgemeinen handelt es sich bei dem in diesem Befehl angegebenen Hilfefenster um einen HTML-Standard [Hilfe Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span><span class="sxs-lookup"><span data-stu-id="08ab2-139">Generally, the help window specified in this command is a standard [HTML Help Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span></span>

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> <span data-ttu-id="08ab2-140">Wenn Sie diese Funktion verwenden, legen Sie die Stapelgröße der ausführbaren Hostingdatei auf mindestens 100K fest.</span><span class="sxs-lookup"><span data-stu-id="08ab2-140">When using this function, set the stack size of the hosting executable to at least 100k.</span></span> <span data-ttu-id="08ab2-141">Wenn die definierte Stapelgröße zu klein ist, wird der zum Ausführen der HTML-Hilfe erstellte Thread ebenfalls mit dieser Stapelgröße erstellt, und der Vorgang kann fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="08ab2-141">If the defined stack size is too small, then the thread created to run HTML Help will also be created with this stack size, and the operation could fail.</span></span> <span data-ttu-id="08ab2-142">Optional können Sie/Stack aus der Link Befehlszeile entfernen und auch beliebige Stapel Einstellungen in der DEF-Datei der ausführbaren Datei entfernen (in diesem Fall ist die Standard Stapelgröße 1 MB).</span><span class="sxs-lookup"><span data-stu-id="08ab2-142">Optionally, you can remove /STACK from the link command line, and also remove any STACK setting in the executable's DEF file (default stack size is 1MB in this case).</span></span> <span data-ttu-id="08ab2-143">Sie können auch die Stapelgröße mit dem/fnumber-Compilerbefehl festlegen (der Compiler übergibt dies als/Stack an den Linker).</span><span class="sxs-lookup"><span data-stu-id="08ab2-143">You can also set the stack size using the /Fnumber compiler command (the compiler will pass this to the linker as /STACK).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08ab2-144">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="08ab2-144">Requirements</span></span>



| <span data-ttu-id="08ab2-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08ab2-145">Requirement</span></span> | <span data-ttu-id="08ab2-146">Wert</span><span class="sxs-lookup"><span data-stu-id="08ab2-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08ab2-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08ab2-147">Minimum supported client</span></span><br/> | <span data-ttu-id="08ab2-148">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08ab2-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08ab2-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08ab2-149">Minimum supported server</span></span><br/> | <span data-ttu-id="08ab2-150">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08ab2-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="08ab2-151">Header</span><span class="sxs-lookup"><span data-stu-id="08ab2-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="08ab2-152"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="08ab2-152"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="08ab2-153">DLL</span><span class="sxs-lookup"><span data-stu-id="08ab2-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08ab2-154"><dt>Shlwapi.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="08ab2-154"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="08ab2-155">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="08ab2-155">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="08ab2-156">**Mlhtmlhelpw** (Unicode) und **mlhtmlhelpa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="08ab2-156">**MLHtmlHelpW** (Unicode) and **MLHtmlHelpA** (ANSI)</span></span><br/>                                               |



 

 
