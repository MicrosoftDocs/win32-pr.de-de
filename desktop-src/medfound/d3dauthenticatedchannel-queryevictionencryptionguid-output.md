---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY- \_ verschlüsselungszugriffbleguid-Abfrage.
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8fa46095c5075b0a36ed691978b73de1e7b8cade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861804"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a><span data-ttu-id="ae88b-103">D3DAUTHENTICATEDCHANNEL \_ queryevictionverschlüsseltionguid- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="ae88b-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT structure</span></span>

<span data-ttu-id="ae88b-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY- \_ verschlüsselungszugriffbleguid**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="ae88b-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="ae88b-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="ae88b-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae88b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae88b-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="ae88b-107">Member</span><span class="sxs-lookup"><span data-stu-id="ae88b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ae88b-108">**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="ae88b-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="ae88b-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="ae88b-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="ae88b-110">**Verschlüsselungsguidindex**</span><span class="sxs-lookup"><span data-stu-id="ae88b-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="ae88b-111">Der Index der Verschlüsselungs-GUID.</span><span class="sxs-lookup"><span data-stu-id="ae88b-111">The index of the encryption GUID.</span></span>

</dd> <dt>

<span data-ttu-id="ae88b-112">**Verschlüsselungs-GUID**</span><span class="sxs-lookup"><span data-stu-id="ae88b-112">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="ae88b-113">Eine GUID, die einen unterstützten Verschlüsselungstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="ae88b-113">A GUID that specifies a supported encryption type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae88b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae88b-114">Requirements</span></span>



| <span data-ttu-id="ae88b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae88b-115">Requirement</span></span> | <span data-ttu-id="ae88b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ae88b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae88b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae88b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ae88b-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae88b-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ae88b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae88b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ae88b-120">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae88b-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ae88b-121">Header</span><span class="sxs-lookup"><span data-stu-id="ae88b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae88b-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae88b-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae88b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae88b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae88b-124">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="ae88b-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="ae88b-125">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="ae88b-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




