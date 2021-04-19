---
description: Um eine der auf dem lokalen Computer registrierten NICs auszuwählen, müssen Sie die getnppblobfromui-Funktion aufrufen.
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: Auswählen einer registrierten NIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367863"
---
# <a name="selecting-a-registered-nic"></a><span data-ttu-id="8347e-103">Auswählen einer registrierten NIC</span><span class="sxs-lookup"><span data-stu-id="8347e-103">Selecting a Registered NIC</span></span>

<span data-ttu-id="8347e-104">Um eine der auf dem lokalen Computer registrierten NICs auszuwählen, müssen Sie die [**getnppblobfromui**](getnppblobfromui.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8347e-104">To select one of the NICs registered on the local computer, call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span> <span data-ttu-id="8347e-105">Diese Funktion verwendet die Netzwerkmonitor-Benutzeroberfläche, um die registrierten NICs anzuzeigen, und gibt das NPP-BLOB zurück, das die ausgewählte NIC darstellt.</span><span class="sxs-lookup"><span data-stu-id="8347e-105">This function uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you select.</span></span> <span data-ttu-id="8347e-106">Sie können alle auf dem lokalen Computer registrierten NICs oder einen kleineren Satz gefilterter NICs anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8347e-106">You can display all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="8347e-107">Wenn Sie die angezeigten NICs filtern möchten, geben Sie einen [*filterblob*](f.md) an, wenn der-Befehl aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8347e-107">To filter the displayed NICs, provide a [*filter BLOB*](f.md) when the call is made.</span></span>

> [!Note]  
> <span data-ttu-id="8347e-108">Wenn die [**getnppblobfromui**](getnppblobfromui.md) -Funktion aufgerufen wird, kommuniziert der [*NPP-Finder*](n.md) mit den NPP-DLLs, um die NPP-BLOB-Strukturen abzurufen, die die registrierten NICs darstellen.</span><span class="sxs-lookup"><span data-stu-id="8347e-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the [*NPP Finder*](n.md) communicates with the NPP DLLs to obtain the NPP BLOB structures that represent the registered NICs.</span></span> <span data-ttu-id="8347e-109">Weitere Informationen und eine Vorgehensweise zur direkten Verwendung der Netzwerkmonitor-Benutzeroberfläche finden Sie im Thema "Auswählen eines Netzwerks" in der Netzwerkmonitor-Online Hilfe.</span><span class="sxs-lookup"><span data-stu-id="8347e-109">For more information, and a procedure about how to use the Network Monitor UI directly, see the "Select a Network Dialog Box" topic in the Network Monitor online help.</span></span>

 

<span data-ttu-id="8347e-110">Wenn Sie die [**getnppblobfromui**](getnppblobfromui.md) -Funktion aufrufen, wird das Dialogfeld **Netzwerk auswählen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8347e-110">When you call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function, the **Select a network** dialog box appears.</span></span> <span data-ttu-id="8347e-111">Darin können Sie die Details der NPPs anzeigen, die auf dem lokalen Computer registriert sind.</span><span class="sxs-lookup"><span data-stu-id="8347e-111">From it, you can view the details of the NPPs registered on the local computer.</span></span> <span data-ttu-id="8347e-112">Diese Informationen umfassen sowohl lokale NPPs als auch Remote-NPPs.</span><span class="sxs-lookup"><span data-stu-id="8347e-112">This information includes both local NPPs and remote NPPs.</span></span> <span data-ttu-id="8347e-113">Im Dialogfeld können Sie eine bestimmte NIC auswählen und die Details der zugehörigen NPP-BLOB-Struktur anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8347e-113">From the dialog box, you can select a specific NIC and view the details of its associated NPP BLOB structure.</span></span>

<span data-ttu-id="8347e-114">In der folgenden Abbildung werden typische Einstellungen eines NDIS-NPP dargestellt, der von Netzwerkmonitor bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8347e-114">The following illustration shows typical settings of an NDIS NPP supplied by Network Monitor.</span></span>

![typische Einstellungen eines vom Netzwerkmonitor bereitgestellten NDIS-NPP](images/networkdb.png)

<span data-ttu-id="8347e-116">In der folgenden Tabelle sind Themen aufgeführt, in denen jede NIC-Auswahlmethode beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8347e-116">The following table lists topics that describe each NIC selection method.</span></span>



| <span data-ttu-id="8347e-117">Informationen über</span><span class="sxs-lookup"><span data-stu-id="8347e-117">For information about</span></span>                                                                          | <span data-ttu-id="8347e-118">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="8347e-118">See</span></span>                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8347e-119">Gibt an, wie ein Filter angegeben wird, der die im Dialogfeld " **Netzwerk auswählen** " angezeigten NICs einschränkt.</span><span class="sxs-lookup"><span data-stu-id="8347e-119">How to specify a filter that limits the NICs displayed in the **Select a network** dialog box.</span></span> | [<span data-ttu-id="8347e-120">Angeben eines filterblobs</span><span class="sxs-lookup"><span data-stu-id="8347e-120">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="8347e-121">So wählen Sie eine NIC aus, indem Sie die [**getnppblobfromui**](getnppblobfromui.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8347e-121">How to select a NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>      | [<span data-ttu-id="8347e-122">Auswählen einer NIC mithilfe von getnppblobfromui</span><span class="sxs-lookup"><span data-stu-id="8347e-122">Selecting a NIC using GetNPPBlobFromUI</span></span>](getnppblobfromui.md)                                       |
| <span data-ttu-id="8347e-123">Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8347e-123">How to select a NIC from a supplied NPP BLOB table.</span></span>                                            | [<span data-ttu-id="8347e-124">Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle</span><span class="sxs-lookup"><span data-stu-id="8347e-124">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



