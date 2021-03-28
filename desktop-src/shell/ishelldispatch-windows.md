---
description: Erstellt ein shellwindows-Objekt und gibt es zurück. Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: Ishelldispatch. Windows-Methode (Shldisp. h)
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
ms.openlocfilehash: cb5f84caebf38deb27c7fb60565167793fead561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753080"
---
# <a name="ishelldispatchwindows-method"></a><span data-ttu-id="728dd-104">Ishelldispatch. Windows-Methode</span><span class="sxs-lookup"><span data-stu-id="728dd-104">IShellDispatch.Windows method</span></span>

<span data-ttu-id="728dd-105">Erstellt ein [**shellwindows**](shellwindows.md) -Objekt und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="728dd-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="728dd-106">Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.</span><span class="sxs-lookup"><span data-stu-id="728dd-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="728dd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="728dd-107">Syntax</span></span>


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="728dd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="728dd-108">Parameters</span></span>

<span data-ttu-id="728dd-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="728dd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="728dd-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="728dd-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="728dd-111">JScript</span><span class="sxs-lookup"><span data-stu-id="728dd-111">JScript</span></span>

<span data-ttu-id="728dd-112">Typ: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="728dd-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="728dd-113">Ein Objekt Verweis auf das [**shellwindows**](shellwindows.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="728dd-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="728dd-114">VB</span><span class="sxs-lookup"><span data-stu-id="728dd-114">VB</span></span>

<span data-ttu-id="728dd-115">Typ: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="728dd-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="728dd-116">Ein Objekt Verweis auf das [**shellwindows**](shellwindows.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="728dd-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="728dd-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="728dd-117">Remarks</span></span>

<span data-ttu-id="728dd-118">Diese Methode wird implementiert und über die [**Shell. Windows**](shell-windows.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="728dd-118">This method is implemented and accessed through the [**Shell.Windows**](shell-windows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="728dd-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="728dd-119">Examples</span></span>

<span data-ttu-id="728dd-120">In den folgenden Beispielen wird **Windows** verwendet, um das [**shellwindows**](shellwindows.md) -Objekt abzurufen und die Anzahl der darin enthaltenen Elemente anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="728dd-120">The following examples use **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="728dd-121">Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="728dd-121">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="728dd-122">JScript</span><span class="sxs-lookup"><span data-stu-id="728dd-122">JScript:</span></span>


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



<span data-ttu-id="728dd-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="728dd-123">VBScript:</span></span>


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



<span data-ttu-id="728dd-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="728dd-124">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="728dd-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="728dd-125">Requirements</span></span>



| <span data-ttu-id="728dd-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="728dd-126">Requirement</span></span> | <span data-ttu-id="728dd-127">Wert</span><span class="sxs-lookup"><span data-stu-id="728dd-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="728dd-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="728dd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="728dd-129">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="728dd-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="728dd-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="728dd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="728dd-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="728dd-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="728dd-132">Header</span><span class="sxs-lookup"><span data-stu-id="728dd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="728dd-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="728dd-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="728dd-134">IDL</span><span class="sxs-lookup"><span data-stu-id="728dd-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="728dd-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="728dd-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="728dd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="728dd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="728dd-137"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="728dd-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
