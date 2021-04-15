---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ outputidcount-Abfrage.
ms.assetid: 8b9fa0dc-bbe5-4382-8acc-59aeadfca825
title: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 86a840de2b36b7089b31d15e8375c17a0610b77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484091"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_output-structure"></a><span data-ttu-id="b2233-103">D3DAUTHENTICATEDCHANNEL \_ queryoutputidcount- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="b2233-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="b2233-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ outputidcount**](d3dauthenticatedquery-outputidcount.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="b2233-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="b2233-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="b2233-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2233-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2233-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
  HANDLE                               CryptoSessionHandle;
  UINT                                 NumOutputIDs;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="b2233-107">Member</span><span class="sxs-lookup"><span data-stu-id="b2233-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2233-108">**Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="b2233-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="b2233-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="b2233-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="b2233-110">**Geräte**</span><span class="sxs-lookup"><span data-stu-id="b2233-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="b2233-111">Ein Handle für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="b2233-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="b2233-112">**Cryptosessionhandle**</span><span class="sxs-lookup"><span data-stu-id="b2233-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="b2233-113">Ein Handle für die Kryptografiesitzung.</span><span class="sxs-lookup"><span data-stu-id="b2233-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="b2233-114">**Numoutputids**</span><span class="sxs-lookup"><span data-stu-id="b2233-114">**NumOutputIDs**</span></span>
</dt> <dd>

<span data-ttu-id="b2233-115">Die Anzahl der Ausgabe-IDs, die dem angegebenen Gerät und der Kryptografiesitzung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b2233-115">The number of output IDs associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2233-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2233-116">Requirements</span></span>



| <span data-ttu-id="b2233-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2233-117">Requirement</span></span> | <span data-ttu-id="b2233-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b2233-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2233-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2233-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2233-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2233-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b2233-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2233-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2233-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2233-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b2233-123">Header</span><span class="sxs-lookup"><span data-stu-id="b2233-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2233-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2233-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2233-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2233-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2233-126">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="b2233-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="b2233-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="b2233-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




