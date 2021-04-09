---
description: Die Windows Sockets 2 (Winsock)-Architektur ist mit der Windows Open System Architecture (WOSA) kompatibel.
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Architektur von Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130416"
---
# <a name="windows-sockets-2-architecture"></a><span data-ttu-id="b1700-103">Architektur von Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="b1700-103">Windows Sockets 2 Architecture</span></span>

<span data-ttu-id="b1700-104">Die Windows Sockets 2-Architektur ist mit der Windows Open System Architecture (WOSA) kompatibel, wie unten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="b1700-104">The Windows Sockets 2 architecture is compliant with the Windows Open System Architecture (WOSA), as illustrated below:</span></span>

![Architektur von Windows Sockets 2](images/ovrvw2-1.png)

<span data-ttu-id="b1700-106">Winsock definiert eine Standard-Service Provider Interface (SPI) zwischen der Anwendungsprogrammierschnittstelle (Application Programming Interface, API), deren Funktionen aus ws2 \_32.dll und den Protokoll Stapeln exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="b1700-106">Winsock defines a standard service provider interface (SPI) between the application programming interface (API), with its functions exported from WS2\_32.dll and the protocol stacks.</span></span> <span data-ttu-id="b1700-107">Folglich ist die Winsock-Unterstützung nicht auf TCP/IP-Protokollstapel beschränkt, wie es bei Windows Sockets 1,1 der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="b1700-107">Consequently, Winsock support is not limited to TCP/IP protocol stacks as is the case for Windows Sockets 1.1.</span></span>

<span data-ttu-id="b1700-108">Mit der Windows Sockets 2-Architektur ist es nicht notwendig oder wünschenswert, dass Stack-Anbieter eine eigene Implementierung von ws2-32.dll bereitstellen \_ , da ein einzelner ws2 \_32.dll in allen Stapeln funktionieren muss.</span><span class="sxs-lookup"><span data-stu-id="b1700-108">With the Windows Sockets 2 architecture, it is not necessary or desirable, for stack vendors to supply their own implementation of WS2\_32.dll, since a single WS2\_32.dll must work across all stacks.</span></span> <span data-ttu-id="b1700-109">Die ws2 \_ -32.dll und Kompatibilitäts-Shims sollten auf die gleiche Weise wie eine Betriebssystem Komponente angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b1700-109">The WS2\_32.dll and compatibility shims should be viewed in the same way as an operating system component.</span></span>

 

 



