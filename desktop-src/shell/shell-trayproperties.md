---
description: Zeigt das Dialogfeld Eigenschaften von Taskleiste und Startmenü an. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und Eigenschaften auswählen.
ms.assetid: 0d82d847-9e6f-461e-b938-fe8fd49a636f
title: Shell. trayproperties-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da3fbfdb2b6aa2517b275041856920c6b2cd1bb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980601"
---
# <a name="shelltrayproperties-method"></a><span data-ttu-id="a4d7f-104">Shell. trayproperties-Methode</span><span class="sxs-lookup"><span data-stu-id="a4d7f-104">Shell.TrayProperties method</span></span>

<span data-ttu-id="a4d7f-105">Zeigt das Dialogfeld **Eigenschaften von Taskleiste und Startmenü** an.</span><span class="sxs-lookup"><span data-stu-id="a4d7f-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="a4d7f-106">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und **Eigenschaften** auswählen.</span><span class="sxs-lookup"><span data-stu-id="a4d7f-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d7f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4d7f-107">Syntax</span></span>


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a><span data-ttu-id="a4d7f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4d7f-108">Parameters</span></span>

<span data-ttu-id="a4d7f-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a4d7f-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="a4d7f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4d7f-110">Examples</span></span>

<span data-ttu-id="a4d7f-111">Das folgende Beispiel zeigt die Verwendung von **trayproperties** .</span><span class="sxs-lookup"><span data-stu-id="a4d7f-111">The following example shows **TrayProperties** in use.</span></span> <span data-ttu-id="a4d7f-112">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a4d7f-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a4d7f-113">JScript</span><span class="sxs-lookup"><span data-stu-id="a4d7f-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



<span data-ttu-id="a4d7f-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="a4d7f-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a4d7f-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a4d7f-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a4d7f-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a4d7f-116">Requirements</span></span>



| <span data-ttu-id="a4d7f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4d7f-117">Requirement</span></span> | <span data-ttu-id="a4d7f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a4d7f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d7f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4d7f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a4d7f-120">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4d7f-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a4d7f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4d7f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a4d7f-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4d7f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a4d7f-123">Header</span><span class="sxs-lookup"><span data-stu-id="a4d7f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4d7f-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4d7f-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a4d7f-125">IDL</span><span class="sxs-lookup"><span data-stu-id="a4d7f-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a4d7f-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a4d7f-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a4d7f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a4d7f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4d7f-128"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a4d7f-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




