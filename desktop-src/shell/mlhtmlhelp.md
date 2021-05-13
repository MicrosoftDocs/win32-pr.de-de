---
description: Zeigt ein Hilfefenster an, das der aktuellen Einstellung der Benutzeroberflächensprache entspricht.
title: MLHtmlHelp-Funktion
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
ms.openlocfilehash: 38d331d57b9484ab6d7a505d929508f30d510ad8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841211"
---
# <a name="mlhtmlhelp-function"></a><span data-ttu-id="6a265-103">MLHtmlHelp-Funktion</span><span class="sxs-lookup"><span data-stu-id="6a265-103">MLHtmlHelp function</span></span>

<span data-ttu-id="6a265-104">\[Diese Funktion ist über Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6a265-104">\[This function is available through Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6a265-105">Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="6a265-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="6a265-106">Zeigt ein Hilfefenster an, das der aktuellen Einstellung der Benutzeroberflächensprache entspricht.</span><span class="sxs-lookup"><span data-stu-id="6a265-106">Displays a help window that corresponds to the current UI language setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a265-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a265-107">Syntax</span></span>


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a><span data-ttu-id="6a265-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a265-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a265-109">*hwndCaller* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6a265-109">*hwndCaller* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a265-110">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="6a265-110">Type: **HWND**</span></span>

<span data-ttu-id="6a265-111">Ein Handle für das übergeordnete Fenster, das diese Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="6a265-111">A handle to the parent window that calls this function.</span></span>

</dd> <dt>

<span data-ttu-id="6a265-112">*pszFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6a265-112">*pszFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a265-113">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="6a265-113">Type: **LPCTSTR**</span></span>

<span data-ttu-id="6a265-114">Ein Zeiger auf einen Puffer, der den vollqualifizierten Pfad einer kompilierten Hilfedatei (.chm) oder eine Themendatei in einer angegebenen Hilfedatei enthält.</span><span class="sxs-lookup"><span data-stu-id="6a265-114">A pointer to a buffer that contains the fully qualified path of a compiled help (.chm) file, or a topic file within a specified help file.</span></span>

</dd> <dt>

<span data-ttu-id="6a265-115">*uCommand* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6a265-115">*uCommand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a265-116">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="6a265-116">Type: **UINT**</span></span>

<span data-ttu-id="6a265-117">Der auszuführende Befehl.</span><span class="sxs-lookup"><span data-stu-id="6a265-117">The command to complete.</span></span> <span data-ttu-id="6a265-118">Diese Funktion unterstützt nur [HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) und [HH \_ DISPLAY TEXT \_ \_ POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command)direkt.</span><span class="sxs-lookup"><span data-stu-id="6a265-118">This function directly supports only [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) and [HH\_DISPLAY\_TEXT\_POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span></span> <span data-ttu-id="6a265-119">Bei einem anderen Befehl wird der Aufruf ohne den *dwCrossCodePage-Wert* an [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api)weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="6a265-119">In the case of any other command, the call is forwarded without the *dwCrossCodePage* value to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span></span>

</dd> <dt>

<span data-ttu-id="6a265-120">*dwData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6a265-120">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a265-121">Typ: **DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="6a265-121">Type: **DWORD\_PTR**</span></span>

<span data-ttu-id="6a265-122">Alle daten, die erforderlich sein können, basierend auf dem Wert des *uCommand-Parameters.*</span><span class="sxs-lookup"><span data-stu-id="6a265-122">Any data that may be required, based on the value of the *uCommand* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6a265-123">*dwCrossCodePage* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6a265-123">*dwCrossCodePage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a265-124">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6a265-124">Type: **DWORD**</span></span>

<span data-ttu-id="6a265-125">Der **DWORD-Wert,** der die Codepage der aktuellen Ui-Spracheinstellung angibt, z. B. CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="6a265-125">The **DWORD** value indicating the code page of the current UI language setting, such as CP\_ACP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a265-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a265-126">Return value</span></span>

<span data-ttu-id="6a265-127">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="6a265-127">Type: **HWND**</span></span>

<span data-ttu-id="6a265-128">Abhängig vom angegebenen *uCommand* und dem Ergebnis gibt **MLHtmlHelp** eine oder beide der folgenden Punkte zurück:</span><span class="sxs-lookup"><span data-stu-id="6a265-128">Depending on the specified *uCommand* and the result, **MLHtmlHelp** returns one or both of the following:</span></span>

-   <span data-ttu-id="6a265-129">Das Handle (hwnd) des Hilfefensters.</span><span class="sxs-lookup"><span data-stu-id="6a265-129">The handle (hwnd) of the help window.</span></span>
-   <span data-ttu-id="6a265-130">**NULL.**</span><span class="sxs-lookup"><span data-stu-id="6a265-130">**NULL**.</span></span> <span data-ttu-id="6a265-131">In einigen Fällen gibt **NULL einen** Fehler an. in anderen Fällen gibt **NULL** an, dass das Hilfefenster noch nicht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6a265-131">In some cases, **NULL** indicates failure; in other cases, **NULL** indicates that the help window has not yet been created.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a265-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a265-132">Remarks</span></span>

<span data-ttu-id="6a265-133">Wenn ein Problem mit dem Pfad der Hilfedatei für die aktuelle Sprache auftritt, wird der Aufruf zur Standardbehandlung an [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="6a265-133">If a problem arises with the path of the help file for the current language, the call is forwarded to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) for standard handling.</span></span>

<span data-ttu-id="6a265-134">Wenn das Hilfefenster geschlossen ist, kehrt der Fokus zum Besitzer zurück, es sei denn, der Besitzer ist der Desktop.</span><span class="sxs-lookup"><span data-stu-id="6a265-134">When the help window is closed, focus returns to the owner unless the owner is the desktop.</span></span> <span data-ttu-id="6a265-135">Wenn *hwndCaller* der Desktop ist, bestimmt das Betriebssystem, wo der Fokus zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6a265-135">If *hwndCaller* is the desktop, then the operating system determines where focus is returned.</span></span>

<span data-ttu-id="6a265-136">Wenn **MLHtmlHelp** darüber hinaus Benachrichtigungsmeldungen aus dem Hilfefenster sendet, werden die Nachrichten an [](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) *hwndCaller* gesendet, solange Sie die Nachverfolgung von Benachrichtigungsmeldungen in der Hilfefensterdefinition aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="6a265-136">In addition, if **MLHtmlHelp** sends any notification messages from the help window, the messages are sent to *hwndCaller* as long as you have enabled [notification message](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) tracking in the help window definition.</span></span>

## <a name="examples"></a><span data-ttu-id="6a265-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a265-137">Examples</span></span>

<span data-ttu-id="6a265-138">Das folgende Beispiel ruft den [Befehl HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) auf, um die Hilfedatei mit dem Namen Help.chm zu öffnen und ihr Standardthema im Hilfefenster mit dem Namen `Mainwin` anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6a265-138">The following example calls the [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) command to open the help file named Help.chm and display its default topic in the help window named `Mainwin`.</span></span> <span data-ttu-id="6a265-139">Im Allgemeinen ist das in diesem Befehl angegebene Hilfefenster ein standardmäßiger [HTML Help Viewer.](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)</span><span class="sxs-lookup"><span data-stu-id="6a265-139">Generally, the help window specified in this command is a standard [HTML Help Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span></span>

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> <span data-ttu-id="6a265-140">Legen Sie bei Verwendung dieser Funktion die Stapelgröße der ausführbaren Hostdatei auf mindestens 100.000 fest.</span><span class="sxs-lookup"><span data-stu-id="6a265-140">When using this function, set the stack size of the hosting executable to at least 100k.</span></span> <span data-ttu-id="6a265-141">Wenn die definierte Stapelgröße zu klein ist, wird der Thread, der zum Ausführen der HTML-Hilfe erstellt wurde, ebenfalls mit dieser Stapelgröße erstellt, und der Vorgang kann fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="6a265-141">If the defined stack size is too small, then the thread created to run HTML Help will also be created with this stack size, and the operation could fail.</span></span> <span data-ttu-id="6a265-142">Optional können Sie /STACK aus der Linkbefehlszeile entfernen und auch alle STACK-Einstellungen in der DEF-Datei der ausführbaren Datei entfernen (in diesem Fall ist die Standardstapelgröße 1 MB).</span><span class="sxs-lookup"><span data-stu-id="6a265-142">Optionally, you can remove /STACK from the link command line, and also remove any STACK setting in the executable's DEF file (default stack size is 1MB in this case).</span></span> <span data-ttu-id="6a265-143">Sie können die Stapelgröße auch mit dem Compilerbefehl /Fnumber festlegen (der Compiler über gibt diese als /STACK an den Linker weiter).</span><span class="sxs-lookup"><span data-stu-id="6a265-143">You can also set the stack size using the /Fnumber compiler command (the compiler will pass this to the linker as /STACK).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a265-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a265-144">Requirements</span></span>



| <span data-ttu-id="6a265-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a265-145">Requirement</span></span> | <span data-ttu-id="6a265-146">Wert</span><span class="sxs-lookup"><span data-stu-id="6a265-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a265-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a265-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6a265-148">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a265-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a265-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a265-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6a265-150">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a265-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6a265-151">Header</span><span class="sxs-lookup"><span data-stu-id="6a265-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a265-152"><dt>Keine</dt></span><span class="sxs-lookup"><span data-stu-id="6a265-152"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="6a265-153">DLL</span><span class="sxs-lookup"><span data-stu-id="6a265-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a265-154"><dt>Shlwapi.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="6a265-154"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="6a265-155">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="6a265-155">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6a265-156">**MLHtmlHelpW** (Unicode) und **MLHtmlHelpA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6a265-156">**MLHtmlHelpW** (Unicode) and **MLHtmlHelpA** (ANSI)</span></span><br/>                                               |



 

 
