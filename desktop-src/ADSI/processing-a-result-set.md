---
title: Verarbeiten eines Resultsets
description: Ein Resultset wird als eine Reihe von Zeilen zurückgegeben.
ms.assetid: e0949c1c-a31a-440a-ae10-2934ffeb7128
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ad422494fd2d384b612989e9e36cec7110e021
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316449"
---
# <a name="processing-a-result-set"></a><span data-ttu-id="d5751-103">Verarbeiten eines Resultsets</span><span class="sxs-lookup"><span data-stu-id="d5751-103">Processing a Result Set</span></span>

<span data-ttu-id="d5751-104">Ein Resultset wird als eine Reihe von Zeilen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5751-104">A result set is returned as a series of rows.</span></span> <span data-ttu-id="d5751-105">Jede Zeile kann ein bestimmtes Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="d5751-105">Each row may or may not contain a given attribute.</span></span> <span data-ttu-id="d5751-106">Mit dem OLE DB-Anbieter wird das Resultset ähnlich wie ein normales SQL-Resultset angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5751-106">With the OLE DB provider, the result set appears similar to a normal SQL result set.</span></span> <span data-ttu-id="d5751-107">Wenn Sie ADO für die Abfrage verwenden, [ADODB. Das Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) -Objekt wird zum Durchlaufen des Resultsets verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5751-107">If you use ADO for the query, the [ADODB.Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) object is used for traversing the result set.</span></span> <span data-ttu-id="d5751-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (nur in Sprachen verfügbar, die Vtable-Bindungen unterstützen) enthält Elemente zum Verschieben des Zeilen Cursors und Überprüfen von Eigenschafts Werten in einer bestimmten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d5751-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (available only from languages that support vtable bindings) contains members for moving the row cursor and checking property values in a given row.</span></span> <span data-ttu-id="d5751-109">Alternativ können Sie [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) verwenden, um Eigenschaften zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d5751-109">Alternatively, you can use [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) to get and set properties.</span></span>

 

 