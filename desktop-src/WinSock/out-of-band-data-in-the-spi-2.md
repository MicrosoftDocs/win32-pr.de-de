---
description: Die Dienstanbieter, die die OOB-Abstraktion (Out-of-Band-Daten) für die Sockets im Stream-Stil unterstützen, müssen der Semantik in diesem Abschnitt entsprechen.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Out-of-Band-Daten in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9808fa301073bcbb06be23a9487c2a1fa4f14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041723"
---
# <a name="out-of-band-data-in-the-spi"></a><span data-ttu-id="4f684-103">Out-of-Band-Daten in der SPI</span><span class="sxs-lookup"><span data-stu-id="4f684-103">Out-of-Band Data in the SPI</span></span>

<span data-ttu-id="4f684-104">Die Dienstanbieter, die die OOB-Abstraktion (Out-of-Band-Daten) für die Sockets im Stream-Stil unterstützen, müssen der Semantik in diesem Abschnitt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4f684-104">The service providers which support the out-of-band data (OOB) abstraction for the stream-style sockets must adhere to the semantics in this section.</span></span> <span data-ttu-id="4f684-105">Wir beschreiben die OOB-Datenverarbeitung auf Protokoll unabhängige Weise.</span><span class="sxs-lookup"><span data-stu-id="4f684-105">We will describe OOB data handling in a protocol-independent manner.</span></span> <span data-ttu-id="4f684-106">Eine Erläuterung der OOB-Daten, die mithilfe von dringenden Daten in TCP/IP-Dienstanbietern implementiert werden, finden Sie in den [Winsock-Anlagen](winsock-annexes.md) .</span><span class="sxs-lookup"><span data-stu-id="4f684-106">Please refer to the [Winsock Annexes](winsock-annexes.md) for a discussion of OOB data implemented using urgent data in TCP/IP service providers.</span></span> <span data-ttu-id="4f684-107">Im folgenden gilt die Verwendung von [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) auch für [**wsprecvfrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f684-107">In the following, the use of [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) also applies to [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).</span></span>

 

 
