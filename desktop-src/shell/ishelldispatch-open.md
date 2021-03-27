---
description: Öffnet den angegebenen Ordner.
ms.assetid: 30FE669A-4AFD-4dfa-9F62-E62E744469C7
title: Ishelldispatch. Open-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d794020313ad776c1d538dc2acb909d562d32f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753088"
---
# <a name="ishelldispatchopen-method"></a><span data-ttu-id="eed55-103">Ishelldispatch. Open-Methode</span><span class="sxs-lookup"><span data-stu-id="eed55-103">IShellDispatch.Open method</span></span>

<span data-ttu-id="eed55-104">Öffnet den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="eed55-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eed55-105">Syntax</span></span>


```JScript
IShellDispatch.Open(
  vDir
)
```


```VB

IShellDispatch.Open( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="eed55-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eed55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed55-107">*vdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eed55-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eed55-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="eed55-108">Type: **Variant**</span></span>

<span data-ttu-id="eed55-109">Eine Zeichenfolge, die den Pfad des Ordners oder einen der [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) -Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="eed55-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="eed55-110">Beachten Sie, dass die in **shellspecialfolderconstants** gefundenen Konstanten Namen in Visual Basic verfügbar sind, jedoch nicht in VBScript oder JScript.</span><span class="sxs-lookup"><span data-stu-id="eed55-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="eed55-111">In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eed55-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="eed55-112">Wenn *vdir* auf eine der [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) festgelegt ist und der spezielle Ordner nicht vorhanden ist, erstellt diese Funktion den Ordner.</span><span class="sxs-lookup"><span data-stu-id="eed55-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eed55-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eed55-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="eed55-114">JScript</span><span class="sxs-lookup"><span data-stu-id="eed55-114">JScript</span></span>

<span data-ttu-id="eed55-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eed55-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="eed55-116">VB</span><span class="sxs-lookup"><span data-stu-id="eed55-116">VB</span></span>

<span data-ttu-id="eed55-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eed55-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eed55-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eed55-118">Remarks</span></span>

<span data-ttu-id="eed55-119">Diese Methode wird implementiert und über die [**Shell. Open**](shell-open.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="eed55-119">This method is implemented and accessed through the [**Shell.Open**](shell-open.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="eed55-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eed55-120">Examples</span></span>

<span data-ttu-id="eed55-121">In den folgenden Beispielen wird die Verwendung von **Open** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="eed55-121">The following examples show the use of **Open** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="eed55-122">JScript</span><span class="sxs-lookup"><span data-stu-id="eed55-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objshell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="eed55-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="eed55-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Open("C:\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="eed55-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="eed55-124">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="eed55-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="eed55-125">Requirements</span></span>



| <span data-ttu-id="eed55-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eed55-126">Requirement</span></span> | <span data-ttu-id="eed55-127">Wert</span><span class="sxs-lookup"><span data-stu-id="eed55-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eed55-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eed55-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eed55-129">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eed55-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="eed55-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eed55-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eed55-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eed55-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="eed55-132">Header</span><span class="sxs-lookup"><span data-stu-id="eed55-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="eed55-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eed55-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="eed55-134">IDL</span><span class="sxs-lookup"><span data-stu-id="eed55-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eed55-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eed55-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="eed55-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eed55-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eed55-137"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="eed55-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed55-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eed55-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed55-139">**Ishelldispatch**</span><span class="sxs-lookup"><span data-stu-id="eed55-139">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="eed55-140">**Erkunden**</span><span class="sxs-lookup"><span data-stu-id="eed55-140">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




