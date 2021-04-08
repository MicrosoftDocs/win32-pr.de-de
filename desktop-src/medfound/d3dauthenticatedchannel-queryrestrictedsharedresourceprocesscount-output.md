---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocesscount-Abfrage.
ms.assetid: dd6286d8-dfb5-413a-ba38-8b99dc8fe305
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 60568e7056ab9df7aafcec1cac7864685c7c6100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749313"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocesscount_output-structure"></a><span data-ttu-id="8c0d1-103">D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocesscount- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="8c0d1-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="8c0d1-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocesscount**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) query.</span></span>

<span data-ttu-id="8c0d1-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="8c0d1-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0d1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c0d1-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumRestrictedSharedResourceProcesses;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="8c0d1-107">Member</span><span class="sxs-lookup"><span data-stu-id="8c0d1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c0d1-108">**Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="8c0d1-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="8c0d1-110">**Numrestrictedsharedresourceprocesses**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-110">**NumRestrictedSharedResourceProcesses**</span></span>
</dt> <dd>

<span data-ttu-id="8c0d1-111">Die Anzahl der Prozesse, die zum Öffnen von freigegebenen Ressourcen mit eingeschränktem Zugriff zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-111">The number of processes allowed to open shared resources that have restricted access.</span></span> <span data-ttu-id="8c0d1-112">Ein Prozess kann eine solche Ressource nur dann öffnen, wenn dem Prozess der Zugriff gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-112">A process cannot open such a resource unless the process has been granted access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c0d1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c0d1-113">Requirements</span></span>



| <span data-ttu-id="8c0d1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c0d1-114">Requirement</span></span> | <span data-ttu-id="8c0d1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8c0d1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0d1-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c0d1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8c0d1-117">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c0d1-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8c0d1-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c0d1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8c0d1-119">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c0d1-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8c0d1-120">Header</span><span class="sxs-lookup"><span data-stu-id="8c0d1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c0d1-121"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c0d1-121"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c0d1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c0d1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0d1-123">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="8c0d1-123">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="8c0d1-124">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-124">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




