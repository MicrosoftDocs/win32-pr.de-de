---
description: Die Peer Distribution-API definiert die folgenden Datentypen.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Datentypen der Peer Distribution-API (peerdist. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357762"
---
# <a name="peer-distribution-api-data-types"></a><span data-ttu-id="f9bb2-103">Datentypen der Peer Distribution-API</span><span class="sxs-lookup"><span data-stu-id="f9bb2-103">Peer Distribution API Data Types</span></span>

<span data-ttu-id="f9bb2-104">Die Peer Distribution-API definiert die folgenden Datentypen.</span><span class="sxs-lookup"><span data-stu-id="f9bb2-104">The Peer Distribution API defines the following data types.</span></span>


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| <span data-ttu-id="f9bb2-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f9bb2-105">Data type</span></span>                                                                                                                     | <span data-ttu-id="f9bb2-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9bb2-106">Description</span></span>                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9bb2-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**Peer- \_ \_ Instanzhandle**</span><span class="sxs-lookup"><span data-stu-id="f9bb2-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**PEERDIST\_INSTANCE\_HANDLE**</span></span>          | <span data-ttu-id="f9bb2-108">Ein Handle, das der Peer Verteilungs Instanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f9bb2-108">A handle associated with the Peer Distribution instance.</span></span> <span data-ttu-id="f9bb2-109">Dieses Handle wird von [**peerdiststartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)erstellt und in den meisten Peer Verteilungs Vorgängen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9bb2-109">This handle is created by [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup), and used in most Peer Distribution operations.</span></span><br/>                                          |
| <span data-ttu-id="f9bb2-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_Inhalts Handle für Peer-dist \_**</span><span class="sxs-lookup"><span data-stu-id="f9bb2-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**PEERDIST\_CONTENT\_HANDLE**</span></span>             | <span data-ttu-id="f9bb2-111">Ein Handle, das dem Inhalt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f9bb2-111">A handle associated with content.</span></span> <span data-ttu-id="f9bb2-112">Dieses Handle wird von " [**Peer-distclientopencontent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) " erstellt und wird beim Öffnen, schließen, hinzufügen oder Veröffentlichen von Inhalten referenziert.</span><span class="sxs-lookup"><span data-stu-id="f9bb2-112">This handle is created by [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) and is referenced when opening, closing, adding, or publishing content.</span></span><br/>                     |
| <span data-ttu-id="f9bb2-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**Peer- \_ ContentInfo- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="f9bb2-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**PEERDIST\_CONTENTINFO\_HANDLE**</span></span> | <span data-ttu-id="f9bb2-114">Ein Handle, das Inhaltsinformationen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f9bb2-114">A handle associated with content information.</span></span> <span data-ttu-id="f9bb2-115">Dieses Handle wird von " [**eterdistserveropencontentinformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)" erstellt und beim Abrufen von codierten Inhaltsinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9bb2-115">This handle is created by [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation), and is used when retrieving encoded content information.</span></span><br/> |
| <span data-ttu-id="f9bb2-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**Peer- \_ Stream- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="f9bb2-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**PEERDIST\_STREAM\_HANDLE**</span></span>                | <span data-ttu-id="f9bb2-117">Ein Handle, das einem Datenstrom zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f9bb2-117">A handle associated with a data stream.</span></span> <span data-ttu-id="f9bb2-118">Dieses Handle wird von " [**eterdistserverpublishstream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) " erstellt, und es wird auf die Veröffentlichung, das Schließen oder das Hinzufügen von gestreuten Inhalten verwiesen.</span><span class="sxs-lookup"><span data-stu-id="f9bb2-118">This handle is created by [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) and is referenced when publishing, closing, or adding to streamed content.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="f9bb2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9bb2-119">Requirements</span></span>



| <span data-ttu-id="f9bb2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9bb2-120">Requirement</span></span> | <span data-ttu-id="f9bb2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f9bb2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9bb2-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9bb2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f9bb2-123">Nur Windows 7 Professional \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9bb2-123">Windows 7 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f9bb2-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9bb2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f9bb2-125">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9bb2-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f9bb2-126">Header</span><span class="sxs-lookup"><span data-stu-id="f9bb2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9bb2-127"><dt>"Peer. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f9bb2-127"><dt>Peerdist.h</dt></span></span> </dl> |



 

 




