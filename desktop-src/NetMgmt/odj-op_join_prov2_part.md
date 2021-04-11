---
title: OP_JOINPROV2_PART
description: OP_JOINPROV2_PART IDL-Definition
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104102523"
---
# <a name="op_joinprov2_part-structure"></a><span data-ttu-id="0719f-103">OP_JOINPROV2_PART Struktur</span><span class="sxs-lookup"><span data-stu-id="0719f-103">OP_JOINPROV2_PART structure</span></span>

<span data-ttu-id="0719f-104">Enthält zusätzliche Informationen, die zum Konfigurieren eines Clients verwendet werden, der einer Domäne hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="0719f-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="0719f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0719f-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a><span data-ttu-id="0719f-106">Member</span><span class="sxs-lookup"><span data-stu-id="0719f-106">Members</span></span>

### <a name="dwflags"></a><span data-ttu-id="0719f-107">dwFlags</span><span class="sxs-lookup"><span data-stu-id="0719f-107">dwFlags</span></span>

<span data-ttu-id="0719f-108">Muss entweder auf NULL oder auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0719f-108">Must be set to either zero or one of the following values:</span></span>

|<span data-ttu-id="0719f-109">Wert</span><span class="sxs-lookup"><span data-stu-id="0719f-109">Value</span></span>|<span data-ttu-id="0719f-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0719f-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="0719f-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="0719f-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span></span>|<span data-ttu-id="0719f-112">Die in "lpsitename" angegebene Site muss als dauerhafter Standort für den Client angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="0719f-112">The site specified in lpSiteName MUST be considered the permanent site for the client.</span></span>|

### <a name="lpnetbiosname"></a><span data-ttu-id="0719f-113">lpnetbiosname</span><span class="sxs-lookup"><span data-stu-id="0719f-113">lpNetbiosName</span></span>

<span data-ttu-id="0719f-114">Enthält den NetBIOS-Namen des Computer Kontos im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="0719f-114">Contains the Netbios name of the machine account in Unicode format.</span></span>

### <a name="lpsitename"></a><span data-ttu-id="0719f-115">lpsitename</span><span class="sxs-lookup"><span data-stu-id="0719f-115">lpSiteName</span></span>

<span data-ttu-id="0719f-116">Enthält den Namen der Active Directory Site, die vom Client verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0719f-116">Contains the name of the Active Directory site that the client should use.</span></span>

### <a name="lpprimarydnsdomain"></a><span data-ttu-id="0719f-117">lpprimarydnsdomain</span><span class="sxs-lookup"><span data-stu-id="0719f-117">lpPrimaryDNSDomain</span></span>

<span data-ttu-id="0719f-118">Enthält den primären DNS-Domänen Namen, den der Client verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="0719f-118">Contains the primary DNS domain name that the client should use.</span></span>

### <a name="dwreserved"></a><span data-ttu-id="0719f-119">dwReserved</span><span class="sxs-lookup"><span data-stu-id="0719f-119">dwReserved</span></span>

<span data-ttu-id="0719f-120">Für zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0719f-120">Reserved for future use and must be set to 0.</span></span>

### <a name="lpreserved"></a><span data-ttu-id="0719f-121">lpReserved</span><span class="sxs-lookup"><span data-stu-id="0719f-121">lpReserved</span></span>

<span data-ttu-id="0719f-122">Für zukünftige Verwendung reserviert und muss auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0719f-122">Reserved for future use and must be set to NULL.</span></span>

## <a name="see-also"></a><span data-ttu-id="0719f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0719f-123">See also</span></span>

[<span data-ttu-id="0719f-124">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="0719f-124">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
