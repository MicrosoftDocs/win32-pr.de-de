---
description: 'Weitere Informationen finden Sie hier: WCHAR'
title: WCHAR
TOCTitle: WCHAR
ms:assetid: 922431b3-bf9a-4aba-bc67-dd33d9aeaac0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269344(v=EXCHG.10)
ms:contentKeyID: 32765633
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
ms.openlocfilehash: 1dfa86cbc771059d941027385090dcbd2f401855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345095"
---
# <a name="wchar"></a><span data-ttu-id="445f2-103">WCHAR</span><span class="sxs-lookup"><span data-stu-id="445f2-103">WCHAR</span></span>


<span data-ttu-id="445f2-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="445f2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="wchar"></a><span data-ttu-id="445f2-105">WCHAR</span><span class="sxs-lookup"><span data-stu-id="445f2-105">WCHAR</span></span>

<span data-ttu-id="445f2-106">Der WCHAR-Datentyp enthält ein 16-Bit-Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="445f2-106">The WCHAR data type contains a 16-bit Unicode character.</span></span>

```cpp
    #if !defined(_NATIVE_WCHAR_T_DEFINED)
    typedef unsigned short WCHAR;
    #else
    typedef wchar_t WCHAR;
    #endif
```

### <a name="data-types"></a><span data-ttu-id="445f2-107">Datentypen</span><span class="sxs-lookup"><span data-stu-id="445f2-107">Data Types</span></span>

<span data-ttu-id="445f2-108">WCHAR</span><span class="sxs-lookup"><span data-stu-id="445f2-108">WCHAR</span></span>

<span data-ttu-id="445f2-109">Ein 16-Bit-Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="445f2-109">A 16-bit Unicode character.</span></span>

### <a name="requirements"></a><span data-ttu-id="445f2-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="445f2-110">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="445f2-111"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="445f2-111"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="445f2-112">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="445f2-112">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="445f2-113"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="445f2-113"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="445f2-114">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="445f2-114">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="445f2-115"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="445f2-115"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="445f2-116">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="445f2-116">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

