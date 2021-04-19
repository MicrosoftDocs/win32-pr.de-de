---
description: 'Weitere Informationen finden Sie hier: JET_PWSTR'
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
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
ms.openlocfilehash: 536ef3bba465f6d152e3483436c1dc1e82277339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362378"
---
# <a name="jet_pwstr"></a><span data-ttu-id="cb0b6-103">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="cb0b6-103">JET_PWSTR</span></span>


<span data-ttu-id="cb0b6-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cb0b6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pwstr"></a><span data-ttu-id="cb0b6-105">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="cb0b6-105">JET_PWSTR</span></span>

<span data-ttu-id="cb0b6-106">Der **JET_PWSTR** -Datentyp enthält eine NULL-terminierte **Unicode** -Zeichenfolge (Char \* ).</span><span class="sxs-lookup"><span data-stu-id="cb0b6-106">The **JET_PWSTR** data type contains a null-terminated **Unicode** string (char \*).</span></span>

<span data-ttu-id="cb0b6-107">**Windows Vista: JET_PWSTR** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cb0b6-107">**Windows Vista:  JET_PWSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a><span data-ttu-id="cb0b6-108">Datentypen</span><span class="sxs-lookup"><span data-stu-id="cb0b6-108">Data Types</span></span>

<span data-ttu-id="cb0b6-109">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="cb0b6-109">JET_PWSTR</span></span>

<span data-ttu-id="cb0b6-110">NULL-terminierte Unicode-Zeichenfolge (Char \* ).</span><span class="sxs-lookup"><span data-stu-id="cb0b6-110">Null-terminated, Unicode string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="cb0b6-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb0b6-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb0b6-112"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cb0b6-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cb0b6-113">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb0b6-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb0b6-114"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cb0b6-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cb0b6-115">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cb0b6-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb0b6-116"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cb0b6-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cb0b6-117">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="cb0b6-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

