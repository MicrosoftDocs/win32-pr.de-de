---
description: Enthält Eingabedaten für einen D3DAUTHENTICATEDCONFIGURE \_ CryptoSession-Befehl.
ms.assetid: eed5591d-20b0-495c-8c05-b9cb3b91deab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2b1cca13bcd37e488cd0ed455098afa62492579f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343024"
---
# <a name="d3dauthenticatedchannel_configurecryptosession-structure"></a><span data-ttu-id="fd215-103">D3DAUTHENTICATEDCHANNEL- \_ Struktur Konfiguration</span><span class="sxs-lookup"><span data-stu-id="fd215-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION structure</span></span>

<span data-ttu-id="fd215-104">Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ CryptoSession**](d3dauthenticatedconfigure-cryptosession.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="fd215-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) command.</span></span>

<span data-ttu-id="fd215-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="fd215-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd215-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd215-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  HANDLE                                  DXVA2DecodeHandle;
  HANDLE                                  CryptoSessionHandle;
  HANDLE                                  DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION;
```



## <a name="members"></a><span data-ttu-id="fd215-107">Member</span><span class="sxs-lookup"><span data-stu-id="fd215-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd215-108">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="fd215-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="fd215-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ - \_ Eingabe**](d3dauthenticatedchannel-configure-input.md) Struktur, die die Befehls-GUID und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="fd215-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="fd215-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="fd215-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="fd215-111">Ein Handle für das DirectX Video Acceleration 2-Decodergerät (DXVA-2).</span><span class="sxs-lookup"><span data-stu-id="fd215-111">A handle to the DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="fd215-112">**Cryptosessionhandle**</span><span class="sxs-lookup"><span data-stu-id="fd215-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="fd215-113">Ein Handle für die Kryptografiesitzung.</span><span class="sxs-lookup"><span data-stu-id="fd215-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="fd215-114">**Geräte**</span><span class="sxs-lookup"><span data-stu-id="fd215-114">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="fd215-115">Ein Handle für das Direct3D-Gerät.</span><span class="sxs-lookup"><span data-stu-id="fd215-115">A handle to the Direct3D device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd215-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd215-116">Requirements</span></span>



| <span data-ttu-id="fd215-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd215-117">Requirement</span></span> | <span data-ttu-id="fd215-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fd215-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd215-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd215-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd215-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd215-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fd215-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd215-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd215-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd215-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fd215-123">Header</span><span class="sxs-lookup"><span data-stu-id="fd215-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd215-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd215-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd215-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd215-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd215-126">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="fd215-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="fd215-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="fd215-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




