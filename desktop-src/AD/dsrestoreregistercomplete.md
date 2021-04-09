---
title: Dsrestoreregistercomplete-Funktion (ntdsbcli. h)
description: Wird aufgerufen, um einen Active Directory Server zu entsperren, nachdem ein Wiederherstellungs Vorgang beendet wurde.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Dsrestoreregistercomplete-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5e5e01b29281860dff59fbcd08a3b48ec66c4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040726"
---
# <a name="dsrestoreregistercomplete-function"></a><span data-ttu-id="15175-104">Dsrestoreregistercomplete-Funktion</span><span class="sxs-lookup"><span data-stu-id="15175-104">DsRestoreRegisterComplete function</span></span>

<span data-ttu-id="15175-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="15175-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="15175-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="15175-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="15175-107">Verwenden Sie stattdessen [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="15175-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="15175-108">Die **dsrestoreregistercomplete** -Funktion wird aufgerufen, um einen Active Directory Server zu entsperren, nachdem ein Wiederherstellungs Vorgang beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="15175-108">The **DsRestoreRegisterComplete** function is called to unlock an Active Directory server after a restore operation is complete.</span></span> <span data-ttu-id="15175-109">Diese Funktion ist Gegenstück zur [**dsrestoreregiester**](dsrestoreregister.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="15175-109">This function is counterpart to the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="15175-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="15175-110">Syntax</span></span>


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a><span data-ttu-id="15175-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="15175-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15175-112">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15175-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15175-113">Enthält das Wiederherstellungs Kontext Handle, das mit der [**dsrestoreprepare**](dsrestoreprepare.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="15175-113">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="15175-114">*hrrestorestate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15175-114">*hrRestoreState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15175-115">Enthält den endgültigen Status des Wiederherstellungs Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="15175-115">Contains the final status of the restore operation.</span></span> <span data-ttu-id="15175-116">Dieser Parameter sollte **S \_ OK** enthalten, wenn der Wiederherstellungs Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="15175-116">This parameter should contain **S\_OK** if the restore operation was successful or an error code otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15175-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15175-117">Return value</span></span>

<span data-ttu-id="15175-118">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="15175-118">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="15175-119">In der folgenden Liste sind die möglichen Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="15175-119">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="15175-120">**Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="15175-120">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="15175-121">Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="15175-121">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="15175-122">Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15175-122">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15175-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15175-123">Remarks</span></span>

<span data-ttu-id="15175-124">Bevor Sie den Domänen Controller neu starten, können Sie diese Funktion zum Bereitstellen des Status des Wiederherstellungs Vorgangs abrufen.</span><span class="sxs-lookup"><span data-stu-id="15175-124">Before you restart the domain controller, call this function to provide the status of the restore operation.</span></span> <span data-ttu-id="15175-125">Wenn der Status nicht erfolgreich ist, wird der Verzeichnisdienst erst gestartet, wenn eine gültige Datenbank wieder hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="15175-125">If the status is not successful, the directory service will not start until a valid database has been restored.</span></span> <span data-ttu-id="15175-126">Diese Funktion schließt den Wiederherstellungs Vorgang ab und ermöglicht es, Active Directory Domain Services zu starten.</span><span class="sxs-lookup"><span data-stu-id="15175-126">This function completes the restore operation and allows Active Directory Domain Services to start.</span></span>

## <a name="requirements"></a><span data-ttu-id="15175-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15175-127">Requirements</span></span>



| <span data-ttu-id="15175-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15175-128">Requirement</span></span> | <span data-ttu-id="15175-129">Wert</span><span class="sxs-lookup"><span data-stu-id="15175-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15175-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15175-130">Minimum supported client</span></span><br/> | <span data-ttu-id="15175-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="15175-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="15175-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15175-132">Minimum supported server</span></span><br/> | <span data-ttu-id="15175-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="15175-133">None supported</span></span><br/>                                                               |
| <span data-ttu-id="15175-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="15175-134">End of client support</span></span><br/>    | <span data-ttu-id="15175-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="15175-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="15175-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="15175-136">End of server support</span></span><br/>    | <span data-ttu-id="15175-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="15175-137">None supported</span></span><br/>                                                               |
| <span data-ttu-id="15175-138">Header</span><span class="sxs-lookup"><span data-stu-id="15175-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="15175-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="15175-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="15175-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="15175-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="15175-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15175-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="15175-142">DLL</span><span class="sxs-lookup"><span data-stu-id="15175-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15175-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15175-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15175-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15175-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15175-145">**Dsrestoreregiester**</span><span class="sxs-lookup"><span data-stu-id="15175-145">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="15175-146">**Dsrestoreprepare**</span><span class="sxs-lookup"><span data-stu-id="15175-146">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="15175-147">**Dssetauthidentity**</span><span class="sxs-lookup"><span data-stu-id="15175-147">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="15175-148">Wiederherstellen eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="15175-148">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="15175-149">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="15175-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

