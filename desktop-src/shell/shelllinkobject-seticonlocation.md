---
description: Legt den Speicherort des Symbols fest, das dem Link zugewiesen ist.
ms.assetid: 257bb8e2-29fa-4d2f-ac2d-3497cf12959c
title: Shelllinkobject. mentikonlocation-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.SetIconLocation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 996f9648e9b9f59e1e84871abac1d6b37e2592d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994910"
---
# <a name="shelllinkobjectseticonlocation-method"></a><span data-ttu-id="c724b-103">Shelllinkobject. mentikonlocation-Methode</span><span class="sxs-lookup"><span data-stu-id="c724b-103">ShellLinkObject.SetIconLocation method</span></span>

<span data-ttu-id="c724b-104">Legt den Speicherort des Symbols fest, das dem Link zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c724b-104">Sets the location of the icon assigned to the link.</span></span>

## <a name="syntax"></a><span data-ttu-id="c724b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c724b-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.SetIconLocation(
  sPath,
  iIndex
)
```



## <a name="parameters"></a><span data-ttu-id="c724b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c724b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c724b-107">*Spath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c724b-107">*sPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c724b-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c724b-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c724b-109">Der voll qualifizierte Pfad der Datei, die das Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="c724b-109">The fully qualified path of the file that contains the icon.</span></span>

</dd> <dt>

<span data-ttu-id="c724b-110">*iIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c724b-110">*iIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c724b-111">Type: **Integer**</span><span class="sxs-lookup"><span data-stu-id="c724b-111">Type: **Integer**</span></span>

<span data-ttu-id="c724b-112">Der Index des Symbols in der durch *Spath* angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="c724b-112">The index of the icon in the file specified by *sPath*.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c724b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c724b-113">Examples</span></span>

<span data-ttu-id="c724b-114">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c724b-114">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c724b-115">JScript</span><span class="sxs-lookup"><span data-stu-id="c724b-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectSetIconLocationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.SetIconLocation(objShellLink.Path, 1);
                    objShellLink.Save();
                }
            }
        }
    }
</script>
```



<span data-ttu-id="c724b-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="c724b-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectSetIconLocationVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.SetIconLocation objShellLink.Path, 1
                                objShellLink.Save
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c724b-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c724b-117">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectSetIconLocationVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.SetIconLocation objShellLink.Path, 1
                            objShellLink.Save
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c724b-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c724b-118">Requirements</span></span>



| <span data-ttu-id="c724b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c724b-119">Requirement</span></span> | <span data-ttu-id="c724b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c724b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c724b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c724b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c724b-122">Nur Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c724b-122">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c724b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c724b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c724b-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c724b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c724b-125">Header</span><span class="sxs-lookup"><span data-stu-id="c724b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c724b-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c724b-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c724b-127">IDL</span><span class="sxs-lookup"><span data-stu-id="c724b-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c724b-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c724b-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c724b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c724b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c724b-130"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="c724b-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
