---
description: Enthält Eingabedaten für einen D3DAUTHENTICATEDCONFIGURE \_ Initialize-Befehl.
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 072d7886a024b1c28e8c3b7f0609dc8dd3e6add8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041559"
---
# <a name="d3dauthenticatedchannel_configureinitialize-structure"></a><span data-ttu-id="aba27-103">D3DAUTHENTICATEDCHANNEL- \_ Struktur neu initialisieren</span><span class="sxs-lookup"><span data-stu-id="aba27-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE structure</span></span>

<span data-ttu-id="aba27-104">Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="aba27-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) command.</span></span>

<span data-ttu-id="aba27-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="aba27-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="aba27-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="aba27-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  UINT                                    StartSequenceQuery;
  UINT                                    StartSequenceConfigure;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE;
```



## <a name="members"></a><span data-ttu-id="aba27-107">Member</span><span class="sxs-lookup"><span data-stu-id="aba27-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="aba27-108">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="aba27-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="aba27-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ - \_ Eingabe**](d3dauthenticatedchannel-configure-input.md) Struktur, die die Befehls-GUID und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="aba27-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="aba27-110">**Startsequencequery**</span><span class="sxs-lookup"><span data-stu-id="aba27-110">**StartSequenceQuery**</span></span>
</dt> <dd>

<span data-ttu-id="aba27-111">Die anfängliche Sequenznummer für Abfragen.</span><span class="sxs-lookup"><span data-stu-id="aba27-111">The initial sequence number for queries.</span></span>

</dd> <dt>

<span data-ttu-id="aba27-112">**Startsequenceconfigure**</span><span class="sxs-lookup"><span data-stu-id="aba27-112">**StartSequenceConfigure**</span></span>
</dt> <dd>

<span data-ttu-id="aba27-113">Die anfängliche Sequenznummer für Befehle.</span><span class="sxs-lookup"><span data-stu-id="aba27-113">The initial sequence number for commands.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aba27-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aba27-114">Remarks</span></span>

<span data-ttu-id="aba27-115">Die Member **startsequencequery** und **startsequenceconfigure** enthalten jeweils eine kryptografisch sichere 32-Bit-Zufallszahl.</span><span class="sxs-lookup"><span data-stu-id="aba27-115">The **StartSequenceQuery** and **StartSequenceConfigure** members each contain a cryptographically secure 32-bit random number.</span></span>

## <a name="requirements"></a><span data-ttu-id="aba27-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aba27-116">Requirements</span></span>



| <span data-ttu-id="aba27-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aba27-117">Requirement</span></span> | <span data-ttu-id="aba27-118">Wert</span><span class="sxs-lookup"><span data-stu-id="aba27-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aba27-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aba27-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aba27-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aba27-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="aba27-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aba27-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aba27-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aba27-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aba27-123">Header</span><span class="sxs-lookup"><span data-stu-id="aba27-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aba27-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="aba27-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aba27-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aba27-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba27-126">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="aba27-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="aba27-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="aba27-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




