---
description: Weitere Informationen finden Sie in der API. SetColumns-Methode.
title: API. SetColumns-Methode
TOCTitle: 'SetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumns(v=EXCHG.10)
ms:contentKeyID: 55100936
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4ed75c668c0000c1d01d521a57ead46055bc8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749473"
---
# <a name="apisetcolumns-method"></a><span data-ttu-id="4754f-103">API. SetColumns-Methode</span><span class="sxs-lookup"><span data-stu-id="4754f-103">Api.SetColumns method</span></span>

<span data-ttu-id="4754f-104">Legt Spalten aus ColumnValue-Objekten fest.</span><span class="sxs-lookup"><span data-stu-id="4754f-104">Sets columns from ColumnValue objects.</span></span>

<span data-ttu-id="4754f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4754f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4754f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4754f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4754f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4754f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.SetColumns(sesid, tableid, values)
```

``` csharp
public static void SetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="4754f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4754f-108">Parameters</span></span>

  - <span data-ttu-id="4754f-109">-sid</span><span class="sxs-lookup"><span data-stu-id="4754f-109">sesid</span></span>  
    <span data-ttu-id="4754f-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4754f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4754f-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="4754f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4754f-112">TableID</span><span class="sxs-lookup"><span data-stu-id="4754f-112">tableid</span></span>  
    <span data-ttu-id="4754f-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4754f-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4754f-114">Der Cursor, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4754f-114">The cursor to update.</span></span> <span data-ttu-id="4754f-115">Ein Update sollte vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="4754f-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="4754f-116">Werte</span><span class="sxs-lookup"><span data-stu-id="4754f-116">values</span></span>  
    <span data-ttu-id="4754f-117">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="4754f-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="4754f-118">Die festzulegenden Werte.</span><span class="sxs-lookup"><span data-stu-id="4754f-118">The values to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="4754f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4754f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4754f-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="4754f-120">Reference</span></span>

[<span data-ttu-id="4754f-121">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="4754f-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4754f-122">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="4754f-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4754f-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4754f-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
