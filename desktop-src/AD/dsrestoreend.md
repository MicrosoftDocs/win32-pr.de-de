---
title: Dsrestoreend-Funktion (ntdsbcli. h)
description: Wird aufgerufen, um einen Wiederherstellungs Vorgang zu beenden.
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- Dsrestoreend-Funktions Active Directory
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabbe216875c2fe934f3c87e32688cd17bc8992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040515"
---
# <a name="dsrestoreend-function"></a><span data-ttu-id="6fd76-104">Dsrestoreend-Funktion</span><span class="sxs-lookup"><span data-stu-id="6fd76-104">DsRestoreEnd function</span></span>

<span data-ttu-id="6fd76-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6fd76-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6fd76-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6fd76-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6fd76-107">Verwenden Sie stattdessen [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="6fd76-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="6fd76-108">Die **dsrestoreend** -Funktion wird aufgerufen, um einen Wiederherstellungs Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="6fd76-108">The **DsRestoreEnd** function is called to terminate a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd76-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fd76-109">Syntax</span></span>


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="6fd76-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fd76-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fd76-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6fd76-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fd76-112">Enthält das Wiederherstellungs Kontext Handle, das mit der [**dsrestoreprepare**](dsrestoreprepare.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6fd76-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fd76-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6fd76-113">Return value</span></span>

<span data-ttu-id="6fd76-114">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6fd76-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="6fd76-115">In der folgenden Liste sind die möglichen Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fd76-115">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="6fd76-116">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="6fd76-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="6fd76-117">*HBC* ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6fd76-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fd76-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fd76-118">Remarks</span></span>

<span data-ttu-id="6fd76-119">Die **dsrestoreend** -Funktion schließt ausstehende Bindungs Handles und führt einen Bereinigungs Vorgang nach einem Wiederherstellungs Versuch aus.</span><span class="sxs-lookup"><span data-stu-id="6fd76-119">The **DsRestoreEnd** function closes outstanding binding handles and performs a cleanup operation after a restore attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd76-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fd76-120">Requirements</span></span>



| <span data-ttu-id="6fd76-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fd76-121">Requirement</span></span> | <span data-ttu-id="6fd76-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6fd76-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd76-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fd76-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6fd76-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6fd76-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6fd76-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fd76-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6fd76-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6fd76-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6fd76-127">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6fd76-127">End of client support</span></span><br/>    | <span data-ttu-id="6fd76-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6fd76-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6fd76-129">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6fd76-129">End of server support</span></span><br/>    | <span data-ttu-id="6fd76-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6fd76-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6fd76-131">Header</span><span class="sxs-lookup"><span data-stu-id="6fd76-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fd76-132"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fd76-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="6fd76-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6fd76-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="6fd76-134"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fd76-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="6fd76-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6fd76-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fd76-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fd76-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fd76-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fd76-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd76-138">**Dsrestoreprepare**</span><span class="sxs-lookup"><span data-stu-id="6fd76-138">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="6fd76-139">Wiederherstellen eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="6fd76-139">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="6fd76-140">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="6fd76-140">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

