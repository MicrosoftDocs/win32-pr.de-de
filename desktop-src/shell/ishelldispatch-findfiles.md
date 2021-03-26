---
description: 'Zeigt das Dialogfeld suchen: alle Dateien an. Dies ist das gleiche wie beim Klicken auf das Startmenü und anschließendes Auswählen von suchen.'
ms.assetid: 6F588D5E-5B6E-4000-BAD5-B557FB975FCA
title: Ishelldispatch. findfiles-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9a9ea407d0ceccfe7706ed481aa80bcda9405ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863147"
---
# <a name="ishelldispatchfindfiles-method"></a><span data-ttu-id="81509-104">Ishelldispatch. findfiles-Methode</span><span class="sxs-lookup"><span data-stu-id="81509-104">IShellDispatch.FindFiles method</span></span>

<span data-ttu-id="81509-105">Zeigt das Dialogfeld **suchen: alle Dateien** an.</span><span class="sxs-lookup"><span data-stu-id="81509-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="81509-106">Dies ist das gleiche wie beim Klicken auf das **Startmenü** und anschließendes Auswählen von **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="81509-106">This is the same as clicking the **Start** menu and then selecting **Search**.</span></span>

## <a name="syntax"></a><span data-ttu-id="81509-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="81509-107">Syntax</span></span>


```JScript
IShellDispatch.FindFiles()
```


```VB

IShellDispatch.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="81509-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="81509-108">Parameters</span></span>

<span data-ttu-id="81509-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="81509-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81509-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81509-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="81509-111">JScript</span><span class="sxs-lookup"><span data-stu-id="81509-111">JScript</span></span>

<span data-ttu-id="81509-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="81509-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="81509-113">VB</span><span class="sxs-lookup"><span data-stu-id="81509-113">VB</span></span>

<span data-ttu-id="81509-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="81509-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81509-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81509-115">Remarks</span></span>

<span data-ttu-id="81509-116">Diese Methode wird implementiert und über die [**Shell. findfiles**](shell-findfiles.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="81509-116">This method is implemented and accessed through the [**Shell.FindFiles**](shell-findfiles.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="81509-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81509-117">Examples</span></span>

<span data-ttu-id="81509-118">In den folgenden Beispielen wird die Verwendung von **findfiles** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="81509-118">The following examples show the use of **FindFiles** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="81509-119">JScript</span><span class="sxs-lookup"><span data-stu-id="81509-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindFiles();
    }
</script>
```



<span data-ttu-id="81509-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="81509-120">VBScript:</span></span>


```VB
<script language="VBScript">
   function fnShellFindFilesVB()
       dim objShell
       
       set objShell = CreateObject("shell.application")
       objshell.FindFiles

       set objShell = nothing
   end function
</script>
```



<span data-ttu-id="81509-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="81509-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="81509-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="81509-122">Requirements</span></span>



| <span data-ttu-id="81509-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81509-123">Requirement</span></span> | <span data-ttu-id="81509-124">Wert</span><span class="sxs-lookup"><span data-stu-id="81509-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81509-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81509-125">Minimum supported client</span></span><br/> | <span data-ttu-id="81509-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81509-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="81509-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81509-127">Minimum supported server</span></span><br/> | <span data-ttu-id="81509-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81509-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="81509-129">Header</span><span class="sxs-lookup"><span data-stu-id="81509-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="81509-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="81509-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="81509-131">IDL</span><span class="sxs-lookup"><span data-stu-id="81509-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81509-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81509-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="81509-133">DLL</span><span class="sxs-lookup"><span data-stu-id="81509-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81509-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="81509-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




