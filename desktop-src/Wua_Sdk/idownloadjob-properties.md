---
description: Die idownloadjob-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Idownloadjob-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345135"
---
# <a name="idownloadjob-properties"></a><span data-ttu-id="58428-103">Idownloadjob-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58428-103">IDownloadJob Properties</span></span>

<span data-ttu-id="58428-104">Die [**idownloadjob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58428-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following properties.</span></span>



| <span data-ttu-id="58428-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="58428-105">Property</span></span>                                        | <span data-ttu-id="58428-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58428-106">Description</span></span>                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58428-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="58428-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | <span data-ttu-id="58428-108">Ruft das aufruferspezifische Zustands Objekt ab, das an die [**iupdatedownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="58428-108">Gets the caller-specific state object that is passed to the [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) method.</span></span>           |
| [<span data-ttu-id="58428-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="58428-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | <span data-ttu-id="58428-110">Ruft die Einstellung ab, die angibt, ob der Aufrufen von [**iupdatedownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) vollständig verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="58428-110">Gets the setting that indicates whether the call to [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) was processed completely.</span></span> |
| [<span data-ttu-id="58428-111">**Updates**</span><span class="sxs-lookup"><span data-stu-id="58428-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | <span data-ttu-id="58428-112">Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der in einem Download angegebenen Updates enthält.</span><span class="sxs-lookup"><span data-stu-id="58428-112">Gets an interface that contains a read-only collection of the updates that are specified in a download.</span></span>                                                  |



 

 

 



