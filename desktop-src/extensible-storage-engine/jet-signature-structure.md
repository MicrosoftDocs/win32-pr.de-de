---
description: 'Weitere Informationen finden Sie hier: JET_SIGNATURE Struktur'
title: JET_SIGNATURE Struktur
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: d6210853e22fda5085980c2fb285411ba431bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343343"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="2759b-103">JET_SIGNATURE Struktur</span><span class="sxs-lookup"><span data-stu-id="2759b-103">JET_SIGNATURE Structure</span></span>


<span data-ttu-id="2759b-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2759b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_signature-structure"></a><span data-ttu-id="2759b-105">JET_SIGNATURE Struktur</span><span class="sxs-lookup"><span data-stu-id="2759b-105">JET_SIGNATURE Structure</span></span>

<span data-ttu-id="2759b-106">Die **JET_SIGNATURE** -Struktur enthält Informationen, mit denen eine Datenbank eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2759b-106">The **JET_SIGNATURE** structure contains information that uniquely identifies a database.</span></span>

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a><span data-ttu-id="2759b-107">Member</span><span class="sxs-lookup"><span data-stu-id="2759b-107">Members</span></span>

<span data-ttu-id="2759b-108">**ulrandom**</span><span class="sxs-lookup"><span data-stu-id="2759b-108">**ulRandom**</span></span>

<span data-ttu-id="2759b-109">Eine zufällig zugewiesene Zahl.</span><span class="sxs-lookup"><span data-stu-id="2759b-109">A randomly assigned number.</span></span>

<span data-ttu-id="2759b-110">**logtimecreate**</span><span class="sxs-lookup"><span data-stu-id="2759b-110">**logtimeCreate**</span></span>

<span data-ttu-id="2759b-111">Die [JET_LOGTIME](./jet-logtime-structure.md) zum Zeitpunkt der Ausführung von [jetkreatedatabase](./jetcreatedatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="2759b-111">The [JET_LOGTIME](./jet-logtime-structure.md) at the time of [JetCreateDatabase](./jetcreatedatabase-function.md) is executed.</span></span>

<span data-ttu-id="2759b-112">**szcomputername**</span><span class="sxs-lookup"><span data-stu-id="2759b-112">**szComputerName**</span></span>

<span data-ttu-id="2759b-113">Der optionale Zeichen folgen Wert des NetBIOS-Namens für den Computer.</span><span class="sxs-lookup"><span data-stu-id="2759b-113">The optional string value of the NetBIOS name for the computer.</span></span> <span data-ttu-id="2759b-114">Dieser Wert kann nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2759b-114">This value may not be set.</span></span>

### <a name="remarks"></a><span data-ttu-id="2759b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2759b-115">Remarks</span></span>

<span data-ttu-id="2759b-116">Diese kann als Element von [JET_DBINFOMISC](./jet-dbinfomisc-structure.md)gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="2759b-116">This can be found as an element of [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="2759b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2759b-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2759b-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2759b-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2759b-119">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2759b-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2759b-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2759b-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2759b-121">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2759b-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2759b-122"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2759b-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2759b-123">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="2759b-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2759b-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2759b-124">See Also</span></span>

[<span data-ttu-id="2759b-125">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="2759b-125">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="2759b-126">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="2759b-126">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="2759b-127">Jetkreatedatabase</span><span class="sxs-lookup"><span data-stu-id="2759b-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)
