---
description: Weitere Informationen finden Sie unter Sequenzierung in mehrwertigen Spalten.
title: Sequenzierung in mehrwertigen Spalten
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563625"
---
# <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="e0f8f-103">Sequenzierung in mehrwertigen Spalten</span><span class="sxs-lookup"><span data-stu-id="e0f8f-103">Sequencing in Multi-Valued Columns</span></span>


<span data-ttu-id="e0f8f-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e0f8f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="e0f8f-105">Sequenzierung in mehrwertigen Spalten</span><span class="sxs-lookup"><span data-stu-id="e0f8f-105">Sequencing in Multi-Valued Columns</span></span>

<span data-ttu-id="e0f8f-106">Die Werte in einer mehrwertigen Spalte werden durch eine Indexnummer identifiziert, die als *itagsequence* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="e0f8f-106">The values in a multi-valued column are identified by an index number called the *itagSequence*.</span></span> <span data-ttu-id="e0f8f-107">Diese Zahl ist ein Verweis auf einen einzelnen Wert der Spalte.</span><span class="sxs-lookup"><span data-stu-id="e0f8f-107">This number is a reference to a single value of the column.</span></span> <span data-ttu-id="e0f8f-108">Diese Zahl wird verwendet, wenn neue Werte in der Spalte festgelegt, abgerufen oder aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="e0f8f-108">This number is used when new values are set, retrieved, or enumerated in the column.</span></span> <span data-ttu-id="e0f8f-109">Die *itagsequence* wird in verschiedenen Strukturen verwendet, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="e0f8f-109">The *itagSequence* is used in various structures, including:</span></span>

  - [<span data-ttu-id="e0f8f-110">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="e0f8f-110">JET_RETINFO</span></span>](./jet-retinfo-structure.md)

  - [<span data-ttu-id="e0f8f-111">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="e0f8f-111">JET_SETINFO</span></span>](./jet-setinfo-structure.md)

  - [<span data-ttu-id="e0f8f-112">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="e0f8f-112">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)

  - [<span data-ttu-id="e0f8f-113">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="e0f8f-113">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)

  - [<span data-ttu-id="e0f8f-114">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="e0f8f-114">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)

<span data-ttu-id="e0f8f-115">Diese *itagsequence* beginnt bei 1 für jeden Wert in der mehrwertigen Spalte.</span><span class="sxs-lookup"><span data-stu-id="e0f8f-115">This *itagSequence* starts at 1 for every value in the multi-valued column.</span></span> <span data-ttu-id="e0f8f-116">Die Sequenznummer wird erhöht, wenn der Spalte neue Werte hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e0f8f-116">The sequence number is increased when new values are added to the column.</span></span> <span data-ttu-id="e0f8f-117">Wenn Sie einen Wert in einer Spalte mit einer *itagsequence* von 0 festlegen, wird angegeben, dass der Wert an den bereits in dieser Spalte bereits in dieser Spalte bereits angefügten Satz von Werten angefügt werden</span><span class="sxs-lookup"><span data-stu-id="e0f8f-117">Setting a value in a column with an *itagSequence* of 0 indicates that the value is to be appended to the set of values already in that column.</span></span> <span data-ttu-id="e0f8f-118">Die Verwendung einer *itagsequence* -Zahl, die größer als die Anzahl der derzeit für eine Spalte festgelegten Werte ist, hat dieselbe Wirkung.</span><span class="sxs-lookup"><span data-stu-id="e0f8f-118">Using an *itagSequence* greater than the number of values currently set for a column will have the same effect.</span></span> <span data-ttu-id="e0f8f-119">Wenn Sie die *itagsequence* eines vorhandenen Werts angeben, wird dieser Wert überschrieben, und es wird kein neuer Wert eingefügt.</span><span class="sxs-lookup"><span data-stu-id="e0f8f-119">Specifying the *itagSequence* of an existing value will overwrite that value, not insert a new one.</span></span> <span data-ttu-id="e0f8f-120">Wenn Sie einen vorhandenen Wert auf NULL festlegen, wird dieser Wert aus dem bereits in dieser Spalte vorhandenen Satz von Werten entfernt.</span><span class="sxs-lookup"><span data-stu-id="e0f8f-120">Setting an existing value to NULL will remove that value from the set of values already in that column.</span></span> <span data-ttu-id="e0f8f-121">Dadurch werden alle nachfolgenden Werte in der Spalte um einen Slot nach unten verschoben, sodass der nachfolgende Zugriff auf diese Werte von *itagsequence* durch eine Zahl kleiner als die zuvor verwendete ist.</span><span class="sxs-lookup"><span data-stu-id="e0f8f-121">This will move all the subsequent values in the column down by one slot such that subsequent access to those values by *itagSequence* will be by a number one less than what was previously used.</span></span>

<span data-ttu-id="e0f8f-122">Das folgende Diagramm zeigt eine *itagsequence* in einer mehrwertigen Spalte.</span><span class="sxs-lookup"><span data-stu-id="e0f8f-122">The following diagram shows an *itagSequence* in a multi-valued column.</span></span> <span data-ttu-id="e0f8f-123">Die Spalte mit dem Namen "Cola" hat drei Einträge: Wert1, Wert2 und Val3 mit *itagsequence* von 1, 2 und 3.</span><span class="sxs-lookup"><span data-stu-id="e0f8f-123">The column named ColA has three entries: Val1, Val2 and Val3 with *itagSequence* of 1, 2, and 3 respectively.</span></span>

<span data-ttu-id="e0f8f-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="e0f8f-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
