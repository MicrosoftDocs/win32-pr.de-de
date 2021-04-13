---
title: OP_CERT_SST_STORE
description: OP_CERT_SST_STORE IDL-Definition
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 294d21d730e1cce478088cddb43686706217ec5b
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104391300"
---
# <a name="op_cert_sst_store-structure"></a><span data-ttu-id="a796b-103">OP_CERT_SST_STORE Struktur</span><span class="sxs-lookup"><span data-stu-id="a796b-103">OP_CERT_SST_STORE structure</span></span>

<span data-ttu-id="a796b-104">Enthält einen serialisierten Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="a796b-104">Contains a serialized certificate store.</span></span>

## <a name="syntax"></a><span data-ttu-id="a796b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a796b-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a><span data-ttu-id="a796b-106">Member</span><span class="sxs-lookup"><span data-stu-id="a796b-106">Members</span></span>

### <a name="storelocation"></a><span data-ttu-id="a796b-107">StoreLocation</span><span class="sxs-lookup"><span data-stu-id="a796b-107">StoreLocation</span></span>

<span data-ttu-id="a796b-108">Enthält einen Bezeichner für den Zertifikat Speicher der [**System Speicherorte**](../seccrypto/system-store-locations.md).</span><span class="sxs-lookup"><span data-stu-id="a796b-108">Contains an identifier for the certificate store from [**System Store Locations**](../seccrypto/system-store-locations.md).</span></span>

### <a name="pstorename"></a><span data-ttu-id="a796b-109">pstorename</span><span class="sxs-lookup"><span data-stu-id="a796b-109">pStoreName</span></span>

<span data-ttu-id="a796b-110">Enthält den Namen des Stores.</span><span class="sxs-lookup"><span data-stu-id="a796b-110">Contains the name of the store.</span></span>

### <a name="cbsst"></a><span data-ttu-id="a796b-111">cbsst</span><span class="sxs-lookup"><span data-stu-id="a796b-111">cbSst</span></span>

<span data-ttu-id="a796b-112">Enthält die Größe des Psst in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a796b-112">Contains the size of pSst in bytes.</span></span>

### <a name="psst"></a><span data-ttu-id="a796b-113">Psst</span><span class="sxs-lookup"><span data-stu-id="a796b-113">pSst</span></span>

<span data-ttu-id="a796b-114">Enthält einen serialisierten Zertifikat Speicher (siehe [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span><span class="sxs-lookup"><span data-stu-id="a796b-114">Contains a serialized certificate store (see [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span></span>

## <a name="see-also"></a><span data-ttu-id="a796b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a796b-115">See also</span></span>

[<span data-ttu-id="a796b-116">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="a796b-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)