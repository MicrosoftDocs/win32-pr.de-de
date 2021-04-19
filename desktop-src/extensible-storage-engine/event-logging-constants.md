---
description: 'Weitere Informationen: Ereignis Protokollierungs Konstanten'
title: Ereignis Protokollierungs Konstanten
TOCTitle: Event Logging Constants
ms:assetid: d24603a9-a9be-4700-bc20-4e3f0661e741
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294101(v=EXCHG.10)
ms:contentKeyID: 32765716
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
ms.openlocfilehash: e7ada5c71b603bf530c62d9f3af238131e305e42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363536"
---
# <a name="event-logging-constants"></a><span data-ttu-id="8e0f8-103">Ereignis Protokollierungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="8e0f8-103">Event Logging Constants</span></span>


<span data-ttu-id="8e0f8-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8e0f8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="event-logging-constants"></a><span data-ttu-id="8e0f8-105">Ereignis Protokollierungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="8e0f8-105">Event Logging Constants</span></span>

<span data-ttu-id="8e0f8-106">Die folgenden Konstanten geben die Detailebene für Ereignisprotokoll Meldungen für den [JET_ParamEventLoggingLevel](./event-log-parameters.md) System-Parameter an.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-106">The following constants indicate the detail level for event log messages for the [JET_ParamEventLoggingLevel](./event-log-parameters.md) system parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e0f8-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="8e0f8-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="8e0f8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e0f8-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e0f8-109">JET_EventLoggingDisable</span><span class="sxs-lookup"><span data-stu-id="8e0f8-109">JET_EventLoggingDisable</span></span><br />
<span data-ttu-id="8e0f8-110">0</span><span class="sxs-lookup"><span data-stu-id="8e0f8-110">0</span></span></p></td>
<td><p><span data-ttu-id="8e0f8-111">Deaktiviert die Ereignisprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-111">Disables event logging.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e0f8-112">JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="8e0f8-112">JET_EventLoggingLevelMax</span></span><br />
<span data-ttu-id="8e0f8-113">100</span><span class="sxs-lookup"><span data-stu-id="8e0f8-113">100</span></span></p></td>
<td><p><span data-ttu-id="8e0f8-114">Legt die maximale Ebene fest, die für Ereignisprotokolle verwendet werden soll, die derzeit 100 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-114">Sets the maximum level to use for event logs, which is currently 100 characters.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="8e0f8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e0f8-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e0f8-116"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8e0f8-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8e0f8-117">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e0f8-118"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8e0f8-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8e0f8-119">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e0f8-120"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8e0f8-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8e0f8-121">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="8e0f8-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8e0f8-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e0f8-122">See Also</span></span>

[<span data-ttu-id="8e0f8-123">Ereignisprotokoll Parameter</span><span class="sxs-lookup"><span data-stu-id="8e0f8-123">Event Log Parameters</span></span>](./event-log-parameters.md)
