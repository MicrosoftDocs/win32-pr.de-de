---
description: Legt die Position eines Elements in der shellansicht fest. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_SETITEMPOS Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b89f2d62-095b-4cad-a47e-2d41e122cb3e
api_name:
- SFVM_SETITEMPOS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 450aeabee6e5edeba466e4a5fe64725c13eea32b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218382"
---
# <a name="sfvm_setitempos-message"></a><span data-ttu-id="9b28b-104">Sfvm- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="9b28b-104">SFVM\_SETITEMPOS message</span></span>

<span data-ttu-id="9b28b-105">Legt die Position eines Elements in der shellansicht fest.</span><span class="sxs-lookup"><span data-stu-id="9b28b-105">Sets the position of an item in the Shell view.</span></span> <span data-ttu-id="9b28b-106">Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b28b-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_SETITEMPOS 

    lParam = (LPSFV_SETITEMPOS)&sip;

            
```



## <a name="parameters"></a><span data-ttu-id="9b28b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b28b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b28b-108">*SIP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b28b-108">*sip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b28b-109">Ein Zeiger auf eine SFV-Struktur von "- [**\_ titempos**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) ".</span><span class="sxs-lookup"><span data-stu-id="9b28b-109">A pointer to an [**SFV\_SETITEMPOS**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b28b-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9b28b-110">Requirements</span></span>



| <span data-ttu-id="9b28b-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b28b-111">Requirement</span></span> | <span data-ttu-id="9b28b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="9b28b-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9b28b-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b28b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9b28b-114">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b28b-114">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9b28b-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b28b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9b28b-116">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b28b-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9b28b-117">Header</span><span class="sxs-lookup"><span data-stu-id="9b28b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b28b-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b28b-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




