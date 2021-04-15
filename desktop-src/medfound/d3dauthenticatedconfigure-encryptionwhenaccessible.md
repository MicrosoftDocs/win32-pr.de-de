---
description: Legt den Verschlüsselungs Grad fest, der vor dem Zugriff auf geschützte Inhalte für die CPU oder den Bus ausgeführt wird.
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8b624c26c81549372e0e09b4a08ce73f6cd3dd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524592"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a><span data-ttu-id="ef832-103">D3DAUTHENTICATEDCONFIGURE \_ verschlüsselt</span><span class="sxs-lookup"><span data-stu-id="ef832-103">D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="ef832-104">Legt den Verschlüsselungs Grad fest, der vor dem Zugriff auf geschützte Inhalte für die CPU oder den Bus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef832-104">Sets the level of encryption that is performed before protected content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="ef832-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef832-105">Requirement</span></span> | <span data-ttu-id="ef832-106">Wert</span><span class="sxs-lookup"><span data-stu-id="ef832-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef832-107">Befehls-GUID</span><span class="sxs-lookup"><span data-stu-id="ef832-107">Command GUID</span></span> | <span data-ttu-id="ef832-108">**D3DAUTHENTICATEDCONFIGURE \_ verschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="ef832-108">**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**</span></span>                                                                     |
| <span data-ttu-id="ef832-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="ef832-109">Input data</span></span>   | [<span data-ttu-id="ef832-110">**D3DAUTHENTICATEDCHANNEL \_ Konfiguration reuncompressedencryption**</span><span class="sxs-lookup"><span data-stu-id="ef832-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION**</span></span>](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

## <a name="remarks"></a><span data-ttu-id="ef832-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef832-111">Remarks</span></span>

<span data-ttu-id="ef832-112">Diese Abfrage wird von den folgenden Kanaltypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ef832-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="ef832-113">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**</span><span class="sxs-lookup"><span data-stu-id="ef832-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="ef832-114">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="ef832-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="ef832-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef832-115">Requirements</span></span>



| <span data-ttu-id="ef832-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef832-116">Requirement</span></span> | <span data-ttu-id="ef832-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ef832-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef832-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef832-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ef832-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef832-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ef832-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef832-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ef832-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef832-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ef832-122">Header</span><span class="sxs-lookup"><span data-stu-id="ef832-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef832-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef832-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef832-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef832-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef832-125">Content Protection-Befehle</span><span class="sxs-lookup"><span data-stu-id="ef832-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="ef832-126">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="ef832-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="ef832-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="ef832-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




