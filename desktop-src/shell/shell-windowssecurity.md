---
description: Zeigt das Dialogfeld Windows-Sicherheit an.
title: Shell. WindowsSecurity-Methode (Shldisp. h)
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
ms.openlocfilehash: bbefa4c772adde64b8142b7e3563315fe4833b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529411"
---
# <a name="shellwindowssecurity-method"></a><span data-ttu-id="79b9f-103">Shell. WindowsSecurity-Methode</span><span class="sxs-lookup"><span data-stu-id="79b9f-103">Shell.WindowsSecurity method</span></span>

<span data-ttu-id="79b9f-104">Zeigt das Dialogfeld **Windows-Sicherheit** an.</span><span class="sxs-lookup"><span data-stu-id="79b9f-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="79b9f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79b9f-105">Syntax</span></span>


```JScript
Shell.WindowsSecurity()
```


```VB

Shell.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="79b9f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79b9f-106">Parameters</span></span>

<span data-ttu-id="79b9f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="79b9f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79b9f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79b9f-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="79b9f-109">JScript</span><span class="sxs-lookup"><span data-stu-id="79b9f-109">JScript</span></span>

<span data-ttu-id="79b9f-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="79b9f-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="79b9f-111">VB</span><span class="sxs-lookup"><span data-stu-id="79b9f-111">VB</span></span>

<span data-ttu-id="79b9f-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="79b9f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79b9f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79b9f-113">Remarks</span></span>

<span data-ttu-id="79b9f-114">Diese Methode zeigt das Dialogfeld an, das nach dem Drücken von STRG + ALT + ENTF oder mithilfe der Option Sicherheit im **Startmenü** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="79b9f-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="79b9f-115">Diese Methode kann nur verwendet werden, wenn eine Verbindung über eine Terminalsitzung mit dem Microsoft-Terminal Server hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="79b9f-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="79b9f-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79b9f-116">Examples</span></span>

<span data-ttu-id="79b9f-117">In den folgenden Beispielen wird die Verwendung von **WindowsSecurity** für JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="79b9f-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="79b9f-118">JScript</span><span class="sxs-lookup"><span data-stu-id="79b9f-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="79b9f-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="79b9f-119">VBScript:</span></span>


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



<span data-ttu-id="79b9f-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="79b9f-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objShell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="79b9f-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="79b9f-121">Requirements</span></span>



| <span data-ttu-id="79b9f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79b9f-122">Requirement</span></span> | <span data-ttu-id="79b9f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="79b9f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79b9f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79b9f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="79b9f-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79b9f-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="79b9f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79b9f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="79b9f-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79b9f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="79b9f-128">Header</span><span class="sxs-lookup"><span data-stu-id="79b9f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="79b9f-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="79b9f-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="79b9f-130">IDL</span><span class="sxs-lookup"><span data-stu-id="79b9f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79b9f-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79b9f-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="79b9f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="79b9f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79b9f-133"><dt>Shell32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="79b9f-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




