---
description: 'Shell.NameSpace-Methode: Erstellt ein Folder-Objekt für den angegebenen Ordner und gibt es zurück.'
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Shell.NameSpace-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fab501912c55aaaf6cab832bf76763672e830d33
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083708"
---
# <a name="shellnamespace-method"></a><span data-ttu-id="19161-103">Shell.NameSpace-Methode</span><span class="sxs-lookup"><span data-stu-id="19161-103">Shell.NameSpace method</span></span>

<span data-ttu-id="19161-104">Erstellt ein [**Folder-Objekt für**](folder.md) den angegebenen Ordner und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="19161-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="19161-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19161-105">Syntax</span></span>


```JScript
retVal = Shell.NameSpace(
  vDir
)
```


```VB

Shell.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="19161-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19161-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19161-107">*vDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="19161-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19161-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="19161-108">Type: **Variant**</span></span>

<span data-ttu-id="19161-109">Der Ordner, für den das Ordnerobjekt [**erstellt werden**](folder.md) soll.</span><span class="sxs-lookup"><span data-stu-id="19161-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="19161-110">Dies kann eine Zeichenfolge sein, die den Pfad des Ordners oder einen der [**ShellSpecialFolderConstants-Werte angibt.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="19161-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="19161-111">Beachten Sie, dass die konstanten Namen in **ShellSpecialFolderConstants** in Visual Basic, aber nicht in VBScript oder JScript verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="19161-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="19161-112">In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19161-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19161-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19161-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="19161-114">JScript</span><span class="sxs-lookup"><span data-stu-id="19161-114">JScript</span></span>

<span data-ttu-id="19161-115">Typ: **[ **Ordner**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="19161-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="19161-116">Objektverweis auf das [**Folder-Objekt**](folder.md) für den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="19161-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="19161-117">Wenn der Ordner nicht erfolgreich erstellt wurde, gibt dieser Wert **NULL zurück.**</span><span class="sxs-lookup"><span data-stu-id="19161-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="19161-118">VB</span><span class="sxs-lookup"><span data-stu-id="19161-118">VB</span></span>

<span data-ttu-id="19161-119">Typ: **[ **Ordner**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="19161-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="19161-120">Objektverweis auf das [**Folder-Objekt**](folder.md) für den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="19161-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="19161-121">Wenn der Ordner nicht erfolgreich erstellt wurde, gibt dieser Wert **NULL zurück.**</span><span class="sxs-lookup"><span data-stu-id="19161-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="19161-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19161-122">Examples</span></span>

<span data-ttu-id="19161-123">Im folgenden Beispiel wird **NameSpace** verwendet.</span><span class="sxs-lookup"><span data-stu-id="19161-123">The following example shows **NameSpace** in use.</span></span> <span data-ttu-id="19161-124">Die richtige Verwendung wird für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="19161-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="19161-125">Jscript:</span><span class="sxs-lookup"><span data-stu-id="19161-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="19161-126">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="19161-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="19161-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="19161-127">Visual Basic:</span></span>


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="19161-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19161-128">Requirements</span></span>



| <span data-ttu-id="19161-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19161-129">Requirement</span></span> | <span data-ttu-id="19161-130">Wert</span><span class="sxs-lookup"><span data-stu-id="19161-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19161-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19161-131">Minimum supported client</span></span><br/> | <span data-ttu-id="19161-132">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19161-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="19161-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19161-133">Minimum supported server</span></span><br/> | <span data-ttu-id="19161-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19161-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="19161-135">Header</span><span class="sxs-lookup"><span data-stu-id="19161-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="19161-136"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="19161-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="19161-137">Idl</span><span class="sxs-lookup"><span data-stu-id="19161-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19161-138"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="19161-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="19161-139">DLL</span><span class="sxs-lookup"><span data-stu-id="19161-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19161-140"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="19161-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




