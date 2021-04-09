---
title: Enumerationsflags
description: Enumerationsflags
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Enumeration
- Enumerationsflags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947725"
---
# <a name="enumeration-flags"></a><span data-ttu-id="47610-105">Enumerationsflags</span><span class="sxs-lookup"><span data-stu-id="47610-105">Enumeration Flags</span></span>



| <span data-ttu-id="47610-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="47610-106">Constant</span></span>               | <span data-ttu-id="47610-107">Wert</span><span class="sxs-lookup"><span data-stu-id="47610-107">Value</span></span>      | <span data-ttu-id="47610-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47610-108">Description</span></span>                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47610-109">RTM-Aufzählungs \_ \_ Start</span><span class="sxs-lookup"><span data-stu-id="47610-109">RTM\_ENUM\_START</span></span>       | <span data-ttu-id="47610-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47610-110">0x00000000</span></span> | <span data-ttu-id="47610-111">Auflisten von Routen oder Zielen ab 0/0.</span><span class="sxs-lookup"><span data-stu-id="47610-111">Enumerate routes or destinations starting at 0/0.</span></span>                                                                                                         |
| <span data-ttu-id="47610-112">RTM-Aufzählung \_ \_ als nächstes</span><span class="sxs-lookup"><span data-stu-id="47610-112">RTM\_ENUM\_NEXT</span></span>        | <span data-ttu-id="47610-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="47610-113">0x00000001</span></span> | <span data-ttu-id="47610-114">Listet Routen oder Ziele ab, beginnend bei der angegebenen Adresse/Maske (z. b. 10/8).</span><span class="sxs-lookup"><span data-stu-id="47610-114">Enumerate routes or destinations starting at the specified address/mask length (such as 10/8).</span></span> <span data-ttu-id="47610-115">Die Enumeration wird bis zum Ende der Routing Tabelle fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="47610-115">The enumeration continues to the end of the routing table.</span></span> |
| <span data-ttu-id="47610-116">RTM-Aufzählungs \_ \_ Bereich</span><span class="sxs-lookup"><span data-stu-id="47610-116">RTM\_ENUM\_RANGE</span></span>       | <span data-ttu-id="47610-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="47610-117">0x00000002</span></span> | <span data-ttu-id="47610-118">Listet Routen oder Ziele in der angegebenen Teilstruktur auf, die durch die Adresse/Maske-Länge (z. b. 10/8) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="47610-118">Enumerate routes or destinations in the specified subtree specified by the address/mask length (such as 10/8).</span></span>                                            |
| <span data-ttu-id="47610-119">RTM \_ \_ alle Endknoten \_ aufzählen</span><span class="sxs-lookup"><span data-stu-id="47610-119">RTM\_ENUM\_ALL\_DESTS</span></span>  | <span data-ttu-id="47610-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47610-120">0x00000000</span></span> | <span data-ttu-id="47610-121">Gibt alle Ziele zurück.</span><span class="sxs-lookup"><span data-stu-id="47610-121">Return all destinations.</span></span>                                                                                                                                  |
| <span data-ttu-id="47610-122">RTM- \_ \_ \_ ermittelungsendknoten</span><span class="sxs-lookup"><span data-stu-id="47610-122">RTM\_ENUM\_OWN\_DESTS</span></span>  | <span data-ttu-id="47610-123">0x01000000</span><span class="sxs-lookup"><span data-stu-id="47610-123">0x01000000</span></span> | <span data-ttu-id="47610-124">Gibt nur die Ziele zurück, die der Client besitzt.</span><span class="sxs-lookup"><span data-stu-id="47610-124">Return only those destinations that the client owns.</span></span>                                                                                                      |
| <span data-ttu-id="47610-125">RTM-Aufzählung für \_ \_ alle \_ Routen</span><span class="sxs-lookup"><span data-stu-id="47610-125">RTM\_ENUM\_ALL\_ROUTES</span></span> | <span data-ttu-id="47610-126">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47610-126">0x00000000</span></span> | <span data-ttu-id="47610-127">Alle Routen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="47610-127">Return all routes.</span></span>                                                                                                                                        |
| <span data-ttu-id="47610-128">RTM-Aufzählungs \_ \_ eigene \_ Routen</span><span class="sxs-lookup"><span data-stu-id="47610-128">RTM\_ENUM\_OWN\_ROUTES</span></span> | <span data-ttu-id="47610-129">0x00010000</span><span class="sxs-lookup"><span data-stu-id="47610-129">0x00010000</span></span> | <span data-ttu-id="47610-130">Gibt nur die Routen zurück, die der Client besitzt.</span><span class="sxs-lookup"><span data-stu-id="47610-130">Return only those routes that the client owns.</span></span>                                                                                                            |



 

 

 




