---
description: Enthält Eingabedaten für einen D3DAUTHENTICATEDCONFIGURE \_ Protection-Befehl.
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fc1daee7bfd9320539a03974ab431c4ba588d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861808"
---
# <a name="d3dauthenticatedchannel_configureprotection-structure"></a><span data-ttu-id="fe148-103">D3DAUTHENTICATEDCHANNEL- \_ Struktur konfigurieren</span><span class="sxs-lookup"><span data-stu-id="fe148-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREPROTECTION structure</span></span>

<span data-ttu-id="fe148-104">Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ Protection**](d3dauthenticatedconfigure-protection.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="fe148-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_PROTECTION**](d3dauthenticatedconfigure-protection.md) command.</span></span>

<span data-ttu-id="fe148-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="fe148-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe148-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe148-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT  Parameters;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS Protections;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION;
```



## <a name="members"></a><span data-ttu-id="fe148-107">Member</span><span class="sxs-lookup"><span data-stu-id="fe148-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe148-108">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="fe148-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="fe148-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ - \_ Eingabe**](d3dauthenticatedchannel-configure-input.md) Struktur, die die Befehls-GUID und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="fe148-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="fe148-110">**Aufheben**</span><span class="sxs-lookup"><span data-stu-id="fe148-110">**Protections**</span></span>
</dt> <dd>

<span data-ttu-id="fe148-111">Eine [**D3DAUTHENTICATEDCHANNEL \_ Protection \_ Flags**](d3dauthenticatedchannel-protection-flags.md) -Struktur, die die Schutz Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="fe148-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe148-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe148-112">Requirements</span></span>



| <span data-ttu-id="fe148-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe148-113">Requirement</span></span> | <span data-ttu-id="fe148-114">Wert</span><span class="sxs-lookup"><span data-stu-id="fe148-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe148-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe148-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fe148-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe148-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fe148-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe148-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fe148-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe148-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fe148-119">Header</span><span class="sxs-lookup"><span data-stu-id="fe148-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe148-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe148-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe148-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe148-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe148-122">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="fe148-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="fe148-123">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="fe148-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




