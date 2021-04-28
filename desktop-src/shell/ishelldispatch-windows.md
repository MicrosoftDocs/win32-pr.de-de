---
description: 'IShellDispatch.Windows-Methode: Erstellt ein ShellWindows-Objekt und gibt es zurück. Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.'
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: IShellDispatch.Windows-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 16991d6a251909e8f3b277894a96e6ad08a7f9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117168"
---
# <a name="ishelldispatchwindows-method"></a><span data-ttu-id="53720-104">IShellDispatch.Windows-Methode</span><span class="sxs-lookup"><span data-stu-id="53720-104">IShellDispatch.Windows method</span></span>

<span data-ttu-id="53720-105">Erstellt ein [**ShellWindows-Objekt**](shellwindows.md) und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="53720-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="53720-106">Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.</span><span class="sxs-lookup"><span data-stu-id="53720-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="53720-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53720-107">Syntax</span></span>


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="53720-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="53720-108">Parameters</span></span>

<span data-ttu-id="53720-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="53720-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53720-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53720-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="53720-111">JScript</span><span class="sxs-lookup"><span data-stu-id="53720-111">JScript</span></span>

<span data-ttu-id="53720-112">Typ: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="53720-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="53720-113">Ein Objektverweis auf das [**ShellWindows-Objekt.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="53720-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="53720-114">VB</span><span class="sxs-lookup"><span data-stu-id="53720-114">VB</span></span>

<span data-ttu-id="53720-115">Typ: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="53720-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="53720-116">Ein Objektverweis auf das [**ShellWindows-Objekt.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="53720-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="53720-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53720-117">Remarks</span></span>

<span data-ttu-id="53720-118">Diese Methode wird implementiert und über die [**Shell.Windows-Methode**](shell-windows.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="53720-118">This method is implemented and accessed through the [**Shell.Windows**](shell-windows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="53720-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53720-119">Examples</span></span>

<span data-ttu-id="53720-120">In den folgenden Beispielen wird **Windows** verwendet, um das [**ShellWindows-Objekt**](shellwindows.md) abzurufen und die Anzahl der darin enthaltenen Elemente anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="53720-120">The following examples use **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="53720-121">Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="53720-121">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="53720-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="53720-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();

        if (objShellWindows != null)
        {
            alert(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="53720-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="53720-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows

        if (not objShellWindows is nothing) then
            alert(objShellWindows.Count)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="53720-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="53720-124">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="53720-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53720-125">Requirements</span></span>



| <span data-ttu-id="53720-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53720-126">Requirement</span></span> | <span data-ttu-id="53720-127">Wert</span><span class="sxs-lookup"><span data-stu-id="53720-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53720-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53720-128">Minimum supported client</span></span><br/> | <span data-ttu-id="53720-129">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53720-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="53720-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53720-130">Minimum supported server</span></span><br/> | <span data-ttu-id="53720-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53720-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53720-132">Header</span><span class="sxs-lookup"><span data-stu-id="53720-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="53720-133"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="53720-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="53720-134">Idl</span><span class="sxs-lookup"><span data-stu-id="53720-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="53720-135"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="53720-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="53720-136">DLL</span><span class="sxs-lookup"><span data-stu-id="53720-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53720-137"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="53720-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
