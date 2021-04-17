---
title: Dsbackupclose-Funktion (ntdsbcli. h)
description: Schließt eine Sicherungsdatei, die mit der dsbackupopenfile-Funktion geöffnet wurde.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- Dsbackupclose-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d03c9cd7f125d223d264236a52120714d5198c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476359"
---
# <a name="dsbackupclose-function"></a><span data-ttu-id="eda8d-104">Dsbackupclose-Funktion</span><span class="sxs-lookup"><span data-stu-id="eda8d-104">DsBackupClose function</span></span>

<span data-ttu-id="eda8d-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="eda8d-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eda8d-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="eda8d-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="eda8d-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="eda8d-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="eda8d-108">Die **dsbackupclose** -Funktion schließt eine Sicherungsdatei, die mit der [**dsbackupopenfile**](dsbackupopenfile.md) -Funktion geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="eda8d-108">The **DsBackupClose** function closes a backup file opened with the [**DsBackupOpenFile**](dsbackupopenfile.md) function.</span></span> <span data-ttu-id="eda8d-109">Für jedes Sicherungs Handle kann jeweils nur eine Datei geöffnet werden. Daher schließt diese Funktion die aktuell geöffnete Datei.</span><span class="sxs-lookup"><span data-stu-id="eda8d-109">For each backup handle, only one file can be opened at a time, so this function closes the currently open file.</span></span>

## <a name="syntax"></a><span data-ttu-id="eda8d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="eda8d-110">Syntax</span></span>


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="eda8d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="eda8d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eda8d-112">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eda8d-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eda8d-113">Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="eda8d-113">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eda8d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eda8d-114">Return value</span></span>

<span data-ttu-id="eda8d-115">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="eda8d-115">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="eda8d-116">In der folgenden Liste sind andere mögliche Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="eda8d-116">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="eda8d-117">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="eda8d-117">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="eda8d-118">*HBC* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="eda8d-118">*hbc* is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eda8d-119">**hrinvalidhandle**</span><span class="sxs-lookup"><span data-stu-id="eda8d-119">**hrInvalidHandle**</span></span>
</dt> <dd>

<span data-ttu-id="eda8d-120">Zurzeit ist keine Datei geöffnet.</span><span class="sxs-lookup"><span data-stu-id="eda8d-120">No file is currently open.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eda8d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eda8d-121">Requirements</span></span>



| <span data-ttu-id="eda8d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eda8d-122">Requirement</span></span> | <span data-ttu-id="eda8d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="eda8d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eda8d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eda8d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eda8d-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eda8d-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eda8d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eda8d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eda8d-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eda8d-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eda8d-128">Header</span><span class="sxs-lookup"><span data-stu-id="eda8d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eda8d-129"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="eda8d-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="eda8d-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eda8d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="eda8d-131"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eda8d-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="eda8d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="eda8d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eda8d-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eda8d-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eda8d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eda8d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eda8d-135">**Dsbackupopenfile**</span><span class="sxs-lookup"><span data-stu-id="eda8d-135">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="eda8d-136">**Dsbackupprepare**</span><span class="sxs-lookup"><span data-stu-id="eda8d-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="eda8d-137">Sichern eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="eda8d-137">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="eda8d-138">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="eda8d-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

