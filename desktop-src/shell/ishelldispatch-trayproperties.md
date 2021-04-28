---
description: 'IShellDispatch.TrayProperties-Methode: Zeigt das Dialogfeld Eigenschaften der Taskleiste und des Startmenüs an. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von Eigenschaften.'
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
title: IShellDispatch.TrayProperties-Methode (Shldisp.h)
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
ms.openlocfilehash: 424d25d7555090e4244d5cd22084171ca2a4fea9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086618"
---
# <a name="ishelldispatchtrayproperties-method"></a><span data-ttu-id="d2c09-104">IShellDispatch.TrayProperties-Methode</span><span class="sxs-lookup"><span data-stu-id="d2c09-104">IShellDispatch.TrayProperties method</span></span>

<span data-ttu-id="d2c09-105">Zeigt das **Dialogfeld Taskleiste und Eigenschaften des Startmenüs** an.</span><span class="sxs-lookup"><span data-stu-id="d2c09-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="d2c09-106">Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von **Eigenschaften.**</span><span class="sxs-lookup"><span data-stu-id="d2c09-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c09-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2c09-107">Syntax</span></span>


```JScript
IShellDispatch.TrayProperties()
```


```VB

IShellDispatch.TrayProperties()
```





## <a name="parameters"></a><span data-ttu-id="d2c09-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2c09-108">Parameters</span></span>

<span data-ttu-id="d2c09-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d2c09-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2c09-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2c09-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d2c09-111">JScript</span><span class="sxs-lookup"><span data-stu-id="d2c09-111">JScript</span></span>

<span data-ttu-id="d2c09-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d2c09-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="d2c09-113">VB</span><span class="sxs-lookup"><span data-stu-id="d2c09-113">VB</span></span>

<span data-ttu-id="d2c09-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d2c09-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2c09-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2c09-115">Remarks</span></span>

<span data-ttu-id="d2c09-116">Diese Methode wird implementiert und über die [**Shell.TrayProperties-Methode aufgerufen.**](shell-trayproperties.md)</span><span class="sxs-lookup"><span data-stu-id="d2c09-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="d2c09-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2c09-117">Examples</span></span>

<span data-ttu-id="d2c09-118">Die folgenden Beispiele zeigen die Verwendung von **TrayProperties** in JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d2c09-118">The following examples show the use of **TrayProperties** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d2c09-119">Jscript:</span><span class="sxs-lookup"><span data-stu-id="d2c09-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>
```



<span data-ttu-id="d2c09-120">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="d2c09-120">VBScript:</span></span>


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



<span data-ttu-id="d2c09-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d2c09-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d2c09-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2c09-122">Requirements</span></span>



| <span data-ttu-id="d2c09-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2c09-123">Requirement</span></span> | <span data-ttu-id="d2c09-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d2c09-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c09-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2c09-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c09-126">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2c09-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d2c09-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2c09-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c09-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2c09-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d2c09-129">Header</span><span class="sxs-lookup"><span data-stu-id="d2c09-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2c09-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="d2c09-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d2c09-131">Idl</span><span class="sxs-lookup"><span data-stu-id="d2c09-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2c09-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2c09-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d2c09-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d2c09-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2c09-134"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="d2c09-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




