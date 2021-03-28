---
description: Erstellt ein neues shellwindows-Objekt, das eine Kopie dieses shellwindows-Objekts ist, und gibt es zurück.
title: ShellWindows._NewEnum-Methode (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows._NewEnum
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 85e84c13-62aa-4502-b642-ca55273a800d
ms.openlocfilehash: ded5ae2c337e80359c012fb63a37aa13cc43b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218058"
---
# <a name="shellwindows_newenum-method"></a><span data-ttu-id="f37ef-103">Shellwindows. \_ Methode ' netwenum '</span><span class="sxs-lookup"><span data-stu-id="f37ef-103">ShellWindows.\_NewEnum method</span></span>

<span data-ttu-id="f37ef-104">Erstellt ein neues [**shellwindows**](shellwindows.md) -Objekt, das eine Kopie dieses **shellwindows** -Objekts ist, und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="f37ef-104">Creates and returns a new [**ShellWindows**](shellwindows.md) object that is a copy of this **ShellWindows** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f37ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f37ef-105">Syntax</span></span>


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a><span data-ttu-id="f37ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f37ef-106">Parameters</span></span>

<span data-ttu-id="f37ef-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f37ef-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f37ef-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f37ef-108">Return value</span></span>

<span data-ttu-id="f37ef-109">Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="f37ef-109">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="f37ef-110">Ein Objekt Verweis auf die [**shellwindows**](shellwindows.md) -Objekt Kopie.</span><span class="sxs-lookup"><span data-stu-id="f37ef-110">An object reference to the [**ShellWindows**](shellwindows.md) object copy.</span></span>

## <a name="examples"></a><span data-ttu-id="f37ef-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f37ef-111">Examples</span></span>

<span data-ttu-id="f37ef-112">Im folgenden Beispiel wird gezeigt, wie " **\_ netwenum** " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f37ef-112">The following example shows **\_NewEnum** in use.</span></span> <span data-ttu-id="f37ef-113">Die richtige Verwendung wird für VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f37ef-113">Proper usage is shown for VBScript and Visual Basic.</span></span> <span data-ttu-id="f37ef-114">Diese Methode kann nicht mit JScript verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f37ef-114">This method cannot be used with JScript.</span></span>

<span data-ttu-id="f37ef-115">VBScript</span><span class="sxs-lookup"><span data-stu-id="f37ef-115">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsNewEnumVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim objEnumItems
            
            for each objEnumItems in objShellWindows
                alert(objEnumItems.Type)
            next
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f37ef-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f37ef-116">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsNewEnumVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Dim vEnumItem As Variant
        
        For Each vEnumItem In objShellWindows
            Debug.Print vEnumItem.Type
        Next vEnumItem
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f37ef-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f37ef-117">Requirements</span></span>



| <span data-ttu-id="f37ef-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f37ef-118">Requirement</span></span> | <span data-ttu-id="f37ef-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f37ef-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f37ef-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f37ef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f37ef-121">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f37ef-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f37ef-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f37ef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f37ef-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f37ef-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f37ef-124">Header</span><span class="sxs-lookup"><span data-stu-id="f37ef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f37ef-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f37ef-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="f37ef-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f37ef-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f37ef-127"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="f37ef-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
