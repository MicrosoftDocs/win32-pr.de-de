---
description: In der \_ Tabelle Storages werden eingebettete OLE-Datenspeicher aufgelistet. Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer SQL-Anweisung auf Sie verwiesen wird.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: _Storages Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864548"
---
# <a name="_storages-table"></a><span data-ttu-id="8c340-104">\_Tabelle "Storages"</span><span class="sxs-lookup"><span data-stu-id="8c340-104">\_Storages Table</span></span>

<span data-ttu-id="8c340-105">In der \_ Tabelle Storages werden eingebettete OLE-Datenspeicher aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8c340-105">The \_Storages table lists embedded OLE data storages.</span></span> <span data-ttu-id="8c340-106">Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer SQL-Anweisung auf Sie verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8c340-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="8c340-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="8c340-107">Column</span></span> | <span data-ttu-id="8c340-108">Typ</span><span class="sxs-lookup"><span data-stu-id="8c340-108">Type</span></span>                 | <span data-ttu-id="8c340-109">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="8c340-109">Key</span></span> | <span data-ttu-id="8c340-110">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="8c340-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="8c340-111">Name</span><span class="sxs-lookup"><span data-stu-id="8c340-111">Name</span></span>   | [<span data-ttu-id="8c340-112">Text</span><span class="sxs-lookup"><span data-stu-id="8c340-112">Text</span></span>](text.md)     | <span data-ttu-id="8c340-113">J</span><span class="sxs-lookup"><span data-stu-id="8c340-113">Y</span></span>   | <span data-ttu-id="8c340-114">N</span><span class="sxs-lookup"><span data-stu-id="8c340-114">N</span></span>        |
| <span data-ttu-id="8c340-115">Daten</span><span class="sxs-lookup"><span data-stu-id="8c340-115">Data</span></span>   | [<span data-ttu-id="8c340-116">Binär (Binary)</span><span class="sxs-lookup"><span data-stu-id="8c340-116">Binary</span></span>](binary.md) | <span data-ttu-id="8c340-117">N</span><span class="sxs-lookup"><span data-stu-id="8c340-117">N</span></span>   | <span data-ttu-id="8c340-118">J</span><span class="sxs-lookup"><span data-stu-id="8c340-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8c340-119">Spalten</span><span class="sxs-lookup"><span data-stu-id="8c340-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8c340-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="8c340-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="8c340-121">Ein eindeutiger Schlüssel, der den Speicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8c340-121">A unique key that identifies the storage.</span></span> <span data-ttu-id="8c340-122">Die maximale Länge des Namens beträgt 31 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8c340-122">The maximum length of Name is 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="8c340-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats</span><span class="sxs-lookup"><span data-stu-id="8c340-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="8c340-124">Die unformatierten Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="8c340-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c340-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c340-125">Remarks</span></span>

<span data-ttu-id="8c340-126">Um einer Datenbank einen OLE-Speicher hinzuzufügen, erstellen Sie einen neuen Datensatz in der \_ Tabelle "Storages" und geben den Namen des Speichers in die Spalte "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="8c340-126">To add an OLE storage to a database, create a new record in the \_Storages table and enter the name of the storage into the Name column.</span></span> <span data-ttu-id="8c340-127">Verwenden Sie [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , um Daten in die Datenspalte dieses Datensatzes zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="8c340-127">Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy data into the Data column of this record.</span></span> <span data-ttu-id="8c340-128">Verwenden Sie abschließend [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , um den Datensatz in die \_ Tabelle "Storages" einzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c340-128">Finally, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the \_Storages table.</span></span>

<span data-ttu-id="8c340-129">Daten können nicht aus der Tabelle "Storages" gelesen werden \_ .</span><span class="sxs-lookup"><span data-stu-id="8c340-129">Data cannot be read from the \_Storages table.</span></span> <span data-ttu-id="8c340-130">Allerdings \_ kann die Storages-Tabelle abgefragt werden, um zu überprüfen, ob ein bestimmter Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8c340-130">However, the \_Storages table can be queried to check for the existence of a specific storage.</span></span> <span data-ttu-id="8c340-131">Dies bedeutet, dass es nicht möglich ist, einen OLE-Speicher von einer Datenbank in eine andere zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="8c340-131">This means that it is not possible to move an OLE storage from one database to another.</span></span> <span data-ttu-id="8c340-132">Sie müssen stattdessen die ursprüngliche Speicherdatei in die neue Datenbank importieren. Zum Löschen eines OLE-Speichers rufen Sie den Datensatz ab, der die Binärdaten enthält, legen Sie die Datenspalte in der \_ Tabelle Storages auf NULL fest, und aktualisieren Sie dann den Datensatz.</span><span class="sxs-lookup"><span data-stu-id="8c340-132">You must instead import the original storage file into the new database.To delete an OLE storage, fetch the record containing the binary data, set the Data column in the \_Storages table to null, and then update the record.</span></span> <span data-ttu-id="8c340-133">Eine alternative Methode besteht darin, den Datensatz einfach entweder mithilfe von [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) oder einer einfachen SQL-Abfrage zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8c340-133">An alternative method is to simply delete the record using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span>

<span data-ttu-id="8c340-134">Um einen OLE-Speicher umzubenennen, aktualisieren Sie die Spalte Name des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="8c340-134">To rename an OLE storage, update the Name column of the record.</span></span>

<span data-ttu-id="8c340-135">Wenn eine Aufbewahrung in dieser Tabelle mithilfe von SQL (alter Table) platziert wird.</span><span class="sxs-lookup"><span data-stu-id="8c340-135">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="8c340-136">Halten) oder eine Spalte mit Hold hinzugefügt wird, muss die Tabelle mit Free freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8c340-136">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="8c340-137">Storages werden erst geschrieben, wenn die Tabelle freigegeben wurde oder ein Commit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8c340-137">Storages are not written until the table has been released or committed.</span></span>

 

 



