---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY- \_ verschlüsselungsreferengen-accessibleguidcount-Abfrage.
ms.assetid: 168f9455-8dc6-473a-ad2c-e51996b63650
title: D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 51668dccdfa15649ec2a062a1231eb0b16e68ff8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340136"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguidcount_output-structure"></a><span data-ttu-id="e0aac-103">D3DAUTHENTICATEDCHANNEL \_ queryevictionverschlüsseltionguidcount- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="e0aac-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUIDCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="e0aac-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY- \_ verschlüsselungsreferengen-accessibleguidcount**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="e0aac-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) query.</span></span>

<span data-ttu-id="e0aac-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="e0aac-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0aac-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0aac-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  NumEncryptionGuids                   UINT;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="e0aac-107">Member</span><span class="sxs-lookup"><span data-stu-id="e0aac-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0aac-108">**Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="e0aac-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="e0aac-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="e0aac-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="e0aac-110">**UINT**</span><span class="sxs-lookup"><span data-stu-id="e0aac-110">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="e0aac-111">Die Anzahl der Verschlüsselungs-GUIDs.</span><span class="sxs-lookup"><span data-stu-id="e0aac-111">The number of encryption GUIDs.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0aac-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0aac-112">Requirements</span></span>



| <span data-ttu-id="e0aac-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0aac-113">Requirement</span></span> | <span data-ttu-id="e0aac-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e0aac-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0aac-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0aac-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e0aac-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0aac-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e0aac-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0aac-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e0aac-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0aac-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e0aac-119">Header</span><span class="sxs-lookup"><span data-stu-id="e0aac-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0aac-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0aac-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0aac-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0aac-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0aac-122">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="e0aac-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="e0aac-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="e0aac-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




