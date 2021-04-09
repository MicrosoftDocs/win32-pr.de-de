---
title: Übertragungs Syntax und NDR64
description: Das NDR Wire Protocol, auch als Übertragungs Syntax bezeichnet, ermöglicht RPC-aufrufen, das Netzwerk zu durchlaufen.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dfec9bc1569ef9a42d0bc844c3b098736f714ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039027"
---
# <a name="transfer-syntax-and-ndr64"></a><span data-ttu-id="e8779-103">Übertragungs Syntax und NDR64</span><span class="sxs-lookup"><span data-stu-id="e8779-103">Transfer Syntax and NDR64</span></span>

<span data-ttu-id="e8779-104">Das NDR Wire Protocol, auch als Übertragungs Syntax bezeichnet, ermöglicht RPC-aufrufen, das Netzwerk zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="e8779-104">The NDR wire protocol, also referred to as transfer syntax, enables RPC calls to traverse the network.</span></span> <span data-ttu-id="e8779-105">Das Wire-Protokoll definiert die Netzwerkdarstellung eines RPC-Aufrufs, z. b. die Reihenfolge, in der Datenmember gemarshallt werden, die Ausrichtung der Daten im Netzwerk, zusätzliche Informationen, die in den Daten enthalten sind, und andere Probleme.</span><span class="sxs-lookup"><span data-stu-id="e8779-105">The wire protocol defines the wire representation of an RPC call, such as the order in which data members are marshaled, alignment of data on the wire, additional information included with the data, and other issues.</span></span> <span data-ttu-id="e8779-106">Das NDR64-Protokoll ist eine Erweiterung der 32-Bit-basierten NDR-Übertragungs Syntax, die speziell erstellt wird, damit Entwickler, die auf 64-Bit-Systeme abzielen, eine optimierte Leistung erzielen können.</span><span class="sxs-lookup"><span data-stu-id="e8779-106">The NDR64 protocol is an extension to the 32-bit based NDR transfer syntax, created specifically to enable developers targeting 64-bit systems to achieve optimized performance.</span></span>

<span data-ttu-id="e8779-107">Die Unterschiede zwischen dem NDR-Wire-Format und dem NDR64 Wire-Format adressieren die unterschiedliche Größe von Zeigern in einer 64-Bit-Umgebung sowie andere Probleme.</span><span class="sxs-lookup"><span data-stu-id="e8779-107">The differences between the NDR wire format and the NDR64 wire format addresses the different size of pointers in a 64-bit environment, as well as other issues.</span></span> <span data-ttu-id="e8779-108">Die NDR64-Mechanismen werden von RPC behandelt.</span><span class="sxs-lookup"><span data-stu-id="e8779-108">The mechanics of NDR64 is handled by RPC.</span></span> <span data-ttu-id="e8779-109">Entwickler müssen nur die Befehlszeilenoption/[**Protocol**](/windows/desktop/Midl/-protocol)**all** Mittel l verwenden, um die Vorteile von NDR64 auf 64-Bit-Plattformen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e8779-109">Developers need only use the /[**protocol**](/windows/desktop/Midl/-protocol)**all** MIDL command line switch to obtain the benefits of NDR64 on 64-bit platforms.</span></span> <span data-ttu-id="e8779-110">NDR64 ist nur auf 64-Bit-Plattformen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e8779-110">NDR64 is available only on 64-bit platforms.</span></span>

 

 