---
description: 'Weitere Informationen finden Sie hier: JET_API_PTR'
title: JET_API_PTR
TOCTitle: JET_API_PTR
ms:assetid: 27b1eeec-1707-4edb-a4b2-2619190c21e7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269209(v=EXCHG.10)
ms:contentKeyID: 32765512
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
ms.openlocfilehash: 687f28fcba3d20c5b72a3089d3a442dd97e2dfb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350089"
---
# <a name="jet_api_ptr"></a><span data-ttu-id="5e0d4-103">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="5e0d4-103">JET_API_PTR</span></span>


<span data-ttu-id="5e0d4-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5e0d4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_api_ptr"></a><span data-ttu-id="5e0d4-105">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="5e0d4-105">JET_API_PTR</span></span>

<span data-ttu-id="5e0d4-106">Der **JET_API_PTR** -Datentyp enthält eine Ganzzahl oder einen Zeiger Wert.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-106">The **JET_API_PTR** data type holds an integer or a pointer value.</span></span>

```cpp
    #if defined(_WIN64)
        typedef unsigned __int64 JET_API_PTR;
    #elif !defined(__midl) && (defined(_X86_) || defined(_M_IX86)) && _MSC_VER >= 1300
        typedef __w64 unsigned long JET_API_PTR;
    #else
        typedef unsigned long JET_API_PTR;
    #endif
```

### <a name="data-types"></a><span data-ttu-id="5e0d4-107">Datentypen</span><span class="sxs-lookup"><span data-stu-id="5e0d4-107">Data Types</span></span>

<span data-ttu-id="5e0d4-108">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="5e0d4-108">JET_API_PTR</span></span>

<span data-ttu-id="5e0d4-109">Wie bei einem **DWORD_PTR** -Datentyp wird der **JET_API_PTR** -Datentyp auf einem 32-Bit-Computer als 4 Bytes und auf einem 64-Bit-Computer auf 8 Bytes festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-109">Like a **DWORD_PTR** data type, the **JET_API_PTR** data type is defined as 4 bytes on a 32-bit machine and 8 bytes on a 64-bit machine.</span></span>

### <a name="remarks"></a><span data-ttu-id="5e0d4-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e0d4-110">Remarks</span></span>

<span data-ttu-id="5e0d4-111">Der **JET_API_PTR** -Datentyp wird verwendet, um die folgenden Datentypen zu definieren:</span><span class="sxs-lookup"><span data-stu-id="5e0d4-111">The **JET_API_PTR** data type is used to define the following data types:</span></span>

  - [<span data-ttu-id="5e0d4-112">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="5e0d4-112">JET_HANDLE</span></span>](./jet-handle.md)

  - [<span data-ttu-id="5e0d4-113">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="5e0d4-113">JET_INSTANCE</span></span>](./jet-instance.md)

  - [<span data-ttu-id="5e0d4-114">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5e0d4-114">JET_SESID</span></span>](./jet-sesid.md)

  - [<span data-ttu-id="5e0d4-115">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5e0d4-115">JET_TABLEID</span></span>](./jet-tableid.md)

  - [<span data-ttu-id="5e0d4-116">JET_LS</span><span class="sxs-lookup"><span data-stu-id="5e0d4-116">JET_LS</span></span>](./jet-ls.md)

### <a name="requirements"></a><span data-ttu-id="5e0d4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e0d4-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e0d4-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5e0d4-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5e0d4-119">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e0d4-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5e0d4-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5e0d4-121">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e0d4-122"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5e0d4-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5e0d4-123">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>
