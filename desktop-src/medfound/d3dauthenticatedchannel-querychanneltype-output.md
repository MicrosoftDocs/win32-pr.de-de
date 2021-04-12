---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ channelType-Abfrage.
ms.assetid: 547f7f26-2b9d-48b1-97cc-84a2202c3900
title: D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3120669da69f13359f49d8b8c38ed7d3e211a8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393290"
---
# <a name="d3dauthenticatedchannel_querychanneltype_output-structure"></a><span data-ttu-id="c2447-103">D3DAUTHENTICATEDCHANNEL \_ querychanneltype- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="c2447-103">D3DAUTHENTICATEDCHANNEL\_QUERYCHANNELTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="c2447-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ channelType**](d3dauthenticatedquery-channeltype.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c2447-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) query.</span></span>

<span data-ttu-id="c2447-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="c2447-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2447-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2447-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DAUTHENTICATEDCHANNELTYPE          ChannelType;
} D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="c2447-107">Member</span><span class="sxs-lookup"><span data-stu-id="c2447-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2447-108">**Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="c2447-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="c2447-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="c2447-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="c2447-110">**ChannelType**</span><span class="sxs-lookup"><span data-stu-id="c2447-110">**ChannelType**</span></span>
</dt> <dd>

<span data-ttu-id="c2447-111">Ein [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) -Wert, der den Kanaltyp angibt.</span><span class="sxs-lookup"><span data-stu-id="c2447-111">A [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) value that specifies the channel type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2447-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2447-112">Requirements</span></span>



| <span data-ttu-id="c2447-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2447-113">Requirement</span></span> | <span data-ttu-id="c2447-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c2447-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2447-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2447-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c2447-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2447-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c2447-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2447-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c2447-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2447-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c2447-119">Header</span><span class="sxs-lookup"><span data-stu-id="c2447-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2447-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2447-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2447-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2447-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2447-122">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="c2447-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="c2447-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="c2447-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




