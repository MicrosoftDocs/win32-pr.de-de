---
description: Sucht das Ziel eines shelllinks, auch wenn das Ziel verschoben oder umbenannt wurde.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: Shelllinkobject. Resolve-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b1cb0760f1ee19acfa10208711e73919fd084ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980800"
---
# <a name="shelllinkobjectresolve-method"></a><span data-ttu-id="cdd53-103">Shelllinkobject. Resolve-Methode</span><span class="sxs-lookup"><span data-stu-id="cdd53-103">ShellLinkObject.Resolve method</span></span>

<span data-ttu-id="cdd53-104">Sucht das Ziel eines shelllinks, auch wenn das Ziel verschoben oder umbenannt wurde.</span><span class="sxs-lookup"><span data-stu-id="cdd53-104">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd53-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdd53-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a><span data-ttu-id="cdd53-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdd53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd53-107">*fFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd53-107">*fFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd53-108">Type: **Integer**</span><span class="sxs-lookup"><span data-stu-id="cdd53-108">Type: **Integer**</span></span>

<span data-ttu-id="cdd53-109">Flags, die die auszuführende Aktion angeben.</span><span class="sxs-lookup"><span data-stu-id="cdd53-109">Flags that specify the action to be taken.</span></span> <span data-ttu-id="cdd53-110">Dies kann eine Kombination der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="cdd53-110">This can be a combination of the following values:</span></span>

<dt>



 <span data-ttu-id="cdd53-111">(1)</span><span class="sxs-lookup"><span data-stu-id="cdd53-111">(1)</span></span>


</dt> <dd>

<span data-ttu-id="cdd53-112">Wenn der Link nicht aufgelöst werden kann, wird kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cdd53-112">Do not display a dialog box if the link cannot be resolved.</span></span> <span data-ttu-id="cdd53-113">Wenn dieses Flag festgelegt ist, gibt das hochwertige Wort von *fFlags* eine Timeout Dauer in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="cdd53-113">When this flag is set, the high-order word of *fFlags* specifies a time-out duration, in milliseconds.</span></span> <span data-ttu-id="cdd53-114">Die Methode gibt zurück, wenn der Link nicht innerhalb der Timeout Dauer aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="cdd53-114">The method returns if the link cannot be resolved within the time-out duration.</span></span> <span data-ttu-id="cdd53-115">Wenn das höchst wertige Wort auf 0 (null) festgelegt ist, wird die Timeout Dauer standardmäßig auf 3000 Millisekunden (3 Sekunden) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cdd53-115">If the high-order word is set to zero, the time-out duration defaults to 3000 milliseconds (3 seconds).</span></span>

</dd> <dt>



 <span data-ttu-id="cdd53-116">(4)</span><span class="sxs-lookup"><span data-stu-id="cdd53-116">(4)</span></span>


</dt> <dd>

<span data-ttu-id="cdd53-117">Wenn sich der Link geändert hat, aktualisieren Sie den Pfad und die Liste der Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="cdd53-117">If the link has changed, update its path and list of identifiers.</span></span>

</dd> <dt>



 <span data-ttu-id="cdd53-118">(8)</span><span class="sxs-lookup"><span data-stu-id="cdd53-118">(8)</span></span>


</dt> <dd>

<span data-ttu-id="cdd53-119">Aktualisieren Sie die Link Informationen nicht.</span><span class="sxs-lookup"><span data-stu-id="cdd53-119">Do not update the link information.</span></span>

</dd> <dt>



 <span data-ttu-id="cdd53-120">(16)</span><span class="sxs-lookup"><span data-stu-id="cdd53-120">(16)</span></span>


</dt> <dd>

<span data-ttu-id="cdd53-121">Führen Sie die Suchheuristik nicht aus.</span><span class="sxs-lookup"><span data-stu-id="cdd53-121">Do not execute the search heuristics.</span></span>

</dd> <dt>



 <span data-ttu-id="cdd53-122">(32)</span><span class="sxs-lookup"><span data-stu-id="cdd53-122">(32)</span></span>


</dt> <dd>

<span data-ttu-id="cdd53-123">Verwenden Sie die Nachverfolgung verteilter Links nicht.</span><span class="sxs-lookup"><span data-stu-id="cdd53-123">Do not use distributed link tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="cdd53-124">(64)</span><span class="sxs-lookup"><span data-stu-id="cdd53-124">(64)</span></span>


</dt> <dd>

<span data-ttu-id="cdd53-125">Deaktivieren Sie die Überwachung verteilter Links.</span><span class="sxs-lookup"><span data-stu-id="cdd53-125">Disable distributed link tracking.</span></span> <span data-ttu-id="cdd53-126">Standardmäßig verfolgt die verteilte Link Verfolgung Wechselmedien auf der Grundlage des Volumenamens auf mehrere Geräte.</span><span class="sxs-lookup"><span data-stu-id="cdd53-126">By default, distributed link tracking tracks removable media across multiple devices based on the volume name.</span></span> <span data-ttu-id="cdd53-127">Außerdem wird der UNC-Pfad verwendet, um Remote Dateisysteme zu verfolgen, deren Laufwerk Buchstabe geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="cdd53-127">It also uses the UNC path to track remote file systems whose drive letter has changed.</span></span> <span data-ttu-id="cdd53-128">Wenn Sie dieses Flag festlegen, werden beide Arten der Nachverfolgung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="cdd53-128">Setting this flag disables both types of tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="cdd53-129">(128)</span><span class="sxs-lookup"><span data-stu-id="cdd53-129">(128)</span></span>


</dt> <dd>

<span data-ttu-id="cdd53-130">Nennen Sie die Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cdd53-130">Call the Windows Installer.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdd53-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdd53-131">Remarks</span></span>

<span data-ttu-id="cdd53-132">Diese Methode ist im Grunde identisch [**mit den zu**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve)lösenden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="cdd53-132">This method is essentially identical in functionality to [**Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span></span> <span data-ttu-id="cdd53-133">Weitere Informationen zur Link Auflösung finden Sie im Abschnitt "Hinweise" auf dieser Seite.</span><span class="sxs-lookup"><span data-stu-id="cdd53-133">For further discussion of link resolution, see the Remarks section of that page.</span></span>

## <a name="examples"></a><span data-ttu-id="cdd53-134">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdd53-134">Examples</span></span>

<span data-ttu-id="cdd53-135">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cdd53-135">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cdd53-136">JScript</span><span class="sxs-lookup"><span data-stu-id="cdd53-136">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
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
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="cdd53-137">VBScript</span><span class="sxs-lookup"><span data-stu-id="cdd53-137">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
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
                                objShellLink.Resolve(1)
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



<span data-ttu-id="cdd53-138">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cdd53-138">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectResolveVB()
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
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cdd53-139">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cdd53-139">Requirements</span></span>



| <span data-ttu-id="cdd53-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdd53-140">Requirement</span></span> | <span data-ttu-id="cdd53-141">Wert</span><span class="sxs-lookup"><span data-stu-id="cdd53-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd53-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdd53-142">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd53-143">Nur Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdd53-143">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cdd53-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdd53-144">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd53-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdd53-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cdd53-146">Header</span><span class="sxs-lookup"><span data-stu-id="cdd53-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdd53-147"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdd53-147"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cdd53-148">IDL</span><span class="sxs-lookup"><span data-stu-id="cdd53-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cdd53-149"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cdd53-149"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cdd53-150">DLL</span><span class="sxs-lookup"><span data-stu-id="cdd53-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdd53-151"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="cdd53-151"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
