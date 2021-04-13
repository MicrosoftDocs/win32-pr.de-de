---
description: 'Weitere Informationen finden Sie hier: JET_SNPROG Struktur'
title: JET_SNPROG Struktur
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484267"
---
# <a name="jet_snprog-structure"></a><span data-ttu-id="5afd7-103">JET_SNPROG Struktur</span><span class="sxs-lookup"><span data-stu-id="5afd7-103">JET_SNPROG Structure</span></span>


<span data-ttu-id="5afd7-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5afd7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snprog-structure"></a><span data-ttu-id="5afd7-105">JET_SNPROG Struktur</span><span class="sxs-lookup"><span data-stu-id="5afd7-105">JET_SNPROG Structure</span></span>

<span data-ttu-id="5afd7-106">Die **JET_SNPROG** -Struktur enthält Informationen zum Fortschritt eines Vorgangs mit langer Ausführungszeit.</span><span class="sxs-lookup"><span data-stu-id="5afd7-106">The **JET_SNPROG** structure contains information about the progress of a long-running operation.</span></span> <span data-ttu-id="5afd7-107">Wenn die Rückruffunktion aufgerufen wird, um den Status des Vorgangs zu benachrichtigen, und der Vorgang noch ausgeführt wird, ist der letzte Parameter der Rückruffunktion ein Zeiger auf eine **JET_SNPROG** Struktur.</span><span class="sxs-lookup"><span data-stu-id="5afd7-107">When the callback function is called to notify the status of the operation and the operation is still in progress, the last parameter of the callback function is a pointer to a **JET_SNPROG** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a><span data-ttu-id="5afd7-108">Member</span><span class="sxs-lookup"><span data-stu-id="5afd7-108">Members</span></span>

<span data-ttu-id="5afd7-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="5afd7-109">**cbStruct**</span></span>

<span data-ttu-id="5afd7-110">Die Größe der **JET_SNPROG** Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5afd7-110">The size of the **JET_SNPROG** structure, in bytes.</span></span> <span data-ttu-id="5afd7-111">Dieser Wert bestätigt, dass die folgenden Felder vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5afd7-111">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="5afd7-112">**cunitdone**</span><span class="sxs-lookup"><span data-stu-id="5afd7-112">**cunitDone**</span></span>

<span data-ttu-id="5afd7-113">Die Anzahl der Arbeitseinheiten, die während der Funktion mit langer Laufzeit bereits abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="5afd7-113">The number of work units that are already completed during the long running function.</span></span>

<span data-ttu-id="5afd7-114">**cunittotal**</span><span class="sxs-lookup"><span data-stu-id="5afd7-114">**cunitTotal**</span></span>

<span data-ttu-id="5afd7-115">Die Anzahl der Arbeitseinheiten, die abgeschlossen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5afd7-115">The number of work units that need to be completed.</span></span> <span data-ttu-id="5afd7-116">Dieser Wert sollte immer größer oder gleich **cunitdone** sein.</span><span class="sxs-lookup"><span data-stu-id="5afd7-116">This value should always be bigger than or equal to **cunitDone**.</span></span>

### <a name="requirements"></a><span data-ttu-id="5afd7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5afd7-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5afd7-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5afd7-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5afd7-119">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5afd7-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5afd7-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5afd7-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5afd7-121">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5afd7-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5afd7-122"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5afd7-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5afd7-123">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="5afd7-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

