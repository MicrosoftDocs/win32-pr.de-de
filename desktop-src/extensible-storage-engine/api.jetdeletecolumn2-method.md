---
description: Weitere Informationen finden Sie in der API. JetDeleteColumn2-Methode.
title: API. JetDeleteColumn2-Methode
TOCTitle: 'JetDeleteColumn2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.DeleteColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn2(v=EXCHG.10)
ms:contentKeyID: 55100680
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0426ca2557dac11c565211162438db6d5c77a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345025"
---
# <a name="apijetdeletecolumn2-method"></a><span data-ttu-id="9140f-103">API. JetDeleteColumn2-Methode</span><span class="sxs-lookup"><span data-stu-id="9140f-103">Api.JetDeleteColumn2 method</span></span>

<span data-ttu-id="9140f-104">Löscht eine Spalte aus einer Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="9140f-104">Deletes a column from a database table.</span></span>

<span data-ttu-id="9140f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9140f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9140f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9140f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9140f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9140f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteColumn2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    grbit As DeleteColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim grbit As DeleteColumnGrbitApi.JetDeleteColumn2(sesid, tableid, _
    column, grbit)
```

``` csharp
public static void JetDeleteColumn2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    DeleteColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9140f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9140f-108">Parameters</span></span>

  - <span data-ttu-id="9140f-109">-sid</span><span class="sxs-lookup"><span data-stu-id="9140f-109">sesid</span></span>  
    <span data-ttu-id="9140f-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9140f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9140f-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9140f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9140f-112">TableID</span><span class="sxs-lookup"><span data-stu-id="9140f-112">tableid</span></span>  
    <span data-ttu-id="9140f-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9140f-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9140f-114">Ein Cursor für die Tabelle, aus der die Spalte gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9140f-114">A cursor on the table to delete the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="9140f-115">column</span><span class="sxs-lookup"><span data-stu-id="9140f-115">column</span></span>  
    <span data-ttu-id="9140f-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9140f-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9140f-117">Der Name der zu löschenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="9140f-117">The name of the column to be deleted.</span></span>

<!-- end list -->

  - <span data-ttu-id="9140f-118">grbit</span><span class="sxs-lookup"><span data-stu-id="9140f-118">grbit</span></span>  
    <span data-ttu-id="9140f-119">Typ: [Microsoft. ISAM. ESENT. Interop. deletecolumngrbit](./deletecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9140f-119">Type: [Microsoft.Isam.Esent.Interop.DeleteColumnGrbit](./deletecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9140f-120">Optionen für das Löschen von Spalten.</span><span class="sxs-lookup"><span data-stu-id="9140f-120">Column deletion options.</span></span>

## <a name="see-also"></a><span data-ttu-id="9140f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9140f-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9140f-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="9140f-122">Reference</span></span>

[<span data-ttu-id="9140f-123">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="9140f-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9140f-124">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="9140f-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9140f-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9140f-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
