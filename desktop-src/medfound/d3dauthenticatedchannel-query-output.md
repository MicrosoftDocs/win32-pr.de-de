---
description: 'Enthält die Antwort der IDirect3DAuthenticatedChannel9:: Query-Methode.'
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127936"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a><span data-ttu-id="9a5ad-103">D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="9a5ad-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT structure</span></span>

<span data-ttu-id="9a5ad-104">Enthält die Antwort der [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-104">Contains the response from the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a5ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a5ad-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="9a5ad-106">Member</span><span class="sxs-lookup"><span data-stu-id="9a5ad-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9a5ad-107">**OMAC**</span><span class="sxs-lookup"><span data-stu-id="9a5ad-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="9a5ad-108">Eine [**D3D \_ OMAC**](d3d-omac.md) -Struktur, die einen Nachrichtenauthentifizierungscode (Mac) der Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="9a5ad-109">Der Treiber verwendet einen AES-basierten, einstufigen CBC-MAC (OMAC), um diesen Wert für den Datenblock zu berechnen, der nach diesem Strukturmember angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="9a5ad-110">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="9a5ad-110">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="9a5ad-111">Eine GUID, die die Abfrage angibt.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-111">A GUID that specifies the query.</span></span> <span data-ttu-id="9a5ad-112">Eine Liste der-Werte finden Sie unter [Content Protection-Abfragen](content-protection-queries.md).</span><span class="sxs-lookup"><span data-stu-id="9a5ad-112">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a5ad-113">**Bewältigen**</span><span class="sxs-lookup"><span data-stu-id="9a5ad-113">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="9a5ad-114">Ein Handle für den authentifizierten Kanal.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="9a5ad-115">**UINT**</span><span class="sxs-lookup"><span data-stu-id="9a5ad-115">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="9a5ad-116">Die Abfrage Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-116">The query sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="9a5ad-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="9a5ad-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="9a5ad-118">Der Ergebniscode für die Abfrage.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-118">The result code for the query.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a5ad-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a5ad-119">Remarks</span></span>

<span data-ttu-id="9a5ad-120">Bei den **memytype**-, **hchannel**-und **sequencenenumdermembern** verwendet der Treiber die gleichen Werte, die von der Anwendung in der [**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**](d3dauthenticatedchannel-query-input.md) Struktur bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-120">For the **QueryType**, **hChannel**, and **SequenceNumber** members, the driver uses in the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure.</span></span> <span data-ttu-id="9a5ad-121">Die Anwendung sollte überprüfen, ob diese Werte entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a5ad-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a5ad-122">Requirements</span></span>



| <span data-ttu-id="9a5ad-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a5ad-123">Requirement</span></span> | <span data-ttu-id="9a5ad-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9a5ad-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5ad-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a5ad-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9a5ad-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a5ad-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9a5ad-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a5ad-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9a5ad-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a5ad-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9a5ad-129">Header</span><span class="sxs-lookup"><span data-stu-id="9a5ad-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a5ad-130"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a5ad-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a5ad-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a5ad-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a5ad-132">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="9a5ad-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="9a5ad-133">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="9a5ad-133">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




