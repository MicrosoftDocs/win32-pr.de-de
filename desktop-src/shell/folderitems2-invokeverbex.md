---
description: Führt ein Verb für eine Auflistung von folderItem-Objekten aus. Bei dieser Methode handelt es sich um eine Erweiterung der invokeverb-Methode, die eine zusätzliche Steuerung des Vorgangs über einen Satz von Flags ermöglicht.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: FolderItems2. invokeverbex-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aa9b986b5cb76f14cc950f522e1e289224c17b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977016"
---
# <a name="folderitems2invokeverbex-method"></a><span data-ttu-id="be394-104">FolderItems2. invokeverbex-Methode</span><span class="sxs-lookup"><span data-stu-id="be394-104">FolderItems2.InvokeVerbEx method</span></span>

<span data-ttu-id="be394-105">Führt ein Verb für eine Auflistung von [**folderItem**](folderitem.md) -Objekten aus.</span><span class="sxs-lookup"><span data-stu-id="be394-105">Executes a verb on a collection of [**FolderItem**](folderitem.md) objects.</span></span> <span data-ttu-id="be394-106">Bei dieser Methode handelt es sich um eine Erweiterung der [**invokeverb**](folderitem-invokeverb.md) -Methode, die eine zusätzliche Steuerung des Vorgangs über einen Satz von Flags ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="be394-106">This method is an extension of the [**InvokeVerb**](folderitem-invokeverb.md) method, allowing additional control of the operation through a set of flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="be394-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="be394-107">Syntax</span></span>


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="be394-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="be394-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be394-109">*vverb* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="be394-109">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be394-110">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="be394-110">Type: **Variant**</span></span>

<span data-ttu-id="be394-111">Eine **Variante** mit der Verb Zeichenfolge, die dem auszuführenden Befehl entspricht.</span><span class="sxs-lookup"><span data-stu-id="be394-111">A **Variant** with the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="be394-112">Wenn kein Verb angegeben ist, wird das Standardverb ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be394-112">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="be394-113">*vArgs* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="be394-113">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be394-114">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="be394-114">Type: **Variant**</span></span>

<span data-ttu-id="be394-115">Eine **Variante** , die aus einer Zeichenfolge mit einem oder mehreren Argumenten für den von *vverb* angegebenen Befehl besteht.</span><span class="sxs-lookup"><span data-stu-id="be394-115">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="be394-116">Das Format dieser Zeichenfolge hängt von dem jeweiligen Verb ab.</span><span class="sxs-lookup"><span data-stu-id="be394-116">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be394-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be394-117">Remarks</span></span>

<span data-ttu-id="be394-118">Ein Verb ist eine Zeichenfolge, die verwendet wird, um eine bestimmte Aktion anzugeben, die einem Element oder einer Auflistung von Elementen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="be394-118">A verb is a string used to specify a particular action associated with an item or collection of items.</span></span> <span data-ttu-id="be394-119">Wenn Sie ein Verb aufrufen, wird in der Regel eine verwandte Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="be394-119">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="be394-120">Wenn Sie z. b. das **geöffnete** Verb in einer txt-Datei aufrufen, wird die Datei normalerweise mit einem Text-Editor geöffnet, in der Regel Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="be394-120">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="be394-121">Weitere Erläuterungen zu Verben finden Sie unter [Starten von Anwendungen](launch.md).</span><span class="sxs-lookup"><span data-stu-id="be394-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

## <a name="examples"></a><span data-ttu-id="be394-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be394-122">Examples</span></span>

<span data-ttu-id="be394-123">Im folgenden Beispiel wird **invokeverbex** verwendet, um das Standardverb ("Öffnen") auf **Arbeitsplatz** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="be394-123">The following example uses **InvokeVerbEx** to invoke the default verb ("open") on **My Computer**.</span></span> <span data-ttu-id="be394-124">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="be394-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="be394-125">JScript</span><span class="sxs-lookup"><span data-stu-id="be394-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



<span data-ttu-id="be394-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="be394-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="be394-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="be394-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="be394-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="be394-128">Requirements</span></span>



| <span data-ttu-id="be394-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be394-129">Requirement</span></span> | <span data-ttu-id="be394-130">Wert</span><span class="sxs-lookup"><span data-stu-id="be394-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be394-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be394-131">Minimum supported client</span></span><br/> | <span data-ttu-id="be394-132">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be394-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be394-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be394-133">Minimum supported server</span></span><br/> | <span data-ttu-id="be394-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be394-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="be394-135">Header</span><span class="sxs-lookup"><span data-stu-id="be394-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="be394-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="be394-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="be394-137">IDL</span><span class="sxs-lookup"><span data-stu-id="be394-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be394-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be394-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="be394-139">DLL</span><span class="sxs-lookup"><span data-stu-id="be394-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be394-140"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="be394-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be394-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="be394-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be394-142">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="be394-142">**FolderItems2**</span></span>](folderitems2-object.md)
</dt> <dt>

[<span data-ttu-id="be394-143">**Invokeverb**</span><span class="sxs-lookup"><span data-stu-id="be394-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




