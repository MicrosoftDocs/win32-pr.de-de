---
description: 'Weitere Informationen finden Sie hier: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106365876"
---
# <a name="jet_grbit"></a><span data-ttu-id="8a1c4-103">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8a1c4-103">JET_GRBIT</span></span>


<span data-ttu-id="8a1c4-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8a1c4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_grbit"></a><span data-ttu-id="8a1c4-105">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8a1c4-105">JET_GRBIT</span></span>

<span data-ttu-id="8a1c4-106">Der **JET_GRBIT** -Datentyp ist eine Gruppe von Bits, die Konstanten enthalten, die für die Funktionen und Strukturen spezifisch sind, in denen Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8a1c4-106">The **JET_GRBIT** data type is a group of bits that contain constants that are specific to the functions and structures in which it is used.</span></span>

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a><span data-ttu-id="8a1c4-107">Datentypen</span><span class="sxs-lookup"><span data-stu-id="8a1c4-107">Data Types</span></span>

<span data-ttu-id="8a1c4-108">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8a1c4-108">JET_GRBIT</span></span>

<span data-ttu-id="8a1c4-109">Im allgemeinen reflektieren die Konstanten, die als Werte für diesen Datentyp verwendet werden, den Namen des API-Elements, in dem Sie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a1c4-109">In general, the constants that are used as values for this data type reflect the name of the API element in which they are used.</span></span> <span data-ttu-id="8a1c4-110">Beispielsweise beginnen alle Konstanten, die an [jetretrievecolnumn](./jetretrievecolumn-function.md) übergebenen werden, mit "JET_bitRetrieve".</span><span class="sxs-lookup"><span data-stu-id="8a1c4-110">For example, all constants passed to [JetRetrieveColumn](./jetretrievecolumn-function.md) begin with "JET_bitRetrieve".</span></span> <span data-ttu-id="8a1c4-111">Ebenso beginnen alle an [jetsetcolumn](./jetsetcolumn-function.md) übergebenen Konstanten mit "JET_bitSet".</span><span class="sxs-lookup"><span data-stu-id="8a1c4-111">Similarly, all constants passed to [JetSetColumn](./jetsetcolumn-function.md) begin with "JET_bitSet".</span></span>

<span data-ttu-id="8a1c4-112">Der Wert 0 (null) bewirkt, dass der-Parameter ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="8a1c4-112">A value of zero causes the parameter to be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="8a1c4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a1c4-113">Remarks</span></span>

<span data-ttu-id="8a1c4-114">Weitere Informationen finden Sie unter der jeweiligen Funktion oder Struktur.</span><span class="sxs-lookup"><span data-stu-id="8a1c4-114">For more information, see the specific function or structure.</span></span> <span data-ttu-id="8a1c4-115">Die Optionen werden in der Regel als ein Satz von Flags, die kombiniert werden können, übermittelt.</span><span class="sxs-lookup"><span data-stu-id="8a1c4-115">The options are usually passed as a set of flags that can be combined.</span></span>

### <a name="requirements"></a><span data-ttu-id="8a1c4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a1c4-116">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a1c4-117"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8a1c4-117"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8a1c4-118">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8a1c4-118">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a1c4-119"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8a1c4-119"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8a1c4-120">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8a1c4-120">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a1c4-121"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8a1c4-121"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8a1c4-122">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="8a1c4-122">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8a1c4-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8a1c4-123">See Also</span></span>

[<span data-ttu-id="8a1c4-124">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="8a1c4-124">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="8a1c4-125">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="8a1c4-125">JetSetColumn</span></span>](./jetsetcolumn-function.md)
