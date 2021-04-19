---
description: Enthält Informationen zu einem Smartcard-Kryptografiedienstanbieter (CSP).
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: KERB_SMARTCARD_CSP_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 03b1a8084e291dde5a4f1f2017e4e97f57640bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363524"
---
# <a name="kerb_smartcard_csp_info-structure"></a><span data-ttu-id="77653-103">KERB \_ Smartcard- \_ CSP- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="77653-103">KERB\_SMARTCARD\_CSP\_INFO structure</span></span>

<span data-ttu-id="77653-104">Die **Info Struktur der KERB \_ Smartcard- \_ CSP \_** enthält Informationen zu einem Smartcard- [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="77653-104">The **KERB\_SMARTCARD\_CSP\_INFO** structure contains information about a smart card [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="77653-105">Diese Struktur ist nicht in einem öffentlichen Header deklariert.</span><span class="sxs-lookup"><span data-stu-id="77653-105">This structure is not declared in a public header.</span></span>

## <a name="syntax"></a><span data-ttu-id="77653-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="77653-106">Syntax</span></span>


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a><span data-ttu-id="77653-107">Member</span><span class="sxs-lookup"><span data-stu-id="77653-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="77653-108">**dwcspinfolen**</span><span class="sxs-lookup"><span data-stu-id="77653-108">**dwCspInfoLen**</span></span>
</dt> <dd>

<span data-ttu-id="77653-109">Die Größe der-Struktur in Bytes, einschließlich angefügter Daten.</span><span class="sxs-lookup"><span data-stu-id="77653-109">The size, in bytes, of this structure, including any appended data.</span></span>

</dd> <dt>

<span data-ttu-id="77653-110">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="77653-110">**MessageType**</span></span>
</dt> <dd>

<span data-ttu-id="77653-111">Der Typ der Nachricht, die übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="77653-111">The type of message being passed.</span></span> <span data-ttu-id="77653-112">Dieser Member muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="77653-112">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="77653-113">**ContextInformation**</span><span class="sxs-lookup"><span data-stu-id="77653-113">**ContextInformation**</span></span>
</dt> <dd>

<span data-ttu-id="77653-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="77653-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="77653-115">**SpaceHolderForWow64**</span><span class="sxs-lookup"><span data-stu-id="77653-115">**SpaceHolderForWow64**</span></span>
</dt> <dd>

<span data-ttu-id="77653-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="77653-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="77653-117">**flags**</span><span class="sxs-lookup"><span data-stu-id="77653-117">**flags**</span></span>
</dt> <dd>

<span data-ttu-id="77653-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="77653-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="77653-119">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="77653-119">**KeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="77653-120">Der private Schlüssel, der aus dem Schlüssel Container verwendet werden soll, der im Puffer- **BBuffer** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="77653-120">The private key to use from the key container specified within the buffer **bBuffer**.</span></span> <span data-ttu-id="77653-121">Der Schlüssel kann einer der folgenden Werte sein, die in Wincrypt. h definiert sind.</span><span class="sxs-lookup"><span data-stu-id="77653-121">The key can be one of the following values, defined in WinCrypt.h.</span></span>



| <span data-ttu-id="77653-122">Wert</span><span class="sxs-lookup"><span data-stu-id="77653-122">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="77653-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="77653-123">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="77653-124"><dt>**Um \_ Keyexchange**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="77653-124"><dt>**AT\_KEYEXCHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="77653-125">Der Schlüssel ist ein Schlüsselaustausch Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="77653-125">The key is a key-exchange key.</span></span><br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="77653-126"><dt>**Um \_ Signatur**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="77653-126"><dt>**AT\_SIGNATURE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="77653-127">Der Schlüssel ist ein Signatur Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="77653-127">The key is a signature key.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="77653-128">**ncardnameoffset**</span><span class="sxs-lookup"><span data-stu-id="77653-128">**nCardNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="77653-129">Die Anzahl der Zeichen im **BBuffer** -Puffer, die dem Namen der Smartcard in diesem Puffer vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="77653-129">The number of characters in the **bBuffer** buffer that precede the name of the smart card in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77653-130">Wenn der Name der Smartcard nicht angegeben wird, muss der Puffer eine leere Zeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="77653-130">If the name of the smart card is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="77653-131">**nreadernameoffset**</span><span class="sxs-lookup"><span data-stu-id="77653-131">**nReaderNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="77653-132">Die Anzahl der Zeichen im **BBuffer** -Puffer, die dem Namen des smartcardreaders in diesem Puffer vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="77653-132">The number of characters in the **bBuffer** buffer that precede the name of the smart card reader in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77653-133">Wenn der Name des smartcardreaders nicht angegeben wird, muss der Puffer eine leere Zeichenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="77653-133">If the name of the smart card reader is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="77653-134">**ncontainernameoffset**</span><span class="sxs-lookup"><span data-stu-id="77653-134">**nContainerNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="77653-135">Die Anzahl der Zeichen im **BBuffer** -Puffer, die dem Namen des Schlüssel Containers in diesem Puffer vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="77653-135">The number of characters in the **bBuffer** buffer that precede the name of the key container in that buffer.</span></span> <span data-ttu-id="77653-136">Diese Zeichenfolge darf nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="77653-136">This string cannot be empty.</span></span>

</dd> <dt>

<span data-ttu-id="77653-137">**ncspnameoffset**</span><span class="sxs-lookup"><span data-stu-id="77653-137">**nCSPNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="77653-138">Die Anzahl der Zeichen im **BBuffer** -Puffer, die dem Namen des CSP in diesem Puffer vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="77653-138">The number of characters in the **bBuffer** buffer that precede the name of the CSP in that buffer.</span></span>

</dd> <dt>

<span data-ttu-id="77653-139">**BBuffer**</span><span class="sxs-lookup"><span data-stu-id="77653-139">**bBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="77653-140">Ein Array von Zeichen, die auf eine Länge von initialisiert werden `sizeof(DWORD)` .</span><span class="sxs-lookup"><span data-stu-id="77653-140">An array of characters initialized to a length of `sizeof(DWORD)`.</span></span> <span data-ttu-id="77653-141">Dieser Puffer enthält die Namen, auf die durch die Member **ncardnameoffset**, **nreadernameoffset**, **ncontainernameoffset** und **ncspnameoffset** verwiesen wird, sowie alle zusätzlichen Daten, die vom CSP bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="77653-141">This buffer contains the names referred to by the **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset**, and **nCSPNameOffset** members, as well as any additional data provided by the CSP.</span></span>

<span data-ttu-id="77653-142">Alle Namen, die nicht bereitgestellt werden, müssen in diesem Puffer durch leere Zeichen folgen dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="77653-142">Any names that are not provided must be represented in this buffer by empty strings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77653-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77653-143">Remarks</span></span>

<span data-ttu-id="77653-144">Wenn diese Struktur serialisiert wird, müssen die Strukturmember an Grenzen ausgerichtet werden, die ein Vielfaches von 2 Bytes sind.</span><span class="sxs-lookup"><span data-stu-id="77653-144">When this structure is serialized, the structure members must be aligned to boundaries that are multiples of 2 bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="77653-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77653-145">Requirements</span></span>



| <span data-ttu-id="77653-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77653-146">Requirement</span></span> | <span data-ttu-id="77653-147">Wert</span><span class="sxs-lookup"><span data-stu-id="77653-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="77653-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77653-148">Minimum supported client</span></span><br/> | <span data-ttu-id="77653-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77653-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="77653-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77653-150">Minimum supported server</span></span><br/> | <span data-ttu-id="77653-151">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77653-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77653-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77653-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77653-153">**KERB \_ Zertifikat \_ Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="77653-153">**KERB\_CERTIFICATE\_LOGON**</span></span>](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
