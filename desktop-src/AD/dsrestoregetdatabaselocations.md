---
title: Dsrestoregetdatabaselocations-Funktion (ntdsbcli. h)
description: Ruft die Speicherorte ab, an denen Sicherungsdateien bei einem Wiederherstellungs Vorgang kopiert werden sollen.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Dsrestoregetdatabaselocations-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bcebb9f3822332269e1db09f3246c128e4ad1f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859060"
---
# <a name="dsrestoregetdatabaselocations-function"></a><span data-ttu-id="a7b1c-104">Dsrestoregetdatabaselocations-Funktion</span><span class="sxs-lookup"><span data-stu-id="a7b1c-104">DsRestoreGetDatabaseLocations function</span></span>

<span data-ttu-id="a7b1c-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a7b1c-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a7b1c-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="a7b1c-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="a7b1c-108">Die **dsrestoregetdatabaselocations** -Funktion Ruft die Speicherorte ab, an denen Sicherungsdateien bei einem Wiederherstellungs Vorgang kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-108">The **DsRestoreGetDatabaseLocations** function obtains the locations where backup files should be copied during a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7b1c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7b1c-109">Syntax</span></span>


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="a7b1c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7b1c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7b1c-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7b1c-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b1c-112">Enthält das Wiederherstellungs Kontext Handle, das mit der [**dsrestoreprepare**](dsrestoreprepare.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a7b1c-113">*pszdatabaselocationlist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a7b1c-113">*pszDatabaseLocationList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b1c-114">Ein Zeiger auf einen Zeichen folgen Zeiger, der die Liste der Daten Bank Speicherorte als UNC-Pfade empfängt.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-114">Pointer to a string pointer that receives the list of database locations as UNC paths.</span></span> <span data-ttu-id="a7b1c-115">Diese Liste empfängt eine mit NULL endend beendete Liste mit einzelnen null-terminierten Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-115">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="a7b1c-116">Dieser Puffer wird durch die Funktion **dsrestoregetdatabaselocations** zugewiesen und muss freigegeben werden, wenn er durch Aufrufen der [**dsbackupfree**](dsbackupfree.md) -Funktion nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-116">This buffer is allocated by the **DsRestoreGetDatabaseLocations** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="a7b1c-117">Das erste Zeichen jedes Datei namens enthält eine der [**bft-Konstanten**](bft-constants.md) , die den Namenstyp identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-117">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the name type.</span></span> <span data-ttu-id="a7b1c-118">Die **dsrestoregetdatabaselocations** -Funktion stellt nur die folgenden namens Typen bereit.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-118">The **DsRestoreGetDatabaseLocations** function only supplies the following name types.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="a7b1c-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**bft- \_ NTDS- \_ Datenbank**</span><span class="sxs-lookup"><span data-stu-id="a7b1c-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="a7b1c-120">Die NTDS-Datenbankdatei sollte in diese Datei kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-120">The NTDS database file should be copied to this file.</span></span> <span data-ttu-id="a7b1c-121">Dies ist die Datei, die beim Durchführen der Sicherung als **bft \_ NTDS- \_ Datenbank** identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-121">This is the file that was identified as **BFT\_NTDS\_DATABASE** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span data-ttu-id="a7b1c-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**bft- \_ Protokoll Verzeichnis \_**</span><span class="sxs-lookup"><span data-stu-id="a7b1c-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="a7b1c-123">Alle Protokolldateien werden in dieses Verzeichnis kopiert.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-123">All log files are copied to this directory.</span></span> <span data-ttu-id="a7b1c-124">Die Protokolldateien wurden als **bft- \_ Protokoll** identifiziert, als die Sicherung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-124">The log files were identified as **BFT\_LOG** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span data-ttu-id="a7b1c-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**bft-Prüf Punkt Verzeichnis \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a7b1c-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="a7b1c-126">Alle Patchdateien werden in dieses Verzeichnis kopiert.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-126">All patch files are copied to this directory.</span></span> <span data-ttu-id="a7b1c-127">Die Patchdateien wurden als **bft- \_ \_ Patchdatei** identifiziert, als die Sicherung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-127">The patch files were identified as **BFT\_PATCH\_FILE** when the backup was performed.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a7b1c-128">*pcbSize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a7b1c-128">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b1c-129">Zeiger auf den **DWORD** -Wert, der die Größe des *pszdatabaselocationlist* -Puffers in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-129">Pointer to **DWORD** value that receives the size, in bytes, of the *pszDatabaseLocationList* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7b1c-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7b1c-130">Return value</span></span>

<span data-ttu-id="a7b1c-131">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-131">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="a7b1c-132">In der folgenden Liste sind die möglichen Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-132">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="a7b1c-133">**Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="a7b1c-133">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="a7b1c-134">Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-134">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="a7b1c-135">Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-135">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="a7b1c-136">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="a7b1c-136">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="a7b1c-137">*HBC*, *pszdatabaselocationlist* oder *pcbSize* sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-137">*hbc*, *pszDatabaseLocationList*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a7b1c-138">**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="a7b1c-138">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="a7b1c-139">Es ist ein Fehler bei der Speicher Belegung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-139">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7b1c-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7b1c-140">Remarks</span></span>

<span data-ttu-id="a7b1c-141">Die **dsrestoregetdatabaselocations** -Funktion kann verwendet werden, um die Wiederherstellungs Verzeichnisse zu erhalten, ohne auf die gesicherten Daten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-141">The **DsRestoreGetDatabaseLocations** function can be used to obtain the restoration directories without access to the backed up data.</span></span> <span data-ttu-id="a7b1c-142">Aufrufen Sie hierzu [**dsrestoreprepare**](dsrestoreprepare.md) mit **null** für den *pvexpiriytoken* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-142">To do this, call [**DsRestorePrepare**](dsrestoreprepare.md) with **NULL** for the *pvExpiryToken* parameter.</span></span> <span data-ttu-id="a7b1c-143">Dies bewirkt, dass **dsrestoreprepare** ein eingeschränktes Kontext Handle zurückgibt, das nur mit der **dsrestoregetdatabaselocations** -Funktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7b1c-143">This causes **DsRestorePrepare** to return a restricted context handle which can only be used with the **DsRestoreGetDatabaseLocations** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7b1c-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7b1c-144">Requirements</span></span>



| <span data-ttu-id="a7b1c-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7b1c-145">Requirement</span></span> | <span data-ttu-id="a7b1c-146">Wert</span><span class="sxs-lookup"><span data-stu-id="a7b1c-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b1c-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7b1c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a7b1c-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7b1c-148">Windows Vista</span></span><br/>                                                                              |
| <span data-ttu-id="a7b1c-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7b1c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a7b1c-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7b1c-150">Windows Server 2008</span></span><br/>                                                                        |
| <span data-ttu-id="a7b1c-151">Header</span><span class="sxs-lookup"><span data-stu-id="a7b1c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7b1c-152"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7b1c-152"><dt>Ntdsbcli.h</dt></span></span> </dl>                 |
| <span data-ttu-id="a7b1c-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a7b1c-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7b1c-154"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7b1c-154"><dt>Ntdsbcli.lib</dt></span></span> </dl>               |
| <span data-ttu-id="a7b1c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="a7b1c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7b1c-156"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7b1c-156"><dt>Ntdsbcli.dll</dt></span></span> </dl>               |
| <span data-ttu-id="a7b1c-157">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a7b1c-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a7b1c-158">**Dsrestoregetdatabaselocationsw** (Unicode) und **dsrestoregetdatabaselocationsa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a7b1c-158">**DsRestoreGetDatabaseLocationsW** (Unicode) and **DsRestoreGetDatabaseLocationsA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7b1c-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7b1c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b1c-160">**Dsrestoreprepare**</span><span class="sxs-lookup"><span data-stu-id="a7b1c-160">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="a7b1c-161">**Dsbackupfree**</span><span class="sxs-lookup"><span data-stu-id="a7b1c-161">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="a7b1c-162">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="a7b1c-162">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="a7b1c-163">Wiederherstellen von Active Directory</span><span class="sxs-lookup"><span data-stu-id="a7b1c-163">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> </dl>

 

