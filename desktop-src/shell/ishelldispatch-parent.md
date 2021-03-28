---
description: Ruft ein-Objekt ab, das das übergeordnete Element des aktuellen-Objekts darstellt.
ms.assetid: 2FDEF8D3-3F5B-43ae-9812-83B4249D9CBB
title: Ishelldispatch. Parent-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 051e6f323b9663b692410d81d85e55a404e99d56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130093"
---
# <a name="ishelldispatchparent-property"></a><span data-ttu-id="5ae7f-103">Ishelldispatch. Parent-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5ae7f-103">IShellDispatch.Parent property</span></span>

<span data-ttu-id="5ae7f-104">Ruft ein-Objekt ab, das das übergeordnete Element des aktuellen-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="5ae7f-104">Retrieves an object that represents the parent of the current object.</span></span>

<span data-ttu-id="5ae7f-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5ae7f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae7f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ae7f-106">Syntax</span></span>


```JScript
objParent = IShellDispatch.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="5ae7f-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5ae7f-107">Property value</span></span>

<span data-ttu-id="5ae7f-108">Eine Variable vom Typ [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die das übergeordnete Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="5ae7f-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ae7f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ae7f-109">Remarks</span></span>

<span data-ttu-id="5ae7f-110">Diese Eigenschaft wird implementiert, und der Zugriff erfolgt über die [**Shell. Parent**](shell-parent.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5ae7f-110">This property is implemented and accessed through the [**Shell.Parent**](shell-parent.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="5ae7f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ae7f-111">Examples</span></span>

<span data-ttu-id="5ae7f-112">In den folgenden Beispielen wird die Verwendung von **Parent** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5ae7f-112">The following examples show the use of **Parent** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5ae7f-113">JScript</span><span class="sxs-lookup"><span data-stu-id="5ae7f-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objshell.Shell_Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="5ae7f-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="5ae7f-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objshell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="5ae7f-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5ae7f-115">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objshell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5ae7f-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5ae7f-116">Requirements</span></span>



| <span data-ttu-id="5ae7f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ae7f-117">Requirement</span></span> | <span data-ttu-id="5ae7f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5ae7f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae7f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ae7f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5ae7f-120">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ae7f-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5ae7f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ae7f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5ae7f-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ae7f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ae7f-123">Header</span><span class="sxs-lookup"><span data-stu-id="5ae7f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ae7f-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ae7f-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5ae7f-125">IDL</span><span class="sxs-lookup"><span data-stu-id="5ae7f-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ae7f-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ae7f-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5ae7f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5ae7f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ae7f-128"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="5ae7f-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
