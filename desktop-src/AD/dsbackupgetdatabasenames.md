---
title: Dsbackupgetdatabasenames-Funktion (ntdsbcli. h)
description: Ruft die Liste der Datenbankdateien ab, die für den angegebenen Sicherungs Kontext gesichert werden sollen.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Dsbackupgetdatabasenames-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6643b17a85727f6e0df4e8deea9609f73afd1e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477136"
---
# <a name="dsbackupgetdatabasenames-function"></a><span data-ttu-id="b7481-104">Dsbackupgetdatabasenames-Funktion</span><span class="sxs-lookup"><span data-stu-id="b7481-104">DsBackupGetDatabaseNames function</span></span>

<span data-ttu-id="b7481-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b7481-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b7481-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b7481-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b7481-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="b7481-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="b7481-108">Die **dsbackupgetdatabasenames** -Funktion Ruft die Liste der Datenbankdateien ab, die für den angegebenen Sicherungs Kontext gesichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7481-108">The **DsBackupGetDatabaseNames** function obtains the list of database files to be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7481-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7481-109">Syntax</span></span>


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="b7481-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7481-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7481-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7481-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7481-112">Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b7481-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b7481-113">*pszattachmentinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b7481-113">*pszAttachmentInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7481-114">Zeiger auf einen Zeichen folgen Zeiger, der die Liste der Daten Bank Dateinamen als UNC-Pfade empfängt.</span><span class="sxs-lookup"><span data-stu-id="b7481-114">Pointer to a string pointer that receives the list of database file names as UNC paths.</span></span> <span data-ttu-id="b7481-115">Dieser Wert muss vor dem Aufrufen von **dsbackupgetdatabasenames** mit **null** initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b7481-115">This value must be initialized to **NULL** prior to calling **DsBackupGetDatabaseNames**.</span></span>

<span data-ttu-id="b7481-116">Diese Liste empfängt eine mit NULL endend beendete Liste mit einzelnen null-terminierten Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="b7481-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="b7481-117">Dieser Puffer wird von der **dsbackupgetdatabasenames** -Funktion zugeordnet und muss freigegeben werden, wenn er durch Aufrufen der [**dsbackupfree**](dsbackupfree.md) -Funktion nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b7481-117">This buffer is allocated by the **DsBackupGetDatabaseNames** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="b7481-118">Das erste Zeichen jedes Datei namens enthält eine der [**bft-Konstanten**](bft-constants.md) , die den Typ des Namens identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b7481-118">The first character of each file name contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span> <span data-ttu-id="b7481-119">Die [**dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md) -Funktion liefert nur die folgenden Typen von Namen.</span><span class="sxs-lookup"><span data-stu-id="b7481-119">The [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function only supplies the following types of names.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="b7481-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**bft- \_ NTDS- \_ Datenbank**</span><span class="sxs-lookup"><span data-stu-id="b7481-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="b7481-121">Die Datei ist eine NTDS-Datenbankdatei.</span><span class="sxs-lookup"><span data-stu-id="b7481-121">The file is an NTDS database file.</span></span> <span data-ttu-id="b7481-122">Diese Datei muss in die als **bft \_ NTDS- \_ Datenbank** identifizierte Datei kopiert werden, wenn die Daten wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b7481-122">This file should be copied to the file identified as **BFT\_NTDS\_DATABASE** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span data-ttu-id="b7481-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**bft- \_ Protokoll**</span><span class="sxs-lookup"><span data-stu-id="b7481-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>


</dt> <dd>

<span data-ttu-id="b7481-124">Bei der Datei handelt es sich um eine Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="b7481-124">The file is a log file.</span></span> <span data-ttu-id="b7481-125">Alle Protokolldateien werden in das Verzeichnis kopiert, das beim Wiederherstellen der Daten als **bft- \_ Protokoll \_** Verzeichnis identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b7481-125">All log files are copied to the directory identified as **BFT\_LOG\_DIR** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span data-ttu-id="b7481-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**bft \_ - \_ Patchdatei**</span><span class="sxs-lookup"><span data-stu-id="b7481-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>


</dt> <dd>

<span data-ttu-id="b7481-127">Bei der Datei handelt es sich um eine Patchdatei.</span><span class="sxs-lookup"><span data-stu-id="b7481-127">The file is a patch file.</span></span> <span data-ttu-id="b7481-128">Alle Patchdateien werden beim Wiederherstellen der Daten in **\_ das als \_ bft** -Prüf Punkt Verzeichnis identifizierte Verzeichnis kopiert.</span><span class="sxs-lookup"><span data-stu-id="b7481-128">All patch files are copied to the directory identified as **BFT\_CHECKPOINT\_DIR** when the data is restored.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b7481-129">*pcbSize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b7481-129">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7481-130">Zeiger auf den **DWORD** -Wert, der die Größe des *pszattachmentinfo* -Puffers in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="b7481-130">Pointer to **DWORD** value that receives the size, in bytes, of the *pszAttachmentInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7481-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7481-131">Return value</span></span>

<span data-ttu-id="b7481-132">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b7481-132">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="b7481-133">In der folgenden Liste sind andere mögliche Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7481-133">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="b7481-134">**Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="b7481-134">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="b7481-135">Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b7481-135">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="b7481-136">Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7481-136">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="b7481-137">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="b7481-137">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="b7481-138">*HBC*, *pszattachmentinfo* oder *pcbSize* sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="b7481-138">*hbc*, *pszAttachmentInfo*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="b7481-139">**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="b7481-139">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="b7481-140">Es ist ein Fehler bei der Speicher Belegung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b7481-140">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7481-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7481-141">Remarks</span></span>

<span data-ttu-id="b7481-142">Die **dsbackupgetdatabasenames** -Funktion stellt eine Liste der für eine Sicherung erforderlichen Datenbankdateien bereit.</span><span class="sxs-lookup"><span data-stu-id="b7481-142">The **DsBackupGetDatabaseNames** function provides a list of the database files necessary for a backup.</span></span> <span data-ttu-id="b7481-143">Eine vollständige Sicherung besteht aus den Datenbankdateien und den Protokolldateien, die von der [**dsbackupgetbackuplogs**](dsbackupgetbackuplogs.md) -Funktion bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b7481-143">A full backup consists of the database files and the log files provided by the [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) function.</span></span> <span data-ttu-id="b7481-144">Inkrementelle Sicherungen von Active Directory Servern werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7481-144">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7481-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7481-145">Requirements</span></span>



| <span data-ttu-id="b7481-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7481-146">Requirement</span></span> | <span data-ttu-id="b7481-147">Wert</span><span class="sxs-lookup"><span data-stu-id="b7481-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7481-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7481-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b7481-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7481-149">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="b7481-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7481-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b7481-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7481-151">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="b7481-152">Header</span><span class="sxs-lookup"><span data-stu-id="b7481-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7481-153"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7481-153"><dt>Ntdsbcli.h</dt></span></span> </dl>       |
| <span data-ttu-id="b7481-154">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b7481-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7481-155"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7481-155"><dt>Ntdsbcli.lib</dt></span></span> </dl>     |
| <span data-ttu-id="b7481-156">DLL</span><span class="sxs-lookup"><span data-stu-id="b7481-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7481-157"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7481-157"><dt>Ntdsbcli.dll</dt></span></span> </dl>     |
| <span data-ttu-id="b7481-158">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="b7481-158">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b7481-159">**Dsbackupgetdatabasenamesw** (Unicode) und **dsbackupgetdatabasenamesa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b7481-159">**DsBackupGetDatabaseNamesW** (Unicode) and **DsBackupGetDatabaseNamesA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7481-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7481-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7481-161">**Dsbackupprepare**</span><span class="sxs-lookup"><span data-stu-id="b7481-161">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="b7481-162">**Dsbackupfree**</span><span class="sxs-lookup"><span data-stu-id="b7481-162">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="b7481-163">**Dsbackupgetbackuplogs**</span><span class="sxs-lookup"><span data-stu-id="b7481-163">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="b7481-164">**Bft-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="b7481-164">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="b7481-165">Sichern eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="b7481-165">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="b7481-166">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="b7481-166">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

