---
description: Um eine NIC aus einer NPP-BLOB-Tabelle auszuwählen, die von Netzwerkmonitor zurückgegeben wird, können Sie die getnppblobtable-Funktion aufrufen. Diese Funktion gibt eine NPP-BLOB-Tabelle zurück, die dann von Ihrer Anwendung aufgelistet werden kann, um die gewünschte NIC auszuwählen.
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: Auswählen einer NIC aus einer zurückgegebenen NPP-BLOB-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08215bb647482ba8544d7eaa033dea7efd9a5ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865184"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a><span data-ttu-id="08e82-104">Auswählen einer NIC aus einer zurückgegebenen NPP-BLOB-Tabelle</span><span class="sxs-lookup"><span data-stu-id="08e82-104">Selecting a NIC from a Returned NPP BLOB table</span></span>

<span data-ttu-id="08e82-105">Um eine NIC aus einer NPP-BLOB-Tabelle auszuwählen, die von Netzwerkmonitor zurückgegeben wird, können Sie die [**getnppblobtable**](getnppblobtable.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="08e82-105">To select a NIC from an NPP BLOB table returned by Network Monitor, call the [**GetNPPBlobTable**](getnppblobtable.md) function.</span></span> <span data-ttu-id="08e82-106">Diese Funktion gibt eine NPP-BLOB-Tabelle zurück, die dann von Ihrer Anwendung aufgelistet werden kann, um die gewünschte NIC auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="08e82-106">This function returns an NPP BLOB table, which can then be enumerated by your application to select the NIC you are interested in.</span></span>

<span data-ttu-id="08e82-107">Wenn Sie diese Funktion aufgerufen haben, können Sie entweder eine BLOB-Tabelle aller auf dem lokalen Computer registrierten NICs oder einen kleineren Satz gefilterter NICs zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="08e82-107">When you call this function you can return either a BLOB table of all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="08e82-108">Wenn Sie die zurückgegebenen NICs filtern möchten, können Sie ein [*filterblob*](f.md) angeben, wenn der-Befehl aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="08e82-108">To filter the NICs that are returned, you can provide a [*filter BLOB*](f.md) when the call is made.</span></span>



| <span data-ttu-id="08e82-109">Informationen über</span><span class="sxs-lookup"><span data-stu-id="08e82-109">For information about</span></span>                                                       | <span data-ttu-id="08e82-110">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="08e82-110">See</span></span>                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08e82-111">Gibt an, wie ein Filter angegeben wird, der die in einer NPP-BLOB-Tabelle zurückgegebenen NICs einschränkt.</span><span class="sxs-lookup"><span data-stu-id="08e82-111">How to specify a filter that limits the NICs returned in an NPP BLOB table.</span></span> | [<span data-ttu-id="08e82-112">Angeben eines filterblobs</span><span class="sxs-lookup"><span data-stu-id="08e82-112">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="08e82-113">Auswählen einer NIC, die auf einem lokalen Computer registriert ist.</span><span class="sxs-lookup"><span data-stu-id="08e82-113">How to select a NIC registered on a local computer.</span></span>                         | [<span data-ttu-id="08e82-114">Auswählen einer registrierten NIC</span><span class="sxs-lookup"><span data-stu-id="08e82-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="08e82-115">Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle</span><span class="sxs-lookup"><span data-stu-id="08e82-115">How to select a NIC from a supplied NPP BLOB table</span></span>                          | [<span data-ttu-id="08e82-116">Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle</span><span class="sxs-lookup"><span data-stu-id="08e82-116">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



