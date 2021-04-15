---
title: Dsbackupprepare-Funktion (ntdsbcli. h)
description: Bereitet das Verzeichnis auf dem angegebenen Server für die Online Sicherung vor und gibt ein Sicherungs Kontext Handle zurück, das bei nachfolgenden Aufrufen anderer Sicherungsfunktionen verwendet wird.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Dsbackupprepare-Funktions Active Directory
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa561a7e41164ece68fb18fd882a8b05d6357cec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477133"
---
# <a name="dsbackupprepare-function"></a><span data-ttu-id="d19aa-104">Dsbackupprepare-Funktion</span><span class="sxs-lookup"><span data-stu-id="d19aa-104">DsBackupPrepare function</span></span>

<span data-ttu-id="d19aa-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d19aa-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d19aa-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d19aa-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d19aa-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="d19aa-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="d19aa-108">Die **dsbackupprepare** -Funktion bereitet das Verzeichnis auf dem angegebenen Server für die Online Sicherung vor und gibt ein Sicherungs Kontext Handle zurück, das bei nachfolgenden Aufrufen anderer Sicherungsfunktionen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d19aa-108">The **DsBackupPrepare** function prepares the directory on the specified server for the online backup and returns a backup context handle used in subsequent calls to other backup functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d19aa-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d19aa-109">Syntax</span></span>


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="d19aa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d19aa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d19aa-111">*szbackupserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d19aa-111">*szBackupServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-112">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des zu sichernden Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="d19aa-112">Pointer to a null-terminated string that contains the name of the server to backup.</span></span> <span data-ttu-id="d19aa-113">Vorangehende umgekehrte Schrägstriche sind optional.</span><span class="sxs-lookup"><span data-stu-id="d19aa-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="d19aa-114">Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d19aa-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="d19aa-115">Der Servername darf keinen Unterstrich ( \_ ) enthalten.</span><span class="sxs-lookup"><span data-stu-id="d19aa-115">The server name cannot contain an underscore (\_) character.</span></span> <span data-ttu-id="d19aa-116">Ein Beispiel für einen Servernamen ist " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="d19aa-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="d19aa-117">*grbit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d19aa-117">*grbit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-118">Bestimmt, ob die Protokolldateien gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="d19aa-118">Determines if the log files will be backed up.</span></span> <span data-ttu-id="d19aa-119">Dieser Wert sollte immer 0 sein, da inkrementelle Sicherungen nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d19aa-119">This value should always be 0 because incremental backups are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d19aa-120">*btbackuptype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d19aa-120">*btBackupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-121">Gibt den Sicherungstyp an.</span><span class="sxs-lookup"><span data-stu-id="d19aa-121">Specifies the type of backup.</span></span> <span data-ttu-id="d19aa-122">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="d19aa-122">This can be one of the following values.</span></span>

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span data-ttu-id="d19aa-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**\_Sicherungstyp \_ voll**</span><span class="sxs-lookup"><span data-stu-id="d19aa-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**BACKUP\_TYPE\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="d19aa-124">Gibt eine vollständige Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="d19aa-124">Specifies a full backup.</span></span> <span data-ttu-id="d19aa-125">Das komplette Verzeichnis (DIT, Protokolldateien und Update Dateien) wird gesichert.</span><span class="sxs-lookup"><span data-stu-id="d19aa-125">The complete directory (DIT, log files, and update files) are backed up.</span></span> <span data-ttu-id="d19aa-126">Alle Daten werden gesichert, und die Transaktionsprotokoll Dateien werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="d19aa-126">All data is backed up and transaction log files are truncated.</span></span> <span data-ttu-id="d19aa-127">Es werden nur vollständige Sicherungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d19aa-127">Only full backups are supported.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span data-ttu-id="d19aa-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_nur Sicherungs Typen \_ Protokolle \_**</span><span class="sxs-lookup"><span data-stu-id="d19aa-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**BACKUP\_TYPE\_LOGS\_ONLY**</span></span>


</dt> <dd>

<span data-ttu-id="d19aa-129">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d19aa-129">This value is not supported.</span></span> <span data-ttu-id="d19aa-130">Gibt an, dass nur die Daten Bank Protokolle und nicht die Datenbank selbst gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="d19aa-130">Specifies that only the database logs, and not the database itself, will be backed up.</span></span> <span data-ttu-id="d19aa-131">Dies wird normalerweise beim Ausführen einer differenziellen oder inkrementellen Sicherung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d19aa-131">This is normally used when performing a differential or incremental backup.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span data-ttu-id="d19aa-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**\_Sicherungstyp \_**</span><span class="sxs-lookup"><span data-stu-id="d19aa-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**BACKUP\_TYPE\_INCREMENTAL**</span></span>


</dt> <dd>

<span data-ttu-id="d19aa-133">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d19aa-133">This value is not supported.</span></span> <span data-ttu-id="d19aa-134">**Dsbackupprepare** gibt **einen \_ ungültigen \_ Parameter** zurück.</span><span class="sxs-lookup"><span data-stu-id="d19aa-134">**DsBackupPrepare** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d19aa-135">*ppvexpiriytoken* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d19aa-135">*ppvExpiryToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-136">Ein Zeiger auf einen **pVoid** -Wert, der einen Zeiger auf ein Ablauf Token empfängt, das dieser Sicherung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d19aa-136">Pointer to a **PVOID** value that receives a pointer to an expiry token associated with this backup.</span></span> <span data-ttu-id="d19aa-137">*pcbexpirytekensize* erhält die Größe dieser Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d19aa-137">*pcbExpiryTokenSize* receives the size, in bytes, of this data.</span></span> <span data-ttu-id="d19aa-138">Der Aufrufer muss den Inhalt dieses Tokens mit der Sicherung speichern, da das Token an [**dsrestoreprepare**](dsrestoreprepare.md) übergeben werden muss, wenn versucht wird, Daten wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="d19aa-138">The caller must save the contents of this token with the backup because the token must be passed to [**DsRestorePrepare**](dsrestoreprepare.md) when attempting to restore data.</span></span> <span data-ttu-id="d19aa-139">Nachdem das Token gespeichert wurde und nicht mehr benötigt wird, muss der Aufrufer den zugeordneten Arbeitsspeicher mithilfe von [**dsbackupfree**](dsbackupfree.md)freigeben.</span><span class="sxs-lookup"><span data-stu-id="d19aa-139">After the token has been stored and is no longer required, the caller should free the allocated memory using [**DsBackupFree**](dsbackupfree.md).</span></span>

</dd> <dt>

<span data-ttu-id="d19aa-140">*pcbexpirytekensize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d19aa-140">*pcbExpiryTokenSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-141">Ein Zeiger auf einen **DWORD** -Wert, der die Größe des Tokens in *ppvexpiriytoken* in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="d19aa-141">Pointer to a **DWORD** value that receives the size, in bytes, of the token in *ppvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="d19aa-142">*phbC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d19aa-142">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-143">Ein Zeiger auf einen **HBC** -Wert, der das Handle für die Sicherung empfängt.</span><span class="sxs-lookup"><span data-stu-id="d19aa-143">Pointer to an **HBC** value that receives the handle for the backup.</span></span> <span data-ttu-id="d19aa-144">Dieses Handle wird verwendet, wenn andere Verzeichnisdienst-Sicherungsfunktionen aufgerufen werden, wie z. b. [**dsbackupopenfile**](dsbackupopenfile.md) und [**dsbackupend**](dsbackupend.md).</span><span class="sxs-lookup"><span data-stu-id="d19aa-144">This handle is used when calling other Directory Service backup functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsBackupEnd**](dsbackupend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d19aa-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d19aa-145">Return value</span></span>

<span data-ttu-id="d19aa-146">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d19aa-146">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="d19aa-147">In der folgenden Liste sind andere mögliche Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d19aa-147">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="d19aa-148">**Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="d19aa-148">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-149">Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d19aa-149">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="d19aa-150">Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d19aa-150">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="d19aa-151">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="d19aa-151">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-152">" *szbackupserver* " oder " *phbcbackupcontext* " sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="d19aa-152">*szBackupServer* or *phbcBackupContext* are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d19aa-153">**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="d19aa-153">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-154">Es ist ein Fehler bei der Speicher Belegung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d19aa-154">A memory allocation failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d19aa-155">**hrcouldnotconnect**</span><span class="sxs-lookup"><span data-stu-id="d19aa-155">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-156">Der Server in " *szbackupserver* " wurde nicht gefunden, ist kein Domänen Controller, oder " *szbackupserver* " ist nicht ordnungsgemäß formatiert.</span><span class="sxs-lookup"><span data-stu-id="d19aa-156">The server in *szBackupServer* could not be found, is not a domain controller or *szBackupServer* is not formatted correctly.</span></span> <span data-ttu-id="d19aa-157">Dieser Wert wird in "ntdsbmsg. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="d19aa-157">This value is defined in ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="d19aa-158">**hrinvalidparam**</span><span class="sxs-lookup"><span data-stu-id="d19aa-158">**hrInvalidParam**</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-159">*ppvexpiriytoken* und/oder *pcbexpirytokensize* sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="d19aa-159">*ppvExpiryToken* and/or *pcbExpiryTokenSize* are invalid.</span></span> <span data-ttu-id="d19aa-160">Dieser Wert wird in "ntdsbmsg. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="d19aa-160">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="d19aa-161">**\_ungültige RPC S- \_ \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="d19aa-161">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="d19aa-162">Die Funktion wird Remote aufgerufen, oder der Server in " *szservername* " ist kein Domänen Controller.</span><span class="sxs-lookup"><span data-stu-id="d19aa-162">The function is called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d19aa-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d19aa-163">Remarks</span></span>

<span data-ttu-id="d19aa-164">Diese Funktion erfordert, dass der Aufrufer über die Berechtigung " **SE \_ Backup \_ Name** " verfügt.</span><span class="sxs-lookup"><span data-stu-id="d19aa-164">This function requires that the caller has the **SE\_BACKUP\_NAME** privilege.</span></span> <span data-ttu-id="d19aa-165">Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um den Sicherheitskontext zu ändern, in dem diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d19aa-165">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to change the security context under which this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="d19aa-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d19aa-166">Requirements</span></span>



| <span data-ttu-id="d19aa-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d19aa-167">Requirement</span></span> | <span data-ttu-id="d19aa-168">Wert</span><span class="sxs-lookup"><span data-stu-id="d19aa-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d19aa-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d19aa-169">Minimum supported client</span></span><br/> | <span data-ttu-id="d19aa-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d19aa-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d19aa-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d19aa-171">Minimum supported server</span></span><br/> | <span data-ttu-id="d19aa-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d19aa-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d19aa-173">Header</span><span class="sxs-lookup"><span data-stu-id="d19aa-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="d19aa-174"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="d19aa-174"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="d19aa-175">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d19aa-175">Library</span></span><br/>                  | <dl> <span data-ttu-id="d19aa-176"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d19aa-176"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="d19aa-177">DLL</span><span class="sxs-lookup"><span data-stu-id="d19aa-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d19aa-178"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d19aa-178"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="d19aa-179">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d19aa-179">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d19aa-180">**Dsbackuppreparew** (Unicode) und **dsbackuppreparea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d19aa-180">**DsBackupPrepareW** (Unicode) and **DsBackupPrepareA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d19aa-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d19aa-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d19aa-182">**Dsrestoreprepare**</span><span class="sxs-lookup"><span data-stu-id="d19aa-182">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="d19aa-183">**Dsbackupfree**</span><span class="sxs-lookup"><span data-stu-id="d19aa-183">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="d19aa-184">**Dsbackupopenfile**</span><span class="sxs-lookup"><span data-stu-id="d19aa-184">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="d19aa-185">**Dsbackupend**</span><span class="sxs-lookup"><span data-stu-id="d19aa-185">**DsBackupEnd**</span></span>](dsbackupend.md)
</dt> <dt>

[<span data-ttu-id="d19aa-186">**Dssetauthidentity**</span><span class="sxs-lookup"><span data-stu-id="d19aa-186">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="d19aa-187">Sichern eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="d19aa-187">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="d19aa-188">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="d19aa-188">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

