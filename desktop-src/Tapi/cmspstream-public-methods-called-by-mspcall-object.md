---
description: Die folgende Liste enthält die cmspstream-Methoden, die vom mspcalljekt aufgerufen werden.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Vom mspcallcenter-Objekt aufgerufene cmspstream-Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351792"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a><span data-ttu-id="f8bba-103">Vom mspcallcenter-Objekt aufgerufene öffentliche cmspstream-Methoden</span><span class="sxs-lookup"><span data-stu-id="f8bba-103">CMSPStream Public Methods Called by MSPCall Object</span></span>



| <span data-ttu-id="f8bba-104">Öffentliche cmspstream-Methoden</span><span class="sxs-lookup"><span data-stu-id="f8bba-104">CMSPStream public methods</span></span>                                 | <span data-ttu-id="f8bba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8bba-105">Description</span></span>                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8bba-106">**Init**</span><span class="sxs-lookup"><span data-stu-id="f8bba-106">**Init**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | <span data-ttu-id="f8bba-107">Wird von **mspcallaufgerufen** , wenn der Stream erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f8bba-107">Called by the **MSPCall** when the stream is created.</span></span>                                   |
| [<span data-ttu-id="f8bba-108">**Abschlusses**</span><span class="sxs-lookup"><span data-stu-id="f8bba-108">**ShutDown**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | <span data-ttu-id="f8bba-109">Wird von **mspcallaufgerufen** , um die Auswahl aller Terminal Objekte aufzuheben und das Aufruf Objekt freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f8bba-109">Called by the **MSPCall** to unselect all terminal objects and release the call object.</span></span> |
| [<span data-ttu-id="f8bba-110">**GetState**</span><span class="sxs-lookup"><span data-stu-id="f8bba-110">**GetState**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | <span data-ttu-id="f8bba-111">Wird vom mspcallobjekt aufgerufen, um den aktuellen Status des Streams abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f8bba-111">Called by the MSPCall object to get the current status of the stream.</span></span>                   |
| [<span data-ttu-id="f8bba-112">**Handletspdata**</span><span class="sxs-lookup"><span data-stu-id="f8bba-112">**HandleTSPData**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | <span data-ttu-id="f8bba-113">Das abgeleitete calltobjekt kann diese Methode aufzurufen, damit der Stream die TSP-Befehle behandelt.</span><span class="sxs-lookup"><span data-stu-id="f8bba-113">Derived call object may call this method to let the stream handle the TSP commands.</span></span>     |
| [<span data-ttu-id="f8bba-114">**Processgraphevent**</span><span class="sxs-lookup"><span data-stu-id="f8bba-114">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | <span data-ttu-id="f8bba-115">Wird vom mspcallobjekt aufgerufen, damit der Stream Diagramm Ereignisse behandelt.</span><span class="sxs-lookup"><span data-stu-id="f8bba-115">Called by the MSPCall object to let the stream handle graph events.</span></span>                     |



 

 

 



