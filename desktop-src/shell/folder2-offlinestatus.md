---
description: Enthält den Offline Status des Ordners.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Folder2. Offlinestatus-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977072"
---
# <a name="folder2offlinestatus-property"></a><span data-ttu-id="a84db-103">Folder2. Offlinestatus (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a84db-103">Folder2.OfflineStatus property</span></span>

<span data-ttu-id="a84db-104">Enthält den Offline Status des Ordners.</span><span class="sxs-lookup"><span data-stu-id="a84db-104">Contains the offline status of the folder.</span></span>

<span data-ttu-id="a84db-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a84db-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a84db-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a84db-106">Syntax</span></span>


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a><span data-ttu-id="a84db-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a84db-107">Property value</span></span>

<span data-ttu-id="a84db-108">Eine **ganze** Zahl, die auf einen der folgenden Werte festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a84db-108">An **Integer** that is set to one of the following values.</span></span>

<dt>



 <span data-ttu-id="a84db-109">(OFS \_ ) Dirtycache)</span><span class="sxs-lookup"><span data-stu-id="a84db-109">(OFS\_DIRTYCACHE)</span></span>


</dt> <dd>

<span data-ttu-id="a84db-110">Der Server ist mit nicht synchronisierten Änderungen online.</span><span class="sxs-lookup"><span data-stu-id="a84db-110">Server is online with unsynchronized changes.</span></span>

</dd> <dt>



 <span data-ttu-id="a84db-111">(OFS \_ ) VSTE</span><span class="sxs-lookup"><span data-stu-id="a84db-111">(OFS\_INACTIVE)</span></span>


</dt> <dd>

<span data-ttu-id="a84db-112">Das Offline Caching ist für diesen Ordner nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a84db-112">Offline caching is not enabled for this folder.</span></span>

</dd> <dt>



 <span data-ttu-id="a84db-113">(OFS \_ ) Aufzu</span><span class="sxs-lookup"><span data-stu-id="a84db-113">(OFS\_OFFLINE)</span></span>


</dt> <dd>

<span data-ttu-id="a84db-114">Der Server ist offline.</span><span class="sxs-lookup"><span data-stu-id="a84db-114">Server is offline.</span></span>

</dd> <dt>



 <span data-ttu-id="a84db-115">(OFS \_ ) Internet</span><span class="sxs-lookup"><span data-stu-id="a84db-115">(OFS\_ONLINE)</span></span>


</dt> <dd>

<span data-ttu-id="a84db-116">Der Server ist online.</span><span class="sxs-lookup"><span data-stu-id="a84db-116">Server is online.</span></span>

</dd> <dt>



 <span data-ttu-id="a84db-117">(OFS \_ ) Serverback)</span><span class="sxs-lookup"><span data-stu-id="a84db-117">(OFS\_SERVERBACK)</span></span>


</dt> <dd>

<span data-ttu-id="a84db-118">Der Server ist offline, kann aber erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="a84db-118">Server is offline but can be reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a84db-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a84db-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a84db-120">Offlinedateien müssen durch Ordneroptionen aktiviert werden, damit **Offlinestatus** ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a84db-120">Offline Files must be enabled through Folder Options for **OfflineStatus** to work correctly.</span></span> <span data-ttu-id="a84db-121">Wenn die Offlinedateien-Option nicht aktiviert ist, gibt die-Eigenschaft **OFS \_ inaktiv** zurück.</span><span class="sxs-lookup"><span data-stu-id="a84db-121">If the Offline Files option is not enabled, the property returns **OFS\_INACTIVE**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a84db-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a84db-122">Examples</span></span>

<span data-ttu-id="a84db-123">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung von **Offlinestatus** für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a84db-123">The following example shows the proper use of **OfflineStatus** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a84db-124">JScript</span><span class="sxs-lookup"><span data-stu-id="a84db-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



<span data-ttu-id="a84db-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="a84db-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="a84db-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a84db-126">Visual Basic:</span></span>


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a84db-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a84db-127">Requirements</span></span>



| <span data-ttu-id="a84db-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a84db-128">Requirement</span></span> | <span data-ttu-id="a84db-129">Wert</span><span class="sxs-lookup"><span data-stu-id="a84db-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a84db-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a84db-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a84db-131">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a84db-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a84db-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a84db-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a84db-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a84db-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a84db-134">Header</span><span class="sxs-lookup"><span data-stu-id="a84db-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a84db-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a84db-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a84db-136">IDL</span><span class="sxs-lookup"><span data-stu-id="a84db-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a84db-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a84db-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a84db-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a84db-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a84db-139"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a84db-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a84db-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a84db-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a84db-141">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="a84db-141">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="a84db-142">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="a84db-142">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




