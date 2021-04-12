---
description: Weitere Informationen finden Sie in der API. jetretrievecolumschlag-Methode.
title: API. jetretrievecolumschlag-Methode
TOCTitle: 'JetRetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100791
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: e4e43d57f4393d6b0d4ce2f1cdbe4ecd8338ec54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218469"
---
# <a name="apijetretrievecolumn-method"></a><span data-ttu-id="a50f6-103">API. jetretrievecolumschlag-Methode</span><span class="sxs-lookup"><span data-stu-id="a50f6-103">Api.JetRetrieveColumn method</span></span>

<span data-ttu-id="a50f6-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="a50f6-104">Include protected members</span></span>  
<span data-ttu-id="a50f6-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="a50f6-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="a50f6-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="a50f6-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a50f6-107">Name</span><span class="sxs-lookup"><span data-stu-id="a50f6-107">Name</span></span></th>
<th><span data-ttu-id="a50f6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a50f6-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="a50f6-111"><a href="dn332995(v=exchg.10).md">Jetretrievecolbin (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, retrievecolumgengrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="a50f6-111"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="a50f6-112">Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="a50f6-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a50f6-113">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a50f6-113">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="a50f6-114">Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a50f6-114">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="a50f6-115">Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist.</span><span class="sxs-lookup"><span data-stu-id="a50f6-115">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="a50f6-116">Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann jetretrievecolumschlag auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, sodass die Größe der Anwendungs Puffer entsprechend angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="a50f6-116">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="a50f6-119"><a href="dn332997(v=exchg.10).md">Jetretrievecolbin (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, retrievecolumgengrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="a50f6-119"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="a50f6-120">Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="a50f6-120">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a50f6-121">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a50f6-121">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="a50f6-122">Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a50f6-122">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="a50f6-123">Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist.</span><span class="sxs-lookup"><span data-stu-id="a50f6-123">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="a50f6-124">Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann jetretrievecolumschlag auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, sodass die Größe der Anwendungs Puffer entsprechend angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="a50f6-124">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a50f6-125">Oben</span><span class="sxs-lookup"><span data-stu-id="a50f6-125">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a50f6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a50f6-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a50f6-127">Referenz</span><span class="sxs-lookup"><span data-stu-id="a50f6-127">Reference</span></span>

[<span data-ttu-id="a50f6-128">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="a50f6-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a50f6-129">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="a50f6-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a50f6-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a50f6-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
