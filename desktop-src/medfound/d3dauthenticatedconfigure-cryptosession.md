---
description: Verknüpft eine Kryptografiesitzung mit einem DXVA-2-Decodergerät (DirectX Video Acceleration 2) und einem Direct3D-Gerät.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 4b6fda19aef9629214aaa410fd43c4d64f16dd29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346046"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a><span data-ttu-id="fc1a6-103">D3DAUTHENTICATEDCONFIGURE \_ CryptoSession</span><span class="sxs-lookup"><span data-stu-id="fc1a6-103">D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION</span></span>

<span data-ttu-id="fc1a6-104">Verknüpft eine Kryptografiesitzung mit einem DXVA-2-Decodergerät (DirectX Video Acceleration 2) und einem Direct3D-Gerät.</span><span class="sxs-lookup"><span data-stu-id="fc1a6-104">Associates a cryptographic session with a DirectX Video Acceleration 2 (DXVA-2) decoder device and a Direct3D device.</span></span>



| <span data-ttu-id="fc1a6-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc1a6-105">Requirement</span></span> | <span data-ttu-id="fc1a6-106">Wert</span><span class="sxs-lookup"><span data-stu-id="fc1a6-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1a6-107">Befehls-GUID</span><span class="sxs-lookup"><span data-stu-id="fc1a6-107">Command GUID</span></span> | <span data-ttu-id="fc1a6-108">**D3DAUTHENTICATEDCONFIGURE \_ CryptoSession**</span><span class="sxs-lookup"><span data-stu-id="fc1a6-108">**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**</span></span>                                                              |
| <span data-ttu-id="fc1a6-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="fc1a6-109">Input data</span></span>   | [<span data-ttu-id="fc1a6-110">**D3DAUTHENTICATEDCHANNEL \_ Konfigurations Sitzung**</span><span class="sxs-lookup"><span data-stu-id="fc1a6-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION**</span></span>](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a><span data-ttu-id="fc1a6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc1a6-111">Remarks</span></span>

<span data-ttu-id="fc1a6-112">Nachdem dieser Befehl gesendet wurde, können Sie die [D3DAUTHENTICATEDQUERY \_ OutputID](d3dauthenticatedquery-outputid.md) -Abfrage senden, um herauszufinden, welche Video Ausgaben der Kryptografiesitzung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fc1a6-112">After this command is sent, you can send the [D3DAUTHENTICATEDQUERY\_OUTPUTID](d3dauthenticatedquery-outputid.md) query to find out which video outputs are associated with the cryptographic session.</span></span>

<span data-ttu-id="fc1a6-113">Der folgende Kanaltyp unterstützt diesen Befehl:</span><span class="sxs-lookup"><span data-stu-id="fc1a6-113">The following channel types support this command:</span></span>

-   <span data-ttu-id="fc1a6-114">**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="fc1a6-114">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="fc1a6-115">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="fc1a6-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="fc1a6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc1a6-116">Requirements</span></span>



| <span data-ttu-id="fc1a6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc1a6-117">Requirement</span></span> | <span data-ttu-id="fc1a6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fc1a6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1a6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc1a6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc1a6-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc1a6-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fc1a6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc1a6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc1a6-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc1a6-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fc1a6-123">Header</span><span class="sxs-lookup"><span data-stu-id="fc1a6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc1a6-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc1a6-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc1a6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc1a6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc1a6-126">Content Protection-Befehle</span><span class="sxs-lookup"><span data-stu-id="fc1a6-126">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="fc1a6-127">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="fc1a6-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="fc1a6-128">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="fc1a6-128">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




