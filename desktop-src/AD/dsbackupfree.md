---
title: Dsbackupfree-Funktion (ntdsbcli. h)
description: Gibt Arbeitsspeicher frei, der durch die Active Directory Domain Services Sicherungs-und Wiederherstellungs Funktionen zugeordnet
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Dsbackupfree-Funktions Active Directory
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27855eeb3417eede371357528457248857c3e626
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858832"
---
# <a name="dsbackupfree-function"></a><span data-ttu-id="f348e-104">Dsbackupfree-Funktion</span><span class="sxs-lookup"><span data-stu-id="f348e-104">DsBackupFree function</span></span>

<span data-ttu-id="f348e-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f348e-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f348e-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f348e-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f348e-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="f348e-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="f348e-108">Die **dsbackupfree** -Funktion gibt Arbeitsspeicher frei, der durch die Active Directory Domain Services Sicherungs-und Wiederherstellungs Funktionen belegt wird</span><span class="sxs-lookup"><span data-stu-id="f348e-108">The **DsBackupFree** function releases memory allocated by the Active Directory Domain Services backup and restore functions.</span></span> <span data-ttu-id="f348e-109">Die folgenden Funktionen weisen Arbeitsspeicher zu, der mit der **dsbackupfree** -Funktion freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="f348e-109">The following functions allocate memory that must be released with the **DsBackupFree** function.</span></span>

-   [<span data-ttu-id="f348e-110">**Dsbackupgetbackuplogs**</span><span class="sxs-lookup"><span data-stu-id="f348e-110">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
-   [<span data-ttu-id="f348e-111">**Dsbackupgetdatabasenames**</span><span class="sxs-lookup"><span data-stu-id="f348e-111">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
-   [<span data-ttu-id="f348e-112">**Dsbackupprepare**</span><span class="sxs-lookup"><span data-stu-id="f348e-112">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
-   [<span data-ttu-id="f348e-113">**Dsrestoregetdatabaselocations**</span><span class="sxs-lookup"><span data-stu-id="f348e-113">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a><span data-ttu-id="f348e-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="f348e-114">Syntax</span></span>


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="f348e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f348e-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f348e-116">*pvbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f348e-116">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f348e-117">Ein Zeiger auf den Speicherpuffer, der freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f348e-117">Pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f348e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f348e-118">Return value</span></span>

<span data-ttu-id="f348e-119">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f348e-119">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f348e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f348e-120">Requirements</span></span>



| <span data-ttu-id="f348e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f348e-121">Requirement</span></span> | <span data-ttu-id="f348e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f348e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f348e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f348e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f348e-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f348e-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f348e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f348e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f348e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f348e-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f348e-127">Header</span><span class="sxs-lookup"><span data-stu-id="f348e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f348e-128"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="f348e-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="f348e-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f348e-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="f348e-130"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f348e-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="f348e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f348e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f348e-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f348e-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f348e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f348e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f348e-134">**Dsbackupgetbackuplogs**</span><span class="sxs-lookup"><span data-stu-id="f348e-134">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="f348e-135">**Dsbackupgetdatabasenames**</span><span class="sxs-lookup"><span data-stu-id="f348e-135">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="f348e-136">**Dsbackupprepare**</span><span class="sxs-lookup"><span data-stu-id="f348e-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="f348e-137">**Dsrestoregetdatabaselocations**</span><span class="sxs-lookup"><span data-stu-id="f348e-137">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="f348e-138">Sichern eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="f348e-138">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="f348e-139">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="f348e-139">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

