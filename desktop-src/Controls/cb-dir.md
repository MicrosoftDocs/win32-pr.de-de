---
title: CB_DIR Meldung (Winuser. h)
description: Fügt der Liste Namen hinzu, die im Kombinations Feld angezeigt werden. In der Meldung werden die Namen von Verzeichnissen und Dateien hinzugefügt, die einer angegebenen Zeichenfolge und einem Satz von Dateiattributen entsprechen. CB \_ dir kann auch zugeordnete Laufwerk Buchstaben zur Liste hinzufügen.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- Windows-Steuerelemente für CB_DIR Meldung
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98cbea5bb88614d5606dd3d5cb165be59f632556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858896"
---
# <a name="cb_dir-message"></a><span data-ttu-id="e3119-106">CB- \_ dir-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e3119-106">CB\_DIR message</span></span>

<span data-ttu-id="e3119-107">Fügt der Liste Namen hinzu, die im Kombinations Feld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e3119-107">Adds names to the list displayed by the combo box.</span></span> <span data-ttu-id="e3119-108">In der Meldung werden die Namen von Verzeichnissen und Dateien hinzugefügt, die einer angegebenen Zeichenfolge und einem Satz von Dateiattributen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e3119-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="e3119-109">**CB \_ DIR** können auch zugeordnete Laufwerk Buchstaben zur Liste hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e3119-109">**CB\_DIR** can also add mapped drive letters to the list.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3119-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3119-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3119-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3119-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3119-112">Die Attribute der Dateien oder Verzeichnisse, die dem Kombinations Feld hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3119-112">The attributes of the files or directories to be added to the combo box.</span></span> <span data-ttu-id="e3119-113">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e3119-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="e3119-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e3119-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="e3119-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e3119-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="e3119-116"><dt>**DDL- \_ Archiv**</dt></span><span class="sxs-lookup"><span data-stu-id="e3119-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="e3119-117">Schließt archivierte Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="e3119-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="e3119-118"><dt>**DDL- \_ Verzeichnis**</dt></span><span class="sxs-lookup"><span data-stu-id="e3119-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="e3119-119">Schließt Unterverzeichnisse ein, die in eckigen Klammern () eingeschlossen sind \[ \] .</span><span class="sxs-lookup"><span data-stu-id="e3119-119">Includes subdirectories, which are enclosed in square brackets (\[ \]).</span></span><br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="e3119-120"><dt>**DDL- \_ Laufwerke**</dt></span><span class="sxs-lookup"><span data-stu-id="e3119-120"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="e3119-121">Alle zugeordneten Laufwerke werden der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e3119-121">All mapped drives are added to the list.</span></span> <span data-ttu-id="e3119-122">Laufwerke werden im Format x aufgelistet \[ -  - \] , wobei *x* für den Laufwerk Buchstaben steht.</span><span class="sxs-lookup"><span data-stu-id="e3119-122">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="e3119-123"><dt>**DDL \_ exklusiv**</dt></span><span class="sxs-lookup"><span data-stu-id="e3119-123"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="e3119-124">Schließt nur Dateien mit den angegebenen Attributen ein.</span><span class="sxs-lookup"><span data-stu-id="e3119-124">Includes only files with the specified attributes.</span></span> <span data-ttu-id="e3119-125">Standardmäßig werden Lese-/schreibdateien aufgelistet, auch wenn DDL- \_ Schreibweise nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e3119-125">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="e3119-126"><dt>**DDL \_ ausgeblendet**</dt></span><span class="sxs-lookup"><span data-stu-id="e3119-126"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="e3119-127">Schließt verborgene Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="e3119-127">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="e3119-128"><dt>**DDL-schreibgeschützt \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e3119-128"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="e3119-129">Schließt schreibgeschützte Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="e3119-129">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="e3119-130"><dt>**DDL- \_ Lesevorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="e3119-130"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="e3119-131">Umfasst Dateien mit Lese-/Schreibzugriff ohne zusätzliche Attribute.</span><span class="sxs-lookup"><span data-stu-id="e3119-131">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="e3119-132">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="e3119-132">This is the default.</span></span><br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="e3119-133"><dt>**DDL- \_ System**</dt></span><span class="sxs-lookup"><span data-stu-id="e3119-133"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="e3119-134">Schließt Systemdateien ein.</span><span class="sxs-lookup"><span data-stu-id="e3119-134">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="e3119-135">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3119-135">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3119-136">Ein **LPCTSTR** -Zeiger auf eine NULL-terminierte Zeichenfolge, die einen absoluten Pfad, einen relativen Pfad oder einen Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="e3119-136">An **LPCTSTR** pointer to a null-terminated string that specifies an absolute path, relative path, or file name.</span></span> <span data-ttu-id="e3119-137">Ein absoluter Pfad kann mit einem Laufwerk Buchstaben (z. b. "d:" \) oder einem UNC-Namen (z. b. " \\ \\ *MachineName* \\ *ShareName*") beginnen.</span><span class="sxs-lookup"><span data-stu-id="e3119-137">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\*machinename*\\*sharename*).</span></span> <span data-ttu-id="e3119-138">Wenn die Zeichenfolge einen Dateinamen oder ein Verzeichnis angibt, das über die vom *wParam* -Parameter angegebenen Attribute verfügt, wird der Dateiname oder das Verzeichnis der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e3119-138">If the string specifies a file name or directory that has the attributes specified by the *wParam* parameter, the file name or directory is added to the list.</span></span> <span data-ttu-id="e3119-139">Wenn der Dateiname oder der Verzeichnisname Platzhalter Zeichen enthält (?</span><span class="sxs-lookup"><span data-stu-id="e3119-139">If the file name or directory name contains wildcard characters (?</span></span> <span data-ttu-id="e3119-140">oder \* ), werden alle Dateien oder Verzeichnisse, die dem Platzhalter Ausdruck entsprechen und die vom *wParam* -Parameter angegebenen Attribute aufweisen, der im Kombinations Feld angezeigten Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e3119-140">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list displayed in the combo box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3119-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3119-141">Return value</span></span>

<span data-ttu-id="e3119-142">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert der null basierte Index des letzten namens, der der Liste hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e3119-142">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="e3119-143">Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="e3119-143">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="e3119-144">Wenn nicht genügend Speicherplatz zum Speichern der neuen Zeichen folgen verfügbar ist, ist der Rückgabewert CB \_ errspace.</span><span class="sxs-lookup"><span data-stu-id="e3119-144">If there is insufficient space to store the new strings, the return value is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3119-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3119-145">Remarks</span></span>

<span data-ttu-id="e3119-146">Wenn *wParam* das DDL \_ -verzeichnisflag enthält und *LPARAM* alle Unterverzeichnisse eines Verzeichnisses der ersten Ebene (z. b. C: Temp) angibt \\ \\ \* , enthält das Listenfeld immer einen ".."-Eintrag für das Stammverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e3119-146">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="e3119-147">Dies gilt auch, wenn das Stammverzeichnis ausgeblendete oder Systemattribute aufweist und die DDL-ausgeblendeten \_ und DDL- \_ systemFlags nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e3119-147">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="e3119-148">Das Stammverzeichnis eines NTFS-Volumes verfügt über verborgene Attribute und Systemattribute.</span><span class="sxs-lookup"><span data-stu-id="e3119-148">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="e3119-149">In der Liste werden lange Dateinamen angezeigt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e3119-149">The list displays long file names, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3119-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3119-150">Requirements</span></span>



| <span data-ttu-id="e3119-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3119-151">Requirement</span></span> | <span data-ttu-id="e3119-152">Wert</span><span class="sxs-lookup"><span data-stu-id="e3119-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3119-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3119-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e3119-154">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3119-154">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e3119-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3119-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e3119-156">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3119-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e3119-157">Header</span><span class="sxs-lookup"><span data-stu-id="e3119-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3119-158"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e3119-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3119-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3119-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="e3119-160">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e3119-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e3119-161">**CB \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="e3119-161">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="e3119-162">**CB \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="e3119-162">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="e3119-163">**Dlgdirlistcombobox**</span><span class="sxs-lookup"><span data-stu-id="e3119-163">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





