---
description: In der \_ Tabelle Streams werden eingebettete OLE-Datenströme aufgelistet. Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer SQL-Anweisung auf Sie verwiesen wird.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: _Streams Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9607097b32acc8a3c2350a00db0b9721a4aa353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358855"
---
# <a name="_streams-table"></a><span data-ttu-id="6ed9d-104">\_Streams-Tabelle</span><span class="sxs-lookup"><span data-stu-id="6ed9d-104">\_Streams Table</span></span>

<span data-ttu-id="6ed9d-105">In der \_ Tabelle Streams werden eingebettete OLE-Datenströme aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-105">The \_Streams table lists embedded OLE data streams.</span></span> <span data-ttu-id="6ed9d-106">Dies ist eine temporäre Tabelle, die nur erstellt wird, wenn von einer SQL-Anweisung auf Sie verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="6ed9d-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="6ed9d-107">Column</span></span> | <span data-ttu-id="6ed9d-108">Typ</span><span class="sxs-lookup"><span data-stu-id="6ed9d-108">Type</span></span>                 | <span data-ttu-id="6ed9d-109">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="6ed9d-109">Key</span></span> | <span data-ttu-id="6ed9d-110">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="6ed9d-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="6ed9d-111">Name</span><span class="sxs-lookup"><span data-stu-id="6ed9d-111">Name</span></span>   | [<span data-ttu-id="6ed9d-112">Text</span><span class="sxs-lookup"><span data-stu-id="6ed9d-112">Text</span></span>](text.md)     | <span data-ttu-id="6ed9d-113">J</span><span class="sxs-lookup"><span data-stu-id="6ed9d-113">Y</span></span>   | <span data-ttu-id="6ed9d-114">N</span><span class="sxs-lookup"><span data-stu-id="6ed9d-114">N</span></span>        |
| <span data-ttu-id="6ed9d-115">Daten</span><span class="sxs-lookup"><span data-stu-id="6ed9d-115">Data</span></span>   | [<span data-ttu-id="6ed9d-116">Binär (Binary)</span><span class="sxs-lookup"><span data-stu-id="6ed9d-116">Binary</span></span>](binary.md) | <span data-ttu-id="6ed9d-117">N</span><span class="sxs-lookup"><span data-stu-id="6ed9d-117">N</span></span>   | <span data-ttu-id="6ed9d-118">J</span><span class="sxs-lookup"><span data-stu-id="6ed9d-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6ed9d-119">Spalten</span><span class="sxs-lookup"><span data-stu-id="6ed9d-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6ed9d-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="6ed9d-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="6ed9d-121">Ein eindeutiger Schlüssel, der den Datenstrom identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-121">A unique key that identifies the stream.</span></span> <span data-ttu-id="6ed9d-122">Die maximale Länge des Namens beträgt 62 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-122">The maximum length of Name is 62 characters.</span></span>

</dd> <dt>

<span data-ttu-id="6ed9d-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats</span><span class="sxs-lookup"><span data-stu-id="6ed9d-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="6ed9d-124">Die unformatierten Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ed9d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ed9d-125">Remarks</span></span>

<span data-ttu-id="6ed9d-126">Um einen OLE-Datenstrom (z. b. ein Objekt des [Binary](binary.md) -Datentyps) aus einer Datei in eine Datenbank zu kopieren, erstellen Sie einen Datensatz in der \_ Streams-Tabelle, und geben Sie den Namen des Datenstroms in die Spalte Name dieses Datensatzes ein. Kopieren Sie die Daten aus der Datei mithilfe von [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)in die Datenspalte.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-126">To copy an OLE data stream (for example, an object of the [Binary](binary.md) data type) from a file into a database, create a record in the \_Streams table and enter the name of the data stream into the Name column of this record and copy the data from the file into the Data column using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span></span> <span data-ttu-id="6ed9d-127">Verwenden Sie [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , um den neuen Datensatz in die Tabelle einzufügen.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-127">Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the new record into the table.</span></span>

<span data-ttu-id="6ed9d-128">Um einen in einer Datenbank eingebetteten binären Datenstrom zu lesen, verwenden Sie eine SQL-Abfrage, um den Datensatz zu suchen und abzurufen, der die Binärdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-128">To read a binary data stream embedded in a database, use a SQL query to find and to fetch the record containing the binary data.</span></span> <span data-ttu-id="6ed9d-129">Verwenden Sie [**msirecordlesestream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) , um die Binärdaten in einen Puffer zu lesen.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-129">Use [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) to read the binary data into a buffer.</span></span>

<span data-ttu-id="6ed9d-130">Um einen binären Datenstrom von einer Datenbank in eine andere zu verschieben, exportieren Sie zuerst die Daten in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-130">To move a binary data stream from one database to another, first export the data to a file.</span></span> <span data-ttu-id="6ed9d-131">Verwenden Sie eine SQL-Abfrage, um den Datenstrom in der Datei zu suchen, und verwenden Sie [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , um die Daten aus der Datei in die Datenspalte der \_ Tabelle Streams der zweiten Datenbank zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-131">Use a SQL query to find the data stream in the file and use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy the data from the file into Data column of \_Streams table of the second database.</span></span> <span data-ttu-id="6ed9d-132">Dadurch wird sichergestellt, dass jede Datenbank über eine eigene Kopie der Binärdaten verfügt.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-132">This ensures that each database has its own copy of the binary data.</span></span> <span data-ttu-id="6ed9d-133">Sie können binäre Daten nicht aus einer Datenbank in eine andere verschieben, indem Sie einfach einen Datensatz mit den Daten aus der ersten Datenbank abrufen und in die zweite Datenbank einfügen.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-133">You cannot move binary data from one database to another simply by fetching a record with the data from the first database and inserting it into the second database.</span></span>

<span data-ttu-id="6ed9d-134">Um einen Datenstrom zu löschen, rufen Sie den Datensatz ab, und legen Sie die Datenspalte vor dem Aktualisieren des Datensatzes auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-134">To delete a data stream, fetch the record and set the Data column to null before updating the record.</span></span> <span data-ttu-id="6ed9d-135">Eine andere Methode besteht darin, den Datensatz aus der Tabelle zu entfernen und ihn entweder mithilfe von [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) oder einer einfachen SQL-Abfrage zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-135">Another method is to remove the record from the table, deleting it using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span> <span data-ttu-id="6ed9d-136">Ein Datenstrom sollte nicht in einen Datensatz abgerufen werden, wenn der Stream aus der Tabelle gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-136">A stream should not be fetched into a record if the stream is deleted from the table.</span></span>

<span data-ttu-id="6ed9d-137">Zum Umbenennen eines OLE-Datenstroms aktualisieren Sie die Spalte "Name" des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-137">To rename an OLE data stream, update the 'Name' column of the record.</span></span>

<span data-ttu-id="6ed9d-138">Wenn eine Aufbewahrung in dieser Tabelle mithilfe von SQL (alter Table) platziert wird.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-138">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="6ed9d-139">Halten) oder eine Spalte mit Hold hinzugefügt wird, muss die Tabelle mit Free freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-139">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="6ed9d-140">Streams werden erst geschrieben, wenn die Tabelle freigegeben oder ein Commit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed9d-140">Streams are not written until the table has been released or committed.</span></span>

 

 



