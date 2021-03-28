---
description: Ruft ein folderitems-Objekt ab, das die Auflistung der Elemente im Ordner darstellt.
ms.assetid: ef2965ec-c8ab-4108-8e5e-b4fd5370521a
title: Folder. Items-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Items
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3cfa0fcd2d8e2e51a67a362b33af34abf5b1427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345408"
---
# <a name="folderitems-method"></a><span data-ttu-id="fc1cc-103">Folder. Items-Methode</span><span class="sxs-lookup"><span data-stu-id="fc1cc-103">Folder.Items method</span></span>

<span data-ttu-id="fc1cc-104">Ruft ein [**folderitems**](folderitems.md) -Objekt ab, das die Auflistung der Elemente im Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="fc1cc-104">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc1cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc1cc-105">Syntax</span></span>


```JScript
retVal = Folder.Items()
```



## <a name="parameters"></a><span data-ttu-id="fc1cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc1cc-106">Parameters</span></span>

<span data-ttu-id="fc1cc-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fc1cc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc1cc-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc1cc-108">Return value</span></span>

<span data-ttu-id="fc1cc-109">Type: **[ **folderitems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="fc1cc-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="fc1cc-110">Ein Objekt Verweis auf das [**folderitems**](folderitems.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="fc1cc-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc1cc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc1cc-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fc1cc-112">Nicht alle Methoden werden für alle Ordner implementiert.</span><span class="sxs-lookup"><span data-stu-id="fc1cc-112">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="fc1cc-113">Beispielsweise ist die Methode " [**Parser Name**](folder-parsename.md) " nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert.</span><span class="sxs-lookup"><span data-stu-id="fc1cc-113">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="fc1cc-114">Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="fc1cc-114">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="fc1cc-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc1cc-115">Examples</span></span>

<span data-ttu-id="fc1cc-116">Im folgenden Beispiel werden **Elemente** verwendet, um die Anzahl der Elemente im Ordner "C: Windows" zu bestimmen \\ .</span><span class="sxs-lookup"><span data-stu-id="fc1cc-116">The following example uses **Items** to determine the number of items in the C:\\Windows folder.</span></span> <span data-ttu-id="fc1cc-117">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc1cc-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fc1cc-118">JScript</span><span class="sxs-lookup"><span data-stu-id="fc1cc-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectItemsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItems = new Object;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                document.write (objFolderItems.Count);
            }
        }
    }
</script>
```



<span data-ttu-id="fc1cc-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="fc1cc-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectItemsVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItems

            set objFolderItems = objFolder.Items

            if (not objFolderItems Is Nothing) then
                document.write objFolderItems.Count
            end if

            set objFolderItem = nothing
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="fc1cc-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="fc1cc-120">Visual Basic:</span></span>


```VB
Private Sub btnFolderObjectItems_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItems As FolderItems

        Set objFolderItems = objFolder.Items()

        If (Not objFolderItems Is Nothing) Then
            Dim vCount As Variant

            vCount = objFolderItems.Count
        End If

        Set objFolderItems = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fc1cc-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fc1cc-121">Requirements</span></span>



| <span data-ttu-id="fc1cc-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc1cc-122">Requirement</span></span> | <span data-ttu-id="fc1cc-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fc1cc-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1cc-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc1cc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fc1cc-125">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc1cc-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fc1cc-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc1cc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fc1cc-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc1cc-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fc1cc-128">Header</span><span class="sxs-lookup"><span data-stu-id="fc1cc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc1cc-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc1cc-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="fc1cc-130">IDL</span><span class="sxs-lookup"><span data-stu-id="fc1cc-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc1cc-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc1cc-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="fc1cc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fc1cc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc1cc-133"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="fc1cc-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




