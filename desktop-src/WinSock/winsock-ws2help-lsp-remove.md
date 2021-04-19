---
description: Änderungs Ereignis für den Winsock-Katalog für einen mehrstufigen Dienstanbieter (LSP).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: WINSOCK_WS2HELP_LSP_REMOVE Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 597cd2f8cfc3bb7727301e64af53671bafbd9469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364107"
---
# <a name="winsock_ws2help_lsp_remove-event"></a><span data-ttu-id="33fb4-103">Winsock \_ WS2HELP \_ LSP- \_ Entfernungs Ereignis</span><span class="sxs-lookup"><span data-stu-id="33fb4-103">WINSOCK\_WS2HELP\_LSP\_REMOVE event</span></span>

> [!Note]  
> <span data-ttu-id="33fb4-104">Mehrstufige Dienstanbieter sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="33fb4-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="33fb4-105">Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="33fb4-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="33fb4-106">Das **Winsock \_ WS2HELP \_ LSP- \_ Entfernungs** Ereignis ist ein Winsock-Katalog Änderungs Ereignis für einen überlappenden Dienstanbieter (LSP).</span><span class="sxs-lookup"><span data-stu-id="33fb4-106">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is a Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="33fb4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="33fb4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33fb4-108">*LSP-Name*</span><span class="sxs-lookup"><span data-stu-id="33fb4-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="33fb4-109">Der Name des LSP, der vom **szprotocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für den zu entfernenden LSP abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="33fb4-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> <dt>

<span data-ttu-id="33fb4-110">*Katalog*</span><span class="sxs-lookup"><span data-stu-id="33fb4-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="33fb4-111">Der Winsock-Katalog (32 Bit oder 64 Bit), in dem der LSP entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="33fb4-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="33fb4-112">Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.</span><span class="sxs-lookup"><span data-stu-id="33fb4-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="33fb4-113">*Installationsprogramm*</span><span class="sxs-lookup"><span data-stu-id="33fb4-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="33fb4-114">Der Modul Dateiname der Anwendung, die den LSP-Befehl zum Entfernen aufruft.</span><span class="sxs-lookup"><span data-stu-id="33fb4-114">The module filename of the application making the LSP remove call.</span></span>

</dd> <dt>

<span data-ttu-id="33fb4-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="33fb4-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="33fb4-116">Der GUID-Wert des Winsock-Transport Anbieters, aus dem der LSP entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="33fb4-116">The GUID value of the Winsock transport provider that the LSP is being removed from.</span></span>

</dd> <dt>

<span data-ttu-id="33fb4-117">*Kategorie*</span><span class="sxs-lookup"><span data-stu-id="33fb4-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="33fb4-118">Der **dwcatalogentryid** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für den LSP, der entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="33fb4-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33fb4-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33fb4-119">Remarks</span></span>

<span data-ttu-id="33fb4-120">Das **Winsock \_ WS2HELP \_ LSP- \_ Entfernungs** Ereignis wird für einen LSP-Entfernungs Vorgang nachverfolgt, wenn ein Protokolleintrag aus dem Winsock-Katalog entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="33fb4-120">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is traced for an LSP removal operation when a protocol entry is removed from the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="33fb4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33fb4-121">Requirements</span></span>



| <span data-ttu-id="33fb4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33fb4-122">Requirement</span></span> | <span data-ttu-id="33fb4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="33fb4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="33fb4-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33fb4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="33fb4-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33fb4-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="33fb4-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33fb4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="33fb4-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33fb4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33fb4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33fb4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33fb4-129">Kontrolle über die Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="33fb4-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="33fb4-130">Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="33fb4-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="33fb4-131">Winsock-Ablauf Verfolgungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="33fb4-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="33fb4-132">Details zur Änderung der Winsock-Katalog Änderung</span><span class="sxs-lookup"><span data-stu-id="33fb4-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
