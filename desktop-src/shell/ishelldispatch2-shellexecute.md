---
description: 'IShellDispatch2.ShellExecute-Methode: Führt einen angegebenen Vorgang für eine angegebene Datei aus.'
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: IShellDispatch2.ShellExecute-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5c058275948d5d96805ae24a76389321d7c69b8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117018"
---
# <a name="ishelldispatch2shellexecute-method"></a><span data-ttu-id="759c7-103">IShellDispatch2.ShellExecute-Methode</span><span class="sxs-lookup"><span data-stu-id="759c7-103">IShellDispatch2.ShellExecute method</span></span>

<span data-ttu-id="759c7-104">Führt einen angegebenen Vorgang für eine angegebene Datei aus.</span><span class="sxs-lookup"><span data-stu-id="759c7-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="759c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="759c7-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="759c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="759c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="759c7-107">*sFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="759c7-107">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="759c7-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="759c7-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="759c7-109">Eine **Zeichenfolge,** die den Namen der Datei enthält, für die **ShellExecute** die durch vOperation angegebene *Aktion ausführen soll.*</span><span class="sxs-lookup"><span data-stu-id="759c7-109">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="759c7-110">*vArguments* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="759c7-110">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="759c7-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="759c7-111">Type: **Variant**</span></span>

<span data-ttu-id="759c7-112">Eine Zeichenfolge, die Parameterwerte für den Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="759c7-112">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="759c7-113">*vDirectory* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="759c7-113">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="759c7-114">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="759c7-114">Type: **Variant**</span></span>

<span data-ttu-id="759c7-115">Der vollqualifizierte Pfad des Verzeichnisses, das die durch sFile angegebene *Datei enthält.*</span><span class="sxs-lookup"><span data-stu-id="759c7-115">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="759c7-116">Wenn dieser Parameter nicht angegeben wird, wird das aktuelle Arbeitsverzeichnis verwendet.</span><span class="sxs-lookup"><span data-stu-id="759c7-116">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="759c7-117">*vOperation* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="759c7-117">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="759c7-118">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="759c7-118">Type: **Variant**</span></span>

<span data-ttu-id="759c7-119">Der Vorgang, der ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="759c7-119">The operation to be performed.</span></span> <span data-ttu-id="759c7-120">Dieser Wert wird auf eine der Verbzeichenfolgen festgelegt, die von der Datei unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="759c7-120">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="759c7-121">Eine Beschreibung der Verben finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="759c7-121">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="759c7-122">Wenn dieser Parameter nicht angegeben wird, wird der Standardvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="759c7-122">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="759c7-123">*vShow* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="759c7-123">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="759c7-124">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="759c7-124">Type: **Variant**</span></span>

<span data-ttu-id="759c7-125">Eine Empfehlung, wie das Anwendungsfenster anfänglich angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="759c7-125">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="759c7-126">Die Anwendung kann diese Empfehlung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="759c7-126">The application can ignore this recommendation.</span></span> <span data-ttu-id="759c7-127">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="759c7-127">This parameter can be one of the following values.</span></span> <span data-ttu-id="759c7-128">Wenn dieser Parameter nicht angegeben ist, verwendet die Anwendung ihren Standardwert.</span><span class="sxs-lookup"><span data-stu-id="759c7-128">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="759c7-129">Wert</span><span class="sxs-lookup"><span data-stu-id="759c7-129">Value</span></span>                                                                                                                               | <span data-ttu-id="759c7-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="759c7-130">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="759c7-131"><dt></dt><dt>0 (0)</dt></span><span class="sxs-lookup"><span data-stu-id="759c7-131"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="759c7-132">Öffnen Sie die Anwendung mit einem ausgeblendeten Fenster.</span><span class="sxs-lookup"><span data-stu-id="759c7-132">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="759c7-133"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="759c7-133"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="759c7-134">Öffnen Sie die Anwendung in einem normalen Fenster.</span><span class="sxs-lookup"><span data-stu-id="759c7-134">Open the application with a normal window.</span></span> <span data-ttu-id="759c7-135">Wenn das Fenster minimiert oder maximiert ist, stellt das System es auf seine ursprüngliche Größe und Position wieder her.</span><span class="sxs-lookup"><span data-stu-id="759c7-135">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="759c7-136"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="759c7-136"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="759c7-137">Öffnen Sie die Anwendung mit einem minimierten Fenster.</span><span class="sxs-lookup"><span data-stu-id="759c7-137">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="759c7-138"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="759c7-138"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="759c7-139">Öffnen Sie die Anwendung mit einem maximierten Fenster.</span><span class="sxs-lookup"><span data-stu-id="759c7-139">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="759c7-140"><dt></dt><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="759c7-140"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="759c7-141">Öffnen Sie die Anwendung mit ihrem Fenster mit der neuesten Größe und Position.</span><span class="sxs-lookup"><span data-stu-id="759c7-141">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="759c7-142">Das aktive Fenster bleibt aktiv.</span><span class="sxs-lookup"><span data-stu-id="759c7-142">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="759c7-143"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="759c7-143"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="759c7-144">Öffnen Sie die Anwendung mit ihrem Fenster in ihrer aktuellen Größe und Position.</span><span class="sxs-lookup"><span data-stu-id="759c7-144">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="759c7-145"><dt></dt><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="759c7-145"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="759c7-146">Öffnen Sie die Anwendung mit einem minimierten Fenster.</span><span class="sxs-lookup"><span data-stu-id="759c7-146">Open the application with a minimized window.</span></span> <span data-ttu-id="759c7-147">Das aktive Fenster bleibt aktiv.</span><span class="sxs-lookup"><span data-stu-id="759c7-147">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="759c7-148"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="759c7-148"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="759c7-149">Öffnen Sie die Anwendung mit ihrem Fenster in dem von der Anwendung angegebenen Standardzustand.</span><span class="sxs-lookup"><span data-stu-id="759c7-149">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="759c7-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="759c7-150">Remarks</span></span>

<span data-ttu-id="759c7-151">Diese Methode wird implementiert und über die [**Shell.ShellExecute-Methode**](./shell-shellexecute.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="759c7-151">This method is implemented and accessed through the [**Shell.ShellExecute**](./shell-shellexecute.md) method.</span></span>

<span data-ttu-id="759c7-152">Diese Methode entspricht dem Starten eines der Befehle, die dem Kontextmenü einer Datei zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="759c7-152">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="759c7-153">Jeder Befehl wird durch eine Verbzeichenfolge dargestellt.</span><span class="sxs-lookup"><span data-stu-id="759c7-153">Each command is represented by a verb string.</span></span> <span data-ttu-id="759c7-154">Die Gruppe der unterstützten Verben variiert von Datei zu Datei.</span><span class="sxs-lookup"><span data-stu-id="759c7-154">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="759c7-155">Das am häufigsten unterstützte Verb ist "open", was in der Regel auch das Standardverb ist.</span><span class="sxs-lookup"><span data-stu-id="759c7-155">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="759c7-156">Andere Verben werden möglicherweise nur von bestimmten Dateitypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="759c7-156">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="759c7-157">Weitere Informationen zu Shellverben finden Sie unter [Starten von Anwendungen](launch.md) oder Erweitern von [Kontextmenüs.](context.md)</span><span class="sxs-lookup"><span data-stu-id="759c7-157">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="759c7-158">Diese Methode ist derzeit in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="759c7-158">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="759c7-159">Beispiele</span><span class="sxs-lookup"><span data-stu-id="759c7-159">Examples</span></span>

<span data-ttu-id="759c7-160">In den folgenden Beispielen wird die Verwendung von **ShellExecute zum** Öffnen des Editors gezeigt.</span><span class="sxs-lookup"><span data-stu-id="759c7-160">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="759c7-161">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="759c7-161">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="759c7-162">Jscript:</span><span class="sxs-lookup"><span data-stu-id="759c7-162">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



<span data-ttu-id="759c7-163">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="759c7-163">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="759c7-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="759c7-164">Requirements</span></span>



| <span data-ttu-id="759c7-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="759c7-165">Requirement</span></span> | <span data-ttu-id="759c7-166">Wert</span><span class="sxs-lookup"><span data-stu-id="759c7-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="759c7-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="759c7-167">Minimum supported client</span></span><br/> | <span data-ttu-id="759c7-168">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="759c7-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="759c7-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="759c7-169">Minimum supported server</span></span><br/> | <span data-ttu-id="759c7-170">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="759c7-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="759c7-171">Header</span><span class="sxs-lookup"><span data-stu-id="759c7-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="759c7-172"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="759c7-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="759c7-173">Idl</span><span class="sxs-lookup"><span data-stu-id="759c7-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="759c7-174"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="759c7-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="759c7-175">DLL</span><span class="sxs-lookup"><span data-stu-id="759c7-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="759c7-176"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="759c7-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
