---
description: Die idownloadprogress-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Idownloadprogress-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958988"
---
# <a name="idownloadprogress-properties"></a><span data-ttu-id="c46bf-103">Idownloadprogress-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c46bf-103">IDownloadProgress Properties</span></span>

<span data-ttu-id="c46bf-104">Die [**idownloadprogress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c46bf-104">The [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="c46bf-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c46bf-105">Property</span></span>                                                                               | <span data-ttu-id="c46bf-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c46bf-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c46bf-107">**Currentupdatebytesherunter geladen**</span><span class="sxs-lookup"><span data-stu-id="c46bf-107">**CurrentUpdateBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | <span data-ttu-id="c46bf-108">Ruft eine Zeichenfolge ab, die angibt, wie viele Daten für die Inhalts Datei oder Dateien des heruntergeladenen Updates in Bytes übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="c46bf-108">Gets a string that specifies how much data has been transferred for the content file or files of the update that is being downloaded, in bytes.</span></span>  |
| [<span data-ttu-id="c46bf-109">**Currentupdatebytestodownload**</span><span class="sxs-lookup"><span data-stu-id="c46bf-109">**CurrentUpdateBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | <span data-ttu-id="c46bf-110">Ruft eine Zeichenfolge ab, die schätzt, wie viele Daten für die Inhalts Datei oder Dateien des heruntergeladenen Updates in Bytes übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c46bf-110">Gets a string that estimates how much data should be transferred for the content file or files of the update that is being downloaded, in bytes.</span></span> |
| [<span data-ttu-id="c46bf-111">**Currentupdatedownloadphase**</span><span class="sxs-lookup"><span data-stu-id="c46bf-111">**CurrentUpdateDownloadPhase**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | <span data-ttu-id="c46bf-112">Ruft einen [**Downloadphase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) -Enumerationswert ab, der die Phase des Downloads angibt, der gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c46bf-112">Gets a [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) enumeration value that specifies the phase of the download that is currently in progress.</span></span>          |
| [<span data-ttu-id="c46bf-113">**Currentupdateingedex**</span><span class="sxs-lookup"><span data-stu-id="c46bf-113">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | <span data-ttu-id="c46bf-114">Ruft einen NULL basierten Indexwert ab, der das Update angibt, das gerade heruntergeladen wird, wenn mehrere Updates ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="c46bf-114">Gets a zero-based index value that specifies the update that is currently being downloaded when multiple updates have been selected.</span></span>             |
| [<span data-ttu-id="c46bf-115">**Currentupdateprozentucomplete**</span><span class="sxs-lookup"><span data-stu-id="c46bf-115">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="c46bf-116">Ruft eine Schätzung des Prozentsatzes des aktuellen Updates ab, das heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="c46bf-116">Gets an estimate of the percentage of the current update that has been downloaded.</span></span>                                                               |
| [<span data-ttu-id="c46bf-117">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="c46bf-117">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | <span data-ttu-id="c46bf-118">Ruft eine Schätzung des Prozentsatzes aller Updates ab, die heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="c46bf-118">Gets an estimate of the percentage of all the updates that have been downloaded.</span></span>                                                                 |
| [<span data-ttu-id="c46bf-119">**Totalbytesherunter geladen**</span><span class="sxs-lookup"><span data-stu-id="c46bf-119">**TotalBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | <span data-ttu-id="c46bf-120">Ruft eine Zeichenfolge ab, die die Gesamtmenge der heruntergeladenen Daten in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="c46bf-120">Gets a string that specifies the total amount of data that has been downloaded, in bytes.</span></span>                                                        |
| [<span data-ttu-id="c46bf-121">**Totalbytestodownload**</span><span class="sxs-lookup"><span data-stu-id="c46bf-121">**TotalBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | <span data-ttu-id="c46bf-122">Ruft eine Zeichenfolge ab, die die Schätzung der Gesamtmenge der heruntergeladenen Daten in Bytes darstellt.</span><span class="sxs-lookup"><span data-stu-id="c46bf-122">Gets a string that represents the estimate of the total amount of data that will be downloaded, in bytes.</span></span>                                        |



 

 

 



