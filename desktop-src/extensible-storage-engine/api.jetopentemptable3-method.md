---
description: Weitere Informationen finden Sie in der API. JetOpenTempTable3-Methode.
title: Api.JetOpenTempTable3-Methode
TOCTitle: 'JetOpenTempTable3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable3(v=EXCHG.10)
ms:contentKeyID: 55100774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e88b5413492c0ae00ed41e569afb49ca6c18e51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352736"
---
# <a name="apijetopentemptable3-method"></a><span data-ttu-id="84365-103">Api.JetOpenTempTable3-Methode</span><span class="sxs-lookup"><span data-stu-id="84365-103">Api.JetOpenTempTable3 method</span></span>

<span data-ttu-id="84365-104">Erstellt eine temporäre Tabelle mit einem einzelnen Index.</span><span class="sxs-lookup"><span data-stu-id="84365-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="84365-105">Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="84365-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="84365-106">Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen.</span><span class="sxs-lookup"><span data-stu-id="84365-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="84365-107">Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="84365-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="84365-108">Siehe auch [jetopentemptable (JET_SESID, \[ \] , Int32, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [jetopentemporarytable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="84365-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="84365-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="84365-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="84365-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="84365-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="84365-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="84365-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable3 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    unicodeindex As JET_UNICODEINDEX, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim unicodeindex As JET_UNICODEINDEX
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable3(sesid, columns, _
    numColumns, unicodeindex, grbit, _
    tableid, columnids)
```

``` csharp
public static void JetOpenTempTable3(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    JET_UNICODEINDEX unicodeindex,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="84365-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="84365-112">Parameters</span></span>

  - <span data-ttu-id="84365-113">-sid</span><span class="sxs-lookup"><span data-stu-id="84365-113">sesid</span></span>  
    <span data-ttu-id="84365-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="84365-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="84365-115">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="84365-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="84365-116">Spalten</span><span class="sxs-lookup"><span data-stu-id="84365-116">columns</span></span>  
    <span data-ttu-id="84365-117">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="84365-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="84365-118">Spaltendefinitionen für die Spalten, die in der temporären Tabelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="84365-118">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="84365-119">NumColumns</span><span class="sxs-lookup"><span data-stu-id="84365-119">numColumns</span></span>  
    <span data-ttu-id="84365-120">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="84365-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="84365-121">Anzahl der Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="84365-121">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="84365-122">unicodeindex</span><span class="sxs-lookup"><span data-stu-id="84365-122">unicodeindex</span></span>  
    <span data-ttu-id="84365-123">Typ: [Microsoft.ISAM.ESENT.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="84365-123">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  
    
    <span data-ttu-id="84365-124">Die Gebiets Schema-ID und die normalisierungs Flags, die verwendet werden, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="84365-124">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="84365-125">Wenn dies nicht der Fall ist, werden die Standardoptionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="84365-125">When this is not present then the default options are used.</span></span>

<!-- end list -->

  - <span data-ttu-id="84365-126">grbit</span><span class="sxs-lookup"><span data-stu-id="84365-126">grbit</span></span>  
    <span data-ttu-id="84365-127">Typ: [Microsoft. ISAM. ESENT. Interop. temptablegrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="84365-127">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="84365-128">Tabellen Erstellungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="84365-128">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="84365-129">TableID</span><span class="sxs-lookup"><span data-stu-id="84365-129">tableid</span></span>  
    <span data-ttu-id="84365-130">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="84365-130">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="84365-131">Gibt die TableID der temporären Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="84365-131">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="84365-132">Wenn Sie diese TableID mit [jetclosetable (JET_SESID JET_TABLEID) schließen, werden](./api.jetclosetable-method.md) die der temporären Tabelle zugeordneten Ressourcen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="84365-132">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="84365-133">columnIds</span><span class="sxs-lookup"><span data-stu-id="84365-133">columnids</span></span>  
    <span data-ttu-id="84365-134">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="84365-134">Type: \[\]</span></span>  
    
    <span data-ttu-id="84365-135">Der Ausgabepuffer, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="84365-135">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="84365-136">Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="84365-136">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="84365-137">Folglich muss die Größe dieses Puffers der Größe des Eingabe Arrays entsprechen.</span><span class="sxs-lookup"><span data-stu-id="84365-137">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="84365-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84365-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="84365-139">Referenz</span><span class="sxs-lookup"><span data-stu-id="84365-139">Reference</span></span>

[<span data-ttu-id="84365-140">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="84365-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="84365-141">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="84365-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="84365-142">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="84365-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
