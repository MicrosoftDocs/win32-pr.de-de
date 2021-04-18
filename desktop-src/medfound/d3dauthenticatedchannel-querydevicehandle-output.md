---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY- \_ abvicehandle-Abfrage.
ms.assetid: f2e0ae6c-dc97-46f7-933f-6c14d83adf18
title: D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b862523c54dc9f483e63cee525dc61c5f469602d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343626"
---
# <a name="d3dauthenticatedchannel_querydevicehandle_output-structure"></a><span data-ttu-id="4de63-103">D3DAUTHENTICATEDCHANNEL \_ querydevicehandle- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="4de63-103">D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT structure</span></span>

<span data-ttu-id="4de63-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY- \_ abvicehandle**](d3dauthenticatedquery-devicehandle.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="4de63-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) query.</span></span>

<span data-ttu-id="4de63-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="4de63-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="4de63-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4de63-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="4de63-107">Member</span><span class="sxs-lookup"><span data-stu-id="4de63-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4de63-108">**Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="4de63-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="4de63-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="4de63-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="4de63-110">**Geräte**</span><span class="sxs-lookup"><span data-stu-id="4de63-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="4de63-111">Ein Handle für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="4de63-111">A handle to the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4de63-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4de63-112">Requirements</span></span>



| <span data-ttu-id="4de63-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4de63-113">Requirement</span></span> | <span data-ttu-id="4de63-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4de63-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4de63-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4de63-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4de63-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4de63-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4de63-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4de63-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4de63-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4de63-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4de63-119">Header</span><span class="sxs-lookup"><span data-stu-id="4de63-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4de63-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4de63-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de63-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4de63-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de63-122">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="4de63-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="4de63-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="4de63-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




