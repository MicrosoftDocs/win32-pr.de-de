---
description: 'IShellDispatch4.ExplorerPolicy-Methode: Ruft den Wert für eine angegebene Windows-Internet Explorer ab.'
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: IShellDispatch4.ExplorerPolicy-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a03d61905bdb1f2b16de11cc604625d8e71a7ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116828"
---
# <a name="ishelldispatch4explorerpolicy-method"></a><span data-ttu-id="374f3-103">IShellDispatch4.ExplorerPolicy-Methode</span><span class="sxs-lookup"><span data-stu-id="374f3-103">IShellDispatch4.ExplorerPolicy method</span></span>

<span data-ttu-id="374f3-104">Ruft den Wert für eine angegebene Windows-Internet Explorer ab.</span><span class="sxs-lookup"><span data-stu-id="374f3-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="374f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="374f3-105">Syntax</span></span>


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="374f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="374f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="374f3-107">*bstrPolicyName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="374f3-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="374f3-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="374f3-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="374f3-109">Eine **Zeichenfolge,** die den Namen der Richtlinie angibt.</span><span class="sxs-lookup"><span data-stu-id="374f3-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="374f3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="374f3-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="374f3-111">JScript</span><span class="sxs-lookup"><span data-stu-id="374f3-111">JScript</span></span>

<span data-ttu-id="374f3-112">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="374f3-112">Type: **Variant\***</span></span>

<span data-ttu-id="374f3-113">Der wert, der dem angegebenen Richtliniennamen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="374f3-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="374f3-114">VB</span><span class="sxs-lookup"><span data-stu-id="374f3-114">VB</span></span>

<span data-ttu-id="374f3-115">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="374f3-115">Type: **Variant\***</span></span>

<span data-ttu-id="374f3-116">Der wert, der dem angegebenen Richtliniennamen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="374f3-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="374f3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="374f3-117">Remarks</span></span>

<span data-ttu-id="374f3-118">Netzwerkadministratoren können die Computerumgebung ihrer Benutzer steuern und verwalten, indem sie Richtlinien festlegen.</span><span class="sxs-lookup"><span data-stu-id="374f3-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="374f3-119">Der angegebene Wertname muss innerhalb des **Unterschlüssels HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **Explorer** sein.</span><span class="sxs-lookup"><span data-stu-id="374f3-119">The specified value name must be within the **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Policies**\\**Explorer** subkey.</span></span> <span data-ttu-id="374f3-120">Wenn der Wertname nicht vorhanden ist, gibt die Methode NULL **zurück.**</span><span class="sxs-lookup"><span data-stu-id="374f3-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="374f3-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="374f3-121">Examples</span></span>

<span data-ttu-id="374f3-122">Die folgenden Beispiele zeigen die ordnungsgemäße Verwendung von **ExplorerPolicy** für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="374f3-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="374f3-123">Jscript:</span><span class="sxs-lookup"><span data-stu-id="374f3-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="374f3-124">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="374f3-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objshell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="374f3-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="374f3-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="374f3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="374f3-126">Requirements</span></span>



| <span data-ttu-id="374f3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="374f3-127">Requirement</span></span> | <span data-ttu-id="374f3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="374f3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="374f3-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="374f3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="374f3-130">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="374f3-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="374f3-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="374f3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="374f3-132">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="374f3-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="374f3-133">Header</span><span class="sxs-lookup"><span data-stu-id="374f3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="374f3-134"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="374f3-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="374f3-135">Idl</span><span class="sxs-lookup"><span data-stu-id="374f3-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="374f3-136"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="374f3-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="374f3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="374f3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="374f3-138"><dt>Shell32.dll (Version 6.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="374f3-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
