---
description: 'IShellDispatch4.WindowsSecurity-Methode: Zeigt das dialogfeld Windows-Sicherheit an.'
title: IShellDispatch4.WindowsSecurity-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.openlocfilehash: 2d7e8cfbd1e7a2a2392b78487c6a58b62de6df6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116808"
---
# <a name="ishelldispatch4windowssecurity-method"></a><span data-ttu-id="48f28-103">IShellDispatch4.WindowsSecurity-Methode</span><span class="sxs-lookup"><span data-stu-id="48f28-103">IShellDispatch4.WindowsSecurity method</span></span>

<span data-ttu-id="48f28-104">Zeigt das **Windows-Sicherheit** An.</span><span class="sxs-lookup"><span data-stu-id="48f28-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f28-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48f28-105">Syntax</span></span>


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="48f28-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48f28-106">Parameters</span></span>

<span data-ttu-id="48f28-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="48f28-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48f28-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48f28-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="48f28-109">JScript</span><span class="sxs-lookup"><span data-stu-id="48f28-109">JScript</span></span>

<span data-ttu-id="48f28-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="48f28-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="48f28-111">VB</span><span class="sxs-lookup"><span data-stu-id="48f28-111">VB</span></span>

<span data-ttu-id="48f28-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="48f28-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48f28-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48f28-113">Remarks</span></span>

<span data-ttu-id="48f28-114">Diese Methode zeigt das Dialogfeld an, das nach dem Drücken von STRG+ALT+DELETE oder mithilfe der Sicherheitsoption im **Startmenü angezeigt** wird.</span><span class="sxs-lookup"><span data-stu-id="48f28-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="48f28-115">Diese Methode kann nur verwendet werden, wenn eine Verbindung zwischen einer Terminalsitzung und Microsoft Terminal Server besteht.</span><span class="sxs-lookup"><span data-stu-id="48f28-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="48f28-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48f28-116">Examples</span></span>

<span data-ttu-id="48f28-117">Die folgenden Beispiele zeigen die Verwendung von **WindowsSecurity** für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="48f28-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="48f28-118">Jscript:</span><span class="sxs-lookup"><span data-stu-id="48f28-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="48f28-119">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="48f28-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="48f28-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="48f28-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="48f28-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48f28-121">Requirements</span></span>



| <span data-ttu-id="48f28-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48f28-122">Requirement</span></span> | <span data-ttu-id="48f28-123">Wert</span><span class="sxs-lookup"><span data-stu-id="48f28-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f28-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48f28-124">Minimum supported client</span></span><br/> | <span data-ttu-id="48f28-125">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48f28-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="48f28-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48f28-126">Minimum supported server</span></span><br/> | <span data-ttu-id="48f28-127">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48f28-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="48f28-128">Header</span><span class="sxs-lookup"><span data-stu-id="48f28-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="48f28-129"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="48f28-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="48f28-130">Idl</span><span class="sxs-lookup"><span data-stu-id="48f28-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48f28-131"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="48f28-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="48f28-132">DLL</span><span class="sxs-lookup"><span data-stu-id="48f28-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48f28-133"><dt>Shell32.dll (Version 6.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="48f28-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




