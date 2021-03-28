---
description: Führt ein Verb für das Element aus.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: FolderItem. invokeverb-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 259ff9613756940d5da8a37585dbf39fb2dc0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524480"
---
# <a name="folderiteminvokeverb-method"></a><span data-ttu-id="99806-103">FolderItem. invokeverb-Methode</span><span class="sxs-lookup"><span data-stu-id="99806-103">FolderItem.InvokeVerb method</span></span>

<span data-ttu-id="99806-104">Führt ein Verb für das Element aus.</span><span class="sxs-lookup"><span data-stu-id="99806-104">Executes a verb on the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="99806-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99806-105">Syntax</span></span>


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a><span data-ttu-id="99806-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99806-107">*vverb* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="99806-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="99806-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="99806-108">Type: **Variant**</span></span>

<span data-ttu-id="99806-109">Eine Zeichenfolge, die das auszuführende Verb angibt.</span><span class="sxs-lookup"><span data-stu-id="99806-109">A string that specifies the verb to be executed.</span></span> <span data-ttu-id="99806-110">Dabei muss es sich um einen der Werte handeln, die von der [**FolderItemVerb.Name**](folderitemverb-name.md) -Eigenschaft des Elements zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="99806-110">It must be one of the values returned by the item's [**FolderItemVerb.Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="99806-111">Wenn kein Verb angegeben ist, wird das Standardverb aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="99806-111">If no verb is specified, the default verb will be invoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99806-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99806-112">Return value</span></span>

<span data-ttu-id="99806-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="99806-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99806-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99806-114">Remarks</span></span>

<span data-ttu-id="99806-115">Ein Verb ist eine Zeichenfolge, die verwendet wird, um eine bestimmte Aktion anzugeben, die ein Element unterstützt.</span><span class="sxs-lookup"><span data-stu-id="99806-115">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="99806-116">Das Aufrufen eines Verbs entspricht dem Auswählen eines Befehls aus dem Kontextmenü eines Elements.</span><span class="sxs-lookup"><span data-stu-id="99806-116">Invoking a verb is equivalent to selecting a command from an item's shortcut menu.</span></span> <span data-ttu-id="99806-117">Wenn Sie ein Verb aufrufen, wird in der Regel eine verwandte Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="99806-117">Typically, invoking a verb launches a related application.</span></span> <span data-ttu-id="99806-118">Wenn Sie z. b. das "Öffnen"-Verb in einer txt-Datei aufrufen, wird die Datei mit einem Text-Editor geöffnet, normalerweise Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="99806-118">For example, invoking the "open" verb on a .txt file opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="99806-119">Weitere Erläuterungen zu Verben finden Sie unter [Starten von Anwendungen](launch.md) .</span><span class="sxs-lookup"><span data-stu-id="99806-119">See [Launching Applications](launch.md) for further discussion of verbs.</span></span>

<span data-ttu-id="99806-120">Das [**folderitemverbs**](folderitemverbs.md) -Objekt stellt die Auflistung der Verben dar, die dem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="99806-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="99806-121">Das Standardverb kann für unterschiedliche Elemente variieren, aber es ist in der Regel "geöffnet".</span><span class="sxs-lookup"><span data-stu-id="99806-121">The default verb may vary for different items, but it is typically "open".</span></span>

## <a name="examples"></a><span data-ttu-id="99806-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99806-122">Examples</span></span>

<span data-ttu-id="99806-123">Im folgenden Beispiel wird **invokeverb** verwendet, um das Standard Verb (in diesem Fall "Öffnen") im Windows-Ordner aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="99806-123">The following example uses **InvokeVerb** to invoke the default verb ("open" in this case) on the Windows folder.</span></span> <span data-ttu-id="99806-124">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="99806-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="99806-125">JScript</span><span class="sxs-lookup"><span data-stu-id="99806-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



<span data-ttu-id="99806-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="99806-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
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
                    dim szReturn
                                
                    objFolderItem.InvokeVerb()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="99806-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="99806-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
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



## <a name="requirements"></a><span data-ttu-id="99806-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="99806-128">Requirements</span></span>



| <span data-ttu-id="99806-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99806-129">Requirement</span></span> | <span data-ttu-id="99806-130">Wert</span><span class="sxs-lookup"><span data-stu-id="99806-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99806-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99806-131">Minimum supported client</span></span><br/> | <span data-ttu-id="99806-132">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99806-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="99806-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99806-133">Minimum supported server</span></span><br/> | <span data-ttu-id="99806-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99806-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="99806-135">Header</span><span class="sxs-lookup"><span data-stu-id="99806-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="99806-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="99806-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="99806-137">IDL</span><span class="sxs-lookup"><span data-stu-id="99806-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99806-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="99806-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="99806-139">DLL</span><span class="sxs-lookup"><span data-stu-id="99806-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99806-140"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="99806-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99806-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="99806-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99806-142">**Von folderItem**</span><span class="sxs-lookup"><span data-stu-id="99806-142">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="99806-143">**Verben**</span><span class="sxs-lookup"><span data-stu-id="99806-143">**Verbs**</span></span>](folderitem-verbs.md)
</dt> <dt>

[<span data-ttu-id="99806-144">**Doit**</span><span class="sxs-lookup"><span data-stu-id="99806-144">**DoIt**</span></span>](folderitemverb-doit.md)
</dt> </dl>

 

 




