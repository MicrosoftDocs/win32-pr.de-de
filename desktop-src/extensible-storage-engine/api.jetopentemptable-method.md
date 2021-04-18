---
description: Weitere Informationen finden Sie in der API. jetopkotemptable-Methode.
title: API. jetopkotemptable-Methode
TOCTitle: 'JetOpenTempTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable(v=EXCHG.10)
ms:contentKeyID: 55100773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa41ce62b8bc2d7f2429acb5de809ad0be44a609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351093"
---
# <a name="apijetopentemptable-method"></a><span data-ttu-id="22f99-103">API. jetopkotemptable-Methode</span><span class="sxs-lookup"><span data-stu-id="22f99-103">Api.JetOpenTempTable method</span></span>

<span data-ttu-id="22f99-104">Erstellt eine temporäre Tabelle mit einem einzelnen Index.</span><span class="sxs-lookup"><span data-stu-id="22f99-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="22f99-105">Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="22f99-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="22f99-106">Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen.</span><span class="sxs-lookup"><span data-stu-id="22f99-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="22f99-107">Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="22f99-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="22f99-108">Siehe auch [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="22f99-108">Also see [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="22f99-109">[Jetopumtemporarytable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="22f99-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="22f99-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="22f99-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="22f99-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="22f99-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="22f99-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="22f99-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable(sesid, columns, _
    numColumns, grbit, tableid, columnids)
```

``` csharp
public static void JetOpenTempTable(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="22f99-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="22f99-113">Parameters</span></span>

  - <span data-ttu-id="22f99-114">-sid</span><span class="sxs-lookup"><span data-stu-id="22f99-114">sesid</span></span>  
    <span data-ttu-id="22f99-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="22f99-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="22f99-116">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="22f99-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="22f99-117">Spalten</span><span class="sxs-lookup"><span data-stu-id="22f99-117">columns</span></span>  
    <span data-ttu-id="22f99-118">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="22f99-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="22f99-119">Spaltendefinitionen für die Spalten, die in der temporären Tabelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="22f99-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="22f99-120">NumColumns</span><span class="sxs-lookup"><span data-stu-id="22f99-120">numColumns</span></span>  
    <span data-ttu-id="22f99-121">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="22f99-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="22f99-122">Anzahl der Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="22f99-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="22f99-123">grbit</span><span class="sxs-lookup"><span data-stu-id="22f99-123">grbit</span></span>  
    <span data-ttu-id="22f99-124">Typ: [Microsoft. ISAM. ESENT. Interop. temptablegrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="22f99-124">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="22f99-125">Tabellen Erstellungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="22f99-125">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="22f99-126">TableID</span><span class="sxs-lookup"><span data-stu-id="22f99-126">tableid</span></span>  
    <span data-ttu-id="22f99-127">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="22f99-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="22f99-128">Gibt die TableID der temporären Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="22f99-128">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="22f99-129">Wenn Sie diese TableID mit [jetclosetable (JET_SESID JET_TABLEID) schließen, werden](./api.jetclosetable-method.md) die der temporären Tabelle zugeordneten Ressourcen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="22f99-129">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="22f99-130">columnIds</span><span class="sxs-lookup"><span data-stu-id="22f99-130">columnids</span></span>  
    <span data-ttu-id="22f99-131">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="22f99-131">Type: \[\]</span></span>  
    
    <span data-ttu-id="22f99-132">Der Ausgabepuffer, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="22f99-132">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="22f99-133">Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="22f99-133">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="22f99-134">Folglich muss die Größe dieses Puffers der Größe des Eingabe Arrays entsprechen.</span><span class="sxs-lookup"><span data-stu-id="22f99-134">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="22f99-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22f99-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="22f99-136">Referenz</span><span class="sxs-lookup"><span data-stu-id="22f99-136">Reference</span></span>

[<span data-ttu-id="22f99-137">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="22f99-137">Api class</span></span>](./api-class.md)

[<span data-ttu-id="22f99-138">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="22f99-138">Api members</span></span>](./api-members.md)

[<span data-ttu-id="22f99-139">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="22f99-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
