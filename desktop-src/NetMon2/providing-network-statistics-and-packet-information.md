---
description: Der Netzwerk Paketanbieter (NPP) ist eine DLL-Datei, die mit dem Netzwerkmonitor-Treiber kommuniziert und Netzwerk Statistiken und Paketdaten bereitstellt.
ms.assetid: ee258bf7-7894-458d-b418-57a19ac985f2
title: Bereitstellen von Netzwerk Statistiken und Paketinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68be6b5b0db1fae2c19f5bc44e6e94a54c63b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368898"
---
# <a name="providing-network-statistics-and-packet-information"></a><span data-ttu-id="70866-103">Bereitstellen von Netzwerk Statistiken und Paketinformationen</span><span class="sxs-lookup"><span data-stu-id="70866-103">Providing Network Statistics and Packet Information</span></span>

<span data-ttu-id="70866-104">Der Netzwerk Paketanbieter (NPP) ist eine DLL-Datei, die mit dem Netzwerkmonitor-Treiber kommuniziert und Netzwerk Statistiken und Paketdaten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="70866-104">The Network Packet Provider (NPP) is a DLL that communicates with the Network Monitor driver and provides network statistics and packet data.</span></span>

<span data-ttu-id="70866-105">Die gängigsten Methoden zur Verwendung des NPP sind:</span><span class="sxs-lookup"><span data-stu-id="70866-105">The most common ways to use the NPP include:</span></span>

-   <span data-ttu-id="70866-106">Netzwerk Statistiken.</span><span class="sxs-lookup"><span data-stu-id="70866-106">Network statistics.</span></span>
-   <span data-ttu-id="70866-107">Rahmen, die in Echtzeit an die Anwendung übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="70866-107">Frames passed to the application in real time.</span></span>
-   <span data-ttu-id="70866-108">Pakete, auf die erst zugegriffen werden kann, nachdem die Erfassung beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="70866-108">Packets accessible only after the capture has been stopped.</span></span>

<span data-ttu-id="70866-109">Dieser Abschnitt schließt folgende Themen ein:</span><span class="sxs-lookup"><span data-stu-id="70866-109">This section includes the following topics:</span></span>

-   [<span data-ttu-id="70866-110">Auswählen einer NIC</span><span class="sxs-lookup"><span data-stu-id="70866-110">Selecting a NIC</span></span>](selecting-a-nic-using-getnppblobfromui.md)
-   [<span data-ttu-id="70866-111">Verwenden von getnppblobtable</span><span class="sxs-lookup"><span data-stu-id="70866-111">Using GetNPPBlobTable</span></span>](using-getnppblobtable.md)

 

 



