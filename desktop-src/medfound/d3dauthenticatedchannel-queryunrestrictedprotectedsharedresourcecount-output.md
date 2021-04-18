---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ unrestrictedprotectedsharedresourcecount-Abfrage.
ms.assetid: c283833d-e98c-4f01-b623-21027a6b90e8
title: D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fd30cff59d35f845903e7f4fdb08cdff61df3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344981"
---
# <a name="d3dauthenticatedchannel_queryunrestrictedprotectedsharedresourcecount_output-structure"></a><span data-ttu-id="ebd89-103">D3DAUTHENTICATEDCHANNEL \_ queryunrestrictedprotectedsharedresourcecount- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="ebd89-103">D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="ebd89-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ unrestrictedprotectedsharedresourcecount**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="ebd89-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) query.</span></span>

<span data-ttu-id="ebd89-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="ebd89-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd89-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebd89-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumUnrestrictedProtectedSharedResources;
} D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="ebd89-107">Member</span><span class="sxs-lookup"><span data-stu-id="ebd89-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ebd89-108">**Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="ebd89-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="ebd89-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="ebd89-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="ebd89-110">**Numunrestrictedprotectedsharedresources**</span><span class="sxs-lookup"><span data-stu-id="ebd89-110">**NumUnrestrictedProtectedSharedResources**</span></span>
</dt> <dd>

<span data-ttu-id="ebd89-111">Die Anzahl geschützter, gemeinsam genutzter Ressourcen, die von einem beliebigen Prozess ohne Einschränkungen geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="ebd89-111">The number of protected, shared resources that can be opened by any process without restrictions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ebd89-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebd89-112">Requirements</span></span>



| <span data-ttu-id="ebd89-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebd89-113">Requirement</span></span> | <span data-ttu-id="ebd89-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ebd89-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd89-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ebd89-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd89-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebd89-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ebd89-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ebd89-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd89-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebd89-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ebd89-119">Header</span><span class="sxs-lookup"><span data-stu-id="ebd89-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebd89-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebd89-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd89-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebd89-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd89-122">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="ebd89-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="ebd89-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="ebd89-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




