---
description: Legt den Namen des Elements fest oder ruft diesen ab.
ms.assetid: 079efc8d-3d08-48b1-bdb1-83f4b89fd633
title: FolderItem.Name-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Name
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f5eb757455b8bbbd4161eae477ca4677eef4fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861787"
---
# <a name="folderitemname-property"></a><span data-ttu-id="57b90-103">FolderItem.Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="57b90-103">FolderItem.Name property</span></span>

<span data-ttu-id="57b90-104">Legt den Namen des Elements fest oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="57b90-104">Sets or gets the item's name.</span></span>

<span data-ttu-id="57b90-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="57b90-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="57b90-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="57b90-106">Syntax</span></span>


```JScript
strName = FolderItem.Name
FolderItem.Name = strName
```



## <a name="property-value"></a><span data-ttu-id="57b90-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="57b90-107">Property value</span></span>

<span data-ttu-id="57b90-108">Eine Variable vom Typ [**BSTR**](/previous-versions/windows/desktop/automat/bstr) , die den Namen des Elements angibt oder empfängt.</span><span class="sxs-lookup"><span data-stu-id="57b90-108">A variable of type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) that specifies or receives the item's name.</span></span>

## <a name="examples"></a><span data-ttu-id="57b90-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57b90-109">Examples</span></span>

<span data-ttu-id="57b90-110">Im folgenden Beispiel wird **Name** verwendet, um den Namen der Autoexec.bat Datei abzurufen. Anschließend wird der Name auf Test.bat zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="57b90-110">The following example uses **Name** to retrieve the name of the Autoexec.bat file, then reset the name to Test.bat.</span></span> <span data-ttu-id="57b90-111">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="57b90-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="57b90-112">JScript</span><span class="sxs-lookup"><span data-stu-id="57b90-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnNameGetSetJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        
        objFolder2 = objShell.NameSpace("C:\\");
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.Name;
                objFolderItem.Name = "TEST.BAT";
            }
        }
    }
</script>
```



<span data-ttu-id="57b90-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="57b90-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnNameGetSetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
                
            set objFolder2 = objShell.NameSpace("C:\")
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.Name
                    objFolderItem.Name = "TEST.BAT"
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="57b90-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="57b90-114">Visual Basic:</span></span>


```VB
Private Sub fnNameGetSetVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\")
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.Name
                    objFolderItem.Name = "TEST.BAT"
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



## <a name="requirements"></a><span data-ttu-id="57b90-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="57b90-115">Requirements</span></span>



| <span data-ttu-id="57b90-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57b90-116">Requirement</span></span> | <span data-ttu-id="57b90-117">Wert</span><span class="sxs-lookup"><span data-stu-id="57b90-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57b90-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57b90-118">Minimum supported client</span></span><br/> | <span data-ttu-id="57b90-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57b90-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="57b90-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57b90-120">Minimum supported server</span></span><br/> | <span data-ttu-id="57b90-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57b90-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="57b90-122">Header</span><span class="sxs-lookup"><span data-stu-id="57b90-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="57b90-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="57b90-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="57b90-124">IDL</span><span class="sxs-lookup"><span data-stu-id="57b90-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57b90-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="57b90-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="57b90-126">DLL</span><span class="sxs-lookup"><span data-stu-id="57b90-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57b90-127"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="57b90-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
