---
description: Enthält Eingabedaten für eine D3DAUTHENTICATEDQUERY \_ CryptoSession-Abfrage.
ms.assetid: 3a4dead8-fe23-41b4-a167-e0430d09248a
title: D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 76b9d09bcb03dbf3742d551c253d3f4982215757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342528"
---
# <a name="d3dauthenticatedchannel_querycryptosession_input-structure"></a><span data-ttu-id="cb18d-103">D3DAUTHENTICATEDCHANNEL \_ querycryptosession- \_ Eingabe Struktur</span><span class="sxs-lookup"><span data-stu-id="cb18d-103">D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_INPUT structure</span></span>

<span data-ttu-id="cb18d-104">Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY \_ CryptoSession**](d3dauthenticatedquery-cryptosession.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cb18d-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) query.</span></span>

<span data-ttu-id="cb18d-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="cb18d-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb18d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb18d-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DXVA2DecodeHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT;
```



## <a name="members"></a><span data-ttu-id="cb18d-107">Member</span><span class="sxs-lookup"><span data-stu-id="cb18d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cb18d-108">**Input** (Eingabe)</span><span class="sxs-lookup"><span data-stu-id="cb18d-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="cb18d-109">Eine [**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**](d3dauthenticatedchannel-query-input.md) Struktur, die die GUID für die Abfrage und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="cb18d-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="cb18d-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="cb18d-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="cb18d-111">Ein Handle für ein DirectX Video Acceleration 2-Decodergerät (DXVA-2).</span><span class="sxs-lookup"><span data-stu-id="cb18d-111">A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb18d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb18d-112">Requirements</span></span>



| <span data-ttu-id="cb18d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb18d-113">Requirement</span></span> | <span data-ttu-id="cb18d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cb18d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb18d-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb18d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cb18d-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb18d-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cb18d-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb18d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cb18d-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb18d-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cb18d-119">Header</span><span class="sxs-lookup"><span data-stu-id="cb18d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb18d-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb18d-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb18d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb18d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb18d-122">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="cb18d-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="cb18d-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="cb18d-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




