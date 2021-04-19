---
description: Änderungs Ereignis für den Winsock-Katalog für einen mehrstufigen Dienstanbieter (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: WINSOCK_WS2HELP_LSP_DISABLE Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350006"
---
# <a name="winsock_ws2help_lsp_disable-event"></a><span data-ttu-id="7619a-103">Winsock \_ WS2HELP \_ LSP-Deaktivierungs \_ Ereignis</span><span class="sxs-lookup"><span data-stu-id="7619a-103">WINSOCK\_WS2HELP\_LSP\_DISABLE event</span></span>

> [!Note]  
> <span data-ttu-id="7619a-104">Mehrstufige Dienstanbieter sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="7619a-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="7619a-105">Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="7619a-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="7619a-106">Das **Winsock \_ WS2HELP \_ LSP \_** -Deaktivierungs Ereignis ist ein Winsock-Katalog Änderungs Ereignis für einen aktivierten Dienstanbieter (LSP).</span><span class="sxs-lookup"><span data-stu-id="7619a-106">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is a Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="7619a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7619a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7619a-108">*LSP-Name*</span><span class="sxs-lookup"><span data-stu-id="7619a-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="7619a-109">Der Name des LSP, der vom **szprotocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das deaktivierte LSP abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7619a-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="7619a-110">*Katalog*</span><span class="sxs-lookup"><span data-stu-id="7619a-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="7619a-111">Der Winsock-Katalog (32 Bit oder 64 Bit), in dem der LSP deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="7619a-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="7619a-112">Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.</span><span class="sxs-lookup"><span data-stu-id="7619a-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="7619a-113">*Installationsprogramm*</span><span class="sxs-lookup"><span data-stu-id="7619a-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="7619a-114">Der Modul Dateiname der Anwendung, die die LSP-Deaktivierung aufruft.</span><span class="sxs-lookup"><span data-stu-id="7619a-114">The module filename of the application making the LSP disable call.</span></span>

</dd> <dt>

<span data-ttu-id="7619a-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7619a-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="7619a-116">Der GUID-Wert des Winsock-Transport Anbieters, für den der LSP deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="7619a-116">The GUID value of the Winsock transport provider that the LSP is being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="7619a-117">*Kategorie*</span><span class="sxs-lookup"><span data-stu-id="7619a-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="7619a-118">Der **dwcatalogentryid** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das deaktivierte LSP.</span><span class="sxs-lookup"><span data-stu-id="7619a-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> </dl>

<span data-ttu-id="7619a-119">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="7619a-119">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7619a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7619a-120">Remarks</span></span>

<span data-ttu-id="7619a-121">Das **Winsock \_ WS2HELP \_ LSP \_** -Deaktivierungs Ereignis wird für einen LSP-Deaktivierungs Vorgang nachverfolgt, wenn ein Protokolleintrag im Winsock-Katalog deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7619a-121">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is traced for an LSP disable operation when a protocol entry is disabled in the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="7619a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7619a-122">Requirements</span></span>



| <span data-ttu-id="7619a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7619a-123">Requirement</span></span> | <span data-ttu-id="7619a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7619a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7619a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7619a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7619a-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7619a-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7619a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7619a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7619a-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7619a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7619a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7619a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7619a-130">Kontrolle über die Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="7619a-130">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="7619a-131">Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="7619a-131">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="7619a-132">Winsock-Ablauf Verfolgungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="7619a-132">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="7619a-133">Details zur Änderung der Winsock-Katalog Änderung</span><span class="sxs-lookup"><span data-stu-id="7619a-133">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
