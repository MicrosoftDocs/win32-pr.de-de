---
description: Führt einen angegebenen Vorgang für eine angegebene Datei aus.
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Shell.ShellExecute-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 83ab9741199bff675245f15dc2ad1ffb20592a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979888"
---
# <a name="shellshellexecute-method"></a><span data-ttu-id="6032b-103">Shell. ShellExecute-Methode</span><span class="sxs-lookup"><span data-stu-id="6032b-103">Shell.ShellExecute method</span></span>

<span data-ttu-id="6032b-104">Führt einen angegebenen Vorgang für eine angegebene Datei aus.</span><span class="sxs-lookup"><span data-stu-id="6032b-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6032b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6032b-105">Syntax</span></span>

<span data-ttu-id="6032b-106">JScript</span><span class="sxs-lookup"><span data-stu-id="6032b-106">JScript:</span></span>

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

<span data-ttu-id="6032b-107">VBScript</span><span class="sxs-lookup"><span data-stu-id="6032b-107">VBScript:</span></span>

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

<span data-ttu-id="6032b-108">VB:</span><span class="sxs-lookup"><span data-stu-id="6032b-108">VB:</span></span>

```vb
Shell.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```

## <a name="parameters"></a><span data-ttu-id="6032b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6032b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6032b-110">*sFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6032b-110">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6032b-111">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6032b-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6032b-112">Eine **Zeichenfolge** , die den Namen der Datei enthält, in der **ShellExecute** die durch *voperation* angegebene Aktion ausführt.</span><span class="sxs-lookup"><span data-stu-id="6032b-112">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="6032b-113">*varguments* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="6032b-113">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6032b-114">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="6032b-114">Type: **Variant**</span></span>

<span data-ttu-id="6032b-115">Eine Zeichenfolge, die Parameterwerte für den Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="6032b-115">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6032b-116">*vdirectory* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="6032b-116">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6032b-117">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="6032b-117">Type: **Variant**</span></span>

<span data-ttu-id="6032b-118">Der voll qualifizierte Pfad des Verzeichnisses, das die von *sFile* angegebene Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="6032b-118">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="6032b-119">Wenn dieser Parameter nicht angegeben wird, wird das aktuelle Arbeitsverzeichnis verwendet.</span><span class="sxs-lookup"><span data-stu-id="6032b-119">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="6032b-120">*voperation* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="6032b-120">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6032b-121">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="6032b-121">Type: **Variant**</span></span>

<span data-ttu-id="6032b-122">Der Vorgang, der ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6032b-122">The operation to be performed.</span></span> <span data-ttu-id="6032b-123">Dieser Wert wird auf eine der Verb Zeichenfolgen festgelegt, die von der Datei unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6032b-123">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="6032b-124">Eine Erläuterung der Verben finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="6032b-124">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="6032b-125">Wenn dieser Parameter nicht angegeben wird, wird der Standard Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6032b-125">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="6032b-126">*vshow* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="6032b-126">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6032b-127">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="6032b-127">Type: **Variant**</span></span>

<span data-ttu-id="6032b-128">Eine Empfehlung, wie das Anwendungsfenster anfänglich angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6032b-128">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="6032b-129">Diese Empfehlung kann von der Anwendung ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="6032b-129">The application can ignore this recommendation.</span></span> <span data-ttu-id="6032b-130">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="6032b-130">This parameter can be one of the following values.</span></span> <span data-ttu-id="6032b-131">Wenn dieser Parameter nicht angegeben wird, verwendet die Anwendung den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="6032b-131">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="6032b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="6032b-132">Value</span></span>                                                                                                                               | <span data-ttu-id="6032b-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6032b-133">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6032b-134"><dt></dt><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6032b-134"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="6032b-135">Öffnen Sie die Anwendung mit einem ausgeblendeten Fenster.</span><span class="sxs-lookup"><span data-stu-id="6032b-135">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="6032b-136"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6032b-136"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="6032b-137">Öffnen Sie die Anwendung mit einem normalen Fenster.</span><span class="sxs-lookup"><span data-stu-id="6032b-137">Open the application with a normal window.</span></span> <span data-ttu-id="6032b-138">Wenn das Fenster minimiert oder maximiert ist, stellt das System die ursprüngliche Größe und Position wieder her.</span><span class="sxs-lookup"><span data-stu-id="6032b-138">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="6032b-139"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6032b-139"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="6032b-140">Öffnen Sie die Anwendung mit einem minimierten Fenster.</span><span class="sxs-lookup"><span data-stu-id="6032b-140">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="6032b-141"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6032b-141"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="6032b-142">Öffnen Sie die Anwendung mit einem maximierten Fenster.</span><span class="sxs-lookup"><span data-stu-id="6032b-142">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="6032b-143"><dt></dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6032b-143"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="6032b-144">Öffnen Sie die Anwendung mit Ihrem Fenster an der aktuellen Größe und Position.</span><span class="sxs-lookup"><span data-stu-id="6032b-144">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="6032b-145">Das aktive Fenster bleibt aktiv.</span><span class="sxs-lookup"><span data-stu-id="6032b-145">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="6032b-146"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6032b-146"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="6032b-147">Öffnen Sie die Anwendung mit Ihrem Fenster an der aktuellen Größe und Position.</span><span class="sxs-lookup"><span data-stu-id="6032b-147">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="6032b-148"><dt></dt><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="6032b-148"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="6032b-149">Öffnen Sie die Anwendung mit einem minimierten Fenster.</span><span class="sxs-lookup"><span data-stu-id="6032b-149">Open the application with a minimized window.</span></span> <span data-ttu-id="6032b-150">Das aktive Fenster bleibt aktiv.</span><span class="sxs-lookup"><span data-stu-id="6032b-150">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="6032b-151"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="6032b-151"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="6032b-152">Öffnen Sie die Anwendung mit Ihrem Fenster im Standardzustand, der von der Anwendung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6032b-152">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6032b-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6032b-153">Remarks</span></span>

<span data-ttu-id="6032b-154">Diese Methode entspricht dem Starten eines der Befehle, die dem Kontextmenü einer Datei zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6032b-154">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="6032b-155">Jeder Befehl wird durch eine Verb Zeichenfolge dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6032b-155">Each command is represented by a verb string.</span></span> <span data-ttu-id="6032b-156">Der Satz unterstützter Verben variiert von Datei zu Datei.</span><span class="sxs-lookup"><span data-stu-id="6032b-156">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="6032b-157">Das am häufigsten unterstützte Verb ist "Open", das in der Regel auch das Standard Verb ist.</span><span class="sxs-lookup"><span data-stu-id="6032b-157">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="6032b-158">Andere Verben können von nur bestimmten Dateitypen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6032b-158">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="6032b-159">Weitere Informationen zu Shellverben finden Sie unter [Starten von Anwendungen](launch.md) oder Erweitern von Kontext [Menüs](context.md).</span><span class="sxs-lookup"><span data-stu-id="6032b-159">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="6032b-160">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6032b-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="6032b-161">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6032b-161">Examples</span></span>

<span data-ttu-id="6032b-162">In den folgenden Beispielen wird die Verwendung von **ShellExecute** zum Öffnen von Notepad veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6032b-162">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="6032b-163">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6032b-163">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="6032b-164">JScript</span><span class="sxs-lookup"><span data-stu-id="6032b-164">JScript:</span></span>


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

<span data-ttu-id="6032b-165">VBScript</span><span class="sxs-lookup"><span data-stu-id="6032b-165">VBScript:</span></span>

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a><span data-ttu-id="6032b-166">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6032b-166">Requirements</span></span>



| <span data-ttu-id="6032b-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6032b-167">Requirement</span></span> | <span data-ttu-id="6032b-168">Wert</span><span class="sxs-lookup"><span data-stu-id="6032b-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6032b-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6032b-169">Minimum supported client</span></span><br/> | <span data-ttu-id="6032b-170">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6032b-170">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6032b-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6032b-171">Minimum supported server</span></span><br/> | <span data-ttu-id="6032b-172">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6032b-172">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6032b-173">Header</span><span class="sxs-lookup"><span data-stu-id="6032b-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="6032b-174"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6032b-174"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6032b-175">IDL</span><span class="sxs-lookup"><span data-stu-id="6032b-175">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6032b-176"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6032b-176"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6032b-177">DLL</span><span class="sxs-lookup"><span data-stu-id="6032b-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6032b-178"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="6032b-178"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
