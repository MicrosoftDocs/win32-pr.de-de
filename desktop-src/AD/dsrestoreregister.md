---
title: Dsrestoreregiester-Funktion (ntdsbcli. h)
description: Registriert einen Wiederherstellungs Vorgang.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Dsrestoreregiester-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 610d49c73ade9bab47c95e90af73bac606f4bd23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040727"
---
# <a name="dsrestoreregister-function"></a><span data-ttu-id="91b57-104">Dsrestoreregiester-Funktion</span><span class="sxs-lookup"><span data-stu-id="91b57-104">DsRestoreRegister function</span></span>

<span data-ttu-id="91b57-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="91b57-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="91b57-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="91b57-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="91b57-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="91b57-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="91b57-108">Die **dsrestoreregiester** -Funktion registriert einen Wiederherstellungs Vorgang. Diese Funktion intersperrt alle nachfolgenden Wiederherstellungs Vorgänge und verhindert, dass das Wiederherstellungs Ziel gestartet wird, bis die [**dsrestoreregistercomplete**](dsrestoreregistercomplete.md) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="91b57-108">The **DsRestoreRegister** function registers a restore operation.This function interlocks all subsequent restore operations and prevents the restore target from starting until the [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="91b57-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="91b57-109">Syntax</span></span>


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a><span data-ttu-id="91b57-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91b57-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91b57-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91b57-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b57-112">Enthält das Wiederherstellungs Kontext Handle, das mit der [**dsrestoreprepare**](dsrestoreprepare.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="91b57-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="91b57-113">*szcheckpointfilepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91b57-113">*szCheckPointFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b57-114">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Pfad der Prüf Punkt Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="91b57-114">Pointer to a null-terminated string that contains the path to the checkpoint file.</span></span> <span data-ttu-id="91b57-115">Dieser Pfad wird von der [**dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md) -Funktion bereitgestellt und verfügt über einen **bft** -Wert von **bft \_ Checkpoint \_ dir**.</span><span class="sxs-lookup"><span data-stu-id="91b57-115">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_CHECKPOINT\_DIR**.</span></span> <span data-ttu-id="91b57-116">Dies entspricht in der Regel dem Pfad der Systemdatenbank.</span><span class="sxs-lookup"><span data-stu-id="91b57-116">Typically this is the same as the system database path.</span></span> <span data-ttu-id="91b57-117">Dieser Pfad ist für eine ordnungsgemäße Sicherungs Wiederherstellungs Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="91b57-117">This path is required for proper backup restore function.</span></span> <span data-ttu-id="91b57-118">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="91b57-118">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="91b57-119">Wenn Sie **null** in diesem Parameter übergeben, tritt während des Wiederherstellungs Vorgangs ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="91b57-119">Passing **NULL** in this parameter will cause an error during the restore process.</span></span>

</dd> <dt>

<span data-ttu-id="91b57-120">*szlogpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91b57-120">*szLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b57-121">Zeiger auf eine auf NULL endende Zeichenfolge, die den Pfad enthält, in dem die Protokolldateien wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="91b57-121">Pointer to a null-terminated string that contains the path where the log files will be restored.</span></span> <span data-ttu-id="91b57-122">Dieser Pfad wird von der [**dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md) -Funktion bereitgestellt und hat den **bft** -Wert **bft \_ log \_ dir**.</span><span class="sxs-lookup"><span data-stu-id="91b57-122">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_LOG\_DIR**.</span></span> <span data-ttu-id="91b57-123">Wenn der Pfad auf ein leeres Verzeichnis verweist, werden neue Protokolldateien erstellt.</span><span class="sxs-lookup"><span data-stu-id="91b57-123">If the path points to an empty directory, new log files are created there.</span></span> <span data-ttu-id="91b57-124">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="91b57-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="91b57-125">*rgrstmap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91b57-125">*rgrstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b57-126">Ein Array von [**EDB- \_ rstmap**](edb-rstmap.md) -Strukturen, das die alten und neuen Pfade für die einzelnen Datenbanken enthält.</span><span class="sxs-lookup"><span data-stu-id="91b57-126">An array of [**EDB\_RSTMAP**](edb-rstmap.md) structures that contains the old and new paths for each database.</span></span> <span data-ttu-id="91b57-127">Es gibt eine Struktur für jede Datenbank.</span><span class="sxs-lookup"><span data-stu-id="91b57-127">There is one structure for each database.</span></span> <span data-ttu-id="91b57-128">Für das Verzeichnis gibt es eine Struktur für die Systemdatenbank und eine andere Struktur für die Verzeichnis Datenbank.</span><span class="sxs-lookup"><span data-stu-id="91b57-128">For the directory, there is a structure for the system database and another structure for the directory database.</span></span> <span data-ttu-id="91b57-129">Die Reihenfolge der Elemente im Array spielt keine Rolle.</span><span class="sxs-lookup"><span data-stu-id="91b57-129">The order of the elements in the array does not matter.</span></span> <span data-ttu-id="91b57-130">Der *crstmap* -Parameter enthält die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="91b57-130">The *crstmap* parameter contains the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="91b57-131">*crstmap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91b57-131">*crstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b57-132">Enthält die Anzahl der Elemente im *rgrstmap* -Array.</span><span class="sxs-lookup"><span data-stu-id="91b57-132">Contains the number of elements in the *rgrstmap* array.</span></span>

</dd> <dt>

<span data-ttu-id="91b57-133">*szbackuplogpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91b57-133">*szBackupLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b57-134">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Pfad enthält, in dem sich die gesicherten Protokolldateien befinden.</span><span class="sxs-lookup"><span data-stu-id="91b57-134">Pointer to a null-terminated string that contains the path where the backed up log files currently reside.</span></span> <span data-ttu-id="91b57-135">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="91b57-135">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="91b57-136">*genlow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91b57-136">*genLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b57-137">Enthält die niedrigste Protokollnummer, die in dieser Wiederherstellungs Sitzung wieder hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="91b57-137">Contains the lowest log number to restore in this restore session.</span></span> <span data-ttu-id="91b57-138">Dabei handelt es sich um eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="91b57-138">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="91b57-139">*genhoch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91b57-139">*genHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b57-140">Enthält die höchste Protokollnummer, die in dieser Wiederherstellungs Sitzung wieder hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="91b57-140">Contains the highest log number to restore in this restore session.</span></span> <span data-ttu-id="91b57-141">Dabei handelt es sich um eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="91b57-141">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91b57-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91b57-142">Return value</span></span>

<span data-ttu-id="91b57-143">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="91b57-143">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="91b57-144">In der folgenden Liste sind die möglichen Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="91b57-144">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="91b57-145">**Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="91b57-145">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="91b57-146">Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="91b57-146">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="91b57-147">Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="91b57-147">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="91b57-148">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="91b57-148">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="91b57-149">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="91b57-149">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="91b57-150">**hrmissingexpirytoken**</span><span class="sxs-lookup"><span data-stu-id="91b57-150">**hrMissingExpiryToken**</span></span>
</dt> <dd>

<span data-ttu-id="91b57-151">Das für [**dsrestoreprepare**](dsrestoreprepare.md) bereitgestellte Ablauf Token war ungültig.</span><span class="sxs-lookup"><span data-stu-id="91b57-151">The expiry token supplied to [**DsRestorePrepare**](dsrestoreprepare.md) was invalid.</span></span> <span data-ttu-id="91b57-152">Dieser Wert wird in "ntdsbmsg. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="91b57-152">This value is defined in Ntdsbmsg.h.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91b57-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91b57-153">Requirements</span></span>



| <span data-ttu-id="91b57-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91b57-154">Requirement</span></span> | <span data-ttu-id="91b57-155">Wert</span><span class="sxs-lookup"><span data-stu-id="91b57-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91b57-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91b57-156">Minimum supported client</span></span><br/> | <span data-ttu-id="91b57-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91b57-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91b57-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91b57-158">Minimum supported server</span></span><br/> | <span data-ttu-id="91b57-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91b57-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91b57-160">Header</span><span class="sxs-lookup"><span data-stu-id="91b57-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="91b57-161"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="91b57-161"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="91b57-162">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91b57-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="91b57-163"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91b57-163"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="91b57-164">DLL</span><span class="sxs-lookup"><span data-stu-id="91b57-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91b57-165"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91b57-165"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="91b57-166">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="91b57-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="91b57-167">**Dsrestoreregisterw** (Unicode) und **dsrestoreregistera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="91b57-167">**DsRestoreRegisterW** (Unicode) and **DsRestoreRegisterA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="91b57-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91b57-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b57-169">**Dsrestoreregistercomplete**</span><span class="sxs-lookup"><span data-stu-id="91b57-169">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="91b57-170">**Dsrestoreprepare**</span><span class="sxs-lookup"><span data-stu-id="91b57-170">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="91b57-171">**Dsrestoregetdatabaselocations**</span><span class="sxs-lookup"><span data-stu-id="91b57-171">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="91b57-172">**Dsrestoreend**</span><span class="sxs-lookup"><span data-stu-id="91b57-172">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> <dt>

[<span data-ttu-id="91b57-173">**EDB- \_ rstmap**</span><span class="sxs-lookup"><span data-stu-id="91b57-173">**EDB\_RSTMAP**</span></span>](edb-rstmap.md)
</dt> <dt>

[<span data-ttu-id="91b57-174">Wiederherstellen von Active Directory</span><span class="sxs-lookup"><span data-stu-id="91b57-174">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="91b57-175">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="91b57-175">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

