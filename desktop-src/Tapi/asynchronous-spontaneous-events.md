---
description: Es gibt eine weitere Klasse von asynchronen Ereignissen neben den oben beschriebenen.
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: Asynchrone, spontane Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd923ba7759ca88994fbf541c9f912ec660a7552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356276"
---
# <a name="asynchronous-spontaneous-events"></a><span data-ttu-id="7f175-103">Asynchrone, spontane Ereignisse</span><span class="sxs-lookup"><span data-stu-id="7f175-103">Asynchronous Spontaneous Events</span></span>

<span data-ttu-id="7f175-104">Es gibt eine weitere Klasse von asynchronen Ereignissen neben den oben beschriebenen.</span><span class="sxs-lookup"><span data-stu-id="7f175-104">There is another class of asynchronous events besides those described above.</span></span> <span data-ttu-id="7f175-105">Diese Ereignisse sind "spontan" in dem Sinne, dass Sie keine direkten Ergebnisse der entsprechenden Anforderungen sind.</span><span class="sxs-lookup"><span data-stu-id="7f175-105">These events are "spontaneous" in the sense that they are not direct results of corresponding requests.</span></span> <span data-ttu-id="7f175-106">Diese Ereignisse werden in solchen Fällen erkannt, wenn ein eingehender Anruf eingeht oder wenn ein ausgehender Anruf von einem "Klingeln" in den Status "antwortet" wechselt.</span><span class="sxs-lookup"><span data-stu-id="7f175-106">These events are detected in such cases as when an incoming call arrives, or when an outbound call goes from a "ringing" to an "answering" state.</span></span> <span data-ttu-id="7f175-107">Wenn TAPI zuerst Interaktionen mit dem TSPI für ein bestimmtes Gerät initialisiert, übergibt es einen Zeiger auf eine Rückruf Prozedur, die aufgerufen wird, um solche spontanen Ereignisse zu melden.</span><span class="sxs-lookup"><span data-stu-id="7f175-107">When TAPI first initializes interactions with the TSPI for a particular device, it passes a pointer to a callback procedure to be called for reporting such spontaneous events.</span></span> <span data-ttu-id="7f175-108">Zusammen mit diesem Prozedur Zeiger ist ein Geräte handle, das der Dienstanbieter als einen der tatsächlichen Parameter des Rückrufs enthält.</span><span class="sxs-lookup"><span data-stu-id="7f175-108">Along with this procedure pointer is a device handle that the service provider includes as one of the actual parameters to the callback.</span></span>

 

 



