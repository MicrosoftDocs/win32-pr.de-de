---
description: 'Weitere Informationen finden Sie hier: JET_RSTINFO Struktur'
title: JET_RSTINFO Struktur
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128665"
---
# <a name="jet_rstinfo-structure"></a><span data-ttu-id="957ac-103">JET_RSTINFO Struktur</span><span class="sxs-lookup"><span data-stu-id="957ac-103">JET_RSTINFO Structure</span></span>


<span data-ttu-id="957ac-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="957ac-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstinfo-structure"></a><span data-ttu-id="957ac-105">JET_RSTINFO Struktur</span><span class="sxs-lookup"><span data-stu-id="957ac-105">JET_RSTINFO Structure</span></span>

<span data-ttu-id="957ac-106">Die **JET_RSTINFO** Struktur enthält Steuerungsinformationen für den Wiederherstellungsprozess, z. b. Informationen zur Daten Bank Verlagerung und Möglichkeit, die Wiederherstellung zu steuern</span><span class="sxs-lookup"><span data-stu-id="957ac-106">The **JET_RSTINFO** structure contains control information for the recovery process like database relocation information and ability to control stopping recovery.</span></span>

<span data-ttu-id="957ac-107">**Windows Vista:** Die **JET_RSTINFO** Struktur wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="957ac-107">**Windows Vista:** The **JET_RSTINFO** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a><span data-ttu-id="957ac-108">Member</span><span class="sxs-lookup"><span data-stu-id="957ac-108">Members</span></span>

<span data-ttu-id="957ac-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="957ac-109">**cbStruct**</span></span>

<span data-ttu-id="957ac-110">Die Größe der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="957ac-110">The size of the structure.</span></span>

<span data-ttu-id="957ac-111">**rgrstmap**</span><span class="sxs-lookup"><span data-stu-id="957ac-111">**rgrstmap**</span></span>

<span data-ttu-id="957ac-112">Die-Struktur, die den alten und den neuen Pfad einer wiederhergestellten Datenbank beschreibt.</span><span class="sxs-lookup"><span data-stu-id="957ac-112">The structure that describes the old and new path of a restored database.</span></span>

<span data-ttu-id="957ac-113">**crstmap**</span><span class="sxs-lookup"><span data-stu-id="957ac-113">**crstmap**</span></span>

<span data-ttu-id="957ac-114">Anzahl der Array Einträge in der rgrstmap.</span><span class="sxs-lookup"><span data-stu-id="957ac-114">Count of array entries in the rgrstmap.</span></span>

<span data-ttu-id="957ac-115">**lgposstopps**</span><span class="sxs-lookup"><span data-stu-id="957ac-115">**lgposStop**</span></span>

<span data-ttu-id="957ac-116">Die Protokoll Position, an der die Wiederherstellung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="957ac-116">The log position to stop recovery at.</span></span> <span data-ttu-id="957ac-117">Es wird keine rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="957ac-117">No undo will be done.</span></span>

<span data-ttu-id="957ac-118">**logtimestoppt**</span><span class="sxs-lookup"><span data-stu-id="957ac-118">**logtimeStop**</span></span>

<span data-ttu-id="957ac-119">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="957ac-119">Reserved for future use.</span></span>

<span data-ttu-id="957ac-120">**pfnstatus**</span><span class="sxs-lookup"><span data-stu-id="957ac-120">**pfnStatus**</span></span>

<span data-ttu-id="957ac-121">Eine Status Funktion zum Melden des Status der Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="957ac-121">A status function for reporting status of recovery.</span></span>

### <a name="requirements"></a><span data-ttu-id="957ac-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="957ac-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="957ac-123"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="957ac-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="957ac-124">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="957ac-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="957ac-125"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="957ac-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="957ac-126">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="957ac-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="957ac-127"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="957ac-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="957ac-128">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="957ac-128">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="957ac-129"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="957ac-129"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="957ac-130">Wird als <strong>JET_RSTINFO_W</strong> (Unicode) und <strong>JET_RSTINFO_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="957ac-130">Implemented as <strong>JET_RSTINFO_W</strong> (Unicode) and <strong>JET_RSTINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="957ac-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="957ac-131">See Also</span></span>

[<span data-ttu-id="957ac-132">JetInit3</span><span class="sxs-lookup"><span data-stu-id="957ac-132">JetInit3</span></span>](./jetinit3-function.md)
