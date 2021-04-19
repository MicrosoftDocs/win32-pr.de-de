---
description: Der drv \_ -Datentyp "drv RequestId" wird verwendet, um einen eindeutigen Bezeichner für eine Anforderung an den Dienstanbieter bereitzustellen.
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9c0db093b06b263bcdc702ff14af7e308033f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350215"
---
# <a name="drv_requestid"></a><span data-ttu-id="52cdf-103">DRV \_ -RequestId</span><span class="sxs-lookup"><span data-stu-id="52cdf-103">DRV\_REQUESTID</span></span>

<span data-ttu-id="52cdf-104">Der **drv-Datentyp "drv \_ RequestId** " wird verwendet, um einen eindeutigen Bezeichner für eine Anforderung an den Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="52cdf-104">The **DRV\_REQUESTID** datatype is used to supply a unique identifier for a request to the service provider.</span></span> <span data-ttu-id="52cdf-105">Ein Wert dieses Typs wird als Parameter an jede Funktion übergeben, die einen asynchronen Vorgang zulässt.</span><span class="sxs-lookup"><span data-stu-id="52cdf-105">A value of this type is passed as a parameter to every function that allows for asynchronous operation.</span></span> <span data-ttu-id="52cdf-106">Wenn der Vorgang asynchron ist, gibt der Dienstanbieter diesen Wert als Rückgabewert der Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="52cdf-106">If the operation is asynchronous, the service provider returns this value as the return value of the function.</span></span> <span data-ttu-id="52cdf-107">Immer wenn der Dienstanbieter auf diese Weise eine Anforderung als asynchron ausweist, muss der Vorgang durch Aufrufen der Funktion [*Abschluss \_ proc*](/windows/win32/api/tspi/nc-tspi-async_completion) Callback abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="52cdf-107">Whenever the service provider flags a request as asynchronous in this way, it must eventually report the operation is complete by calling the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function.</span></span>

<span data-ttu-id="52cdf-108">TAPI stellt sicher, dass die von ihm bereitgestellten **drv \_ -RequestId-** Werte genau positiv sind, d. h. zwischen den Werten von 0x00000001 und 0x7FFFFFFF (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="52cdf-108">TAPI ensures that the **DRV\_REQUESTID** values it supplies are strictly positive, that is, between the values of 0x00000001 and 0x7FFFFFFF, inclusive.</span></span> <span data-ttu-id="52cdf-109">Außerdem sind die Werte insofern eindeutig, als dass kein Wert, der von einer Funktion zurückgegeben wird, um die Anforderung als asynchron zu markieren, wieder verwendet wird, bevor der Vorgang als beendet gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="52cdf-109">Furthermore, the values are unique in that no value returned from a function to flag the request as asynchronous will be re-used before the operation is reported complete.</span></span>

 

 
