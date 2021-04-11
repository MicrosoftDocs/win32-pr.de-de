---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ OutputID-Abfrage.
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 26686126fd2a5cb942c88ea485f753d2432499dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041557"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a><span data-ttu-id="fd6e6-103">D3DAUTHENTICATEDCHANNEL \_ queryroutputid- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="fd6e6-103">D3DAUTHENTICATEDCHANNEL\_QUERYROUTPUTID\_OUTPUT structure</span></span>

<span data-ttu-id="fd6e6-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ OutputID**](d3dauthenticatedquery-outputid.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="fd6e6-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="fd6e6-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6e6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd6e6-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="fd6e6-107">Member</span><span class="sxs-lookup"><span data-stu-id="fd6e6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd6e6-108">**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="fd6e6-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="fd6e6-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="fd6e6-110">**Geräte**</span><span class="sxs-lookup"><span data-stu-id="fd6e6-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="fd6e6-111">Ein Handle für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="fd6e6-112">**Cryptosessionhandle**</span><span class="sxs-lookup"><span data-stu-id="fd6e6-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="fd6e6-113">Ein Handle für die Kryptografiesitzung.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="fd6e6-114">**Outputidindex**</span><span class="sxs-lookup"><span data-stu-id="fd6e6-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="fd6e6-115">Der Index der Ausgabe-ID, die im **OutputID** -Member angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-115">The index of the output ID given in the **OutputID** member.</span></span>

</dd> <dt>

<span data-ttu-id="fd6e6-116">**OutputID**</span><span class="sxs-lookup"><span data-stu-id="fd6e6-116">**OutputID**</span></span>
</dt> <dd>

<span data-ttu-id="fd6e6-117">Eine Ausgabe-ID, die dem angegebenen Gerät und der angegebenen Kryptografiesitzung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fd6e6-117">An output ID that is associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd6e6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd6e6-118">Requirements</span></span>



| <span data-ttu-id="fd6e6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd6e6-119">Requirement</span></span> | <span data-ttu-id="fd6e6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fd6e6-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6e6-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd6e6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6e6-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd6e6-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fd6e6-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd6e6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6e6-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd6e6-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fd6e6-125">Header</span><span class="sxs-lookup"><span data-stu-id="fd6e6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd6e6-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd6e6-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd6e6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd6e6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6e6-128">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="fd6e6-128">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="fd6e6-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="fd6e6-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




