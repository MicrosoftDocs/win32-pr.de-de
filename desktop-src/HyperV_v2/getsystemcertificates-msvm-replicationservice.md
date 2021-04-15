---
description: Ruft die System Zertifikate auf einem Host System ab.
ms.assetid: d470a57d-85b9-4d31-bb2c-9b6f21e2860d
title: Getsystemzertifikate-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetSystemCertificates
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5464d420b7fc019a0829d7255dafb1716e5e9f5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525241"
---
# <a name="getsystemcertificates-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="f0246-103">Getsystemzertifikate-Methode der MSVM \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="f0246-103">GetSystemCertificates method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="f0246-104">Ruft die System Zertifikate auf einem Host System ab.</span><span class="sxs-lookup"><span data-stu-id="f0246-104">Retrieves the system certificates on a host system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0246-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0246-105">Syntax</span></span>


```mof
uint32 GetSystemCertificates(
  [out] string EncodedCertificates[]
);
```



## <a name="parameters"></a><span data-ttu-id="f0246-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0246-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0246-107">*Encodzertifikate* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0246-107">*EncodedCertificates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0246-108">Bei erfolgreicher Ausführung empfängt die Zertifikate, die im persönlichen Speicher für den lokalen Computer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f0246-108">If successful, receives the certificates available from the Personal store for the local machine.</span></span> <span data-ttu-id="f0246-109">Jeder Eintrag ist eine Basis 64-codierte Zertifikat Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f0246-109">Each entry is a base 64 encoded certificate string.</span></span> <span data-ttu-id="f0246-110">Diese Zeichenfolge kann in ein Bytearray konvertiert werden, indem ein X509Certificate2-Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f0246-110">This string can be converted to a byte array by constructing an X509Certificate2 object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0246-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0246-111">Return value</span></span>

<span data-ttu-id="f0246-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="f0246-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f0246-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="f0246-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="f0246-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="f0246-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="f0246-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="f0246-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="f0246-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="f0246-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="f0246-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-121">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="f0246-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="f0246-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="f0246-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="f0246-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="f0246-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f0246-126">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="f0246-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f0246-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0246-127">Requirements</span></span>



| <span data-ttu-id="f0246-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0246-128">Requirement</span></span> | <span data-ttu-id="f0246-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f0246-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0246-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0246-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f0246-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0246-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f0246-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0246-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f0246-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0246-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0246-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0246-134">Namespace</span></span><br/>                | <span data-ttu-id="f0246-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f0246-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f0246-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f0246-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0246-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f0246-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0246-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f0246-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0246-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0246-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f0246-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0246-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0246-141">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="f0246-141">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

 




