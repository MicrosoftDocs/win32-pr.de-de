---
description: 'Weitere Informationen finden Sie hier: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d1d4fa75c8a41528e9868bc94fa638042d01cff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214389"
---
# <a name="jet_snt"></a><span data-ttu-id="fa765-103">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="fa765-103">JET_SNT</span></span>


<span data-ttu-id="fa765-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fa765-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snt"></a><span data-ttu-id="fa765-105">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="fa765-105">JET_SNT</span></span>

<span data-ttu-id="fa765-106">Die [JET_SNT]() Gruppe von Konstanten beschreibt die Punkte des Status eines Vorgangs, über die Informationen angefordert werden, die in einem Rückruf der [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) Rückruffunktion angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="fa765-106">The [JET_SNT]() group of constants describe the points of the progress of an operation about which information is requested in a call to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa765-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="fa765-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="fa765-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa765-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa765-109">JET_sntBegin</span><span class="sxs-lookup"><span data-stu-id="fa765-109">JET_sntBegin</span></span><br />
<span data-ttu-id="fa765-110">5</span><span class="sxs-lookup"><span data-stu-id="fa765-110">5</span></span></p></td>
<td><p><span data-ttu-id="fa765-111">Der Anfang eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fa765-111">The beginning of an operation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa765-112">JET_sntRequirements</span><span class="sxs-lookup"><span data-stu-id="fa765-112">JET_sntRequirements</span></span><br />
<span data-ttu-id="fa765-113">7</span><span class="sxs-lookup"><span data-stu-id="fa765-113">7</span></span></p></td>
<td><p><span data-ttu-id="fa765-114">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fa765-114">Not supported.</span></span></p>
<p><span data-ttu-id="fa765-115"><strong>Windows 2000-Server:</strong>  Der Vorgang wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="fa765-115"><strong>Windows 2000 Server:</strong>  The operation is started.</span></span> <span data-ttu-id="fa765-116">In diesem Fall sollte der letzte Parameter der Rückruffunktion ein gültiger Zeiger auf eine <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> Struktur sein, die die Gesamtzahl der auszuführenden Einheiten angibt.</span><span class="sxs-lookup"><span data-stu-id="fa765-116">In this case, the last parameter of the callback function should be a valid pointer to a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure indicating the total number of units to be executed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa765-117">JET_sntProgress</span><span class="sxs-lookup"><span data-stu-id="fa765-117">JET_sntProgress</span></span><br />
<span data-ttu-id="fa765-118">0</span><span class="sxs-lookup"><span data-stu-id="fa765-118">0</span></span></p></td>
<td><p><span data-ttu-id="fa765-119">Die Anzahl der abgeschlossenen Einheiten und die Anzahl der Einheiten, die noch ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fa765-119">The number of units completed and number of units yet to be done.</span></span> <span data-ttu-id="fa765-120">Diese Informationen werden in den Elementen einer <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fa765-120">This information is returned in the members of a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa765-121">JET_sntComplete</span><span class="sxs-lookup"><span data-stu-id="fa765-121">JET_sntComplete</span></span><br />
<span data-ttu-id="fa765-122">6</span><span class="sxs-lookup"><span data-stu-id="fa765-122">6</span></span></p></td>
<td><p><span data-ttu-id="fa765-123">Der Abschluss eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fa765-123">The completion of an operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa765-124">JET_sntFail</span><span class="sxs-lookup"><span data-stu-id="fa765-124">JET_sntFail</span></span><br />
<span data-ttu-id="fa765-125">3</span><span class="sxs-lookup"><span data-stu-id="fa765-125">3</span></span></p></td>
<td><p><span data-ttu-id="fa765-126">Der Fehler eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fa765-126">The failure of an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa765-127">JET_sntRecoveryStep</span><span class="sxs-lookup"><span data-stu-id="fa765-127">JET_sntRecoveryStep</span></span><br />
<span data-ttu-id="fa765-128">8</span><span class="sxs-lookup"><span data-stu-id="fa765-128">8</span></span></p></td>
<td><p><span data-ttu-id="fa765-129">Die Wiederherstellungs Steuerung eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fa765-129">The recovery control of an operation.</span></span></p>
<div class="alert">

> [!NOTE]
> <P><span data-ttu-id="fa765-130">Dieser Wert gilt nicht für Versionen des Windows-Betriebssystems, beginnend mit Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fa765-130">This value is not applicable to versions of the Windows operating system starting with Windows 8.</span></span></P>


</div></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="fa765-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa765-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa765-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fa765-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fa765-133">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fa765-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa765-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fa765-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fa765-135">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fa765-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa765-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fa765-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fa765-137">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="fa765-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="fa765-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fa765-138">See Also</span></span>

[<span data-ttu-id="fa765-139">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="fa765-139">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="fa765-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="fa765-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="fa765-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="fa765-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)
