---
description: Enthält den GRL-Header (Global Sperrlist).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: GRL_HEADER Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342785"
---
# <a name="grl_header-structure"></a><span data-ttu-id="49f33-103">GRL- \_ Header Struktur</span><span class="sxs-lookup"><span data-stu-id="49f33-103">GRL\_HEADER structure</span></span>

<span data-ttu-id="49f33-104">Enthält den GRL-Header (Global Sperrlist).</span><span class="sxs-lookup"><span data-stu-id="49f33-104">Contains the global revocation list (GRL) header.</span></span>

## <a name="syntax"></a><span data-ttu-id="49f33-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49f33-105">Syntax</span></span>


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a><span data-ttu-id="49f33-106">Member</span><span class="sxs-lookup"><span data-stu-id="49f33-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="49f33-107">**wszidentifier**</span><span class="sxs-lookup"><span data-stu-id="49f33-107">**wszIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-108">Der GRL-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="49f33-108">The GRL identifier.</span></span> <span data-ttu-id="49f33-109">Der Wert ist immer L "msgrl".</span><span class="sxs-lookup"><span data-stu-id="49f33-109">The value is always L"MSGRL".</span></span>

</dd> <dt>

<span data-ttu-id="49f33-110">**wformatmajor**</span><span class="sxs-lookup"><span data-stu-id="49f33-110">**wFormatMajor**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-111">Die Hauptversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="49f33-111">The major version number.</span></span> <span data-ttu-id="49f33-112">Der Wert muss derzeit 1 lauten.</span><span class="sxs-lookup"><span data-stu-id="49f33-112">Currently the value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-113">**wformatminor**</span><span class="sxs-lookup"><span data-stu-id="49f33-113">**wFormatMinor**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-114">Die Nebenversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="49f33-114">The minor version number.</span></span> <span data-ttu-id="49f33-115">Derzeit muss der Wert 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="49f33-115">Currently the value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-116">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="49f33-116">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-117">Ein **FILETIME** -Wert, der angibt, wann die Datei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="49f33-117">A **FILETIME** value that specifies when the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-118">**dwsequencenumschlag**</span><span class="sxs-lookup"><span data-stu-id="49f33-118">**dwSequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-119">Die GRL-Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="49f33-119">The GRL version number.</span></span> <span data-ttu-id="49f33-120">Der Wert muss aktuell mindestens 3 sein.</span><span class="sxs-lookup"><span data-stu-id="49f33-120">Currently the value must be at least 3</span></span>

</dd> <dt>

<span data-ttu-id="49f33-121">**dwforcerebootversion**</span><span class="sxs-lookup"><span data-stu-id="49f33-121">**dwForceRebootVersion**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-122">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="49f33-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-123">**dwforceprocessrestartversion**</span><span class="sxs-lookup"><span data-stu-id="49f33-123">**dwForceProcessRestartVersion**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-124">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="49f33-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-125">**cbrevocationsectionoffset**</span><span class="sxs-lookup"><span data-stu-id="49f33-125">**cbRevocationSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-126">Der Offset in Bytes vom Anfang der GRL zum Core-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="49f33-126">The offset, in bytes, from the start of the GRL to the Core section.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-127">**"krevokedkernelbinaries"**</span><span class="sxs-lookup"><span data-stu-id="49f33-127">**cRevokedKernelBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-128">Die Anzahl der in der GRL aufgelisteten, gesperrten Kernel-Binärdateien.</span><span class="sxs-lookup"><span data-stu-id="49f33-128">The number of revoked kernel binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-129">**"krevokeduserbinaries"**</span><span class="sxs-lookup"><span data-stu-id="49f33-129">**cRevokedUserBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-130">Die Anzahl der gesperrten Binärdateien im Benutzermodus, die in der GRL aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="49f33-130">The number of revoked user-mode binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-131">**"krevokedzertifikate"**</span><span class="sxs-lookup"><span data-stu-id="49f33-131">**cRevokedCertificates**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-132">Die Anzahl der in der GRL aufgeführten gesperrten Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="49f33-132">The number of revoked certificates listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-133">**ctreudroots**</span><span class="sxs-lookup"><span data-stu-id="49f33-133">**cTrustedRoots**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-134">Die Anzahl der in der GRL aufgelisteten vertrauenswürdigen Stämme.</span><span class="sxs-lookup"><span data-stu-id="49f33-134">The number of trusted roots listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-135">**cbextensiblesectionoffset**</span><span class="sxs-lookup"><span data-stu-id="49f33-135">**cbExtensibleSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-136">Der Offset in Bytes vom Anfang der GRL bis zum Extensible-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="49f33-136">The offset, in bytes, from the start of the GRL to the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-137">**cextensibleentries**</span><span class="sxs-lookup"><span data-stu-id="49f33-137">**cExtensibleEntries**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-138">Die Anzahl der Einträge im Extensible-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="49f33-138">The number of entries in the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-139">**cbrenewalsectionoffset**</span><span class="sxs-lookup"><span data-stu-id="49f33-139">**cbRenewalSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-140">Der Offset in Bytes vom Anfang der GRL bis zum Verlängerungen-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="49f33-140">The offset, in bytes, from the start of the GRL to the Renewals section.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-141">**"krevokedkernelbinaryverlängerungen"**</span><span class="sxs-lookup"><span data-stu-id="49f33-141">**cRevokedKernelBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-142">Die Anzahl der binären Kernel-Erneuerungen, die in der GRL aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="49f33-142">The number of kernel binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-143">**"krevokeduserbinaryerneuerals"**</span><span class="sxs-lookup"><span data-stu-id="49f33-143">**cRevokedUserBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-144">Die Anzahl der Binär Erneuerungen im Benutzermodus, die in der GRL aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="49f33-144">The number of user-mode binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-145">**"krevokedcertificaterenewals"**</span><span class="sxs-lookup"><span data-stu-id="49f33-145">**cRevokedCertificateRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-146">Die Anzahl der Zertifikat Erneuerungen, die in der GRL aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="49f33-146">The number of certificate renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-147">**cbsignaturecoreoffset**</span><span class="sxs-lookup"><span data-stu-id="49f33-147">**cbSignatureCoreOffset**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-148">Der Offset in Bytes vom Anfang der GRL bis zur Kern Abschnitts Signatur.</span><span class="sxs-lookup"><span data-stu-id="49f33-148">The offset, in bytes, from the start of the GRL to the Core section signature.</span></span>

</dd> <dt>

<span data-ttu-id="49f33-149">**cbsignatureexum ffset**</span><span class="sxs-lookup"><span data-stu-id="49f33-149">**cbSignatureExtOffset**</span></span>
</dt> <dd>

<span data-ttu-id="49f33-150">Der Offset in Bytes vom Anfang der GRL bis zur erweiterbaren Abschnitts Signatur.</span><span class="sxs-lookup"><span data-stu-id="49f33-150">The offset, in bytes, from the start of the GRL to the Extensible section signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49f33-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49f33-151">Remarks</span></span>

<span data-ttu-id="49f33-152">Alle ganzzahligen Werte in der GRL haben eine Little-Endian-Byte Reihe.</span><span class="sxs-lookup"><span data-stu-id="49f33-152">All integers in the GRL have little-endian byte ordering.</span></span> <span data-ttu-id="49f33-153">Alle-Strukturen sind auf 1-Byte-Grenzen ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="49f33-153">All structures are aligned to 1-byte boundaries.</span></span>

<span data-ttu-id="49f33-154">Diese Struktur ist nicht in einem SDK-Header deklariert.</span><span class="sxs-lookup"><span data-stu-id="49f33-154">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="49f33-155">Um diese Struktur zu verwenden, fügen Sie die hier gezeigte Deklaration dem Quellcode hinzu.</span><span class="sxs-lookup"><span data-stu-id="49f33-155">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="49f33-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49f33-156">Requirements</span></span>



| <span data-ttu-id="49f33-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49f33-157">Requirement</span></span> | <span data-ttu-id="49f33-158">Wert</span><span class="sxs-lookup"><span data-stu-id="49f33-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49f33-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49f33-159">Minimum supported client</span></span><br/> | <span data-ttu-id="49f33-160">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49f33-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49f33-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49f33-161">Minimum supported server</span></span><br/> | <span data-ttu-id="49f33-162">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49f33-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49f33-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49f33-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f33-164">OPM-Zertifikat Sperrung</span><span class="sxs-lookup"><span data-stu-id="49f33-164">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="49f33-165">OPM-Strukturen</span><span class="sxs-lookup"><span data-stu-id="49f33-165">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




