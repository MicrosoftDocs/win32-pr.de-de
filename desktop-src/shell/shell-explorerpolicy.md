---
description: Ruft den Wert für eine angegebene Windows Internet Explorer-Richtlinie ab.
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Shell. explorerpolicy-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fea5192990b8c19c8ddfe8ffad6efe21b98625c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980864"
---
# <a name="shellexplorerpolicy-method"></a><span data-ttu-id="9dffc-103">Shell. explorerpolicy-Methode</span><span class="sxs-lookup"><span data-stu-id="9dffc-103">Shell.ExplorerPolicy method</span></span>

<span data-ttu-id="9dffc-104">Ruft den Wert für eine angegebene Windows Internet Explorer-Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="9dffc-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dffc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dffc-105">Syntax</span></span>


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="9dffc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dffc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dffc-107">*bstraupolicyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dffc-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dffc-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="9dffc-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="9dffc-109">Eine **Zeichenfolge** , die den Namen der Richtlinie angibt.</span><span class="sxs-lookup"><span data-stu-id="9dffc-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dffc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9dffc-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9dffc-111">JScript</span><span class="sxs-lookup"><span data-stu-id="9dffc-111">JScript</span></span>

<span data-ttu-id="9dffc-112">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="9dffc-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="9dffc-113">Der Wert, der dem angegebenen Richtlinien Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9dffc-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="9dffc-114">VB</span><span class="sxs-lookup"><span data-stu-id="9dffc-114">VB</span></span>

<span data-ttu-id="9dffc-115">Typ: _*Variant \**_</span><span class="sxs-lookup"><span data-stu-id="9dffc-115">Type: _*Variant\**_</span></span>

<span data-ttu-id="9dffc-116">Der Wert, der dem angegebenen Richtlinien Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9dffc-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dffc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dffc-117">Remarks</span></span>

<span data-ttu-id="9dffc-118">Netzwerkadministratoren können die Computerumgebung Ihrer Benutzer durch Festlegen von Richtlinien steuern und verwalten.</span><span class="sxs-lookup"><span data-stu-id="9dffc-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="9dffc-119">Der angegebene Wertname muss im Unterschlüssel "_ \*HKEY \_ Current \_ User **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer\*\*" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9dffc-119">The specified value name must be within the _ *HKEY\_CURRENT\_USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer*\* subkey.</span></span> <span data-ttu-id="9dffc-120">Wenn der Wertname nicht vorhanden ist, gibt die Methode **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="9dffc-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="9dffc-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9dffc-121">Examples</span></span>

<span data-ttu-id="9dffc-122">In den folgenden Beispielen wird die ordnungsgemäße Verwendung von **explorerpolicy** für JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="9dffc-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9dffc-123">JScript</span><span class="sxs-lookup"><span data-stu-id="9dffc-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="9dffc-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="9dffc-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objShell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9dffc-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="9dffc-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objShell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9dffc-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9dffc-126">Requirements</span></span>



| <span data-ttu-id="9dffc-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dffc-127">Requirement</span></span> | <span data-ttu-id="9dffc-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9dffc-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dffc-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9dffc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9dffc-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dffc-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="9dffc-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9dffc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9dffc-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dffc-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9dffc-133">Header</span><span class="sxs-lookup"><span data-stu-id="9dffc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dffc-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dffc-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9dffc-135">IDL</span><span class="sxs-lookup"><span data-stu-id="9dffc-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9dffc-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9dffc-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9dffc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9dffc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dffc-138"><dt>Shell32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="9dffc-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
