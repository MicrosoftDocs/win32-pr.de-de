---
description: 'Weitere Informationen finden Sie hier: JET_CONVERT Struktur'
title: JET_CONVERT Struktur
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863184"
---
# <a name="jet_convert-structure"></a><span data-ttu-id="98de7-103">JET_CONVERT Struktur</span><span class="sxs-lookup"><span data-stu-id="98de7-103">JET_CONVERT Structure</span></span>


<span data-ttu-id="98de7-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="98de7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_convert-structure"></a><span data-ttu-id="98de7-105">JET_CONVERT Struktur</span><span class="sxs-lookup"><span data-stu-id="98de7-105">JET_CONVERT Structure</span></span>

<span data-ttu-id="98de7-106">Die **JET_CONVERT** Struktur enthält den Namen einer früheren ESE-Version-dll, die zum Lesen von Datenbanken verwendet wird, die mit dieser früheren Version erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="98de7-106">The **JET_CONVERT** structure contains the name of an earlier ESE version DLL that is used for reading a databases that are created with that earlier version.</span></span> <span data-ttu-id="98de7-107">Außerdem werden andere Flags bereitgestellt, um die Art der Konvertierung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="98de7-107">In addition, other flags are provided to control the nature of the conversion.</span></span>

<span data-ttu-id="98de7-108">**Windows Server 2003:** Die Funktion in [jetcompact](./jetcompact-function.md) , die eine Konvertierung durchgeführt hat, wurde aus dem Produkt in Windows Server 2003 entfernt.</span><span class="sxs-lookup"><span data-stu-id="98de7-108">**Windows Server 2003:** The feature in [JetCompact](./jetcompact-function.md) that performed a conversion was removed from the product in Windows Server 2003.</span></span> <span data-ttu-id="98de7-109">Sie wird nur in Windows 2000 und Windows XP unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98de7-109">It is only supported in Windows 2000 and Windows XP.</span></span>

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a><span data-ttu-id="98de7-110">Member</span><span class="sxs-lookup"><span data-stu-id="98de7-110">Members</span></span>

<span data-ttu-id="98de7-111">**Szolddll**</span><span class="sxs-lookup"><span data-stu-id="98de7-111">**SzOldDll**</span></span>

<span data-ttu-id="98de7-112">Der Name, einschließlich der Pfadinformationen, zur früheren Version der ESE-dll.</span><span class="sxs-lookup"><span data-stu-id="98de7-112">The name, including path information, to the earlier version of the ESE DLL.</span></span>

<span data-ttu-id="98de7-113">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="98de7-113">**fFlags**</span></span>

<span data-ttu-id="98de7-114">Ist für das System reserviert.</span><span class="sxs-lookup"><span data-stu-id="98de7-114">Reserved for system use.</span></span>

<span data-ttu-id="98de7-115">**nicht ordnungsgemäß**</span><span class="sxs-lookup"><span data-stu-id="98de7-115">**fSchemaChangesOnly**</span></span>

<span data-ttu-id="98de7-116">Ist für das System reserviert.</span><span class="sxs-lookup"><span data-stu-id="98de7-116">Reserved for system use.</span></span>

### <a name="requirements"></a><span data-ttu-id="98de7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98de7-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98de7-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="98de7-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="98de7-119">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="98de7-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98de7-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="98de7-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="98de7-121">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="98de7-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98de7-122"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="98de7-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="98de7-123">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="98de7-123">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98de7-124"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="98de7-124"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="98de7-125">Wird als <strong>JET_CONVERT_W</strong> (Unicode) und <strong>JET_CONVERT_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="98de7-125">Implemented as <strong>JET_CONVERT_W</strong> (Unicode) and <strong>JET_CONVERT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="98de7-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="98de7-126">See Also</span></span>

[<span data-ttu-id="98de7-127">Jetcompact</span><span class="sxs-lookup"><span data-stu-id="98de7-127">JetCompact</span></span>](./jetcompact-function.md)
