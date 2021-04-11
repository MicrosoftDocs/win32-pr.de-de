---
description: Weitere Informationen finden Sie in der API. JetOpenTempTable2-Methode.
title: API. JetOpenTempTable2-Methode
TOCTitle: 'JetOpenTempTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable2(v=EXCHG.10)
ms:contentKeyID: 55100777
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fd3f0e04db6519fbcaa1c2d2fa9060d2d993d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218280"
---
# <a name="apijetopentemptable2-method"></a><span data-ttu-id="d6529-103">API. JetOpenTempTable2-Methode</span><span class="sxs-lookup"><span data-stu-id="d6529-103">Api.JetOpenTempTable2 method</span></span>

<span data-ttu-id="d6529-104">Erstellt eine temporäre Tabelle mit einem einzelnen Index.</span><span class="sxs-lookup"><span data-stu-id="d6529-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="d6529-105">Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d6529-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="d6529-106">Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen.</span><span class="sxs-lookup"><span data-stu-id="d6529-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="d6529-107">Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="d6529-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="d6529-108">Siehe auch [jetopentemptable (JET_SESID, \[ \] , Int32, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="d6529-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="d6529-109">[Jetopumtemporarytable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="d6529-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="d6529-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6529-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d6529-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d6529-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6529-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6529-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable2 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    lcid As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim lcid As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable2(sesid, columns, _
    numColumns, lcid, grbit, tableid, _
    columnids)
```

``` csharp
public static void JetOpenTempTable2(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    int lcid,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="d6529-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6529-113">Parameters</span></span>

  - <span data-ttu-id="d6529-114">-sid</span><span class="sxs-lookup"><span data-stu-id="d6529-114">sesid</span></span>  
    <span data-ttu-id="d6529-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d6529-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d6529-116">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d6529-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6529-117">Spalten</span><span class="sxs-lookup"><span data-stu-id="d6529-117">columns</span></span>  
    <span data-ttu-id="d6529-118">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="d6529-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="d6529-119">Spaltendefinitionen für die Spalten, die in der temporären Tabelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6529-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6529-120">NumColumns</span><span class="sxs-lookup"><span data-stu-id="d6529-120">numColumns</span></span>  
    <span data-ttu-id="d6529-121">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d6529-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d6529-122">Anzahl der Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d6529-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6529-123">lcid</span><span class="sxs-lookup"><span data-stu-id="d6529-123">lcid</span></span>  
    <span data-ttu-id="d6529-124">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d6529-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d6529-125">Die Gebiets Schema-ID, die zum Vergleichen von Unicode-Schlüssel Spaltendaten in der temporären Tabelle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6529-125">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="d6529-126">Jedes Gebiets Schema kann verwendet werden, solange das entsprechende Sprachpaket auf dem Computer installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d6529-126">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6529-127">grbit</span><span class="sxs-lookup"><span data-stu-id="d6529-127">grbit</span></span>  
    <span data-ttu-id="d6529-128">Typ: [Microsoft. ISAM. ESENT. Interop. temptablegrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d6529-128">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d6529-129">Tabellen Erstellungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="d6529-129">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6529-130">TableID</span><span class="sxs-lookup"><span data-stu-id="d6529-130">tableid</span></span>  
    <span data-ttu-id="d6529-131">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d6529-131">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d6529-132">Gibt die TableID der temporären Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="d6529-132">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="d6529-133">Wenn Sie diese TableID mit [jetclosetable (JET_SESID JET_TABLEID) schließen, werden](./api.jetclosetable-method.md) die der temporären Tabelle zugeordneten Ressourcen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="d6529-133">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6529-134">columnIds</span><span class="sxs-lookup"><span data-stu-id="d6529-134">columnids</span></span>  
    <span data-ttu-id="d6529-135">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="d6529-135">Type: \[\]</span></span>  
    
    <span data-ttu-id="d6529-136">Der Ausgabepuffer, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d6529-136">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="d6529-137">Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d6529-137">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="d6529-138">Folglich muss die Größe dieses Puffers der Größe des Eingabe Arrays entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d6529-138">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6529-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6529-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6529-140">Referenz</span><span class="sxs-lookup"><span data-stu-id="d6529-140">Reference</span></span>

[<span data-ttu-id="d6529-141">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="d6529-141">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d6529-142">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="d6529-142">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d6529-143">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="d6529-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
