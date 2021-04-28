---
description: 'IShellDispatch.BrowseForFolder-Methode: Erstellt ein Dialogfeld, in dem der Benutzer einen Ordner auswählen und dann das Ordnerobjekt des ausgewählten Ordners zurückgibt.'
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: IShellDispatch.BrowseForFolder-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ee6202c7029e2c27684e15d96dd6c38680cb0678
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086688"
---
# <a name="ishelldispatchbrowseforfolder-method"></a><span data-ttu-id="aa5ee-103">IShellDispatch.BrowseForFolder-Methode</span><span class="sxs-lookup"><span data-stu-id="aa5ee-103">IShellDispatch.BrowseForFolder method</span></span>

<span data-ttu-id="aa5ee-104">Erstellt ein Dialogfeld, in dem der Benutzer einen Ordner auswählen und dann das Ordnerobjekt des ausgewählten [**Ordners zurückgibt.**](folder.md)</span><span class="sxs-lookup"><span data-stu-id="aa5ee-104">Creates a dialog box that enables the user to select a folder and then returns the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa5ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa5ee-105">Syntax</span></span>


```JScript
retVal = IShellDispatch.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

IShellDispatch.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a><span data-ttu-id="aa5ee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa5ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa5ee-107">*Hwnd* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aa5ee-107">*Hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa5ee-108">Typ: **Integer**</span><span class="sxs-lookup"><span data-stu-id="aa5ee-108">Type: **Integer**</span></span>

<span data-ttu-id="aa5ee-109">Das Handle für das übergeordnete Fenster des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-109">The handle to the parent window of the dialog box.</span></span> <span data-ttu-id="aa5ee-110">Dieser Wert kann auch 0 sein.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-110">This value can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="aa5ee-111">*sTitle* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aa5ee-111">*sTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa5ee-112">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="aa5ee-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="aa5ee-113">Ein **Zeichenfolgenwert,** der den im Dialogfeld Durchsuchen **angezeigten Titel** darstellt.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-113">A **String** value that represents the title displayed inside the **Browse** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="aa5ee-114">*iOptions* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aa5ee-114">*iOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa5ee-115">Typ: **Integer**</span><span class="sxs-lookup"><span data-stu-id="aa5ee-115">Type: **Integer**</span></span>

<span data-ttu-id="aa5ee-116">Ein **Ganzzahlwert,** der die Optionen für die Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-116">An **Integer** value that contains the options for the method.</span></span> <span data-ttu-id="aa5ee-117">Dies kann 0 (null) oder eine Kombination der Werte sein, die unter dem **ulFlags-Element** der [**BROWSEINFO-Struktur aufgeführt**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) sind.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-117">This can be zero or a combination of the values listed under the **ulFlags** member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aa5ee-118">*vRootFolder* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="aa5ee-118">*vRootFolder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aa5ee-119">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="aa5ee-119">Type: **Variant**</span></span>

<span data-ttu-id="aa5ee-120">Der Stammordner, der im Dialogfeld verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-120">The root folder to use in the dialog box.</span></span> <span data-ttu-id="aa5ee-121">Der Benutzer kann in der Struktur nicht höher als in diesem Ordner suchen.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-121">The user cannot browse higher in the tree than this folder.</span></span> <span data-ttu-id="aa5ee-122">Wenn dieser Wert nicht angegeben wird, ist der Stammordner, der im Dialogfeld verwendet wird, der Desktop.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-122">If this value is not specified, the root folder used in the dialog box is the desktop.</span></span> <span data-ttu-id="aa5ee-123">Dieser Wert kann eine Zeichenfolge sein, die den Pfad des Ordners oder einen der [**ShellSpecialFolderConstants-Werte angibt.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="aa5ee-123">This value can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="aa5ee-124">Beachten Sie, dass die konstanten Namen in **ShellSpecialFolderConstants** in Visual Basic, aber nicht in VBScript oder JScript verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-124">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="aa5ee-125">In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-125">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa5ee-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa5ee-126">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="aa5ee-127">JScript</span><span class="sxs-lookup"><span data-stu-id="aa5ee-127">JScript</span></span>

<span data-ttu-id="aa5ee-128">Typ: **\* \* FOLDER**</span><span class="sxs-lookup"><span data-stu-id="aa5ee-128">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="aa5ee-129">Ein Objektverweis auf das [**Folder-Objekt**](folder.md) des ausgewählten Ordners.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-129">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="aa5ee-130">VB</span><span class="sxs-lookup"><span data-stu-id="aa5ee-130">VB</span></span>

<span data-ttu-id="aa5ee-131">Typ: **\* \* FOLDER**</span><span class="sxs-lookup"><span data-stu-id="aa5ee-131">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="aa5ee-132">Ein Objektverweis auf das [**Folder-Objekt**](folder.md) des ausgewählten Ordners.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-132">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa5ee-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa5ee-133">Remarks</span></span>

<span data-ttu-id="aa5ee-134">Diese Methode wird implementiert und über die [**Shell.BrowseForFolder-Methode**](shell-browseforfolder.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-134">This method is implemented and accessed through the [**Shell.BrowseForFolder**](shell-browseforfolder.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="aa5ee-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa5ee-135">Examples</span></span>

<span data-ttu-id="aa5ee-136">In den folgenden Beispielen wird **BrowseForFolder** verwendet, um ein Suchfenster mit dem Titel "Beispiel" anzuzeigen, das sich im Windows-Ordner befindet.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-136">The following examples use **BrowseForFolder** to display a browse window titled "Example" rooted at the Windows folder.</span></span> <span data-ttu-id="aa5ee-137">Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa5ee-137">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="aa5ee-138">Jscript:</span><span class="sxs-lookup"><span data-stu-id="aa5ee-138">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



<span data-ttu-id="aa5ee-139">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="aa5ee-139">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="aa5ee-140">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="aa5ee-140">Visual Basic:</span></span>


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="aa5ee-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa5ee-141">Requirements</span></span>



| <span data-ttu-id="aa5ee-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa5ee-142">Requirement</span></span> | <span data-ttu-id="aa5ee-143">Wert</span><span class="sxs-lookup"><span data-stu-id="aa5ee-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa5ee-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa5ee-144">Minimum supported client</span></span><br/> | <span data-ttu-id="aa5ee-145">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa5ee-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="aa5ee-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa5ee-146">Minimum supported server</span></span><br/> | <span data-ttu-id="aa5ee-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa5ee-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aa5ee-148">Header</span><span class="sxs-lookup"><span data-stu-id="aa5ee-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa5ee-149"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="aa5ee-149"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="aa5ee-150">Idl</span><span class="sxs-lookup"><span data-stu-id="aa5ee-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aa5ee-151"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa5ee-151"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="aa5ee-152">DLL</span><span class="sxs-lookup"><span data-stu-id="aa5ee-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa5ee-153"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="aa5ee-153"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
