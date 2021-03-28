---
description: Erstellt ein Dialogfeld, das dem Benutzer ermöglicht, einen Ordner auszuwählen, und gibt dann das Ordner Objekt des ausgewählten Ordners zurück.
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: Ishelldispatch. browsforfolder-Methode (Shldisp. h)
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
ms.openlocfilehash: 4e603bb08b4b98ba4008aa4ea162c9b59e5d42da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130101"
---
# <a name="ishelldispatchbrowseforfolder-method"></a><span data-ttu-id="4c557-103">Ishelldispatch. browsforfolder-Methode</span><span class="sxs-lookup"><span data-stu-id="4c557-103">IShellDispatch.BrowseForFolder method</span></span>

<span data-ttu-id="4c557-104">Erstellt ein Dialogfeld, das dem Benutzer ermöglicht, einen Ordner auszuwählen, und gibt dann das [**Ordner**](folder.md) Objekt des ausgewählten Ordners zurück.</span><span class="sxs-lookup"><span data-stu-id="4c557-104">Creates a dialog box that enables the user to select a folder and then returns the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c557-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c557-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="4c557-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c557-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c557-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c557-107">*Hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c557-108">Type: **Integer**</span><span class="sxs-lookup"><span data-stu-id="4c557-108">Type: **Integer**</span></span>

<span data-ttu-id="4c557-109">Das Handle für das übergeordnete Fenster des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="4c557-109">The handle to the parent window of the dialog box.</span></span> <span data-ttu-id="4c557-110">Dieser Wert kann auch 0 sein.</span><span class="sxs-lookup"><span data-stu-id="4c557-110">This value can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4c557-111">*stitle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c557-111">*sTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c557-112">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4c557-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4c557-113">Ein **Zeichen** folgen Wert, der den Titel darstellt, der im Dialogfeld **Durchsuchen** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4c557-113">A **String** value that represents the title displayed inside the **Browse** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4c557-114">*ioptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c557-114">*iOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c557-115">Type: **Integer**</span><span class="sxs-lookup"><span data-stu-id="4c557-115">Type: **Integer**</span></span>

<span data-ttu-id="4c557-116">Ein **ganzzahliger** Wert, der die Optionen für die Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="4c557-116">An **Integer** value that contains the options for the method.</span></span> <span data-ttu-id="4c557-117">Dies kann 0 (null) sein oder eine Kombination der Werte sein, die unter dem **ulflags** -Member der [**Browseinfo**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) -Struktur aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4c557-117">This can be zero or a combination of the values listed under the **ulFlags** member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4c557-118">*vrootfolder* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="4c557-118">*vRootFolder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c557-119">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4c557-119">Type: **Variant**</span></span>

<span data-ttu-id="4c557-120">Der Stamm Ordner, der im Dialogfeld verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c557-120">The root folder to use in the dialog box.</span></span> <span data-ttu-id="4c557-121">Der Benutzer kann nicht in der Struktur nach oben navigieren als in diesem Ordner.</span><span class="sxs-lookup"><span data-stu-id="4c557-121">The user cannot browse higher in the tree than this folder.</span></span> <span data-ttu-id="4c557-122">Wenn dieser Wert nicht angegeben wird, ist der Stamm Ordner, der im Dialogfeld verwendet wird, der Desktop.</span><span class="sxs-lookup"><span data-stu-id="4c557-122">If this value is not specified, the root folder used in the dialog box is the desktop.</span></span> <span data-ttu-id="4c557-123">Bei diesem Wert kann es sich um eine Zeichenfolge handeln, die den Pfad des Ordners oder einen der [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) -Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="4c557-123">This value can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="4c557-124">Beachten Sie, dass die in **shellspecialfolderconstants** gefundenen Konstanten Namen in Visual Basic verfügbar sind, jedoch nicht in VBScript oder JScript.</span><span class="sxs-lookup"><span data-stu-id="4c557-124">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="4c557-125">In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c557-125">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c557-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c557-126">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="4c557-127">JScript</span><span class="sxs-lookup"><span data-stu-id="4c557-127">JScript</span></span>

<span data-ttu-id="4c557-128">Typ: **Ordner \* \***</span><span class="sxs-lookup"><span data-stu-id="4c557-128">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="4c557-129">Ein Objekt Verweis auf das [**Ordner**](folder.md) Objekt des ausgewählten Ordners.</span><span class="sxs-lookup"><span data-stu-id="4c557-129">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="4c557-130">VB</span><span class="sxs-lookup"><span data-stu-id="4c557-130">VB</span></span>

<span data-ttu-id="4c557-131">Typ: **Ordner \* \***</span><span class="sxs-lookup"><span data-stu-id="4c557-131">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="4c557-132">Ein Objekt Verweis auf das [**Ordner**](folder.md) Objekt des ausgewählten Ordners.</span><span class="sxs-lookup"><span data-stu-id="4c557-132">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c557-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c557-133">Remarks</span></span>

<span data-ttu-id="4c557-134">Diese Methode wird implementiert und über die [**Shell. browsforfolder**](shell-browseforfolder.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4c557-134">This method is implemented and accessed through the [**Shell.BrowseForFolder**](shell-browseforfolder.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="4c557-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c557-135">Examples</span></span>

<span data-ttu-id="4c557-136">In den folgenden Beispielen wird **browsforfolder** verwendet, um ein Durchsuchen-Fenster mit dem Titel "example" im Windows-Ordner anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4c557-136">The following examples use **BrowseForFolder** to display a browse window titled "Example" rooted at the Windows folder.</span></span> <span data-ttu-id="4c557-137">Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c557-137">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4c557-138">JScript</span><span class="sxs-lookup"><span data-stu-id="4c557-138">JScript:</span></span>


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



<span data-ttu-id="4c557-139">VBScript</span><span class="sxs-lookup"><span data-stu-id="4c557-139">VBScript:</span></span>


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



<span data-ttu-id="4c557-140">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4c557-140">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4c557-141">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4c557-141">Requirements</span></span>



| <span data-ttu-id="4c557-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c557-142">Requirement</span></span> | <span data-ttu-id="4c557-143">Wert</span><span class="sxs-lookup"><span data-stu-id="4c557-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c557-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c557-144">Minimum supported client</span></span><br/> | <span data-ttu-id="4c557-145">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c557-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4c557-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c557-146">Minimum supported server</span></span><br/> | <span data-ttu-id="4c557-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c557-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4c557-148">Header</span><span class="sxs-lookup"><span data-stu-id="4c557-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c557-149"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c557-149"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4c557-150">IDL</span><span class="sxs-lookup"><span data-stu-id="4c557-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c557-151"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c557-151"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4c557-152">DLL</span><span class="sxs-lookup"><span data-stu-id="4c557-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c557-153"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="4c557-153"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
