---
description: Netzwerkmonitor bietet drei Funktionen zum Auswählen einer Netzwerkschnittstellenkarte (NIC). Diese Funktionen bieten drei Möglichkeiten zum Auflisten eines Satzes von NICs und zum Auswählen des zu verwendenden NICs. In der folgenden Tabelle sind diese Funktionen aufgeführt.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Auswählen einer Netzwerkschnittstellenkarte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131192"
---
# <a name="selecting-a-network-interface-card"></a><span data-ttu-id="3202b-105">Auswählen einer Netzwerkschnittstellenkarte</span><span class="sxs-lookup"><span data-stu-id="3202b-105">Selecting a Network Interface Card</span></span>

<span data-ttu-id="3202b-106">Netzwerkmonitor bietet drei Funktionen zum Auswählen einer Netzwerkschnittstellenkarte (NIC).</span><span class="sxs-lookup"><span data-stu-id="3202b-106">Network Monitor provides three functions for selecting a network interface card (NIC).</span></span> <span data-ttu-id="3202b-107">Diese Funktionen bieten drei Möglichkeiten zum Auflisten eines Satzes von NICs und zum Auswählen des zu verwendenden NICs.</span><span class="sxs-lookup"><span data-stu-id="3202b-107">These functions provide three ways to enumerate a set of NICs and select the one you want to use.</span></span> <span data-ttu-id="3202b-108">In der folgenden Tabelle sind diese Funktionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3202b-108">The following table lists these functions.</span></span>



| <span data-ttu-id="3202b-109">Funktion</span><span class="sxs-lookup"><span data-stu-id="3202b-109">Function</span></span>                                                 | <span data-ttu-id="3202b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3202b-110">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3202b-111">**Getnppblobfromui**</span><span class="sxs-lookup"><span data-stu-id="3202b-111">**GetNPPBlobFromUI**</span></span>](getnppblobfromui.md)             | <span data-ttu-id="3202b-112">Verwendet die Netzwerkmonitor-Benutzeroberfläche, um die registrierten NICs anzuzeigen, und gibt das NPP-BLOB zurück, das die NIC darstellt, an der Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="3202b-112">Uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you are interested in.</span></span>           |
| [<span data-ttu-id="3202b-113">**Getnppblobtable**</span><span class="sxs-lookup"><span data-stu-id="3202b-113">**GetNPPBlobTable**</span></span>](getnppblobtable.md)               | <span data-ttu-id="3202b-114">Gibt eine BLOB-Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="3202b-114">Returns a BLOB table.</span></span> <span data-ttu-id="3202b-115">Die Anwendung muss die Tabelle auflisten und einen NPP-BLOB auswählen.</span><span class="sxs-lookup"><span data-stu-id="3202b-115">The application must enumerate the table and select an NPP BLOB.</span></span>                                                       |
| [<span data-ttu-id="3202b-116">**Selectnppblobfromtable**</span><span class="sxs-lookup"><span data-stu-id="3202b-116">**SelectNPPBlobFromTable**</span></span>](selectnppblobfromtable.md) | <span data-ttu-id="3202b-117">Verwendet die Netzwerkmonitor-Schnittstelle, um die angegebenen NPP-BLOBs anzuzeigen, und gibt das NPP-BLOB zurück, das die NIC darstellt, an der Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="3202b-117">Uses the Network Monitor interface to display the supplied NPP BLOBs and returns the NPP BLOB that represents the NIC you are interested in.</span></span> |



 

<span data-ttu-id="3202b-118">Jede NIC wird durch einen NPP-Binary Large Object (BLOB) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3202b-118">Each NIC is represented by an NPP binary large object (BLOB).</span></span> <span data-ttu-id="3202b-119">Diese Funktionen können ein einzelnes NPP-BLOB von den auf dem Computer registrierten, einem einzelnen NPP-BLOB aus einer bereitgestellten NPP-BLOB-Tabelle oder einer Tabelle mit NPP-BLOBs zurückgeben, die der Aufrufer dann verwenden muss, um ein bestimmtes BLOB auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3202b-119">These functions can return a single NPP BLOB from those registered on the computer, a single NPP BLOB from a supplied NPP BLOB table, or a table of NPP BLOBs that the caller must then use to select a specific BLOB.</span></span> <span data-ttu-id="3202b-120">In den ersten beiden Fällen zeigt die Netzwerkmonitor-Benutzeroberfläche bei der Auswahl aus den registrierten NICs oder einer bereitgestellten NPP-BLOB-Tabelle die NICs an, die Sie auswählen können.</span><span class="sxs-lookup"><span data-stu-id="3202b-120">In the first two cases, when selecting from the registered NICs or from a supplied NPP BLOB table, the Network Monitor UI displays the NICs you can select.</span></span>

> [!Note]  
> <span data-ttu-id="3202b-121">Netzwerkmonitor verwendet eine Funktion mit dem Namen NPP Finder, um die auf dem lokalen Computer registrierten NICs aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="3202b-121">Network Monitor uses a feature called the NPP Finder to enumerate the NICs registered on the local computer.</span></span> <span data-ttu-id="3202b-122">Der NPP-Finder ist eine Komponente von Npptools.dll.</span><span class="sxs-lookup"><span data-stu-id="3202b-122">The NPP Finder is a component of Npptools.dll.</span></span>

 



| <span data-ttu-id="3202b-123">Informationen über</span><span class="sxs-lookup"><span data-stu-id="3202b-123">For information about</span></span>                            | <span data-ttu-id="3202b-124">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="3202b-124">See</span></span>                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3202b-125">Auswählen einer auf dem lokalen Computer registrierten NIC</span><span class="sxs-lookup"><span data-stu-id="3202b-125">Selecting a NIC registered on the local computer</span></span> | [<span data-ttu-id="3202b-126">Auswählen einer registrierten NIC</span><span class="sxs-lookup"><span data-stu-id="3202b-126">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="3202b-127">Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle</span><span class="sxs-lookup"><span data-stu-id="3202b-127">Selecting a NIC from a supplied NPP BLOB table</span></span>   | [<span data-ttu-id="3202b-128">Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle</span><span class="sxs-lookup"><span data-stu-id="3202b-128">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| <span data-ttu-id="3202b-129">Abrufen einer NPP-BLOB-Tabelle</span><span class="sxs-lookup"><span data-stu-id="3202b-129">Retrieving an NPP BLOB table</span></span>                     | [<span data-ttu-id="3202b-130">Auswählen einer NIC aus einer zurückgegebenen NPP-BLOB-Tabelle</span><span class="sxs-lookup"><span data-stu-id="3202b-130">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



