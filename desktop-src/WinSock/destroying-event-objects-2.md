---
description: Verwenden von wpucloseevent zum Zerstören eines Ereignis Objekts (Anwendung oder Dienstanbieter), wenn das Ereignis Objekt nicht mehr benötigt wird.
ms.assetid: ad6f7018-3647-4ab8-9a77-d833d18cd4b6
title: Zerstören von Ereignis Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f0a17f623d0dd9ebceaf76b963ce72306000b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343539"
---
# <a name="destroying-event-objects"></a><span data-ttu-id="ef993-103">Zerstören von Ereignis Objekten</span><span class="sxs-lookup"><span data-stu-id="ef993-103">Destroying Event Objects</span></span>

<span data-ttu-id="ef993-104">Die Entität, die ein Ereignis Objekt (Anwendung oder Dienstanbieter) erstellt, ist dafür verantwortlich, Sie zu zerstören, wenn Sie nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ef993-104">The entity that creates an event object (application or service provider) is responsible for destroying it when it is no longer required.</span></span> <span data-ttu-id="ef993-105">Dienstanbieter führen dies über **wpucloseevent** durch.</span><span class="sxs-lookup"><span data-stu-id="ef993-105">Service providers do this through **WPUCloseEvent**.</span></span>

 

 



