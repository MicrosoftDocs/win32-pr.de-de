---
description: Weitere Informationen finden Sie in der API. retrievecolumschlag-Methode.
title: API. retrievecolumschlag-Methode
TOCTitle: 'RetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100835
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 3bcb5effcfc59e155007fbd9e1733d95db058970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758977"
---
# <a name="apiretrievecolumn-method"></a><span data-ttu-id="a2081-103">API. retrievecolumschlag-Methode</span><span class="sxs-lookup"><span data-stu-id="a2081-103">Api.RetrieveColumn method</span></span>

<span data-ttu-id="a2081-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="a2081-104">Include protected members</span></span>  
<span data-ttu-id="a2081-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="a2081-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="a2081-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="a2081-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a2081-107">Name</span><span class="sxs-lookup"><span data-stu-id="a2081-107">Name</span></span></th>
<th><span data-ttu-id="a2081-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2081-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="a2081-111"><a href="dn334041(v=exchg.10).md">Retrievecolumschlag (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span><span class="sxs-lookup"><span data-stu-id="a2081-111"><a href="dn334041(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a2081-112">Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="a2081-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a2081-113">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a2081-113">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="a2081-116"><a href="dn334060(v=exchg.10).md">Retrievecolbin (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="a2081-116"><a href="dn334060(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="a2081-117">Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="a2081-117">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a2081-118">Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a2081-118">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="a2081-119">Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a2081-119">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="a2081-120">Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist.</span><span class="sxs-lookup"><span data-stu-id="a2081-120">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="a2081-121">Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann jetretrievecolumschlag auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, sodass die Größe der Anwendungs Puffer entsprechend angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2081-121">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a2081-122">Oben</span><span class="sxs-lookup"><span data-stu-id="a2081-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a2081-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2081-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a2081-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="a2081-124">Reference</span></span>

[<span data-ttu-id="a2081-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="a2081-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a2081-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="a2081-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a2081-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a2081-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
