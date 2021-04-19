---
description: Der Microsoft Peer Distribution-Dienst unterstützt die folgenden Strukturen.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Peer Distribution-API-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348616"
---
# <a name="peer-distribution-api-structures"></a><span data-ttu-id="2c121-103">Peer Distribution-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2c121-103">Peer Distribution API Structures</span></span>

<span data-ttu-id="2c121-104">Der Microsoft Peer Distribution-Dienst unterstützt die folgenden Strukturen.</span><span class="sxs-lookup"><span data-stu-id="2c121-104">The Microsoft Peer Distribution service supports the following structures.</span></span>



| <span data-ttu-id="2c121-105">Struktur</span><span class="sxs-lookup"><span data-stu-id="2c121-105">Structure</span></span>                                                              | <span data-ttu-id="2c121-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c121-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c121-107">**\_ \_ grundlegende \_ Informationen zum Peer-dist-Client**</span><span class="sxs-lookup"><span data-stu-id="2c121-107">**PEERDIST\_CLIENT\_BASIC\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | <span data-ttu-id="2c121-108">Gibt an, ob viele Clients gleichzeitig denselben Inhalt herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2c121-108">Indicates whether or not there are many clients simultaneously downloading the same content.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="2c121-109">**\_Inhalts Kennzeichen für Peer-dist \_**</span><span class="sxs-lookup"><span data-stu-id="2c121-109">**PEERDIST\_CONTENT\_TAG**</span></span>](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | <span data-ttu-id="2c121-110">Enthält ein vom Client bereitgestelltes Tag, das ein Eingabe Wert für " [**Peer-distclientopencontent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)" ist.</span><span class="sxs-lookup"><span data-stu-id="2c121-110">Contains a client supplied tag which is an input value for [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span></span> <span data-ttu-id="2c121-111">Das Tag ist dem Inhalts Segment zugeordnet und wird in Content Management-APIs wie z. b. " [**Peer-distclientflushcontent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c121-111">The tag is associated with the content segment and is used in content management APIs, like [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span></span> |
| [<span data-ttu-id="2c121-112">**Peer-dist- \_ Veröffentlichungs \_ Optionen**</span><span class="sxs-lookup"><span data-stu-id="2c121-112">**PEERDIST\_PUBLICATION\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | <span data-ttu-id="2c121-113">Enthält Veröffentlichungs Optionen, einschließlich der API-Versionsinformationen und möglicher Optionsflags.</span><span class="sxs-lookup"><span data-stu-id="2c121-113">Contains publication options, including the API version information and possible option flags.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="2c121-114">**Peer \_ Abruf \_ Optionen**</span><span class="sxs-lookup"><span data-stu-id="2c121-114">**PEER\_RETRIEVAL\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | <span data-ttu-id="2c121-115">Enthält die Version der abzurufenden Inhaltsinformationen.</span><span class="sxs-lookup"><span data-stu-id="2c121-115">Contains version of the content information to retrieve.</span></span>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="2c121-116">**peerdist- \_ Status \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="2c121-116">**PEERDIST\_STATUS\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | <span data-ttu-id="2c121-117">Enthält Informationen zum aktuellen Status und zu den Funktionen des BranchCache-Dienstanbieter auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="2c121-117">Contains information about the current status and capabilities of the BranchCache service on the local computer.</span></span>                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="2c121-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c121-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c121-119">Peer Distribution-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="2c121-119">Peer Distribution API Reference</span></span>](peer-distribution-api-reference.md)
</dt> </dl>

 

 



