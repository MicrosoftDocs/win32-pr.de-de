---
description: Wenn Sie eine registrierte Netzwerkschnittstellenkarte (NIC) auswählen, die auf einem lokalen Computer aufgeführt ist, können Sie einen filterblob verwenden, um die NICs zu ignorieren, an denen Sie nicht interessiert sind.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Angeben eines filterblobs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8754b8f7ea5388b730fd2dfb65e26e24a906d648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349021"
---
# <a name="specifying-a-filter-blob"></a><span data-ttu-id="7d522-103">Angeben eines filterblobs</span><span class="sxs-lookup"><span data-stu-id="7d522-103">Specifying a Filter BLOB</span></span>

<span data-ttu-id="7d522-104">Wenn Sie eine registrierte Netzwerkschnittstellenkarte (NIC) auswählen, die auf einem lokalen Computer aufgeführt ist, können Sie einen [*filterblob*](f.md) verwenden, um die NICs zu ignorieren, an denen Sie nicht interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="7d522-104">When you select a registered network interface card (NIC) listed on a local computer, you can use a [*filter BLOB*](f.md) to disregard the NICs you are not interested in.</span></span> <span data-ttu-id="7d522-105">Beispielsweise können Sie die Suche nach einem bestimmten Kartentyp (z. b. Ethernet) oder auf eine bestimmte MAC-Adresse einschränken.</span><span class="sxs-lookup"><span data-stu-id="7d522-105">For example, you could restrict the search for a specific type of card (such as ETHERNET) or a specific MAC address.</span></span>

<span data-ttu-id="7d522-106">Während der Suche nach einer NIC muss jeder Eintrag im filterblob mit einem entsprechenden Eintrag im NPP-BLOB übereinstimmen, der die NIC darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d522-106">During the search for a NIC, every entry in the filter BLOB must match an equivalent entry in the NPP BLOB that represents the NIC.</span></span> <span data-ttu-id="7d522-107">Filterblobzeichen können auch [*spezielle blobzeichen*](s.md)sein.</span><span class="sxs-lookup"><span data-stu-id="7d522-107">Filter BLOBs can also be [*special BLOBs*](s.md).</span></span>

<span data-ttu-id="7d522-108">Wenn die [**getnppblobfromui**](getnppblobfromui.md) -Funktion aufgerufen wird, schränkt das filterblob die im Dialogfeld " **Netzwerk auswählen** " angezeigten NICs ein.</span><span class="sxs-lookup"><span data-stu-id="7d522-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the filter BLOB restricts the NICs displayed in the **Select a network** dialog box.</span></span> <span data-ttu-id="7d522-109">Wenn die [**getnppblobtable**](getnppblobtable.md) -Funktion aufgerufen wird, schränkt das filterblob die in der BLOB-Tabelle zurückgegebenen NICs ein.</span><span class="sxs-lookup"><span data-stu-id="7d522-109">When the [**GetNPPBlobTable**](getnppblobtable.md) function is called, the filter BLOB restricts the NICs returned in the BLOB table.</span></span>

<span data-ttu-id="7d522-110">Wenn Sie den Filter verwenden möchten, müssen Sie ein filterblob erstellen, die Werte der Eigenschaften festlegen, nach denen Sie filtern möchten (einschließlich aller speziellen BLOB-Einträge), und dann den blobfilter und einen Aufrufen der [**getnppblobtable**](getnppblobtable.md) -oder [**getnppblobfromui**](getnppblobfromui.md) -Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="7d522-110">To use the filter, you must create a filter BLOB, set the values of the properties you want to filter on (including any special BLOB entries), and then specify the BLOB filter and a call to the [**GetNPPBlobTable**](getnppblobtable.md) or [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>



| <span data-ttu-id="7d522-111">Für Informationen zu</span><span class="sxs-lookup"><span data-stu-id="7d522-111">For information on</span></span>                                 | <span data-ttu-id="7d522-112">Siehe</span><span class="sxs-lookup"><span data-stu-id="7d522-112">See</span></span>                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d522-113">Auswählen einer auf einem lokalen Computer registrierten NIC</span><span class="sxs-lookup"><span data-stu-id="7d522-113">How to select a NIC registered on a local computer</span></span> | [<span data-ttu-id="7d522-114">Auswählen einer registrierten NIC</span><span class="sxs-lookup"><span data-stu-id="7d522-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="7d522-115">Abrufen einer NPP-BLOB-Tabelle</span><span class="sxs-lookup"><span data-stu-id="7d522-115">Retrieving an NPP BLOB table</span></span>                       | [<span data-ttu-id="7d522-116">Auswählen einer NIC aus einer zurückgegebenen NPP-BLOB-Tabelle</span><span class="sxs-lookup"><span data-stu-id="7d522-116">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



