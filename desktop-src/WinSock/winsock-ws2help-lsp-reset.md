---
description: Das Änderungs Ereignis für den Winsock-Katalog für einen Winsock-Katalog Zurücksetzungs Vorgang.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: WINSOCK_WS2HELP_LSP_RESET Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 219eb85dec0cdda77ca8741ae42df1f63d1a7dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364106"
---
# <a name="winsock_ws2help_lsp_reset-event"></a><span data-ttu-id="87418-103">Winsock \_ WS2HELP \_ LSP \_ Reset-Ereignis</span><span class="sxs-lookup"><span data-stu-id="87418-103">WINSOCK\_WS2HELP\_LSP\_RESET event</span></span>

> [!Note]  
> <span data-ttu-id="87418-104">Mehrstufige Dienstanbieter sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="87418-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="87418-105">Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="87418-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="87418-106">Das **Winsock \_ WS2HELP \_ LSP \_ Reset** -Ereignis ist ein Winsock-Katalog Änderungs Ereignis für einen Winsock-Katalog Zurücksetzungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="87418-106">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is a Winsock catalog change event for a Winsock catalog reset operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="87418-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="87418-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87418-108">*Katalog*</span><span class="sxs-lookup"><span data-stu-id="87418-108">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="87418-109">Der Winsock-Katalog (32-Bit oder 64-Bit), der zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="87418-109">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="87418-110">Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.</span><span class="sxs-lookup"><span data-stu-id="87418-110">This is an integer value that is either 32 or 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87418-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87418-111">Remarks</span></span>

<span data-ttu-id="87418-112">Das **Winsock \_ WS2HELP \_ LSP \_ Reset** -Ereignis wird für einen LSP-Vorgang (Winsock-Schicht-Dienstanbieter) nachverfolgt, wenn der Winsock-Katalog zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="87418-112">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is traced for an Winsock Layered Service Provider (LSP) operation when the Winsock catalog is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="87418-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87418-113">Requirements</span></span>



| <span data-ttu-id="87418-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87418-114">Requirement</span></span> | <span data-ttu-id="87418-115">Wert</span><span class="sxs-lookup"><span data-stu-id="87418-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87418-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87418-116">Minimum supported client</span></span><br/> | <span data-ttu-id="87418-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87418-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="87418-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87418-118">Minimum supported server</span></span><br/> | <span data-ttu-id="87418-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87418-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87418-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87418-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87418-121">Kontrolle über die Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="87418-121">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="87418-122">Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="87418-122">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="87418-123">Winsock-Ablauf Verfolgungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="87418-123">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="87418-124">Details zur Änderung der Winsock-Katalog Änderung</span><span class="sxs-lookup"><span data-stu-id="87418-124">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
