---
description: Führt ein Verb für ein shellelement aus.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Shellfolderitem. invokeverbex-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978160"
---
# <a name="shellfolderiteminvokeverbex-method"></a><span data-ttu-id="88037-103">Shellfolderitem. invokeverbex-Methode</span><span class="sxs-lookup"><span data-stu-id="88037-103">ShellFolderItem.InvokeVerbEx method</span></span>

<span data-ttu-id="88037-104">Führt ein Verb für ein shellelement aus.</span><span class="sxs-lookup"><span data-stu-id="88037-104">Executes a verb on a Shell item.</span></span>

## <a name="syntax"></a><span data-ttu-id="88037-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88037-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="88037-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="88037-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88037-107">*vverb* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="88037-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88037-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="88037-108">Type: **Variant**</span></span>

<span data-ttu-id="88037-109">Eine **Variante** , die die Verb Zeichenfolge enthält, die dem auszuführenden Befehl entspricht.</span><span class="sxs-lookup"><span data-stu-id="88037-109">A **Variant** that contains the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="88037-110">Dabei muss es sich um einen der Werte handeln, die von der [**Name**](folderitemverb-name.md) -Eigenschaft des Elements zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="88037-110">It must be one of the values returned by the item's [**Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="88037-111">Wenn kein Verb angegeben ist, wird das Standardverb ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88037-111">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="88037-112">*vArgs* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="88037-112">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88037-113">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="88037-113">Type: **Variant**</span></span>

<span data-ttu-id="88037-114">Eine **Variante** , die aus einer Zeichenfolge mit einem oder mehreren Argumenten für den von *vverb* angegebenen Befehl besteht.</span><span class="sxs-lookup"><span data-stu-id="88037-114">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="88037-115">Das Format dieser Zeichenfolge hängt von dem jeweiligen Verb ab.</span><span class="sxs-lookup"><span data-stu-id="88037-115">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88037-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88037-116">Remarks</span></span>

<span data-ttu-id="88037-117">Ein Verb ist eine Zeichenfolge, die verwendet wird, um eine bestimmte Aktion anzugeben, die ein Element unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88037-117">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="88037-118">Wenn Sie ein Verb aufrufen, wird in der Regel eine verwandte Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="88037-118">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="88037-119">Wenn Sie z. b. das **geöffnete** Verb in einer txt-Datei aufrufen, wird die Datei normalerweise mit einem Text-Editor geöffnet, in der Regel Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="88037-119">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="88037-120">Das [**folderitemverbs**](folderitemverbs.md) -Objekt stellt die Auflistung der Verben dar, die dem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="88037-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="88037-121">Weitere Erläuterungen zu Verben finden Sie unter [Starten von Anwendungen](launch.md).</span><span class="sxs-lookup"><span data-stu-id="88037-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

<span data-ttu-id="88037-122">Diese Methode ähnelt [**invokeverb**](folderitem-invokeverb.md), aber Sie ermöglicht Ihnen, Argumente für den Befehl und den Befehl selbst anzugeben.</span><span class="sxs-lookup"><span data-stu-id="88037-122">This method is similar to [**InvokeVerb**](folderitem-invokeverb.md), but it allows you to specify arguments to the command as well as the command itself.</span></span>

## <a name="examples"></a><span data-ttu-id="88037-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88037-123">Examples</span></span>

<span data-ttu-id="88037-124">Die folgenden Beispiele zeigen die ordnungsgemäße Verwendung dieser Methode in JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="88037-124">The following examples show the proper use of this method in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="88037-125">JScript</span><span class="sxs-lookup"><span data-stu-id="88037-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
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
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



<span data-ttu-id="88037-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="88037-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="88037-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="88037-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="88037-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="88037-128">Requirements</span></span>



| <span data-ttu-id="88037-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88037-129">Requirement</span></span> | <span data-ttu-id="88037-130">Wert</span><span class="sxs-lookup"><span data-stu-id="88037-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88037-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88037-131">Minimum supported client</span></span><br/> | <span data-ttu-id="88037-132">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88037-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88037-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88037-133">Minimum supported server</span></span><br/> | <span data-ttu-id="88037-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88037-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="88037-135">Header</span><span class="sxs-lookup"><span data-stu-id="88037-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="88037-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="88037-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="88037-137">IDL</span><span class="sxs-lookup"><span data-stu-id="88037-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="88037-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="88037-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="88037-139">DLL</span><span class="sxs-lookup"><span data-stu-id="88037-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88037-140"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="88037-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88037-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="88037-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88037-142">**Shellfolderitem**</span><span class="sxs-lookup"><span data-stu-id="88037-142">**ShellFolderItem**</span></span>](shellfolderitem-object.md)
</dt> <dt>

[<span data-ttu-id="88037-143">**Invokeverb**</span><span class="sxs-lookup"><span data-stu-id="88037-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




