---
description: Änderungs Ereignis für den Winsock-Katalog für einen mehrstufigen Dienstanbieter (LSP).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: WINSOCK_WS2HELP_LSP_INSTALL Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2d95a77f68bafd29fde3bbf34336d9b31d2a412e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960304"
---
# <a name="winsock_ws2help_lsp_install-event"></a><span data-ttu-id="d6dcd-103">Winsock \_ WS2HELP \_ LSP- \_ Installations Ereignis</span><span class="sxs-lookup"><span data-stu-id="d6dcd-103">WINSOCK\_WS2HELP\_LSP\_INSTALL event</span></span>

> [!Note]  
> <span data-ttu-id="d6dcd-104">Mehrstufige Dienstanbieter sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="d6dcd-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="d6dcd-105">Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="d6dcd-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="d6dcd-106">Das **Winsock \_ WS2HELP \_ LSP \_** -Installations Ereignis ist ein Winsock-Katalog Änderungs Ereignis für einen mehrstufigen Dienstanbieter (LSP).</span><span class="sxs-lookup"><span data-stu-id="d6dcd-106">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is a Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="d6dcd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6dcd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6dcd-108">*LSP-Name*</span><span class="sxs-lookup"><span data-stu-id="d6dcd-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="d6dcd-109">Der Name des LSP, der vom **szprotocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für den installierten LSP abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d6dcd-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> <dt>

<span data-ttu-id="d6dcd-110">*Katalog*</span><span class="sxs-lookup"><span data-stu-id="d6dcd-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="d6dcd-111">Der Winsock-Katalog (32-Bit oder 64-Bit), in dem der LSP installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d6dcd-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="d6dcd-112">Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.</span><span class="sxs-lookup"><span data-stu-id="d6dcd-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="d6dcd-113">*Installationsprogramm*</span><span class="sxs-lookup"><span data-stu-id="d6dcd-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="d6dcd-114">Der Modul Dateiname der Anwendung, die die LSP-Installation aufruft.</span><span class="sxs-lookup"><span data-stu-id="d6dcd-114">The module filename of the application making the LSP install call.</span></span>

</dd> <dt>

<span data-ttu-id="d6dcd-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="d6dcd-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="d6dcd-116">Der GUID-Wert des Winsock-Transport Anbieters, unter dem der LSP installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d6dcd-116">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span>

</dd> <dt>

<span data-ttu-id="d6dcd-117">*Kategorie*</span><span class="sxs-lookup"><span data-stu-id="d6dcd-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="d6dcd-118">Der **dwcatalogentryid** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das zu installierende LSP.</span><span class="sxs-lookup"><span data-stu-id="d6dcd-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6dcd-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6dcd-119">Remarks</span></span>

<span data-ttu-id="d6dcd-120">Das **Winsock \_ WS2HELP \_ LSP- \_ Installations** Ereignis wird für einen LSP-Installationsvorgang nachverfolgt, wenn ein Protokolleintrag im Winsock-Katalog installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d6dcd-120">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is traced for an LSP install operation when a protocol entry is installed into the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6dcd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6dcd-121">Requirements</span></span>



| <span data-ttu-id="d6dcd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6dcd-122">Requirement</span></span> | <span data-ttu-id="d6dcd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d6dcd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6dcd-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6dcd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d6dcd-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6dcd-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d6dcd-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6dcd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d6dcd-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6dcd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6dcd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6dcd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6dcd-129">Kontrolle über die Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="d6dcd-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="d6dcd-130">Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="d6dcd-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="d6dcd-131">Winsock-Ablauf Verfolgungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="d6dcd-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="d6dcd-132">Details zur Änderung der Winsock-Katalog Änderung</span><span class="sxs-lookup"><span data-stu-id="d6dcd-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
