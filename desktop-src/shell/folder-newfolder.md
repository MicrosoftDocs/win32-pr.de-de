---
description: Erstellt einen neuen Ordner.
ms.assetid: 7a552e5a-e9a3-4fcf-bc6b-17e8bc39af87
title: Folder. NewFolder-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.NewFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 86784aa071be22cd16a06d9d4516970d2924079a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959699"
---
# <a name="foldernewfolder-method"></a><span data-ttu-id="00127-103">Folder. NewFolder-Methode</span><span class="sxs-lookup"><span data-stu-id="00127-103">Folder.NewFolder method</span></span>

<span data-ttu-id="00127-104">Erstellt einen neuen Ordner.</span><span class="sxs-lookup"><span data-stu-id="00127-104">Creates a new folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="00127-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00127-105">Syntax</span></span>


```JScript
Folder.NewFolder(
  bName,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="00127-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00127-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00127-107">*bName*</span><span class="sxs-lookup"><span data-stu-id="00127-107">*bName*</span></span> 
</dt> <dd>

<span data-ttu-id="00127-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="00127-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="00127-109">Eine Zeichenfolge, die den Namen des neuen Ordners angibt.</span><span class="sxs-lookup"><span data-stu-id="00127-109">A string that specifies the name of the new folder.</span></span>

</dd> <dt>

<span data-ttu-id="00127-110">*voptions* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="00127-110">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="00127-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="00127-111">Type: **Variant**</span></span>

<span data-ttu-id="00127-112">Dieser Wert wird derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="00127-112">This value is not currently used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00127-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00127-113">Return value</span></span>

<span data-ttu-id="00127-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="00127-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00127-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00127-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="00127-116">Nicht alle Methoden werden für alle Ordner implementiert.</span><span class="sxs-lookup"><span data-stu-id="00127-116">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="00127-117">Beispielsweise ist die Methode " [**Parser Name**](folder-parsename.md) " nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert.</span><span class="sxs-lookup"><span data-stu-id="00127-117">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="00127-118">Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="00127-118">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="00127-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00127-119">Examples</span></span>

<span data-ttu-id="00127-120">Im folgenden Beispiel wird **NewFolder** verwendet, um den neuen Ordner "C: TestFolder" zu erstellen \\ .</span><span class="sxs-lookup"><span data-stu-id="00127-120">The following example uses **NewFolder** to create the new folder C:\\TestFolder.</span></span> <span data-ttu-id="00127-121">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="00127-121">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="00127-122">JScript</span><span class="sxs-lookup"><span data-stu-id="00127-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectNewFolderJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\");
        if (objFolder != null)
        {
            objFolder.NewFolder("TestFolder");
        }
    }
</script>
```



<span data-ttu-id="00127-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="00127-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectNewFolderVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            objFolder.NewFolder("TestFolder")
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="00127-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="00127-124">Visual Basic:</span></span>


```VB
Private Sub btnNewFolder_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\")

    If (Not objFolder Is Nothing) Then
        objFolder.NewFolder ("TestFolder")
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="00127-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="00127-125">Requirements</span></span>



| <span data-ttu-id="00127-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00127-126">Requirement</span></span> | <span data-ttu-id="00127-127">Wert</span><span class="sxs-lookup"><span data-stu-id="00127-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00127-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00127-128">Minimum supported client</span></span><br/> | <span data-ttu-id="00127-129">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00127-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="00127-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00127-130">Minimum supported server</span></span><br/> | <span data-ttu-id="00127-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00127-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="00127-132">Header</span><span class="sxs-lookup"><span data-stu-id="00127-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="00127-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="00127-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="00127-134">IDL</span><span class="sxs-lookup"><span data-stu-id="00127-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="00127-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="00127-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="00127-136">DLL</span><span class="sxs-lookup"><span data-stu-id="00127-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00127-137"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="00127-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
