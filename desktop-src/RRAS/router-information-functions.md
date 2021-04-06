---
title: Routerinformationsfunktionen
description: Verwenden Sie die folgenden Funktionen, um die Header und Blöcke der Routerinformationen zu bearbeiten. Ein Informations Header besteht aus privaten metadatendaten und Informations Blöcken. Informationsblöcke sind Arrays von Informationsstrukturen verschiedener Typen.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036231"
---
# <a name="router-information-functions"></a><span data-ttu-id="2553b-105">Routerinformationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="2553b-105">Router Information Functions</span></span>

<span data-ttu-id="2553b-106">Verwenden Sie die folgenden Funktionen, um die Header und Blöcke der Routerinformationen zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="2553b-106">Use the following functions to manipulate router information headers and blocks.</span></span> <span data-ttu-id="2553b-107">Ein Informations Header besteht aus privaten metadatendaten und Informations Blöcken.</span><span class="sxs-lookup"><span data-stu-id="2553b-107">An information header is composed of private meta-data and information blocks.</span></span> <span data-ttu-id="2553b-108">Informationsblöcke sind Arrays von [Informationsstrukturen](router-information-structures.md) verschiedener [Typen](router-information-enumerations.md).</span><span class="sxs-lookup"><span data-stu-id="2553b-108">Information blocks are arrays of [information structures](router-information-structures.md) of various [types](router-information-enumerations.md).</span></span>

<span data-ttu-id="2553b-109">Die folgenden Funktionen bearbeiten Informations Header:</span><span class="sxs-lookup"><span data-stu-id="2553b-109">The following functions manipulate information headers:</span></span>

-   [<span data-ttu-id="2553b-110">**Mprinfocreate**</span><span class="sxs-lookup"><span data-stu-id="2553b-110">**MprInfoCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [<span data-ttu-id="2553b-111">**Mprinfodelete**</span><span class="sxs-lookup"><span data-stu-id="2553b-111">**MprInfoDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [<span data-ttu-id="2553b-112">**Mprinfoduplicate**</span><span class="sxs-lookup"><span data-stu-id="2553b-112">**MprInfoDuplicate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [<span data-ttu-id="2553b-113">**Mprinforemoveall**</span><span class="sxs-lookup"><span data-stu-id="2553b-113">**MprInfoRemoveAll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

<span data-ttu-id="2553b-114">Die folgenden Funktionen bearbeiten Informationsblöcke innerhalb eines Informations Headers:</span><span class="sxs-lookup"><span data-stu-id="2553b-114">The following functions manipulate information blocks within an information header:</span></span>

-   [<span data-ttu-id="2553b-115">**Mprinfoblockadd**</span><span class="sxs-lookup"><span data-stu-id="2553b-115">**MprInfoBlockAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [<span data-ttu-id="2553b-116">**Mprinfoblockfind**</span><span class="sxs-lookup"><span data-stu-id="2553b-116">**MprInfoBlockFind**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [<span data-ttu-id="2553b-117">**Mprinfoblockquerysize**</span><span class="sxs-lookup"><span data-stu-id="2553b-117">**MprInfoBlockQuerySize**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [<span data-ttu-id="2553b-118">**Mprinfoblockremove**</span><span class="sxs-lookup"><span data-stu-id="2553b-118">**MprInfoBlockRemove**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [<span data-ttu-id="2553b-119">**Mprinfoblockset**</span><span class="sxs-lookup"><span data-stu-id="2553b-119">**MprInfoBlockSet**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

<span data-ttu-id="2553b-120">Viele der [routerverwaltungs-und Konfigurationsfunktionen](understanding-mprinfo-functions-and-information-headers.md) verwenden Informations Header.</span><span class="sxs-lookup"><span data-stu-id="2553b-120">Many of the [router administration and configuration functions](understanding-mprinfo-functions-and-information-headers.md) use information headers.</span></span>

 

 




