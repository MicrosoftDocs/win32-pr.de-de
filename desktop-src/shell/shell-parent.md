---
description: Ruft ein-Objekt ab, das das übergeordnete Element des aktuellen-Objekts darstellt.
ms.assetid: 76c2f72c-5ef6-4f2c-bdfc-62ced6dbc504
title: Shell. Parent-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a121e4f87be1163429156f22dfe7bd55f1345f43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979769"
---
# <a name="shellparent-property"></a><span data-ttu-id="64485-103">Shell. Parent-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="64485-103">Shell.Parent property</span></span>

<span data-ttu-id="64485-104">Ruft ein-Objekt ab, das das übergeordnete Element des aktuellen-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="64485-104">Gets an object that represents the parent of the current object.</span></span>

<span data-ttu-id="64485-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="64485-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="64485-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="64485-106">Syntax</span></span>


```JScript
objParent = Shell.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="64485-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="64485-107">Property value</span></span>

<span data-ttu-id="64485-108">Eine Variable vom Typ [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die das übergeordnete Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="64485-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="examples"></a><span data-ttu-id="64485-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64485-109">Examples</span></span>

<span data-ttu-id="64485-110">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung des über **geordneten** Elements für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="64485-110">The following example shows the proper use of **Parent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="64485-111">JScript</span><span class="sxs-lookup"><span data-stu-id="64485-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objShell.Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="64485-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="64485-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objShell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="64485-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="64485-113">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objShell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="64485-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="64485-114">Requirements</span></span>



| <span data-ttu-id="64485-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64485-115">Requirement</span></span> | <span data-ttu-id="64485-116">Wert</span><span class="sxs-lookup"><span data-stu-id="64485-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64485-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64485-117">Minimum supported client</span></span><br/> | <span data-ttu-id="64485-118">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64485-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="64485-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64485-119">Minimum supported server</span></span><br/> | <span data-ttu-id="64485-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64485-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="64485-121">Header</span><span class="sxs-lookup"><span data-stu-id="64485-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="64485-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="64485-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="64485-123">IDL</span><span class="sxs-lookup"><span data-stu-id="64485-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64485-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="64485-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="64485-125">DLL</span><span class="sxs-lookup"><span data-stu-id="64485-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64485-126"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="64485-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
