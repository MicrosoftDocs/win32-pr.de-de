---
description: 'Shell.WindowsSecurity-Methode: Zeigt das Dialogfeld Windows-Sicherheit an.'
title: Shell.WindowsSecurity-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 94916E29-5960-4010-B2C6-0FAA1E4BF72D
ms.openlocfilehash: 7e04cc6d3a1a25f459da9f533fc562b1fc9d0b06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083598"
---
# <a name="shellwindowssecurity-method"></a><span data-ttu-id="b0d6c-103">Shell.WindowsSecurity-Methode</span><span class="sxs-lookup"><span data-stu-id="b0d6c-103">Shell.WindowsSecurity method</span></span>

<span data-ttu-id="b0d6c-104">Zeigt das Dialogfeld **Windows-Sicherheit** an.</span><span class="sxs-lookup"><span data-stu-id="b0d6c-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d6c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0d6c-105">Syntax</span></span>


```JScript
Shell.WindowsSecurity()
```


```VB

Shell.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="b0d6c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0d6c-106">Parameters</span></span>

<span data-ttu-id="b0d6c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b0d6c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0d6c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0d6c-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b0d6c-109">JScript</span><span class="sxs-lookup"><span data-stu-id="b0d6c-109">JScript</span></span>

<span data-ttu-id="b0d6c-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b0d6c-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b0d6c-111">VB</span><span class="sxs-lookup"><span data-stu-id="b0d6c-111">VB</span></span>

<span data-ttu-id="b0d6c-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b0d6c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0d6c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0d6c-113">Remarks</span></span>

<span data-ttu-id="b0d6c-114">Diese Methode zeigt das Dialogfeld an, das angezeigt wird, nachdem Sie STRG+ALT+DELETE gedrückt oder die Sicherheitsoption im **Startmenü** verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="b0d6c-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="b0d6c-115">Diese Methode kann nur verwendet werden, wenn sie von einer Terminalsitzung mit Microsoft Terminal Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b0d6c-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b0d6c-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0d6c-116">Examples</span></span>

<span data-ttu-id="b0d6c-117">Die folgenden Beispiele zeigen die Verwendung von **WindowsSecurity** für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b0d6c-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b0d6c-118">Jscript:</span><span class="sxs-lookup"><span data-stu-id="b0d6c-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="b0d6c-119">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="b0d6c-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b0d6c-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b0d6c-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objShell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b0d6c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0d6c-121">Requirements</span></span>



| <span data-ttu-id="b0d6c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0d6c-122">Requirement</span></span> | <span data-ttu-id="b0d6c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b0d6c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d6c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0d6c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b0d6c-125">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0d6c-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="b0d6c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0d6c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b0d6c-127">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0d6c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b0d6c-128">Header</span><span class="sxs-lookup"><span data-stu-id="b0d6c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0d6c-129"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b0d6c-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b0d6c-130">Idl</span><span class="sxs-lookup"><span data-stu-id="b0d6c-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0d6c-131"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0d6c-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b0d6c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b0d6c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0d6c-133"><dt>Shell32.dll (Version 6.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b0d6c-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




