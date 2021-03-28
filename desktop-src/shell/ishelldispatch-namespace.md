---
description: Erstellt ein Ordner Objekt für den angegebenen Ordner und gibt dieses zurück.
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Ishelldispatch. Namespace-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 069752a5e81949889dce5539e3f23960a12c9736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527344"
---
# <a name="ishelldispatchnamespace-method"></a><span data-ttu-id="cc1ee-103">Ishelldispatch. Namespace-Methode</span><span class="sxs-lookup"><span data-stu-id="cc1ee-103">IShellDispatch.NameSpace method</span></span>

<span data-ttu-id="cc1ee-104">Erstellt ein [**Ordner**](folder.md) Objekt für den angegebenen Ordner und gibt dieses zurück.</span><span class="sxs-lookup"><span data-stu-id="cc1ee-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc1ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc1ee-105">Syntax</span></span>


```JScript
retVal = IShellDispatch.NameSpace(
  vDir
)
```


```VB

IShellDispatch.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="cc1ee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc1ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc1ee-107">*vdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc1ee-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1ee-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="cc1ee-108">Type: **Variant**</span></span>

<span data-ttu-id="cc1ee-109">Der Ordner, für den das [**Ordner**](folder.md) Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc1ee-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="cc1ee-110">Dabei kann es sich um eine Zeichenfolge handeln, die den Pfad des Ordners oder einen der [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) -Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="cc1ee-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="cc1ee-111">Beachten Sie, dass die in **shellspecialfolderconstants** gefundenen Konstanten Namen in Visual Basic verfügbar sind, jedoch nicht in VBScript oder JScript.</span><span class="sxs-lookup"><span data-stu-id="cc1ee-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="cc1ee-112">In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc1ee-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc1ee-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc1ee-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cc1ee-114">JScript</span><span class="sxs-lookup"><span data-stu-id="cc1ee-114">JScript</span></span>

<span data-ttu-id="cc1ee-115">Typ: **[ **Ordner**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cc1ee-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="cc1ee-116">Objekt Verweis auf das [**Ordner**](folder.md) Objekt für den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="cc1ee-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="cc1ee-117">Wenn der Ordner nicht erfolgreich erstellt wurde, gibt dieser Wert **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="cc1ee-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="cc1ee-118">VB</span><span class="sxs-lookup"><span data-stu-id="cc1ee-118">VB</span></span>

<span data-ttu-id="cc1ee-119">Typ: **[ **Ordner**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cc1ee-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="cc1ee-120">Objekt Verweis auf das [**Ordner**](folder.md) Objekt für den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="cc1ee-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="cc1ee-121">Wenn der Ordner nicht erfolgreich erstellt wurde, gibt dieser Wert **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="cc1ee-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc1ee-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc1ee-122">Remarks</span></span>

<span data-ttu-id="cc1ee-123">Diese Methode wird implementiert, und der Zugriff erfolgt über die [**Shell. Namespace**](shell-namespace.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cc1ee-123">This method is implemented and accessed through the [**Shell.NameSpace**](shell-namespace.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="cc1ee-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc1ee-124">Examples</span></span>

<span data-ttu-id="cc1ee-125">In den folgenden Beispielen wird die Verwendung von [**Namespace**](shell-namespace.md) in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="cc1ee-125">The following examples show the use of [**NameSpace**](shell-namespace.md) in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cc1ee-126">JScript</span><span class="sxs-lookup"><span data-stu-id="cc1ee-126">JScript:</span></span>


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



<span data-ttu-id="cc1ee-127">VBScript</span><span class="sxs-lookup"><span data-stu-id="cc1ee-127">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="cc1ee-128">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cc1ee-128">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cc1ee-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cc1ee-129">Requirements</span></span>



| <span data-ttu-id="cc1ee-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc1ee-130">Requirement</span></span> | <span data-ttu-id="cc1ee-131">Wert</span><span class="sxs-lookup"><span data-stu-id="cc1ee-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1ee-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc1ee-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cc1ee-133">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc1ee-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cc1ee-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc1ee-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cc1ee-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc1ee-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cc1ee-136">Header</span><span class="sxs-lookup"><span data-stu-id="cc1ee-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc1ee-137"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc1ee-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cc1ee-138">IDL</span><span class="sxs-lookup"><span data-stu-id="cc1ee-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cc1ee-139"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cc1ee-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cc1ee-140">DLL</span><span class="sxs-lookup"><span data-stu-id="cc1ee-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc1ee-141"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="cc1ee-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




