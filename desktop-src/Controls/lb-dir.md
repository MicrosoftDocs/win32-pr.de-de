---
title: LB_DIR Meldung (Winuser. h)
description: Fügt der Liste Namen hinzu, die von einem Listenfeld angezeigt werden. In der Meldung werden die Namen von Verzeichnissen und Dateien hinzugefügt, die einer angegebenen Zeichenfolge und einem Satz von Dateiattributen entsprechen. Mit dem lb-Verzeichnis \_ können auch zugeordnete Laufwerk Buchstaben zum Listenfeld hinzugefügt werden.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- Windows-Steuerelemente für LB_DIR Meldung
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80abddbce13adec2e66824057fc5e873def306ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105999"
---
# <a name="lb_dir-message"></a><span data-ttu-id="b8b4b-106">LB- \_ dir-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b8b4b-106">LB\_DIR message</span></span>

<span data-ttu-id="b8b4b-107">Fügt der Liste Namen hinzu, die von einem Listenfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-107">Adds names to the list displayed by a list box.</span></span> <span data-ttu-id="b8b4b-108">In der Meldung werden die Namen von Verzeichnissen und Dateien hinzugefügt, die einer angegebenen Zeichenfolge und einem Satz von Dateiattributen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="b8b4b-109">**Lb \_ DIR** können auch zugeordnete Laufwerk Buchstaben zum Listenfeld hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-109">**LB\_DIR** can also add mapped drive letters to the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8b4b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8b4b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8b4b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8b4b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8b4b-112">Die Attribute der Dateien oder Verzeichnisse, die dem Listenfeld hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-112">The attributes of the files or directories to be added to the list box.</span></span> <span data-ttu-id="b8b4b-113">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="b8b4b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b8b4b-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="b8b4b-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b8b4b-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="b8b4b-116"><dt>**DDL- \_ Archiv**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b4b-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="b8b4b-117">Schließt archivierte Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="b8b4b-118"><dt>**DDL- \_ Verzeichnis**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b4b-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="b8b4b-119">Enthält Unterverzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-119">Includes subdirectories.</span></span> <span data-ttu-id="b8b4b-120">Unterverzeichnis Namen werden in eckige Klammern ( \[ \] ) eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-120">Subdirectory names are enclosed in square brackets (\[ \]).</span></span><br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="b8b4b-121"><dt>**DDL- \_ Laufwerke**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b4b-121"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="b8b4b-122">Alle zugeordneten Laufwerke werden der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-122">All mapped drives are added to the list.</span></span> <span data-ttu-id="b8b4b-123">Laufwerke werden im Format x aufgelistet \[ -  - \] , wobei *x* für den Laufwerk Buchstaben steht.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-123">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="b8b4b-124"><dt>**DDL \_ exklusiv**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b4b-124"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="b8b4b-125">Schließt nur Dateien mit den angegebenen Attributen ein.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-125">Includes only files with the specified attributes.</span></span> <span data-ttu-id="b8b4b-126">Standardmäßig werden Lese-/schreibdateien aufgelistet, auch wenn DDL- \_ Schreibweise nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-126">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="b8b4b-127"><dt>**DDL \_ ausgeblendet**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b4b-127"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="b8b4b-128">Schließt verborgene Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-128">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="b8b4b-129"><dt>**DDL-schreibgeschützt \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b4b-129"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="b8b4b-130">Schließt schreibgeschützte Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-130">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="b8b4b-131"><dt>**DDL- \_ Lesevorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b4b-131"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="b8b4b-132">Umfasst Dateien mit Lese-/Schreibzugriff ohne zusätzliche Attribute.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-132">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="b8b4b-133">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-133">This is the default setting.</span></span><br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="b8b4b-134"><dt>**DDL- \_ System**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b4b-134"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="b8b4b-135">Schließt Systemdateien ein.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-135">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="b8b4b-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8b4b-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8b4b-137">Ein Zeiger auf die NULL-terminierte Zeichenfolge, die einen absoluten Pfad, einen relativen Pfad oder einen Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-137">A pointer to the null-terminated string that specifies an absolute path, relative path, or filename.</span></span> <span data-ttu-id="b8b4b-138">Ein absoluter Pfad kann mit einem Laufwerk Buchstaben (z. b. "d:" \) oder einem UNC-Namen (z. b. " \\ \\ *MachineName* \\ *ShareName*") beginnen.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-138">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\ *machinename*\\ *sharename*).</span></span>

<span data-ttu-id="b8b4b-139">Wenn die Zeichenfolge einen Dateinamen oder ein Verzeichnis angibt, das über die vom *wParam* -Parameter angegebenen Attribute verfügt, wird der Dateiname oder das Verzeichnis der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-139">If the string specifies a filename or directory that has the attributes specified by the *wParam* parameter, the filename or directory is added to the list.</span></span> <span data-ttu-id="b8b4b-140">Wenn der Dateiname oder der Verzeichnisname Platzhalter Zeichen (?</span><span class="sxs-lookup"><span data-stu-id="b8b4b-140">If the filename or directory name contains wildcard characters (?</span></span> <span data-ttu-id="b8b4b-141">oder \* ), werden alle Dateien oder Verzeichnisse, die dem Platzhalter Ausdruck entsprechen und die vom *wParam* -Parameter angegebenen Attribute aufweisen, der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-141">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8b4b-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8b4b-142">Return value</span></span>

<span data-ttu-id="b8b4b-143">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert der null basierte Index des letzten namens, der der Liste hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-143">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="b8b4b-144">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-144">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="b8b4b-145">Wenn nicht genügend Speicherplatz zum Speichern der neuen Zeichen folgen verfügbar ist, ist der Rückgabewert "lb \_ errspace".</span><span class="sxs-lookup"><span data-stu-id="b8b4b-145">If there is insufficient space to store the new strings, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8b4b-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8b4b-146">Remarks</span></span>

<span data-ttu-id="b8b4b-147">Die " [**lb- \_ InitStorage**](lb-initstorage.md) "-Nachricht beschleunigt die Initialisierung von Listenfeldern, die über eine große Anzahl von Elementen (mehr als 100) verfügen.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-147">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="b8b4b-148">Sie reserviert die angegebene Menge an Arbeitsspeicher, sodass nachfolgende **lb- \_ dir** -Nachrichten die kürzeste Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-148">It reserves the specified amount of memory so that subsequent **LB\_DIR** messages take the shortest possible time.</span></span> <span data-ttu-id="b8b4b-149">Sie können Schätzwerte für den *wParam* -Parameter und den *LPARAM* -Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-149">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="b8b4b-150">Wenn Sie den Wert überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie unterschätzen, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-150">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="b8b4b-151">Wenn *wParam* das DDL \_ -verzeichnisflag enthält und *LPARAM* alle Unterverzeichnisse eines Verzeichnisses der ersten Ebene (z. b. C: Temp) angibt \\ \\ \* , enthält das Listenfeld immer einen ".."-Eintrag für das Stammverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-151">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="b8b4b-152">Dies gilt auch, wenn das Stammverzeichnis ausgeblendete oder Systemattribute aufweist und die DDL-ausgeblendeten \_ und DDL- \_ systemFlags nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-152">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="b8b4b-153">Das Stammverzeichnis eines NTFS-Volumes verfügt über verborgene Attribute und Systemattribute.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-153">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="b8b4b-154">In der Liste werden lange Dateinamen angezeigt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-154">The list displays long filenames, if any.</span></span>

<span data-ttu-id="b8b4b-155">Für eine ANSI-Anwendung konvertiert das System den Text in einem Listenfeld mithilfe von CP ACP in Unicode \_ .</span><span class="sxs-lookup"><span data-stu-id="b8b4b-155">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="b8b4b-156">Dies kann zu Problemen führen.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-156">This can cause problems.</span></span> <span data-ttu-id="b8b4b-157">Beispielsweise werden Zeichen mit untergeordneten Zeichen in einem nicht-Unicode-Listenfeld in einem japanischen Fenster gegartet.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-157">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="b8b4b-158">Um dieses Problem zu beheben, kompilieren Sie die Anwendung entweder als Unicode, oder verwenden Sie ein vom Besitzer gezeichnetes Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-158">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b4b-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8b4b-159">Requirements</span></span>



| <span data-ttu-id="b8b4b-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8b4b-160">Requirement</span></span> | <span data-ttu-id="b8b4b-161">Wert</span><span class="sxs-lookup"><span data-stu-id="b8b4b-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b4b-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8b4b-162">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b4b-163">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8b4b-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b8b4b-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8b4b-164">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b4b-165">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8b4b-165">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b8b4b-166">Header</span><span class="sxs-lookup"><span data-stu-id="b8b4b-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8b4b-167"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b8b4b-167"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8b4b-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8b4b-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b4b-169">**Dlgdirlist**</span><span class="sxs-lookup"><span data-stu-id="b8b4b-169">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





