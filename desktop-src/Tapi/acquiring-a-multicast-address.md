---
description: Im folgenden Code Fragment wird veranschaulicht, wie eine Multicast Adresse für eine Konferenz angefordert und festgelegt wird.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Abrufen einer Multicast Adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128729"
---
# <a name="acquiring-a-multicast-address"></a><span data-ttu-id="76f1f-103">Abrufen einer Multicast Adresse</span><span class="sxs-lookup"><span data-stu-id="76f1f-103">Acquiring a Multicast Address</span></span>

<span data-ttu-id="76f1f-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76f1f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="76f1f-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="76f1f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="76f1f-106">Im folgenden Code Fragment wird veranschaulicht, wie eine Multicast Adresse für eine Konferenz angefordert und festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="76f1f-106">The following code fragment illustrates how to request and set a multicast address for a conference.</span></span>

<span data-ttu-id="76f1f-107">Der Einfachheit halber zeigt dieses Fragment die Zuweisung einer Multicast Adresse zu einem Medien Element an.</span><span class="sxs-lookup"><span data-stu-id="76f1f-107">For the sake of simplicity, this fragment shows the assignment of one multicast address to one media item.</span></span> <span data-ttu-id="76f1f-108">In der Aktualität werden die Auswahl eines Bereichs, die Multicast Adress Anforderung und die Zuweisung für jedes Medien Element, das an der Konferenz beteiligt ist, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76f1f-108">In actuality, the selection of a scope, the multicast address request, and the assignment will be performed for every media item involved in the conference.</span></span>

<span data-ttu-id="76f1f-109">Dieses Fragment geht davon aus, dass bereits [eine Verbindung mit einem ILS-Server](connecting-to-an-ils-server.md) hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="76f1f-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span> <span data-ttu-id="76f1f-110">Die hier gezeigten Vorgänge werden im Abschnitt "Ändern der Einstellungen bei Bedarf" unter [Erstellen einer Konferenzankündigung](creating-a-conference-announcement.md)durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="76f1f-110">The operations shown here would be performed in the "Modify the settings if necessary" section of [Creating a Conference Announcement](creating-a-conference-announcement.md).</span></span>


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a><span data-ttu-id="76f1f-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76f1f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76f1f-112">Multicast-com-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="76f1f-112">Multicast COM Interfaces</span></span>](multicast-com-interfaces.md)
</dt> <dt>

[<span data-ttu-id="76f1f-113">**Imcastaddressallocation**</span><span class="sxs-lookup"><span data-stu-id="76f1f-113">**IMcastAddressAllocation**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[<span data-ttu-id="76f1f-114">**Imcastscope**</span><span class="sxs-lookup"><span data-stu-id="76f1f-114">**IMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[<span data-ttu-id="76f1f-115">**Imcastleaseinfo**</span><span class="sxs-lookup"><span data-stu-id="76f1f-115">**IMcastLeaseInfo**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[<span data-ttu-id="76f1f-116">**Ienummcastscope**</span><span class="sxs-lookup"><span data-stu-id="76f1f-116">**IEnumMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[<span data-ttu-id="76f1f-117">**Itconfererceblob**</span><span class="sxs-lookup"><span data-stu-id="76f1f-117">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="76f1f-118">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="76f1f-118">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="76f1f-119">**Itmediacollection**</span><span class="sxs-lookup"><span data-stu-id="76f1f-119">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="76f1f-120">**Ienumbstr**</span><span class="sxs-lookup"><span data-stu-id="76f1f-120">**IEnumBstr**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[<span data-ttu-id="76f1f-121">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="76f1f-121">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="76f1f-122">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="76f1f-122">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 



