---
description: 'Weitere Informationen finden Sie unter: API. jetcomputestats-Methode'
title: API. jetcomputestats-Methode
TOCTitle: 'JetComputeStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetComputeStats(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcomputestats(v=EXCHG.10)
ms:contentKeyID: 55100667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b102aca5971656232fae02684aeab30322d208b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214360"
---
# <a name="apijetcomputestats-method"></a><span data-ttu-id="68d30-103">API. jetcomputestats-Methode</span><span class="sxs-lookup"><span data-stu-id="68d30-103">Api.JetComputeStats method</span></span>

<span data-ttu-id="68d30-104">Führt jeden Index einer Tabelle aus, um die Anzahl der Einträge in einem Index und die Anzahl der unterschiedlichen Schlüssel in einem Index exakt zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="68d30-104">Walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="68d30-105">Diese Informationen werden in Verbindung mit der Anzahl von Datenbankseiten, die für einen Index zugeordnet sind, und dem aktuellen Zeitpunkt der Berechnung in den Index Metadaten in der Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="68d30-105">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="68d30-106">Diese Daten können anschließend mit Informations Vorgängen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="68d30-106">This data can be subsequently retrieved with information operations.</span></span>

<span data-ttu-id="68d30-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="68d30-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="68d30-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="68d30-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="68d30-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="68d30-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetComputeStats ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetComputeStats(sesid, tableid)
```

``` csharp
public static void JetComputeStats(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="68d30-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="68d30-110">Parameters</span></span>

  - <span data-ttu-id="68d30-111">-sid</span><span class="sxs-lookup"><span data-stu-id="68d30-111">sesid</span></span>  
    <span data-ttu-id="68d30-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="68d30-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="68d30-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="68d30-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="68d30-114">TableID</span><span class="sxs-lookup"><span data-stu-id="68d30-114">tableid</span></span>  
    <span data-ttu-id="68d30-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="68d30-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="68d30-116">Die Tabelle, für die die Statistiken berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="68d30-116">The table that the statistics will be computed on.</span></span>

## <a name="see-also"></a><span data-ttu-id="68d30-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68d30-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="68d30-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="68d30-118">Reference</span></span>

[<span data-ttu-id="68d30-119">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="68d30-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="68d30-120">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="68d30-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="68d30-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="68d30-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
