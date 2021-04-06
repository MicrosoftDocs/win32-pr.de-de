---
title: Dsbackupend-Funktion (ntdsbcli. h)
description: Wird aufgerufen, um einen Sicherungs Vorgang zu beenden.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Dsbackupend-Funktions Active Directory
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9663eedec7bc298ef594990baababcf2083546e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858833"
---
# <a name="dsbackupend-function"></a><span data-ttu-id="25ccf-104">Dsbackupend-Funktion</span><span class="sxs-lookup"><span data-stu-id="25ccf-104">DsBackupEnd function</span></span>

<span data-ttu-id="25ccf-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="25ccf-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="25ccf-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="25ccf-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="25ccf-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="25ccf-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="25ccf-108">Die **dsbackupend** -Funktion wird aufgerufen, um einen Sicherungs Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="25ccf-108">The **DsBackupEnd** function is called to terminate a backup operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="25ccf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="25ccf-109">Syntax</span></span>


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="25ccf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="25ccf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25ccf-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25ccf-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ccf-112">Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="25ccf-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25ccf-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25ccf-113">Return value</span></span>

<span data-ttu-id="25ccf-114">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="25ccf-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="25ccf-115">In der folgenden Liste sind andere mögliche Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="25ccf-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="25ccf-116">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="25ccf-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="25ccf-117">*HBC* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="25ccf-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25ccf-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25ccf-118">Remarks</span></span>

<span data-ttu-id="25ccf-119">Die **dsbackupend** -Funktion schließt ausstehende Bindungs Handles und führt nach einem erfolgreichen oder nicht erfolgreichen Sicherungs Versuch eine Bereinigung durch.</span><span class="sxs-lookup"><span data-stu-id="25ccf-119">The **DsBackupEnd** function closes outstanding binding handles and performs a cleanup after a successful or unsuccessful backup attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="25ccf-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25ccf-120">Requirements</span></span>



| <span data-ttu-id="25ccf-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25ccf-121">Requirement</span></span> | <span data-ttu-id="25ccf-122">Wert</span><span class="sxs-lookup"><span data-stu-id="25ccf-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25ccf-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25ccf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="25ccf-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25ccf-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25ccf-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25ccf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="25ccf-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25ccf-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25ccf-127">Header</span><span class="sxs-lookup"><span data-stu-id="25ccf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="25ccf-128"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="25ccf-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="25ccf-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25ccf-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="25ccf-130"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25ccf-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="25ccf-131">DLL</span><span class="sxs-lookup"><span data-stu-id="25ccf-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25ccf-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25ccf-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25ccf-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25ccf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ccf-134">**Dssetauthidentity**</span><span class="sxs-lookup"><span data-stu-id="25ccf-134">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="25ccf-135">Sichern eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="25ccf-135">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="25ccf-136">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="25ccf-136">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

