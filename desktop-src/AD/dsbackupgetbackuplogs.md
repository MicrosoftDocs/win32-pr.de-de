---
title: Dsbackupgetbackuplogs-Funktion (ntdsbcli. h)
description: Ruft die Liste der Protokolldateien ab, die für den angegebenen Sicherungs Kontext gesichert werden müssen.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Dsbackupgetbackuplogs-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a02c5c7234810623a95dea030f0c623cca92293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956588"
---
# <a name="dsbackupgetbackuplogs-function"></a><span data-ttu-id="327d7-104">Dsbackupgetbackuplogs-Funktion</span><span class="sxs-lookup"><span data-stu-id="327d7-104">DsBackupGetBackupLogs function</span></span>

<span data-ttu-id="327d7-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="327d7-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="327d7-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="327d7-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="327d7-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="327d7-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="327d7-108">Die **dsbackupgetbackuplogs** -Funktion Ruft die Liste der Protokolldateien ab, die für den angegebenen Sicherungs Kontext gesichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="327d7-108">The **DsBackupGetBackupLogs** function obtains the list of log files that must be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="327d7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="327d7-109">Syntax</span></span>


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="327d7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="327d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="327d7-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="327d7-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="327d7-112">Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="327d7-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="327d7-113">*pszbackuplogfiles* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="327d7-113">*pszBackupLogFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="327d7-114">Zeiger auf einen Zeichen folgen Zeiger, der die Liste der Protokoll Dateinamen als UNC-Pfade empfängt.</span><span class="sxs-lookup"><span data-stu-id="327d7-114">Pointer to a string pointer that receives the list of log file names as UNC paths.</span></span> <span data-ttu-id="327d7-115">Initialisieren Sie diesen Wert vor dem Aufrufen von **dsbackupgetbackuplogs** in **null** .</span><span class="sxs-lookup"><span data-stu-id="327d7-115">Initialize this value to **NULL** before calling **DsBackupGetBackupLogs**.</span></span>

<span data-ttu-id="327d7-116">Diese Liste empfängt eine mit NULL endend beendete Liste mit einzelnen null-terminierten Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="327d7-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="327d7-117">Dieser Puffer wird von der **dsbackupgetbackuplogs** -Funktion zugewiesen und muss freigegeben werden, wenn er durch Aufrufen der [**dsbackupfree**](dsbackupfree.md) -Funktion nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="327d7-117">This buffer is allocated by the **DsBackupGetBackupLogs** function and must be freed when no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="327d7-118">Das erste Zeichen jedes Datei namens enthält eine der [**bft-Konstanten**](bft-constants.md) , die den Typ des Namens identifiziert.</span><span class="sxs-lookup"><span data-stu-id="327d7-118">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span>

</dd> <dt>

<span data-ttu-id="327d7-119">*pcbSize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="327d7-119">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="327d7-120">Zeiger auf den **DWORD** -Wert, der die Größe des *pszbackuplogfiles* -Puffers in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="327d7-120">Pointer to **DWORD** value that receives the size, in bytes, of the *pszBackupLogFiles* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="327d7-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="327d7-121">Return value</span></span>

<span data-ttu-id="327d7-122">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="327d7-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="327d7-123">In der folgenden Liste sind andere mögliche Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="327d7-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="327d7-124">**Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="327d7-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="327d7-125">Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="327d7-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="327d7-126">Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="327d7-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="327d7-127">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="327d7-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="327d7-128">*HBC*, *pszbackuplogfiles* oder *pcbSize* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="327d7-128">*hbc*, *pszBackupLogFiles*, or *pcbSize* is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="327d7-129">**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="327d7-129">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="327d7-130">Es ist ein Fehler bei der Speicher Belegung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="327d7-130">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="327d7-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="327d7-131">Remarks</span></span>

<span data-ttu-id="327d7-132">Die Funktion **dsbackupgetbackuplogs** enthält eine Liste der Protokolldateien, die für eine Sicherung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="327d7-132">The **DsBackupGetBackupLogs** function provides a list of the log files necessary for a backup.</span></span> <span data-ttu-id="327d7-133">Eine vollständige Sicherung besteht aus den Datenbankdateien, die von der Funktion [**dsbackupgetdatabasenames**](dsbackupgetdatabasenames.md) und den Protokolldateien bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="327d7-133">A full backup consists of the database files provided by the [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) function and the log files.</span></span> <span data-ttu-id="327d7-134">Inkrementelle Sicherungen von Active Directory Servern werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="327d7-134">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="327d7-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="327d7-135">Requirements</span></span>



| <span data-ttu-id="327d7-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="327d7-136">Requirement</span></span> | <span data-ttu-id="327d7-137">Wert</span><span class="sxs-lookup"><span data-stu-id="327d7-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="327d7-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="327d7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="327d7-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="327d7-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="327d7-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="327d7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="327d7-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="327d7-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="327d7-142">Header</span><span class="sxs-lookup"><span data-stu-id="327d7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="327d7-143"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="327d7-143"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="327d7-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="327d7-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="327d7-145"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="327d7-145"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="327d7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="327d7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="327d7-147"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="327d7-147"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="327d7-148">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="327d7-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="327d7-149">**Dsbackupgetbackuplogsw** (Unicode) und **dsbackupgetbackuplogsa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="327d7-149">**DsBackupGetBackupLogsW** (Unicode) and **DsBackupGetBackupLogsA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="327d7-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="327d7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="327d7-151">**Dsbackupfree**</span><span class="sxs-lookup"><span data-stu-id="327d7-151">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="327d7-152">**Dsbackupgetdatabasenames**</span><span class="sxs-lookup"><span data-stu-id="327d7-152">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="327d7-153">**Bft-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="327d7-153">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="327d7-154">Sichern eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="327d7-154">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="327d7-155">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="327d7-155">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

