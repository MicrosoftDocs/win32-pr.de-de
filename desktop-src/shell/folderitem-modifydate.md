---
description: Für eine Datei legt das Datum und die Uhrzeit der letzten Änderung fest oder ruft diese ab. Für einen Ordner Ruft das Datum und die Uhrzeit der letzten Änderung eines Ordners ab, kann jedoch nicht festgelegt werden.
ms.assetid: bb60c800-863b-469b-b937-9816b8b338bf
title: FolderItem. ModifyDate-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.ModifyDate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b9ea5fa6b611a0311840507fb2068d08801a5bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127849"
---
# <a name="folderitemmodifydate-property"></a><span data-ttu-id="e4482-104">FolderItem. ModifyDate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e4482-104">FolderItem.ModifyDate property</span></span>

<span data-ttu-id="e4482-105">Für eine Datei legt das Datum und die Uhrzeit der letzten Änderung fest oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="e4482-105">For a file, sets or gets the date and time that it was last modified.</span></span> <span data-ttu-id="e4482-106">Für einen Ordner Ruft das Datum und die Uhrzeit der letzten Änderung eines Ordners ab, kann jedoch nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e4482-106">For a folder, retrieves the date and time that a folder was last modified, but cannot set it.</span></span>

<span data-ttu-id="e4482-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e4482-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4482-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4482-108">Syntax</span></span>


```JScript
iModifyDate = FolderItem.ModifyDate
FolderItem.ModifyDate = iModifyDate
```



## <a name="property-value"></a><span data-ttu-id="e4482-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e4482-109">Property value</span></span>

<span data-ttu-id="e4482-110">**Datum** , das das Datum und die Uhrzeit der letzten Änderung des Elements angibt oder empfängt.</span><span class="sxs-lookup"><span data-stu-id="e4482-110">**Date** that specifies or receives the date and time that the item was last modified.</span></span>

## <a name="examples"></a><span data-ttu-id="e4482-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4482-111">Examples</span></span>

<span data-ttu-id="e4482-112">Im folgenden Beispiel wird **ModifyDate** verwendet, um das Datum der letzten Änderung von Notepad abzurufen und dann auf eine sehr lange Zeit zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="e4482-112">The following example uses **ModifyDate** to retrieve the last modified date of Notepad and then reset it to a very long time ago.</span></span> <span data-ttu-id="e4482-113">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4482-113">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e4482-114">JScript</span><span class="sxs-lookup"><span data-stu-id="e4482-114">JScript:</span></span>


```JScript
<script language="JScript">
    function fnModifyDateGetSetJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.ModifyDate;
                objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM";
            }
        }
    }
</script>
```



<span data-ttu-id="e4482-115">VBScript</span><span class="sxs-lookup"><span data-stu-id="e4482-115">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnModifyDateGetSetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.ModifyDate
                    objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM"
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e4482-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e4482-116">Visual Basic:</span></span>


```VB
Private Sub fnModifyDateGetSetVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.ModifyDate
                    objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM"
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e4482-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e4482-117">Requirements</span></span>



| <span data-ttu-id="e4482-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4482-118">Requirement</span></span> | <span data-ttu-id="e4482-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e4482-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4482-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4482-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e4482-121">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4482-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e4482-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4482-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e4482-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4482-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e4482-124">Header</span><span class="sxs-lookup"><span data-stu-id="e4482-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4482-125"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4482-125"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e4482-126">IDL</span><span class="sxs-lookup"><span data-stu-id="e4482-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4482-127"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4482-127"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e4482-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e4482-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4482-129"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="e4482-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




