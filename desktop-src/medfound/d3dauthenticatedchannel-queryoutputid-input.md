---
description: Enthält Eingabedaten für eine D3DAUTHENTICATEDQUERY \_ OutputID-Abfrage.
ms.assetid: 8864c298-be9a-4ff4-a9c5-996b62937c18
title: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7c64d43261ccc849772372110ad73169c698cd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344016"
---
# <a name="d3dauthenticatedchannel_queryoutputid_input-structure"></a><span data-ttu-id="4df95-103">D3DAUTHENTICATEDCHANNEL \_ queryoutputid- \_ Eingabe Struktur</span><span class="sxs-lookup"><span data-stu-id="4df95-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT structure</span></span>

<span data-ttu-id="4df95-104">Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY \_ OutputID**](d3dauthenticatedquery-outputid.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="4df95-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="4df95-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="4df95-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="4df95-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4df95-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
  UINT                                OutputIDIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT;
```



## <a name="members"></a><span data-ttu-id="4df95-107">Member</span><span class="sxs-lookup"><span data-stu-id="4df95-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4df95-108">**Input** (Eingabe)</span><span class="sxs-lookup"><span data-stu-id="4df95-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="4df95-109">Eine [**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**](d3dauthenticatedchannel-query-input.md) Struktur, die die GUID für die Abfrage und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="4df95-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="4df95-110">**Geräte**</span><span class="sxs-lookup"><span data-stu-id="4df95-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="4df95-111">Ein Handle für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="4df95-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="4df95-112">**Cryptosessionhandle**</span><span class="sxs-lookup"><span data-stu-id="4df95-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="4df95-113">Ein Handle für die Kryptografiesitzung.</span><span class="sxs-lookup"><span data-stu-id="4df95-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="4df95-114">**Outputidindex**</span><span class="sxs-lookup"><span data-stu-id="4df95-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="4df95-115">Der Index der Ausgabe-ID.</span><span class="sxs-lookup"><span data-stu-id="4df95-115">The index of the output ID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4df95-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4df95-116">Requirements</span></span>



| <span data-ttu-id="4df95-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4df95-117">Requirement</span></span> | <span data-ttu-id="4df95-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4df95-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4df95-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4df95-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4df95-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4df95-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4df95-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4df95-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4df95-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4df95-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4df95-123">Header</span><span class="sxs-lookup"><span data-stu-id="4df95-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4df95-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4df95-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df95-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4df95-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df95-126">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="4df95-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="4df95-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="4df95-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




