---
title: MPTHREAT_INFOEX_BEHAVIOR Struktur (mpclient. h)
description: Enthält Verhaltens Änderungs spezifische Informationen.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- MPTHREAT_INFOEX_BEHAVIOR Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_INFOEX_BEHAVIOR Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743176"
---
# <a name="mpthreat_infoex_behavior-structure"></a><span data-ttu-id="e0e6e-105">Mpthreat- \_ INFOEX- \_ Verhaltens Struktur</span><span class="sxs-lookup"><span data-stu-id="e0e6e-105">MPTHREAT\_INFOEX\_BEHAVIOR structure</span></span>

<span data-ttu-id="e0e6e-106">Enthält Verhaltens Änderungs spezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="e0e6e-106">Contains behavior modification-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e6e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0e6e-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a><span data-ttu-id="e0e6e-108">Member</span><span class="sxs-lookup"><span data-stu-id="e0e6e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0e6e-109">**SignatureId**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-109">**SignatureID**</span></span>
</dt> <dd>

<span data-ttu-id="e0e6e-110">Typ: **ularge \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-110">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="e0e6e-111">Signatur-ID der Verhaltensänderung, die von der Engine zum Zeitpunkt der Erkennung angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e0e6e-111">Behavior modification signature ID given by the engine at the time of detection.</span></span>

</dd> <dt>

<span data-ttu-id="e0e6e-112">**EngineVersion**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-112">**EngineVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e0e6e-113">Typ: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-113">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="e0e6e-114">Engine-Modulversion.</span><span class="sxs-lookup"><span data-stu-id="e0e6e-114">Engine module version.</span></span>

</dd> <dt>

<span data-ttu-id="e0e6e-115">**Asdelta-signatureversion**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-115">**ASDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e0e6e-116">Typ: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-116">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="e0e6e-117">AntiSpyware-Signatur Version.</span><span class="sxs-lookup"><span data-stu-id="e0e6e-117">Antispyware signature version.</span></span>

</dd> <dt>

<span data-ttu-id="e0e6e-118">**Avdelta-signatureversion**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-118">**AVDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e0e6e-119">Typ: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-119">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="e0e6e-120">Antivirus-Signatur Version</span><span class="sxs-lookup"><span data-stu-id="e0e6e-120">Antivirus signature version</span></span>

</dd> <dt>

<span data-ttu-id="e0e6e-121">**Hashtyp**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-121">**HashType**</span></span>
</dt> <dd>

<span data-ttu-id="e0e6e-122">Typ: **[ **MP \_ - \_ Hashtyp**](mp-hash-type.md)**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-122">Type: **[**MP\_HASH\_TYPE**](mp-hash-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0e6e-123">Der verwendete Hashtyp.</span><span class="sxs-lookup"><span data-stu-id="e0e6e-123">Hash type used.</span></span> <span data-ttu-id="e0e6e-124">Siehe [**MP \_ - \_ Hashtyp**](mp-hash-type.md).</span><span class="sxs-lookup"><span data-stu-id="e0e6e-124">See [**MP\_HASH\_TYPE**](mp-hash-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0e6e-125">**"Fdelta-Wert"**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-125">**FidelityValue**</span></span>
</dt> <dd>

<span data-ttu-id="e0e6e-126">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e0e6e-127">Fidelity-Wert.</span><span class="sxs-lookup"><span data-stu-id="e0e6e-127">Fidelity value.</span></span>

</dd> <dt>

<span data-ttu-id="e0e6e-128">**Hashwert**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-128">**HashValue**</span></span>
</dt> <dd>

<span data-ttu-id="e0e6e-129">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="e0e6e-130">Der Hash der Datei.</span><span class="sxs-lookup"><span data-stu-id="e0e6e-130">The hash of the file.</span></span>

</dd> <dt>

<span data-ttu-id="e0e6e-131">**TargetFileName**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-131">**TargetFileName**</span></span>
</dt> <dd>

<span data-ttu-id="e0e6e-132">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="e0e6e-133">Der Pfad und der Name der Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="e0e6e-133">The path and name of the targeted file.</span></span>

</dd> <dt>

<span data-ttu-id="e0e6e-134">**Targetflehash**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-134">**TargetFileHash**</span></span>
</dt> <dd>

<span data-ttu-id="e0e6e-135">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="e0e6e-136">Der Hash der Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="e0e6e-136">The hash of the targeted file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0e6e-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0e6e-137">Requirements</span></span>



| <span data-ttu-id="e0e6e-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0e6e-138">Requirement</span></span> | <span data-ttu-id="e0e6e-139">Wert</span><span class="sxs-lookup"><span data-stu-id="e0e6e-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e6e-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0e6e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e0e6e-141">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0e6e-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e0e6e-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0e6e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e0e6e-143">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0e6e-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0e6e-144">Header</span><span class="sxs-lookup"><span data-stu-id="e0e6e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0e6e-145"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0e6e-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0e6e-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0e6e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e6e-147">**MP \_ - \_ Hashtyp**</span><span class="sxs-lookup"><span data-stu-id="e0e6e-147">**MP\_HASH\_TYPE**</span></span>](mp-hash-type.md)
</dt> </dl>

 

 





