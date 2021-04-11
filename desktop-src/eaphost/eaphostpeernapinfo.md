---
title: Eaphosteternapinfo-Struktur (eaphostpeer-APIs. h)
description: Enthält die Netzwerk Zugriffsschutz-Informationen (Network Access Protection, NAP) für einen EAP-Supplicant.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- Eaphosteternapinfo-Struktur EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040924"
---
# <a name="eaphostpeernapinfo-structure"></a><span data-ttu-id="c2985-104">Eaphostpeer-Napinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="c2985-104">EapHostPeerNapInfo structure</span></span>

<span data-ttu-id="c2985-105">Die **eaphostpeernapinfo** -Struktur enthält die Netzwerk Zugriffsschutz-Informationen (Network Access Protection, NAP) für einen EAP-Supplicant.</span><span class="sxs-lookup"><span data-stu-id="c2985-105">The **EapHostPeerNapInfo** structure contains the Network Access Protection (NAP) information on an EAP supplicant.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2985-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2985-106">Syntax</span></span>


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a><span data-ttu-id="c2985-107">Member</span><span class="sxs-lookup"><span data-stu-id="c2985-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2985-108">**isolationstate**</span><span class="sxs-lookup"><span data-stu-id="c2985-108">**isolationState**</span></span>
</dt> <dd>

<span data-ttu-id="c2985-109">Eine [**Isolations \_ Zustands**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) Struktur, die den NAP-Isolations Status eines Computers angibt.</span><span class="sxs-lookup"><span data-stu-id="c2985-109">An [**ISOLATION\_STATE**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) structure that specifies the NAP isolation state of a computer.</span></span> <span data-ttu-id="c2985-110">Der Isolations Zustand bestimmt die Ebene des gewährten Netzwerk Zugriffs.</span><span class="sxs-lookup"><span data-stu-id="c2985-110">The isolation state determines the level of network access granted.</span></span>

</dd> <dt>

<span data-ttu-id="c2985-111">**probationtime**</span><span class="sxs-lookup"><span data-stu-id="c2985-111">**probationTime**</span></span>
</dt> <dd>

<span data-ttu-id="c2985-112">Eine **probationtime** -Struktur, die die Zeit angibt, die benötigt wird, um die Verbindung außerhalb der Quarantäne zu stellen, nach der die Verbindung getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="c2985-112">A **ProbationTime** structure that specifies the time required for the connection to come out of quarantine after which the connection will be dropped.</span></span> <span data-ttu-id="c2985-113">Eine **probationtime** -Struktur ist mit einer [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur identisch.</span><span class="sxs-lookup"><span data-stu-id="c2985-113">A **ProbationTime** structure is identical to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c2985-114">**stringcorrelationidlength**</span><span class="sxs-lookup"><span data-stu-id="c2985-114">**stringCorrelationIdLength**</span></span>
</dt> <dd>

<span data-ttu-id="c2985-115">Die Länge (in Byte) der NAP- [stringcorrelationid](/windows/desktop/NAP/nap-datatypes) , die dieser Struktur folgt.</span><span class="sxs-lookup"><span data-stu-id="c2985-115">The length, in bytes, of the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) that follows this structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2985-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2985-116">Remarks</span></span>

<span data-ttu-id="c2985-117">Die **eaphostpeer-Napinfo** -Struktur ist der NAP- [stringcorrelationid](/windows/desktop/NAP/nap-datatypes) des Datentyps **WCHAR** im RPC-Bytestream vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="c2985-117">The **EapHostPeerNapInfo** structure precedes the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) of data type **WCHAR** in the RPC byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2985-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2985-118">Requirements</span></span>



| <span data-ttu-id="c2985-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2985-119">Requirement</span></span> | <span data-ttu-id="c2985-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c2985-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2985-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2985-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c2985-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2985-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c2985-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2985-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c2985-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2985-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c2985-125">Header</span><span class="sxs-lookup"><span data-stu-id="c2985-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2985-126"><dt>Eaphostpeer-APIs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2985-126"><dt>Eaphostpeerapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2985-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2985-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2985-128">EAPHost-Supplicant-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c2985-128">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="c2985-129">**Eaphostpeergetauthstatus**</span><span class="sxs-lookup"><span data-stu-id="c2985-129">**EapHostPeerGetAuthStatus**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[<span data-ttu-id="c2985-130">**Eaphostpeer-methodauthparametriams**</span><span class="sxs-lookup"><span data-stu-id="c2985-130">**EapHostPeerMethodAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

