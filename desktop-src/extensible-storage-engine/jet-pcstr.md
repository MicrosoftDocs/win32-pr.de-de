---
description: 'Weitere Informationen finden Sie hier: JET_PCSTR'
title: JET_PCSTR
TOCTitle: JET_PCSTR
ms:assetid: 5826e6b9-5297-421f-abaa-016708bf16f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269254(v=EXCHG.10)
ms:contentKeyID: 32765556
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
ms.openlocfilehash: 2786435822fefb56b09c3bb434612dc1fbf13f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218597"
---
# <a name="jet_pcstr"></a><span data-ttu-id="42884-103">JET_PCSTR</span><span class="sxs-lookup"><span data-stu-id="42884-103">JET_PCSTR</span></span>


<span data-ttu-id="42884-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="42884-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pcstr"></a><span data-ttu-id="42884-105">JET_PCSTR</span><span class="sxs-lookup"><span data-stu-id="42884-105">JET_PCSTR</span></span>

<span data-ttu-id="42884-106">Der **JET_PCSTR** -Datentyp enthält eine NULL-terminierte, Konstante **ASCII** -Zeichenfolge (Char \* ).</span><span class="sxs-lookup"><span data-stu-id="42884-106">The **JET_PCSTR** data type contains a null-terminated, constant **ASCII** string (char \*).</span></span>

<span data-ttu-id="42884-107">**Windows Vista: JET_PCSTR** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="42884-107">**Windows Vista:  JET_PCSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated const char *  JET_PCSTR;
```

### <a name="data-types"></a><span data-ttu-id="42884-108">Datentypen</span><span class="sxs-lookup"><span data-stu-id="42884-108">Data Types</span></span>

<span data-ttu-id="42884-109">JET_PCSTR</span><span class="sxs-lookup"><span data-stu-id="42884-109">JET_PCSTR</span></span>

<span data-ttu-id="42884-110">NULL-terminierte, Konstante ASCII-Zeichenfolge (Char \* ).</span><span class="sxs-lookup"><span data-stu-id="42884-110">Null-terminated, constant ASCII string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="42884-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42884-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42884-112"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="42884-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="42884-113">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="42884-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42884-114"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="42884-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="42884-115">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="42884-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42884-116"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="42884-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="42884-117">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="42884-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

