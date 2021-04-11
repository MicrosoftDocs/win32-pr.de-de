---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ currentverschlüsseltion. Accessible-Abfrage.
ms.assetid: 66735ce3-c16b-4eca-9283-5d3bc37d73d3
title: D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cfc0075678163b273acad72fa1724cbca8a29cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127924"
---
# <a name="d3dauthenticatedchannel_queryuncompressedencryptionlevel_output-structure"></a><span data-ttu-id="9f740-103">D3DAUTHENTICATEDCHANNEL \_ queryuncompressedencryptionlevel- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="9f740-103">D3DAUTHENTICATEDCHANNEL\_QUERYUNCOMPRESSEDENCRYPTIONLEVEL\_OUTPUT structure</span></span>

<span data-ttu-id="9f740-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ currentverschlüsseltion. Accessible**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="9f740-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) query.</span></span>

<span data-ttu-id="9f740-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="9f740-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f740-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f740-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  GUID                                 EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="9f740-107">Member</span><span class="sxs-lookup"><span data-stu-id="9f740-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9f740-108">**Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="9f740-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="9f740-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="9f740-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="9f740-110">**Verschlüsselungs-GUID**</span><span class="sxs-lookup"><span data-stu-id="9f740-110">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="9f740-111">Eine GUID, die den aktuellen Verschlüsselungstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="9f740-111">A GUID that specifies the current encryption type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f740-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f740-112">Requirements</span></span>



| <span data-ttu-id="9f740-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f740-113">Requirement</span></span> | <span data-ttu-id="9f740-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9f740-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f740-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f740-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9f740-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f740-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9f740-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f740-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9f740-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f740-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9f740-119">Header</span><span class="sxs-lookup"><span data-stu-id="9f740-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f740-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f740-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f740-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f740-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f740-122">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="9f740-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="9f740-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="9f740-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




