---
title: Dsbackuptruneurelogs-Funktion (ntdsbcli. h)
description: Verkürzt die zuvor gelesenen Sicherungs Protokolle.
ms.assetid: fae2e19f-08b8-410f-a735-dd4d41fc71a6
ms.tgt_platform: multiple
keywords:
- Dsbackuptruneurelogs-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupTruncateLogs
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051ced828656c6b6e5af156e2d1a69c3b741cdce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517666"
---
# <a name="dsbackuptruncatelogs-function"></a><span data-ttu-id="995fc-104">Dsbackuptruneurelogs-Funktion</span><span class="sxs-lookup"><span data-stu-id="995fc-104">DsBackupTruncateLogs function</span></span>

<span data-ttu-id="995fc-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="995fc-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="995fc-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="995fc-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="995fc-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="995fc-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="995fc-108">Die **dsbackuptruneurelogs** -Funktion verkürzt die zuvor gelesenen Sicherungs Protokolle.</span><span class="sxs-lookup"><span data-stu-id="995fc-108">The **DsBackupTruncateLogs** function truncates the previously read backup logs.</span></span>

## <a name="syntax"></a><span data-ttu-id="995fc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="995fc-109">Syntax</span></span>


```C++
HRESULT DsBackupTruncateLogs(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="995fc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="995fc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="995fc-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="995fc-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="995fc-112">Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="995fc-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="995fc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="995fc-113">Return value</span></span>

<span data-ttu-id="995fc-114">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="995fc-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="995fc-115">In der folgenden Liste sind andere mögliche Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="995fc-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="995fc-116">**Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="995fc-116">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="995fc-117">Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="995fc-117">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="995fc-118">Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="995fc-118">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="995fc-119">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="995fc-119">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="995fc-120">*HBC* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="995fc-120">*hbc* is invalid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="995fc-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="995fc-121">Remarks</span></span>

<span data-ttu-id="995fc-122">Verwenden Sie die Funktion **dsbackuptruneurelogs** , wenn eine vollständige oder inkrementelle Sicherung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="995fc-122">Use the **DsBackupTruncateLogs** function when a full or incremental backup has completed successfully.</span></span>

> [!Caution]  
> <span data-ttu-id="995fc-123">Wenn diese Funktion nach einer differenziellen Sicherung aufgerufen wird, gehen alle Informationen zur inkrementellen Sicherung verloren.</span><span class="sxs-lookup"><span data-stu-id="995fc-123">If this function is called after a differential backup, all of the incremental backup information will be lost.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="995fc-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="995fc-124">Requirements</span></span>



| <span data-ttu-id="995fc-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="995fc-125">Requirement</span></span> | <span data-ttu-id="995fc-126">Wert</span><span class="sxs-lookup"><span data-stu-id="995fc-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="995fc-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="995fc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="995fc-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="995fc-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="995fc-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="995fc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="995fc-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="995fc-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="995fc-131">Header</span><span class="sxs-lookup"><span data-stu-id="995fc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="995fc-132"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="995fc-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="995fc-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="995fc-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="995fc-134"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="995fc-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="995fc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="995fc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="995fc-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="995fc-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="995fc-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="995fc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="995fc-138">**Dsbackupprepare**</span><span class="sxs-lookup"><span data-stu-id="995fc-138">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="995fc-139">**Dsbackupgetbackuplogs**</span><span class="sxs-lookup"><span data-stu-id="995fc-139">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="995fc-140">**Dssetcurrentbackuplog**</span><span class="sxs-lookup"><span data-stu-id="995fc-140">**DsSetCurrentBackupLog**</span></span>](dssetcurrentbackuplog.md)
</dt> <dt>

[<span data-ttu-id="995fc-141">Sichern eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="995fc-141">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="995fc-142">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="995fc-142">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

