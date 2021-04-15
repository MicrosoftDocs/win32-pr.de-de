---
description: Weitere Informationen finden Sie in der API. retrievecolumschlag-Methode.
title: API. retrievecolumschlag-Methode
TOCTitle: 'RetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100867
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c981ad8b8e90db10bb8735aa349315b769e6641f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524715"
---
# <a name="apiretrievecolumns-method"></a><span data-ttu-id="07150-103">API. retrievecolumschlag-Methode</span><span class="sxs-lookup"><span data-stu-id="07150-103">Api.RetrieveColumns method</span></span>

<span data-ttu-id="07150-104">Ruft Spalten in ColumnValue-Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="07150-104">Retrieves columns into ColumnValue objects.</span></span>

<span data-ttu-id="07150-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="07150-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="07150-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="07150-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="07150-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="07150-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub RetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.RetrieveColumns(sesid, tableid, _
    values)
```

``` csharp
public static void RetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="07150-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="07150-108">Parameters</span></span>

  - <span data-ttu-id="07150-109">-sid</span><span class="sxs-lookup"><span data-stu-id="07150-109">sesid</span></span>  
    <span data-ttu-id="07150-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="07150-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="07150-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="07150-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="07150-112">TableID</span><span class="sxs-lookup"><span data-stu-id="07150-112">tableid</span></span>  
    <span data-ttu-id="07150-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="07150-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="07150-114">Der Cursor Ruft die Daten aus ab.</span><span class="sxs-lookup"><span data-stu-id="07150-114">The cursor retrieve the data from.</span></span> <span data-ttu-id="07150-115">Der Cursor muss auf einem Datensatz positioniert werden.</span><span class="sxs-lookup"><span data-stu-id="07150-115">The cursor should be positioned on a record.</span></span>

<!-- end list -->

  - <span data-ttu-id="07150-116">Werte</span><span class="sxs-lookup"><span data-stu-id="07150-116">values</span></span>  
    <span data-ttu-id="07150-117">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="07150-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="07150-118">Die abzurufenden Werte.</span><span class="sxs-lookup"><span data-stu-id="07150-118">The values to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="07150-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07150-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="07150-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="07150-120">Reference</span></span>

[<span data-ttu-id="07150-121">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="07150-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="07150-122">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="07150-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="07150-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="07150-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
