---
description: Die iupdatedownloader-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Iupdatedownloader-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752081"
---
# <a name="iupdatedownloader-properties"></a><span data-ttu-id="00c46-103">Iupdatedownloader-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00c46-103">IUpdateDownloader Properties</span></span>

<span data-ttu-id="00c46-104">Die [**iupdatedownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="00c46-104">The [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) interface defines the following properties.</span></span>



| <span data-ttu-id="00c46-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="00c46-105">Property</span></span>                                                             | <span data-ttu-id="00c46-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00c46-106">Description</span></span>                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00c46-107">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="00c46-107">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | <span data-ttu-id="00c46-108">Ruft die aktuelle Client Anwendung ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="00c46-108">Gets and sets the current client application.</span></span>                                                                                                                              |
| [<span data-ttu-id="00c46-109">**Isforced**</span><span class="sxs-lookup"><span data-stu-id="00c46-109">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | <span data-ttu-id="00c46-110">Ruft einen booleschen Wert ab, der angibt, ob der Windows Update-Agent (WUA) das Herunterladen von Updates erzwingt, die bereits installiert sind oder nicht installiert werden können, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="00c46-110">Gets and sets a Boolean value that indicates whether the Windows Update Agent (WUA) forces the download of updates that are already installed or that cannot be installed.</span></span> |
| [<span data-ttu-id="00c46-111">**Priorität**</span><span class="sxs-lookup"><span data-stu-id="00c46-111">**Priority**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | <span data-ttu-id="00c46-112">Ruft die Prioritäts Ebene des Downloads ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="00c46-112">Gets and sets the priority level of the download.</span></span>                                                                                                                          |
| [<span data-ttu-id="00c46-113">**Updates**</span><span class="sxs-lookup"><span data-stu-id="00c46-113">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | <span data-ttu-id="00c46-114">Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der für den Download angegebenen Updates enthält, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="00c46-114">Gets and sets an interface that contains a read-only collection of the updates that are specified for download.</span></span>                                                            |



 

 

 



