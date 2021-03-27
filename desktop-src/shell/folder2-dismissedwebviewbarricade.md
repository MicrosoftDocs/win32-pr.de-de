---
description: Wird als Antwort auf die webansichtenbarricade aufgerufen, die vom Benutzer verworfen wird.
ms.assetid: 170893b6-c947-45b1-b717-a93a0b083bda
title: Folder2. dismissedwebviewbarricade-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.DismissedWebViewBarricade
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cdedc7292b0dd52ca903b944993e32df1ec2c3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131633"
---
# <a name="folder2dismissedwebviewbarricade-method"></a><span data-ttu-id="28641-103">Folder2. dismissedwebviewbarricade-Methode</span><span class="sxs-lookup"><span data-stu-id="28641-103">Folder2.DismissedWebViewBarricade method</span></span>

<span data-ttu-id="28641-104">Wird als Antwort auf die webansichtenbarricade aufgerufen, die vom Benutzer verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="28641-104">Called in response to the web view barricade being dismissed by the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="28641-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28641-105">Syntax</span></span>


```JScript
Folder2.DismissedWebViewBarricade()
```



## <a name="parameters"></a><span data-ttu-id="28641-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="28641-106">Parameters</span></span>

<span data-ttu-id="28641-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="28641-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28641-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28641-108">Return value</span></span>

<span data-ttu-id="28641-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="28641-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28641-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28641-110">Remarks</span></span>

<span data-ttu-id="28641-111">Eine Anwendung ruft diese Methode auf, nachdem der Benutzer die webansichtenbarricade geschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="28641-111">An application calls this method after the user dismisses the web view barricade.</span></span>

## <a name="examples"></a><span data-ttu-id="28641-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28641-112">Examples</span></span>

<span data-ttu-id="28641-113">Im folgenden Beispiel wird **dismissedwebviewbarricade** verwendet, um anzugeben, dass die webansichtenbarricade für den Ordner "C: \\ Windows" verworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="28641-113">The following example uses **DismissedWebViewBarricade** to specify that the web view barricade for the C:\\Windows folder has been dismissed.</span></span> <span data-ttu-id="28641-114">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28641-114">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="28641-115">JScript</span><span class="sxs-lookup"><span data-stu-id="28641-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectDismissedWebViewBarricadeJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            objFolder2.DismissedWebViewBarricade();
        }
    }
</script>
```



<span data-ttu-id="28641-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="28641-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectDismissedWebViewBarricadeVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            objFolder2.DismissedWebViewBarricade()
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="28641-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="28641-117">Visual Basic:</span></span>


```VB
Private Sub btnDismissedWebViewBarricade_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.DismissedWebViewBarricade
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="28641-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="28641-118">Requirements</span></span>



| <span data-ttu-id="28641-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28641-119">Requirement</span></span> | <span data-ttu-id="28641-120">Wert</span><span class="sxs-lookup"><span data-stu-id="28641-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28641-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28641-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28641-122">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28641-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28641-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28641-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28641-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28641-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="28641-125">Header</span><span class="sxs-lookup"><span data-stu-id="28641-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="28641-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="28641-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="28641-127">IDL</span><span class="sxs-lookup"><span data-stu-id="28641-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28641-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="28641-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="28641-129">DLL</span><span class="sxs-lookup"><span data-stu-id="28641-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28641-130"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="28641-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28641-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="28641-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28641-132">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="28641-132">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="28641-133">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="28641-133">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




