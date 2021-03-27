---
description: Erstellt ein folderItem-Objekt, das ein bestimmtes Element darstellt, und gibt es zurück.
ms.assetid: 3af7052c-fb81-4a96-9bf9-379b0365a376
title: Folder. para Name-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParseName
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ea9a8090a794f23693ae4fef10556bc207f16531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749176"
---
# <a name="folderparsename-method"></a><span data-ttu-id="95d6a-103">Folder. Parser Name-Methode</span><span class="sxs-lookup"><span data-stu-id="95d6a-103">Folder.ParseName method</span></span>

<span data-ttu-id="95d6a-104">Erstellt ein [**folderItem**](folderitem.md) -Objekt, das ein bestimmtes Element darstellt, und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="95d6a-104">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d6a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95d6a-105">Syntax</span></span>


```JScript
retVal = Folder.ParseName(
  bName
)
```



## <a name="parameters"></a><span data-ttu-id="95d6a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95d6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d6a-107">*bName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95d6a-107">*bName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d6a-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="95d6a-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="95d6a-109">Eine Zeichenfolge, die den Namen des Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="95d6a-109">A string that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d6a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95d6a-110">Return value</span></span>

<span data-ttu-id="95d6a-111">Type: **[ **folderItem**](folderitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="95d6a-111">Type: **[**FolderItem**](folderitem.md)\*\***</span></span>

<span data-ttu-id="95d6a-112">Ein Objekt Verweis auf das [**folderItem**](folderitem.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="95d6a-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="95d6a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95d6a-113">Remarks</span></span>

<span data-ttu-id="95d6a-114">" **Parser Name** " sollte nicht für virtuelle Ordner wie "eigene Dokumente" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95d6a-114">**ParseName** should not be used for virtual folders such as My Documents.</span></span>

## <a name="examples"></a><span data-ttu-id="95d6a-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95d6a-115">Examples</span></span>

<span data-ttu-id="95d6a-116">Im folgenden Beispiel wird " **Parser Name** " verwendet, um ein Objekt zu erstellen, das das Ordner Element Clock.avi im Ordner "C: Windows" darstellt \\ .</span><span class="sxs-lookup"><span data-stu-id="95d6a-116">The following example uses **ParseName** to create an object representing the folder item Clock.avi in the C:\\Windows folder.</span></span> <span data-ttu-id="95d6a-117">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95d6a-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="95d6a-118">JScript</span><span class="sxs-lookup"><span data-stu-id="95d6a-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectParseNameJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="95d6a-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="95d6a-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectParseNameVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="95d6a-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="95d6a-120">Visual Basic:</span></span>


```VB
Private Sub btnParseName_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder.ParseName("clock.avi")
            'Add code here.
            Debug.Print "passed"
        Set objFolderItem = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="95d6a-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="95d6a-121">Requirements</span></span>



| <span data-ttu-id="95d6a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95d6a-122">Requirement</span></span> | <span data-ttu-id="95d6a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="95d6a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d6a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95d6a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95d6a-125">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95d6a-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="95d6a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95d6a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95d6a-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95d6a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95d6a-128">Header</span><span class="sxs-lookup"><span data-stu-id="95d6a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="95d6a-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="95d6a-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="95d6a-130">IDL</span><span class="sxs-lookup"><span data-stu-id="95d6a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95d6a-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95d6a-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="95d6a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="95d6a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95d6a-133"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="95d6a-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
