---
description: 'Shell.Windows-Methode: Erstellt ein ShellWindows-Objekt und gibt es zurück. Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.'
title: Shell.Windows-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ffa6311c-8bbe-45c4-9b06-069779d2306d
ms.openlocfilehash: d46e27781dc569b473615926509f51ed9d089af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104068"
---
# <a name="shellwindows-method"></a><span data-ttu-id="de941-104">Shell.Windows-Methode</span><span class="sxs-lookup"><span data-stu-id="de941-104">Shell.Windows method</span></span>

<span data-ttu-id="de941-105">Erstellt ein [**ShellWindows-Objekt**](shellwindows.md) und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="de941-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="de941-106">Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.</span><span class="sxs-lookup"><span data-stu-id="de941-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="de941-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="de941-107">Syntax</span></span>


```JScript
retVal = Shell.Windows()
```


```VB

Shell.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="de941-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de941-108">Parameters</span></span>

<span data-ttu-id="de941-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="de941-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de941-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de941-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="de941-111">JScript</span><span class="sxs-lookup"><span data-stu-id="de941-111">JScript</span></span>

<span data-ttu-id="de941-112">Typ: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="de941-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="de941-113">Ein Objektverweis auf das [**ShellWindows-Objekt.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="de941-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="de941-114">VB</span><span class="sxs-lookup"><span data-stu-id="de941-114">VB</span></span>

<span data-ttu-id="de941-115">Typ: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="de941-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="de941-116">Ein Objektverweis auf das [**ShellWindows-Objekt.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="de941-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="de941-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de941-117">Examples</span></span>

<span data-ttu-id="de941-118">Im folgenden Beispiel wird **Windows** verwendet, um das [**ShellWindows-Objekt**](shellwindows.md) abzurufen und die Anzahl der darin enthaltenen Elemente anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="de941-118">The following example uses **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="de941-119">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="de941-119">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="de941-120">Jscript:</span><span class="sxs-lookup"><span data-stu-id="de941-120">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objShell.Windows();

        if (objShellWindows != null)
        {
            var Shell = new ActiveXObject("WScript.Shell");
            Shell.Popup(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="de941-121">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="de941-121">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVBS()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objShell.Windows

        if (not objShellWindows is nothing) then
            WScript.Echo objShellWindows.Count
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="de941-122">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="de941-122">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objShell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="de941-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de941-123">Requirements</span></span>



| <span data-ttu-id="de941-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de941-124">Requirement</span></span> | <span data-ttu-id="de941-125">Wert</span><span class="sxs-lookup"><span data-stu-id="de941-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de941-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de941-126">Minimum supported client</span></span><br/> | <span data-ttu-id="de941-127">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de941-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="de941-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de941-128">Minimum supported server</span></span><br/> | <span data-ttu-id="de941-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de941-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="de941-130">Header</span><span class="sxs-lookup"><span data-stu-id="de941-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="de941-131"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="de941-131"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="de941-132">Idl</span><span class="sxs-lookup"><span data-stu-id="de941-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="de941-133"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="de941-133"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="de941-134">DLL</span><span class="sxs-lookup"><span data-stu-id="de941-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de941-135"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="de941-135"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
