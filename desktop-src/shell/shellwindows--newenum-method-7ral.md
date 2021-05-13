---
description: Erstellt ein neues ShellWindows-Objekt, das eine Kopie dieses ShellWindows-Objekts ist, und gibt es zurück.
title: ShellWindows._NewEnum -Methode (Exdisp.h)
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
ms.openlocfilehash: 944da80196db12d0bfa5d64767c5e6c2e8ff733e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841251"
---
# <a name="shellwindows_newenum-method"></a><span data-ttu-id="4e86d-103">ShellWindows. \_ NewEnum-Methode</span><span class="sxs-lookup"><span data-stu-id="4e86d-103">ShellWindows.\_NewEnum method</span></span>

<span data-ttu-id="4e86d-104">Erstellt ein neues [**ShellWindows-Objekt,**](shellwindows.md) das eine Kopie dieses **ShellWindows-Objekts** ist, und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="4e86d-104">Creates and returns a new [**ShellWindows**](shellwindows.md) object that is a copy of this **ShellWindows** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e86d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e86d-105">Syntax</span></span>


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a><span data-ttu-id="4e86d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e86d-106">Parameters</span></span>

<span data-ttu-id="4e86d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4e86d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e86d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e86d-108">Return value</span></span>

<span data-ttu-id="4e86d-109">Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="4e86d-109">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="4e86d-110">Ein Objektverweis auf die [**ShellWindows-Objektkopie.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="4e86d-110">An object reference to the [**ShellWindows**](shellwindows.md) object copy.</span></span>

## <a name="examples"></a><span data-ttu-id="4e86d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e86d-111">Examples</span></span>

<span data-ttu-id="4e86d-112">Im folgenden Beispiel wird **\_ NewEnum** verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e86d-112">The following example shows **\_NewEnum** in use.</span></span> <span data-ttu-id="4e86d-113">Die richtige Verwendung wird für VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4e86d-113">Proper usage is shown for VBScript and Visual Basic.</span></span> <span data-ttu-id="4e86d-114">Diese Methode kann nicht mit JScript verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e86d-114">This method cannot be used with JScript.</span></span>

<span data-ttu-id="4e86d-115">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="4e86d-115">VBScript:</span></span>


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



<span data-ttu-id="4e86d-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4e86d-116">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4e86d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e86d-117">Requirements</span></span>



| <span data-ttu-id="4e86d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e86d-118">Requirement</span></span> | <span data-ttu-id="4e86d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4e86d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e86d-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e86d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e86d-121">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e86d-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4e86d-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e86d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e86d-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e86d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4e86d-124">Header</span><span class="sxs-lookup"><span data-stu-id="4e86d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e86d-125"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="4e86d-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="4e86d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4e86d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e86d-127"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="4e86d-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
