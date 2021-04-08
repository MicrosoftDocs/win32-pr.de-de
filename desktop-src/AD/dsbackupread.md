---
title: Dsbackupread-Funktion (ntdsbcli. h)
description: Liest einen Datenblock aus der aktuellen geöffneten Datei in einen Puffer.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Dsbackupread-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409c2a7d93503aad4edff88070c0458efc961d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949783"
---
# <a name="dsbackupread-function"></a><span data-ttu-id="1669f-104">Dsbackupread-Funktion</span><span class="sxs-lookup"><span data-stu-id="1669f-104">DsBackupRead function</span></span>

<span data-ttu-id="1669f-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1669f-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1669f-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1669f-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1669f-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="1669f-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="1669f-108">Die **dsbackupread** -Funktion liest einen Datenblock aus der aktuellen geöffneten Datei in einen Puffer.</span><span class="sxs-lookup"><span data-stu-id="1669f-108">The **DsBackupRead** function reads a block of data from the current open file, into a buffer.</span></span> <span data-ttu-id="1669f-109">Es wird erwartet, dass die Client Anwendung diese Funktion wiederholt aufruft, bis die gesamte Sicherungsdatei empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="1669f-109">The client application is expected to call this function repeatedly until the entire backup file has been received.</span></span> <span data-ttu-id="1669f-110">Die [**dsbackupopenfile**](dsbackupopenfile.md) -Funktion stellt die gesamte Größe der Sicherungsdatei bereit.</span><span class="sxs-lookup"><span data-stu-id="1669f-110">The [**DsBackupOpenFile**](dsbackupopenfile.md) function provides the entire size of the backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1669f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1669f-111">Syntax</span></span>


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="1669f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1669f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1669f-113">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1669f-113">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1669f-114">Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="1669f-114">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1669f-115">*pvbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1669f-115">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1669f-116">Zeiger auf einen Puffer, der die Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="1669f-116">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="1669f-117">Dieser Puffer muss mindestens eine Größe von *cbbuffer* Bytes aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1669f-117">This buffer must be at least *cbBuffer* bytes in size.</span></span>

</dd> <dt>

<span data-ttu-id="1669f-118">*cbbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1669f-118">*cbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1669f-119">Enthält die Größe (in Bytes) des Puffers bei *pvbuffer*.</span><span class="sxs-lookup"><span data-stu-id="1669f-119">Contains the size, in bytes, of the buffer at *pvBuffer*.</span></span> <span data-ttu-id="1669f-120">Dieser Wert muss ein Vielfaches von 8192 sein und muss größer oder gleich 24576 sein.</span><span class="sxs-lookup"><span data-stu-id="1669f-120">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="1669f-121">*pcbread* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1669f-121">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1669f-122">Ein Zeiger auf einen **DWORD** -Wert, der die tatsächliche Anzahl von gelesenen Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="1669f-122">Pointer to a **DWORD** value that receives the actual number of bytes read.</span></span> <span data-ttu-id="1669f-123">Dies kann weniger als die Anzahl der angeforderten Bytes sein, da einige Transporte den übertragenen Puffer fragmentieren, anstatt den gesamten Puffer mit Daten zu füllen.</span><span class="sxs-lookup"><span data-stu-id="1669f-123">This may be less than the number of bytes requested because some transports fragment the buffer being transmitted instead of filling the entire buffer with data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1669f-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1669f-124">Return value</span></span>

<span data-ttu-id="1669f-125">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1669f-125">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="1669f-126">Folgende Fehlercodes sind möglich:</span><span class="sxs-lookup"><span data-stu-id="1669f-126">Possible error codes include the following.</span></span>

<dl> <dt>

<span data-ttu-id="1669f-127">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="1669f-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="1669f-128">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1669f-128">One or more parameters are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1669f-129">**Fehler \_ handle \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="1669f-129">**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd>

<span data-ttu-id="1669f-130">Das Ende der Sicherungsdatei wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="1669f-130">The end of the backup file was reached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1669f-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1669f-131">Requirements</span></span>



| <span data-ttu-id="1669f-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1669f-132">Requirement</span></span> | <span data-ttu-id="1669f-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1669f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1669f-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1669f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1669f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1669f-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1669f-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1669f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1669f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1669f-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1669f-138">Header</span><span class="sxs-lookup"><span data-stu-id="1669f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1669f-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="1669f-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="1669f-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1669f-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="1669f-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1669f-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="1669f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1669f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1669f-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1669f-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1669f-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1669f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1669f-145">**Dsbackupopenfile**</span><span class="sxs-lookup"><span data-stu-id="1669f-145">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="1669f-146">**Dsbackupprepare**</span><span class="sxs-lookup"><span data-stu-id="1669f-146">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="1669f-147">**Dsbackupfree**</span><span class="sxs-lookup"><span data-stu-id="1669f-147">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="1669f-148">Sichern eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="1669f-148">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="1669f-149">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="1669f-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

