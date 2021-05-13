---
description: Kopiert ein Element oder Elemente in einen Ordner.
title: Folder.CopyHere-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: 1466e5d01715c0c820cbc7cd9809c51e4963ec56
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842141"
---
# <a name="foldercopyhere-method"></a><span data-ttu-id="17d15-103">Folder.CopyHere-Methode</span><span class="sxs-lookup"><span data-stu-id="17d15-103">Folder.CopyHere method</span></span>

<span data-ttu-id="17d15-104">Kopiert ein Element oder Elemente in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="17d15-104">Copies an item or items to a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d15-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17d15-105">Syntax</span></span>


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="17d15-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17d15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17d15-107">*vItem*</span><span class="sxs-lookup"><span data-stu-id="17d15-107">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="17d15-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="17d15-108">Type: **Variant**</span></span>

<span data-ttu-id="17d15-109">Das zu kopierende Element oder die zu kopierende Elemente.</span><span class="sxs-lookup"><span data-stu-id="17d15-109">The item or items to copy.</span></span> <span data-ttu-id="17d15-110">Dies kann eine Zeichenfolge sein, die einen Dateinamen, ein [**FolderItem-Objekt**](folderitem.md) oder ein [**FolderItems-Objekt**](folderitems.md) darstellt.</span><span class="sxs-lookup"><span data-stu-id="17d15-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="17d15-111">*vOptions* \[ Optional\]</span><span class="sxs-lookup"><span data-stu-id="17d15-111">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="17d15-112">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="17d15-112">Type: **Variant**</span></span>

<span data-ttu-id="17d15-113">Optionen für den Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="17d15-113">Options for the copy operation.</span></span> <span data-ttu-id="17d15-114">Dieser Wert kann 0 (null) oder eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="17d15-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="17d15-115">Diese Werte basieren auf Flags, die für die Verwendung mit dem **fFlags-Member** der [**C++-SHFILEOPSTRUCT-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) definiert sind.</span><span class="sxs-lookup"><span data-stu-id="17d15-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="17d15-116">Jeder Shellnamespace muss eine eigene Implementierung dieser Flags bereitstellen, und jeder Namespace kann einige oder sogar alle dieser Flags ignorieren.</span><span class="sxs-lookup"><span data-stu-id="17d15-116">Each Shell namespace must provide its own implementation of these flags, and each namespace can choose to ignore some or even all of these flags.</span></span> <span data-ttu-id="17d15-117">Diese Flags werden nicht anhand des Namens für Visual Basic, VBScript oder JScript definiert. Daher müssen Sie sie selbst definieren oder ihre numerischen Entsprechungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="17d15-117">These flags are not defined by name for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

> [!Note]  
> <span data-ttu-id="17d15-118">In einigen Fällen, z. B. komprimierten Dateien (ZIP-Dateien), werden einige Optionsflags möglicherweise entwurfsweise ignoriert.</span><span class="sxs-lookup"><span data-stu-id="17d15-118">In some cases, such as compressed (.zip) files, some option flags may be ignored by design.</span></span>

 

<dt>



 <span data-ttu-id="17d15-119">(4)</span><span class="sxs-lookup"><span data-stu-id="17d15-119">(4)</span></span>


</dt> <dd>

<span data-ttu-id="17d15-120">Zeigen Sie kein Statusdialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="17d15-120">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="17d15-121">(8)</span><span class="sxs-lookup"><span data-stu-id="17d15-121">(8)</span></span>


</dt> <dd>

<span data-ttu-id="17d15-122">Geben Sie der Datei, die mit einem neuen Namen betrieben wird, einen Verschiebungs-, Kopier- oder Umbenennungsvorgang, wenn bereits eine Datei mit dem Zielnamen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="17d15-122">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="17d15-123">(16)</span><span class="sxs-lookup"><span data-stu-id="17d15-123">(16)</span></span>


</dt> <dd>

<span data-ttu-id="17d15-124">Antworten Sie für alle angezeigten Dialogfelder mit "Ja zu allen".</span><span class="sxs-lookup"><span data-stu-id="17d15-124">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="17d15-125">(64)</span><span class="sxs-lookup"><span data-stu-id="17d15-125">(64)</span></span>


</dt> <dd>

<span data-ttu-id="17d15-126">Behalten Sie nach Möglichkeit rückgängige Informationen bei.</span><span class="sxs-lookup"><span data-stu-id="17d15-126">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="17d15-127">(128)</span><span class="sxs-lookup"><span data-stu-id="17d15-127">(128)</span></span>


</dt> <dd>

<span data-ttu-id="17d15-128">Führen Sie den Vorgang für Dateien nur aus, wenn ein Platzhalterdateiname ( \* . \* ) angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="17d15-128">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="17d15-129">(256)</span><span class="sxs-lookup"><span data-stu-id="17d15-129">(256)</span></span>


</dt> <dd>

<span data-ttu-id="17d15-130">Zeigt ein Statusdialogfeld an, zeigt jedoch nicht die Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="17d15-130">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="17d15-131">(512)</span><span class="sxs-lookup"><span data-stu-id="17d15-131">(512)</span></span>


</dt> <dd>

<span data-ttu-id="17d15-132">Bestätigen Sie die Erstellung eines neuen Verzeichnisses nicht, wenn für den Vorgang ein Verzeichnis erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="17d15-132">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="17d15-133">(1024)</span><span class="sxs-lookup"><span data-stu-id="17d15-133">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="17d15-134">Zeigen Sie keine Benutzeroberfläche an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="17d15-134">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="17d15-135">(2048)</span><span class="sxs-lookup"><span data-stu-id="17d15-135">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="17d15-136">Version 4.71.</span><span class="sxs-lookup"><span data-stu-id="17d15-136">Version 4.71.</span></span>](versions.md) <span data-ttu-id="17d15-137">Kopieren Sie nicht die Sicherheitsattribute der Datei.</span><span class="sxs-lookup"><span data-stu-id="17d15-137">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="17d15-138">(4096)</span><span class="sxs-lookup"><span data-stu-id="17d15-138">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="17d15-139">Wird nur im lokalen Verzeichnis verwendet.</span><span class="sxs-lookup"><span data-stu-id="17d15-139">Only operate in the local directory.</span></span> <span data-ttu-id="17d15-140">Arbeiten Sie nicht rekursiv in Unterverzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="17d15-140">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="17d15-141">(8192)</span><span class="sxs-lookup"><span data-stu-id="17d15-141">(8192)</span></span>


</dt> <dd>

[<span data-ttu-id="17d15-142">Version 5.0.</span><span class="sxs-lookup"><span data-stu-id="17d15-142">Version 5.0.</span></span>](versions.md) <span data-ttu-id="17d15-143">Kopieren Sie verbundene Dateien nicht als Gruppe.</span><span class="sxs-lookup"><span data-stu-id="17d15-143">Do not copy connected files as a group.</span></span> <span data-ttu-id="17d15-144">Kopieren Sie nur die angegebenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="17d15-144">Only copy the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17d15-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17d15-145">Return value</span></span>

<span data-ttu-id="17d15-146">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="17d15-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17d15-147">Hinweise</span><span class="sxs-lookup"><span data-stu-id="17d15-147">Remarks</span></span>

<span data-ttu-id="17d15-148">Das aufrufende Programm erhält keine Benachrichtigung, um anzugeben, dass die Kopie abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="17d15-148">No notification is given to the calling program to indicate that the copy has completed.</span></span>

> [!Note]  
> <span data-ttu-id="17d15-149">Nicht alle Methoden werden für alle Ordner implementiert.</span><span class="sxs-lookup"><span data-stu-id="17d15-149">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="17d15-150">Beispielsweise wird die [**ParseName-Methode**](folder-parsename.md) nicht für den ordner Systemsteuerung (CSIDL \_ CONTROLS) implementiert.</span><span class="sxs-lookup"><span data-stu-id="17d15-150">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="17d15-151">Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800A01BD (Dezimalzahl 445) ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="17d15-151">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="17d15-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17d15-152">Examples</span></span>

<span data-ttu-id="17d15-153">Im folgenden Beispiel wird **CopyHere** verwendet, um die Autoexec.bat-Datei aus dem Stammverzeichnis in das Verzeichnis C: Windows zu \\ kopieren.</span><span class="sxs-lookup"><span data-stu-id="17d15-153">The following example uses **CopyHere** to copy the Autoexec.bat file from the root directory to the C:\\Windows directory.</span></span> <span data-ttu-id="17d15-154">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17d15-154">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="17d15-155">Jscript:</span><span class="sxs-lookup"><span data-stu-id="17d15-155">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



<span data-ttu-id="17d15-156">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="17d15-156">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



<span data-ttu-id="17d15-157">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="17d15-157">Visual Basic:</span></span>


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="17d15-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17d15-158">Requirements</span></span>



| <span data-ttu-id="17d15-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17d15-159">Requirement</span></span> | <span data-ttu-id="17d15-160">Wert</span><span class="sxs-lookup"><span data-stu-id="17d15-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17d15-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17d15-161">Minimum supported client</span></span><br/> | <span data-ttu-id="17d15-162">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17d15-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="17d15-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17d15-163">Minimum supported server</span></span><br/> | <span data-ttu-id="17d15-164">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17d15-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="17d15-165">Header</span><span class="sxs-lookup"><span data-stu-id="17d15-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="17d15-166"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="17d15-166"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="17d15-167">Idl</span><span class="sxs-lookup"><span data-stu-id="17d15-167">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17d15-168"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="17d15-168"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="17d15-169">DLL</span><span class="sxs-lookup"><span data-stu-id="17d15-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17d15-170"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="17d15-170"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17d15-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17d15-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d15-172">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="17d15-172">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




