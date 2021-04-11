---
description: Enthält Eingabedaten für eine D3DAUTHENTICATEDQUERY \_ outputidcount-Abfrage.
ms.assetid: cc68b39f-4645-46a6-a752-549b070cf23b
title: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 93f58bcd05efb8c173986186d631c713195d8363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127932"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_input-structure"></a><span data-ttu-id="d3e72-103">D3DAUTHENTICATEDCHANNEL \_ queryoutputidcount- \_ Eingabe Struktur</span><span class="sxs-lookup"><span data-stu-id="d3e72-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT structure</span></span>

<span data-ttu-id="d3e72-104">Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY \_ outputidcount**](d3dauthenticatedquery-outputidcount.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="d3e72-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="d3e72-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="d3e72-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e72-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3e72-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT;
```



## <a name="members"></a><span data-ttu-id="d3e72-107">Member</span><span class="sxs-lookup"><span data-stu-id="d3e72-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3e72-108">**Input** (Eingabe)</span><span class="sxs-lookup"><span data-stu-id="d3e72-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="d3e72-109">Eine [**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**](d3dauthenticatedchannel-query-input.md) Struktur, die die GUID für die Abfrage und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="d3e72-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="d3e72-110">**Geräte**</span><span class="sxs-lookup"><span data-stu-id="d3e72-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="d3e72-111">Ein Handle für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="d3e72-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="d3e72-112">**Cryptosessionhandle**</span><span class="sxs-lookup"><span data-stu-id="d3e72-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="d3e72-113">Ein Handle für die Kryptografiesitzung.</span><span class="sxs-lookup"><span data-stu-id="d3e72-113">A handle to the cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3e72-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3e72-114">Requirements</span></span>



| <span data-ttu-id="d3e72-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3e72-115">Requirement</span></span> | <span data-ttu-id="d3e72-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d3e72-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e72-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3e72-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e72-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3e72-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d3e72-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3e72-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e72-120">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3e72-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d3e72-121">Header</span><span class="sxs-lookup"><span data-stu-id="d3e72-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e72-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e72-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3e72-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3e72-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e72-124">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="d3e72-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="d3e72-125">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="d3e72-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




