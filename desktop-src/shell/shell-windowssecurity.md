---
description: 'Shell.WindowsSecurity-Methode: Zeigt das dialogfeld Windows-Sicherheit an.'
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
ms.openlocfilehash: 2c6e18ba2388909390b856deb03b65b078f810d9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840861"
---
# <a name="shellwindowssecurity-method"></a><span data-ttu-id="caa58-103">Shell.WindowsSecurity-Methode</span><span class="sxs-lookup"><span data-stu-id="caa58-103">Shell.WindowsSecurity method</span></span>

<span data-ttu-id="caa58-104">Zeigt das **Windows-Sicherheit** An.</span><span class="sxs-lookup"><span data-stu-id="caa58-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="caa58-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="caa58-105">Syntax</span></span>


```JScript
Shell.WindowsSecurity()
```


```VB

Shell.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="caa58-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="caa58-106">Parameters</span></span>

<span data-ttu-id="caa58-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="caa58-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="caa58-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="caa58-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="caa58-109">JScript</span><span class="sxs-lookup"><span data-stu-id="caa58-109">JScript</span></span>

<span data-ttu-id="caa58-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="caa58-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="caa58-111">VB</span><span class="sxs-lookup"><span data-stu-id="caa58-111">VB</span></span>

<span data-ttu-id="caa58-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="caa58-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="caa58-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="caa58-113">Remarks</span></span>

<span data-ttu-id="caa58-114">Diese Methode zeigt das Dialogfeld an, das nach dem Drücken von STRG+ALT+DELETE oder mithilfe der Sicherheitsoption im **Startmenü angezeigt** wird.</span><span class="sxs-lookup"><span data-stu-id="caa58-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="caa58-115">Diese Methode kann nur verwendet werden, wenn eine Verbindung zwischen einer Terminalsitzung und Microsoft Terminal Server besteht.</span><span class="sxs-lookup"><span data-stu-id="caa58-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="caa58-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="caa58-116">Examples</span></span>

<span data-ttu-id="caa58-117">Die folgenden Beispiele zeigen die Verwendung von **WindowsSecurity** für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="caa58-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="caa58-118">Jscript:</span><span class="sxs-lookup"><span data-stu-id="caa58-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="caa58-119">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="caa58-119">VBScript:</span></span>


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



<span data-ttu-id="caa58-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="caa58-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objShell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="caa58-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="caa58-121">Requirements</span></span>



| <span data-ttu-id="caa58-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="caa58-122">Requirement</span></span> | <span data-ttu-id="caa58-123">Wert</span><span class="sxs-lookup"><span data-stu-id="caa58-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caa58-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="caa58-124">Minimum supported client</span></span><br/> | <span data-ttu-id="caa58-125">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="caa58-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="caa58-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="caa58-126">Minimum supported server</span></span><br/> | <span data-ttu-id="caa58-127">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="caa58-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="caa58-128">Header</span><span class="sxs-lookup"><span data-stu-id="caa58-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="caa58-129"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="caa58-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="caa58-130">Idl</span><span class="sxs-lookup"><span data-stu-id="caa58-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="caa58-131"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="caa58-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="caa58-132">DLL</span><span class="sxs-lookup"><span data-stu-id="caa58-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caa58-133"><dt>Shell32.dll (Version 6.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="caa58-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




