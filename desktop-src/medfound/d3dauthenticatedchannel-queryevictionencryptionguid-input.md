---
description: Enthält Eingabedaten für eine D3DAUTHENTICATEDQUERY- \_ verschlüsselungszugangs-accessibleguid-Abfrage.
ms.assetid: 0e24e393-3f63-4c6f-aca1-f73ced3490ba
title: D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1c4500d27577883f46d00580dcc7e306b4008cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393286"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_input-structure"></a><span data-ttu-id="9c197-103">D3DAUTHENTICATEDCHANNEL \_ queryevictionverschlüsseltionguid- \_ Eingabe Struktur</span><span class="sxs-lookup"><span data-stu-id="9c197-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT structure</span></span>

<span data-ttu-id="9c197-104">Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY- \_ verschlüsselungszugangs-accessibleguid**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="9c197-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="9c197-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="9c197-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c197-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c197-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                EncryptionGuidIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT;
```



## <a name="members"></a><span data-ttu-id="9c197-107">Member</span><span class="sxs-lookup"><span data-stu-id="9c197-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9c197-108">**Input** (Eingabe)</span><span class="sxs-lookup"><span data-stu-id="9c197-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="9c197-109">Eine [**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**](d3dauthenticatedchannel-query-input.md) Struktur, die die GUID für die Abfrage und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="9c197-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="9c197-110">**Verschlüsselungsguidindex**</span><span class="sxs-lookup"><span data-stu-id="9c197-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="9c197-111">Der Index der Verschlüsselungs-GUID.</span><span class="sxs-lookup"><span data-stu-id="9c197-111">The index of the encryption GUID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c197-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c197-112">Requirements</span></span>



| <span data-ttu-id="9c197-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c197-113">Requirement</span></span> | <span data-ttu-id="9c197-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9c197-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c197-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c197-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9c197-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c197-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9c197-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c197-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9c197-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c197-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9c197-119">Header</span><span class="sxs-lookup"><span data-stu-id="9c197-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c197-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c197-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c197-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c197-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c197-122">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="9c197-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="9c197-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="9c197-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




