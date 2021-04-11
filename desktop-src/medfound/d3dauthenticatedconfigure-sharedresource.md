---
description: Ermöglicht einem Prozess, eine freigegebene Ressource zu öffnen, oder deaktiviert das Öffnen von freigegebenen Ressourcen durch einen Prozess.
ms.assetid: 5fa2b88f-e946-436c-953e-04e0e338146c
title: D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7404a4bed3ac3b1d4002bb03c45d7732500b77e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214322"
---
# <a name="d3dauthenticatedconfigure_sharedresource"></a><span data-ttu-id="3ebfc-103">D3DAUTHENTICATEDCONFIGURE \_ SharedResource</span><span class="sxs-lookup"><span data-stu-id="3ebfc-103">D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE</span></span>

<span data-ttu-id="3ebfc-104">Ermöglicht einem Prozess, eine freigegebene Ressource zu öffnen, oder deaktiviert das Öffnen von freigegebenen Ressourcen durch einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="3ebfc-104">Enables a process to open a shared resource, or disables a process from opening shared resources.</span></span>



| <span data-ttu-id="3ebfc-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ebfc-105">Requirement</span></span> | <span data-ttu-id="3ebfc-106">Wert</span><span class="sxs-lookup"><span data-stu-id="3ebfc-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ebfc-107">Befehls-GUID</span><span class="sxs-lookup"><span data-stu-id="3ebfc-107">Command GUID</span></span> | <span data-ttu-id="3ebfc-108">**D3DAUTHENTICATEDCONFIGURE \_ SharedResource**</span><span class="sxs-lookup"><span data-stu-id="3ebfc-108">**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**</span></span>                                                               |
| <span data-ttu-id="3ebfc-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="3ebfc-109">Input data</span></span>   | [<span data-ttu-id="3ebfc-110">**D3DAUTHENTICATEDCHANNEL- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="3ebfc-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE**</span></span>](d3dauthenticatedchannel-configuresharedresource.md) |



 

## <a name="remarks"></a><span data-ttu-id="3ebfc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ebfc-111">Remarks</span></span>

<span data-ttu-id="3ebfc-112">Diese Abfrage wird von den folgenden Kanaltypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3ebfc-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="3ebfc-113">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="3ebfc-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_D3D9**</span></span>
-   <span data-ttu-id="3ebfc-114">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="3ebfc-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="3ebfc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ebfc-115">Requirements</span></span>



| <span data-ttu-id="3ebfc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ebfc-116">Requirement</span></span> | <span data-ttu-id="3ebfc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3ebfc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ebfc-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ebfc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3ebfc-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ebfc-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3ebfc-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ebfc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3ebfc-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ebfc-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3ebfc-122">Header</span><span class="sxs-lookup"><span data-stu-id="3ebfc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ebfc-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ebfc-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ebfc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ebfc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ebfc-125">Content Protection-Befehle</span><span class="sxs-lookup"><span data-stu-id="3ebfc-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="3ebfc-126">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="3ebfc-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="3ebfc-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="3ebfc-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




