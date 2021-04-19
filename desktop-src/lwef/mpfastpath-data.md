---
title: MPFASTPATH_DATA Struktur (mpclient. h)
description: FastPath-Aktualisierungs Benachrichtigung.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- MPFASTPATH_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPFASTPATH_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342007"
---
# <a name="mpfastpath_data-structure"></a><span data-ttu-id="7c884-105">Mpfastpath- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="7c884-105">MPFASTPATH\_DATA structure</span></span>

<span data-ttu-id="7c884-106">FastPath-Aktualisierungs Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="7c884-106">FastPath update notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c884-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c884-107">Syntax</span></span>


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a><span data-ttu-id="7c884-108">Member</span><span class="sxs-lookup"><span data-stu-id="7c884-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c884-109">**SignatureType**</span><span class="sxs-lookup"><span data-stu-id="7c884-109">**SignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="7c884-110">Typ: **[ **MP- \_ Signatur \_ Typen**](mp-signature-type.md)**</span><span class="sxs-lookup"><span data-stu-id="7c884-110">Type: **[**MP\_SIGNATURE\_TYPE**](mp-signature-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7c884-111">Signaturtyp.</span><span class="sxs-lookup"><span data-stu-id="7c884-111">Signature type.</span></span>

</dd> <dt>

<span data-ttu-id="7c884-112">**Fastpathsignaturetype**</span><span class="sxs-lookup"><span data-stu-id="7c884-112">**FastPathSignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="7c884-113">Typ: **[ **MP- \_ FastPath- \_ Typ**](mp-fastpath-type.md)**</span><span class="sxs-lookup"><span data-stu-id="7c884-113">Type: **[**MP\_FASTPATH\_TYPE**](mp-fastpath-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7c884-114">FastPath-Signaturtyp.</span><span class="sxs-lookup"><span data-stu-id="7c884-114">FastPath signature type.</span></span>

</dd> <dt>

<span data-ttu-id="7c884-115">**Fastpathsignatureversion**</span><span class="sxs-lookup"><span data-stu-id="7c884-115">**FastPathSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7c884-116">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7c884-116">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7c884-117">FastPath-Signatur Version (optional).</span><span class="sxs-lookup"><span data-stu-id="7c884-117">FastPath signature version (optional).</span></span>

</dd> <dt>

<span data-ttu-id="7c884-118">**Compilationtimestamp**</span><span class="sxs-lookup"><span data-stu-id="7c884-118">**CompilationTimestamp**</span></span>
</dt> <dd>

<span data-ttu-id="7c884-119">Typ: **ularge \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="7c884-119">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="7c884-120">Kompilierungszeit Stempel (UTC).</span><span class="sxs-lookup"><span data-stu-id="7c884-120">Compilation timestamp (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="7c884-121">**PersistenceType**</span><span class="sxs-lookup"><span data-stu-id="7c884-121">**PersistenceType**</span></span>
</dt> <dd>

<span data-ttu-id="7c884-122">Typ: **[ **MP \_ - \_ persistenzlimit- \_ Typ**](mp-persistence-limit-type.md)**</span><span class="sxs-lookup"><span data-stu-id="7c884-122">Type: **[**MP\_PERSISTENCE\_LIMIT\_TYPE**](mp-persistence-limit-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7c884-123">Persistenztyp (optional).</span><span class="sxs-lookup"><span data-stu-id="7c884-123">Persistence type (optional).</span></span>

</dd> <dt>

<span data-ttu-id="7c884-124">**Persistencevalue**</span><span class="sxs-lookup"><span data-stu-id="7c884-124">**PersistenceValue**</span></span>
</dt> <dd>

<span data-ttu-id="7c884-125">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7c884-125">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7c884-126">Persistenzwert (optional).</span><span class="sxs-lookup"><span data-stu-id="7c884-126">Persistence value (optional).</span></span>

</dd> <dt>

<span data-ttu-id="7c884-127">**Persistencepath**</span><span class="sxs-lookup"><span data-stu-id="7c884-127">**PersistencePath**</span></span>
</dt> <dd>

<span data-ttu-id="7c884-128">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7c884-128">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7c884-129">Persistenzpfad (optional).</span><span class="sxs-lookup"><span data-stu-id="7c884-129">Persistence path (optional).</span></span>

</dd> <dt>

<span data-ttu-id="7c884-130">**`Reason`**</span><span class="sxs-lookup"><span data-stu-id="7c884-130">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="7c884-131">Typ: **[ **MP- \_ Entfernungs \_ Grund**](mp-removal-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="7c884-131">Type: **[**MP\_REMOVAL\_REASON**](mp-removal-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7c884-132">Grund für das Entfernen der Signatur.</span><span class="sxs-lookup"><span data-stu-id="7c884-132">Reason for signature removal.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c884-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c884-133">Requirements</span></span>



| <span data-ttu-id="7c884-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c884-134">Requirement</span></span> | <span data-ttu-id="7c884-135">Wert</span><span class="sxs-lookup"><span data-stu-id="7c884-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c884-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c884-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7c884-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c884-137">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7c884-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c884-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7c884-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c884-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c884-140">Header</span><span class="sxs-lookup"><span data-stu-id="7c884-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c884-141"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c884-141"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c884-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c884-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c884-143">**MP- \_ FastPath- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="7c884-143">**MP\_FASTPATH\_TYPE**</span></span>](mp-fastpath-type.md)
</dt> <dt>

[<span data-ttu-id="7c884-144">**MP \_ - \_ persistenzgrenzwert \_**</span><span class="sxs-lookup"><span data-stu-id="7c884-144">**MP\_PERSISTENCE\_LIMIT\_TYPE**</span></span>](mp-persistence-limit-type.md)
</dt> <dt>

[<span data-ttu-id="7c884-145">**MP- \_ Signatur \_ Typen**</span><span class="sxs-lookup"><span data-stu-id="7c884-145">**MP\_SIGNATURE\_TYPE**</span></span>](mp-signature-type.md)
</dt> </dl>

 

 





