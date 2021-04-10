---
description: 'Weitere Informationen finden Sie hier: JET_LGPOS Struktur'
title: JET_LGPOS Struktur
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: 25f00c73a4bb922a8152335babe222b539c70ade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042665"
---
# <a name="jet_lgpos-structure"></a><span data-ttu-id="00eaf-103">JET_LGPOS Struktur</span><span class="sxs-lookup"><span data-stu-id="00eaf-103">JET_LGPOS Structure</span></span>


<span data-ttu-id="00eaf-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="00eaf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_lgpos-structure"></a><span data-ttu-id="00eaf-105">JET_LGPOS Struktur</span><span class="sxs-lookup"><span data-stu-id="00eaf-105">JET_LGPOS Structure</span></span>

<span data-ttu-id="00eaf-106">Die **JET_LGPOS** -Struktur enthält Daten, die für den Protokollierungs Mechanismus der Datenbank-Engine intern sind.</span><span class="sxs-lookup"><span data-stu-id="00eaf-106">The **JET_LGPOS** structure holds data that is internal to the logging mechanism of the database engine.</span></span> <span data-ttu-id="00eaf-107">Diese Struktur wird als intern betrachtet.</span><span class="sxs-lookup"><span data-stu-id="00eaf-107">This structure is considered internal.</span></span>

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a><span data-ttu-id="00eaf-108">Member</span><span class="sxs-lookup"><span data-stu-id="00eaf-108">Members</span></span>

<span data-ttu-id="00eaf-109">**besiegt**</span><span class="sxs-lookup"><span data-stu-id="00eaf-109">**ib**</span></span>

<span data-ttu-id="00eaf-110">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00eaf-110">Supports the ESE infrastructure and cannot be used from your code.</span></span>

<span data-ttu-id="00eaf-111">**ISEC**</span><span class="sxs-lookup"><span data-stu-id="00eaf-111">**isec**</span></span>

<span data-ttu-id="00eaf-112">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00eaf-112">Supports the ESE infrastructure and cannot be used from your code.</span></span>

<span data-ttu-id="00eaf-113">**lGeneration**</span><span class="sxs-lookup"><span data-stu-id="00eaf-113">**lGeneration**</span></span>

<span data-ttu-id="00eaf-114">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00eaf-114">Supports the ESE infrastructure and cannot be used from your code.</span></span>

### <a name="requirements"></a><span data-ttu-id="00eaf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00eaf-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00eaf-116"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="00eaf-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="00eaf-117">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="00eaf-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00eaf-118"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="00eaf-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="00eaf-119">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="00eaf-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00eaf-120"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="00eaf-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="00eaf-121">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="00eaf-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="00eaf-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="00eaf-122">See Also</span></span>

[<span data-ttu-id="00eaf-123">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="00eaf-123">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="00eaf-124">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="00eaf-124">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
