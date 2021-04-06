---
title: Dssetcurrentbackuplog-Funktion (ntdsbcli. h)
description: Legt die aktuelle Sicherungs Protokollnummer nach einer erfolgreichen Wiederherstellung fest.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Dssetcurrentbackuplog-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859022"
---
# <a name="dssetcurrentbackuplog-function"></a><span data-ttu-id="de453-104">Dssetcurrentbackuplog-Funktion</span><span class="sxs-lookup"><span data-stu-id="de453-104">DsSetCurrentBackupLog function</span></span>

<span data-ttu-id="de453-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="de453-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="de453-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="de453-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="de453-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="de453-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="de453-108">Die **dssetcurrentbackuplog** -Funktion legt die aktuelle Sicherungs Protokollnummer nach einer erfolgreichen Wiederherstellung fest.</span><span class="sxs-lookup"><span data-stu-id="de453-108">The **DsSetCurrentBackupLog** function sets the current backup log number after a successful restore.</span></span> <span data-ttu-id="de453-109">Da Active Directory Domain Services nur zirkuläre Protokollierung unterstützen, wird diese Funktion normalerweise nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="de453-109">Because Active Directory Domain Services only support circular logging, this function is not normally used.</span></span>

## <a name="syntax"></a><span data-ttu-id="de453-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="de453-110">Syntax</span></span>


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a><span data-ttu-id="de453-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="de453-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de453-112">*szservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de453-112">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de453-113">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Servers enthält, für den die Sicherungs Protokollnummer festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="de453-113">Pointer to a null-terminated string that contains the name of the server to set the backup log number for.</span></span> <span data-ttu-id="de453-114">Vorangehende umgekehrte Schrägstriche sind optional.</span><span class="sxs-lookup"><span data-stu-id="de453-114">Preceding backslashes are optional.</span></span> <span data-ttu-id="de453-115">Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="de453-115">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="de453-116">Der Servername darf keine Unterstriche ( \_ ) enthalten.</span><span class="sxs-lookup"><span data-stu-id="de453-116">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="de453-117">Ein Beispiel für einen Servernamen ist " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="de453-117">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="de453-118">*dwcurrentlog* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de453-118">*dwCurrentLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de453-119">Enthält die festzulegende Sicherungs Protokollnummer.</span><span class="sxs-lookup"><span data-stu-id="de453-119">Contains the backup log number to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de453-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de453-120">Return value</span></span>

<span data-ttu-id="de453-121">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="de453-121">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="de453-122">In der folgenden Liste sind die möglichen Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="de453-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="de453-123">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="de453-123">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="de453-124">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="de453-124">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="de453-125">**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="de453-125">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="de453-126">Es ist ein Fehler bei der Speicher Belegung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="de453-126">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de453-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de453-127">Remarks</span></span>

<span data-ttu-id="de453-128">Es ist normalerweise nicht erforderlich, die **dssetcurrentbackuplog** -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="de453-128">It is not normally required to call the **DsSetCurrentBackupLog** function.</span></span> <span data-ttu-id="de453-129">Die Sicherungsfunktionen bestimmen und legen die zuletzt gesicherte Protokollnummer automatisch fest.</span><span class="sxs-lookup"><span data-stu-id="de453-129">The backup functions automatically determine and set the last log number backed up.</span></span> <span data-ttu-id="de453-130">Verwenden Sie **dssetcurrentbackuplog** , um zu verhindern, dass eine andere inkrementelle Sicherung erfolgreich durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de453-130">Use **DsSetCurrentBackupLog** to prevent another incremental backup from succeeding until a full backup is performed.</span></span>

## <a name="requirements"></a><span data-ttu-id="de453-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de453-131">Requirements</span></span>



| <span data-ttu-id="de453-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de453-132">Requirement</span></span> | <span data-ttu-id="de453-133">Wert</span><span class="sxs-lookup"><span data-stu-id="de453-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de453-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de453-134">Minimum supported client</span></span><br/> | <span data-ttu-id="de453-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de453-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de453-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de453-136">Minimum supported server</span></span><br/> | <span data-ttu-id="de453-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de453-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de453-138">Header</span><span class="sxs-lookup"><span data-stu-id="de453-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="de453-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="de453-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="de453-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de453-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="de453-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de453-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="de453-142">DLL</span><span class="sxs-lookup"><span data-stu-id="de453-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de453-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de453-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="de453-144">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="de453-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="de453-145">**Dssetcurrentbackuplogw** (Unicode) und **dssetcurrentbackuploga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="de453-145">**DsSetCurrentBackupLogW** (Unicode) and **DsSetCurrentBackupLogA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="de453-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de453-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de453-147">Sichern und Wiederherstellen eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="de453-147">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="de453-148">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="de453-148">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

