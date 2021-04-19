---
description: Sockaddr-Strukturen und Annahmen der Byte Reihenfolge in Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Annahmen der Byte Reihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe6abf9ed46302bd037d1eb130b18c5568518cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346943"
---
# <a name="byte-ordering-assumptions"></a><span data-ttu-id="db581-103">Annahmen der Byte Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="db581-103">Byte Ordering Assumptions</span></span>

<span data-ttu-id="db581-104">Ein Dienstanbieter sollte alle [**sockaddr**](sockaddr-2.md) -Komponenten, die vom Adress familienparameter ausgenommen sind, so behandeln, als ob Sie sich in der Netzwerk-Byte Reihenfolge befinden, und der Adress familienparameter wie in der Byte Reihenfolge des lokalen Computers.</span><span class="sxs-lookup"><span data-stu-id="db581-104">A service provider should treat all [**sockaddr**](sockaddr-2.md) components exclusive of the address family parameter as if they are in the network byte order, and the address family parameter as in the local computer's byte order.</span></span> <span data-ttu-id="db581-105">Es liegt in der Verantwortung der Winsock-Anwendung, sicherzustellen, dass die in **sockaddr** -Strukturen enthaltenen Adressen ordnungsgemäß angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="db581-105">It is the Winsock application's responsibility to make sure that addresses contained in **sockaddr** structures are properly arranged.</span></span> <span data-ttu-id="db581-106">Die Winsock-API bietet eine Reihe von Konvertierungs Routinen, um diese Aufgabe zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="db581-106">The Winsock API provides a number of conversion routines to simplify this task.</span></span> <span data-ttu-id="db581-107">Derzeit verstehen diese Routinen die Konvertierung zwischen der natürlichen Byte Reihenfolge des lokalen Hosts und der Bytesortierung von Big-Endian oder Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="db581-107">Currently these routines understand conversion between the local host's natural byte order and either big-Endian or little-Endian network byte ordering.</span></span> <span data-ttu-id="db581-108">Die Winsock-Architektur kann in Zukunft andere Byte Reihenfolge Schemas unterstützen.</span><span class="sxs-lookup"><span data-stu-id="db581-108">The Winsock architecture can support other byte ordering schemes in the future.</span></span>

 

 



