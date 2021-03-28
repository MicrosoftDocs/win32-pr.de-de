---
description: Verschiebt ein Element oder Elemente in diesen Ordner.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Folder. muvehere-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749177"
---
# <a name="foldermovehere-method"></a><span data-ttu-id="777fe-103">Folder. muvehere-Methode</span><span class="sxs-lookup"><span data-stu-id="777fe-103">Folder.MoveHere method</span></span>

<span data-ttu-id="777fe-104">Verschiebt ein Element oder Elemente in diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="777fe-104">Moves an item or items to this folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="777fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="777fe-105">Syntax</span></span>


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="777fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="777fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="777fe-107">*vitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="777fe-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="777fe-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="777fe-108">Type: **Variant**</span></span>

<span data-ttu-id="777fe-109">Das Element oder die Elemente, die verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="777fe-109">The item or items to move.</span></span> <span data-ttu-id="777fe-110">Dabei kann es sich um eine Zeichenfolge handeln, die einen Dateinamen, ein [**folderItem**](folderitem.md) -Objekt oder ein [**folderitems**](folderitems.md) -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="777fe-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="777fe-111">*voptions* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="777fe-111">*vOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="777fe-112">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="777fe-112">Type: **Variant**</span></span>

<span data-ttu-id="777fe-113">Optionen für den Verschiebungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="777fe-113">Options for the move operation.</span></span> <span data-ttu-id="777fe-114">Dieser Wert kann 0 (null) oder eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="777fe-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="777fe-115">Diese Werte basieren auf Flags, die für die Verwendung mit dem **fFlags** -Member der C++ [**shfleopstruct**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) -Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="777fe-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="777fe-116">Diese Flags sind nicht für Visual Basic, VBScript oder JScript definiert, sodass Sie Sie selbst definieren oder deren numerische Entsprechungen verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="777fe-116">These flags are not defined as such for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

<dt>



 <span data-ttu-id="777fe-117">(4)</span><span class="sxs-lookup"><span data-stu-id="777fe-117">(4)</span></span>


</dt> <dd>

<span data-ttu-id="777fe-118">Zeigt kein Status Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="777fe-118">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="777fe-119">(8)</span><span class="sxs-lookup"><span data-stu-id="777fe-119">(8)</span></span>


</dt> <dd>

<span data-ttu-id="777fe-120">Übergeben Sie die Datei mit einem neuen Namen in einem Verschiebungs-, Kopier-oder Umbenennungs Vorgang, wenn bereits eine Datei mit dem Zielnamen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="777fe-120">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="777fe-121">(16)</span><span class="sxs-lookup"><span data-stu-id="777fe-121">(16)</span></span>


</dt> <dd>

<span data-ttu-id="777fe-122">Antworten Sie für jedes Dialogfeld, das angezeigt wird, mit "Ja, alle".</span><span class="sxs-lookup"><span data-stu-id="777fe-122">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="777fe-123">(64)</span><span class="sxs-lookup"><span data-stu-id="777fe-123">(64)</span></span>


</dt> <dd>

<span data-ttu-id="777fe-124">Behalten Sie die rückgängig-Informationen bei, sofern möglich.</span><span class="sxs-lookup"><span data-stu-id="777fe-124">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="777fe-125">(128)</span><span class="sxs-lookup"><span data-stu-id="777fe-125">(128)</span></span>


</dt> <dd>

<span data-ttu-id="777fe-126">Der Vorgang wird nur für Dateien durchgeführt, wenn ein Platzhalter Dateiname ( \* . \* ) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="777fe-126">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="777fe-127">(256)</span><span class="sxs-lookup"><span data-stu-id="777fe-127">(256)</span></span>


</dt> <dd>

<span data-ttu-id="777fe-128">Zeigt ein Status Dialogfeld an, aber die Dateinamen werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="777fe-128">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="777fe-129">(512)</span><span class="sxs-lookup"><span data-stu-id="777fe-129">(512)</span></span>


</dt> <dd>

<span data-ttu-id="777fe-130">Bestätigen Sie die Erstellung eines neuen Verzeichnisses nicht, wenn der Vorgang zum Erstellen eines neuen Verzeichnisses erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="777fe-130">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="777fe-131">(1024)</span><span class="sxs-lookup"><span data-stu-id="777fe-131">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="777fe-132">Wenn ein Fehler auftritt, wird keine Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="777fe-132">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="777fe-133">(2048)</span><span class="sxs-lookup"><span data-stu-id="777fe-133">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="777fe-134">Version 4,71.</span><span class="sxs-lookup"><span data-stu-id="777fe-134">Version 4.71.</span></span>](versions.md) <span data-ttu-id="777fe-135">Kopieren Sie die Sicherheits Attribute der Datei nicht.</span><span class="sxs-lookup"><span data-stu-id="777fe-135">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="777fe-136">(4096)</span><span class="sxs-lookup"><span data-stu-id="777fe-136">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="777fe-137">Nur im lokalen Verzeichnis ausführen.</span><span class="sxs-lookup"><span data-stu-id="777fe-137">Only operate in the local directory.</span></span> <span data-ttu-id="777fe-138">Arbeiten Sie nicht rekursiv in Unterverzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="777fe-138">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="777fe-139">(9182)</span><span class="sxs-lookup"><span data-stu-id="777fe-139">(9182)</span></span>


</dt> <dd>

[<span data-ttu-id="777fe-140">Version 5,0.</span><span class="sxs-lookup"><span data-stu-id="777fe-140">Version 5.0.</span></span>](versions.md) <span data-ttu-id="777fe-141">Verschieben Sie verbundene Dateien nicht als Gruppe.</span><span class="sxs-lookup"><span data-stu-id="777fe-141">Do not move connected files as a group.</span></span> <span data-ttu-id="777fe-142">Verschieben Sie nur die angegebenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="777fe-142">Only move the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="777fe-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="777fe-143">Return value</span></span>

<span data-ttu-id="777fe-144">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="777fe-144">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="777fe-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="777fe-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="777fe-146">Nicht alle Methoden werden für alle Ordner implementiert.</span><span class="sxs-lookup"><span data-stu-id="777fe-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="777fe-147">Beispielsweise ist die Methode " [**Parser Name**](folder-parsename.md) " nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert.</span><span class="sxs-lookup"><span data-stu-id="777fe-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="777fe-148">Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="777fe-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="777fe-149">Beispiele</span><span class="sxs-lookup"><span data-stu-id="777fe-149">Examples</span></span>

<span data-ttu-id="777fe-150">Im folgenden Beispiel wird **movehere** verwendet, um die Datei Temp.txt aus dem Stammverzeichnis des Laufwerks c in den Ordner c: Windows zu verschieben \\ .</span><span class="sxs-lookup"><span data-stu-id="777fe-150">The following example uses **MoveHere** to move the file Temp.txt from the root directory of the C drive to the C:\\Windows folder.</span></span> <span data-ttu-id="777fe-151">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="777fe-151">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="777fe-152">JScript</span><span class="sxs-lookup"><span data-stu-id="777fe-152">JScript:</span></span>


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



<span data-ttu-id="777fe-153">VBScript</span><span class="sxs-lookup"><span data-stu-id="777fe-153">VBScript:</span></span>


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="777fe-154">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="777fe-154">Visual Basic:</span></span>


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="777fe-155">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="777fe-155">Requirements</span></span>



| <span data-ttu-id="777fe-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="777fe-156">Requirement</span></span> | <span data-ttu-id="777fe-157">Wert</span><span class="sxs-lookup"><span data-stu-id="777fe-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="777fe-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="777fe-158">Minimum supported client</span></span><br/> | <span data-ttu-id="777fe-159">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="777fe-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="777fe-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="777fe-160">Minimum supported server</span></span><br/> | <span data-ttu-id="777fe-161">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="777fe-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="777fe-162">Header</span><span class="sxs-lookup"><span data-stu-id="777fe-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="777fe-163"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="777fe-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="777fe-164">IDL</span><span class="sxs-lookup"><span data-stu-id="777fe-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="777fe-165"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="777fe-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="777fe-166">DLL</span><span class="sxs-lookup"><span data-stu-id="777fe-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="777fe-167"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="777fe-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




