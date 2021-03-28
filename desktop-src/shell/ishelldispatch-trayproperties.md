---
description: Zeigt das Dialogfeld Eigenschaften von Taskleiste und Startmenü an. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und Eigenschaften auswählen.
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
title: Ishelldispatch. trayproperties-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f5e22dd48b77035aab3754a4c8e3d2c414ec606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959128"
---
# <a name="ishelldispatchtrayproperties-method"></a><span data-ttu-id="3959d-104">Ishelldispatch. trayproperties-Methode</span><span class="sxs-lookup"><span data-stu-id="3959d-104">IShellDispatch.TrayProperties method</span></span>

<span data-ttu-id="3959d-105">Zeigt das Dialogfeld **Eigenschaften von Taskleiste und Startmenü** an.</span><span class="sxs-lookup"><span data-stu-id="3959d-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="3959d-106">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und **Eigenschaften** auswählen.</span><span class="sxs-lookup"><span data-stu-id="3959d-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3959d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3959d-107">Syntax</span></span>


```JScript
IShellDispatch.TrayProperties()
```


```VB

IShellDispatch.TrayProperties()
```





## <a name="parameters"></a><span data-ttu-id="3959d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3959d-108">Parameters</span></span>

<span data-ttu-id="3959d-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3959d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3959d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3959d-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="3959d-111">JScript</span><span class="sxs-lookup"><span data-stu-id="3959d-111">JScript</span></span>

<span data-ttu-id="3959d-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3959d-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="3959d-113">VB</span><span class="sxs-lookup"><span data-stu-id="3959d-113">VB</span></span>

<span data-ttu-id="3959d-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3959d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3959d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3959d-115">Remarks</span></span>

<span data-ttu-id="3959d-116">Diese Methode ist implementiert, und der Zugriff erfolgt über die [**Shell. trayproperties**](shell-trayproperties.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3959d-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="3959d-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3959d-117">Examples</span></span>

<span data-ttu-id="3959d-118">In den folgenden Beispielen wird die Verwendung von **trayproperties** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3959d-118">The following examples show the use of **TrayProperties** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3959d-119">JScript</span><span class="sxs-lookup"><span data-stu-id="3959d-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>
```



<span data-ttu-id="3959d-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="3959d-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="3959d-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3959d-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3959d-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3959d-122">Requirements</span></span>



| <span data-ttu-id="3959d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3959d-123">Requirement</span></span> | <span data-ttu-id="3959d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3959d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3959d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3959d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3959d-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3959d-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3959d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3959d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3959d-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3959d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3959d-129">Header</span><span class="sxs-lookup"><span data-stu-id="3959d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3959d-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3959d-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3959d-131">IDL</span><span class="sxs-lookup"><span data-stu-id="3959d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3959d-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3959d-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3959d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3959d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3959d-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="3959d-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




