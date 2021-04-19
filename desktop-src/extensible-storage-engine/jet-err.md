---
description: 'Weitere Informationen finden Sie hier: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
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
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106363193"
---
# <a name="jet_err"></a><span data-ttu-id="40cf7-103">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="40cf7-103">JET_ERR</span></span>


<span data-ttu-id="40cf7-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="40cf7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_err"></a><span data-ttu-id="40cf7-105">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="40cf7-105">JET_ERR</span></span>

<span data-ttu-id="40cf7-106">Der **JET_ERR** -Datentyp enthält einen [Fehlercode für die erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="40cf7-106">The **JET_ERR** data type contains an [Extensible Storage Engine error code](./extensible-storage-engine-error-codes.md).</span></span>

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a><span data-ttu-id="40cf7-107">Datentypen</span><span class="sxs-lookup"><span data-stu-id="40cf7-107">Data Types</span></span>

<span data-ttu-id="40cf7-108">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="40cf7-108">JET_ERR</span></span>

<span data-ttu-id="40cf7-109">Ein NULL-Wert (entspricht JET_errSuccess) gibt an, dass der-Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="40cf7-109">A zero value (corresponding to JET_errSuccess) indicates that the call succeeded.</span></span> <span data-ttu-id="40cf7-110">Ein positiver Wert warnt vor einer nicht schwerwiegenden Bedingung, die während eines anderweitig erfolgreichen Aufrufes aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="40cf7-110">A positive value warns of a non-fatal condition that occurred during an otherwise successful call.</span></span> <span data-ttu-id="40cf7-111">Ein negativer Wert gibt an, dass der-Befehl fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="40cf7-111">A negative value indicates that the call failed.</span></span>

### <a name="remarks"></a><span data-ttu-id="40cf7-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40cf7-112">Remarks</span></span>

<span data-ttu-id="40cf7-113">Informationen zum Zurückgeben von Fehlern als HRESULTs finden Sie unter [Fehler des Extensible Storage Engine](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="40cf7-113">For information about returning errors as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="40cf7-114">Informationen zu Flags zum Konfigurieren der Datenbank für die Fehlerbehandlung finden Sie unter Parameter für die [Fehlerbehandlung](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="40cf7-114">For information about flags for configuring the database to handle errors, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="40cf7-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40cf7-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40cf7-116"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="40cf7-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="40cf7-117">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="40cf7-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40cf7-118"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="40cf7-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="40cf7-119">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="40cf7-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40cf7-120"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="40cf7-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="40cf7-121">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="40cf7-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="40cf7-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="40cf7-122">See Also</span></span>

[<span data-ttu-id="40cf7-123">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="40cf7-123">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="40cf7-124">Fehler Codes für erweiterbare Speicher-Engine</span><span class="sxs-lookup"><span data-stu-id="40cf7-124">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="40cf7-125">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="40cf7-125">Error Handling Parameters</span></span>](./error-handling-parameters.md)
