---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY- \_ Schutz Abfrage.
ms.assetid: eb99089a-5e8e-4970-9c40-7f6a9662b5ec
title: D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: d68cafdf545d93a290e90c54be134977e51de4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524603"
---
# <a name="d3dauthenticatedchannel_queryprotection_output-structure"></a><span data-ttu-id="f779b-103">D3DAUTHENTICATEDCHANNEL \_ queryprotection- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="f779b-103">D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT structure</span></span>

<span data-ttu-id="f779b-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY- \_ Schutz**](d3dauthenticatedquery-protection.md) Abfrage.</span><span class="sxs-lookup"><span data-stu-id="f779b-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_PROTECTION**](d3dauthenticatedquery-protection.md) query.</span></span>

<span data-ttu-id="f779b-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="f779b-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="f779b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f779b-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT     Output;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS ProtectionFlags;
} D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="f779b-107">Member</span><span class="sxs-lookup"><span data-stu-id="f779b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f779b-108">**Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="f779b-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="f779b-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="f779b-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="f779b-110">**Schutzflags**</span><span class="sxs-lookup"><span data-stu-id="f779b-110">**ProtectionFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f779b-111">Eine [**D3DAUTHENTICATEDCHANNEL \_ Protection \_ Flags**](d3dauthenticatedchannel-protection-flags.md) -Struktur, die die Schutz Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="f779b-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f779b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f779b-112">Requirements</span></span>



| <span data-ttu-id="f779b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f779b-113">Requirement</span></span> | <span data-ttu-id="f779b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f779b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f779b-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f779b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f779b-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f779b-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f779b-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f779b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f779b-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f779b-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f779b-119">Header</span><span class="sxs-lookup"><span data-stu-id="f779b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f779b-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f779b-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f779b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f779b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f779b-122">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="f779b-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="f779b-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="f779b-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




