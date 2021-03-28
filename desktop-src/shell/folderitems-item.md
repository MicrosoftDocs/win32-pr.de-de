---
description: Ruft das folderItem-Objekt für ein angegebenes Element in der Auflistung ab.
ms.assetid: 164f823d-12d9-4950-a881-63837c53760d
title: Folderitems. Item-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ed670ed4af3882e38faf2699429c3d1c076f3056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977040"
---
# <a name="folderitemsitem-method"></a><span data-ttu-id="3f3bb-103">Folderitems. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="3f3bb-103">FolderItems.Item method</span></span>

<span data-ttu-id="3f3bb-104">Ruft das [**folderItem**](folderitem.md) -Objekt für ein angegebenes Element in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="3f3bb-104">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f3bb-105">Syntax</span></span>


```JScript
FolderItems.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="3f3bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f3bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f3bb-107">*iIndex* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3f3bb-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3bb-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="3f3bb-108">Type: **Variant**</span></span>

<span data-ttu-id="3f3bb-109">Der nullbasierte Index des abzurufenden Elements.</span><span class="sxs-lookup"><span data-stu-id="3f3bb-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="3f3bb-110">Dieser Wert muss kleiner sein als der Wert der [**count**](folderitems-count.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3f3bb-110">This value must be less than the value of the [**Count**](folderitems-count.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f3bb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f3bb-111">Return value</span></span>

<span data-ttu-id="3f3bb-112">Ein Objekt Verweis auf das [**folderItem**](folderitem.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3f3bb-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="3f3bb-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f3bb-113">Examples</span></span>

<span data-ttu-id="3f3bb-114">Im folgenden Beispiel wird das- **Element** verwendet, um das [**folderItem**](folderitem.md) -Objekt abzurufen, das die Notepad.exe Datei im Windows-Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="3f3bb-114">The following example uses **Item** to retrieve the [**FolderItem**](folderitem.md) object representing the Notepad.exe file found in the Windows folder.</span></span> <span data-ttu-id="3f3bb-115">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f3bb-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3f3bb-116">JScript</span><span class="sxs-lookup"><span data-stu-id="3f3bb-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var objFolderItem;
                
                objFolderItem = objFolderItems.Item(objFolderItems.Count - 1);
                alert(objFolderItem.Name);
            }
        }
    }
</script>
```



<span data-ttu-id="3f3bb-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="3f3bb-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim objFolderItem
                    
                    set objFolderItem = objFolderItems.Item
                        if (not objFolderItem is nothing) then
                            alert(objFolderItem.Name)
                        end if
                    set objFolderItem = nothing
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="3f3bb-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3f3bb-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsItemVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim objFolderItem As FolderItem
                    
                    Set objFolderItem = objFolderItems.Item("NOTEPAD.EXE")
                        If (Not objFolderItem Is Nothing) Then
                            Debug.Print objFolderItem.Path
                        End If
                    Set objFolderItem = Nothing
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3f3bb-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3f3bb-119">Requirements</span></span>



| <span data-ttu-id="3f3bb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f3bb-120">Requirement</span></span> | <span data-ttu-id="3f3bb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3f3bb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3bb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f3bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3f3bb-123">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f3bb-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3f3bb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f3bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3f3bb-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f3bb-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3f3bb-126">Header</span><span class="sxs-lookup"><span data-stu-id="3f3bb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f3bb-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f3bb-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3f3bb-128">IDL</span><span class="sxs-lookup"><span data-stu-id="3f3bb-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3f3bb-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3f3bb-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3f3bb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3f3bb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f3bb-131"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="3f3bb-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f3bb-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3f3bb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f3bb-133">**Folderitems**</span><span class="sxs-lookup"><span data-stu-id="3f3bb-133">**FolderItems**</span></span>](folderitems.md)
</dt> </dl>

 

 




