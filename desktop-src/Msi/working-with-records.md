---
description: Das Installationsprogramm stellt Funktionen bereit, die die Datensätze in einer Installations Datenbank bearbeiten. Diese Funktionen können in Verbindung mit den in Arbeiten mit Abfragen beschriebenen Funktionen verwendet werden, um tatsächliche Änderungen in einer Datenbank vorzunehmen.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Arbeiten mit Datensätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3252dc29bf755d08494dbdc2326bf45a4afb1c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349483"
---
# <a name="working-with-records"></a><span data-ttu-id="9076a-104">Arbeiten mit Datensätzen</span><span class="sxs-lookup"><span data-stu-id="9076a-104">Working with Records</span></span>

<span data-ttu-id="9076a-105">Das Installationsprogramm stellt Funktionen bereit, die die Datensätze in einer Installations Datenbank bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9076a-105">The installer supplies functions that manipulate the records in an installation database.</span></span> <span data-ttu-id="9076a-106">Diese Funktionen können in Verbindung mit den in [Arbeiten mit Abfragen](working-with-queries.md) beschriebenen Funktionen verwendet werden, um tatsächliche Änderungen in einer Datenbank vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="9076a-106">These functions can be used in conjunction with the functions described in [Working with Queries](working-with-queries.md) to make actual changes in a database.</span></span>

<span data-ttu-id="9076a-107">Die folgenden Funktionen erstellen oder entfernen Datensätze:</span><span class="sxs-lookup"><span data-stu-id="9076a-107">The following functions create or remove records:</span></span>

-   <span data-ttu-id="9076a-108">Um einen neuen Datensatz für eine Datenbank zu erstellen, rufen Sie die [**msikreaterecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9076a-108">To create a new record for a database, call the [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) function.</span></span>
-   <span data-ttu-id="9076a-109">Wenn Sie Daten aus einem Datensatz löschen möchten, legen Sie jedes Feld durch Aufrufen der [**msirecordcleardata**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) -Funktion auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="9076a-109">To clear data from a record, set each field to null by calling the [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) function.</span></span>

<span data-ttu-id="9076a-110">Die folgenden Funktionen füllen bestimmte Felder der Datensätze aus:</span><span class="sxs-lookup"><span data-stu-id="9076a-110">The following functions fill specified fields of records:</span></span>

-   <span data-ttu-id="9076a-111">Um einen Datensatz auf eine ganze Zahl festzulegen, müssen Sie die [**msirecordsetinteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9076a-111">To set a record to an integer, call the [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) function.</span></span>
-   <span data-ttu-id="9076a-112">Um einen Datensatz auf eine Zeichenfolge festzulegen, müssen Sie die [**msirecordsetstring**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9076a-112">To set a record to a string, call the [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) function.</span></span>
-   <span data-ttu-id="9076a-113">Um eine vollständige Datei in ein Datenstrom Feld einzufügen, müssen Sie die [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9076a-113">To insert an entire file into a stream field, call the [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) function.</span></span>

<span data-ttu-id="9076a-114">Die folgenden Funktionen lesen Werte aus angegebenen Feldern von Datensätzen:</span><span class="sxs-lookup"><span data-stu-id="9076a-114">The following functions read values from specified fields of records:</span></span>

-   <span data-ttu-id="9076a-115">Um einen ganzzahligen Wert aus einem Feld zu lesen, müssen Sie die [**msirecordgetinteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9076a-115">To read an integer value from a field, call the [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) function.</span></span>
-   <span data-ttu-id="9076a-116">Um einen Zeichen folgen Wert abzurufen, rufen Sie die [**msirecordgetstring**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9076a-116">To retrieve a string value, call the [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) function.</span></span>
-   <span data-ttu-id="9076a-117">Um einen Stream abzurufen, rufen Sie die [**msirecordlesstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9076a-117">To obtain a stream, call the [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) function.</span></span>
-   <span data-ttu-id="9076a-118">Um zu ermitteln, ob ein bestimmtes Feld eines Datensatzes Null ist, müssen Sie die [**msirecordisnull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9076a-118">To determine if a particular field of a record is null, call the [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) function.</span></span>

<span data-ttu-id="9076a-119">Die folgenden Funktionen sind Informationsdaten Satz Funktionen:</span><span class="sxs-lookup"><span data-stu-id="9076a-119">The following functions are informational record functions:</span></span>

-   <span data-ttu-id="9076a-120">Um die Anzahl von Feldern zu erhalten, die ein Datensatz enthält, nennen Sie die [**msirecordgetfieldcount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9076a-120">To get the number of fields a record contains, call the [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) function.</span></span>
-   <span data-ttu-id="9076a-121">Um die Größe eines Felds abzurufen, nennen Sie die [**msirecorddatasize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9076a-121">To get the size of a field, call the [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) function.</span></span> <span data-ttu-id="9076a-122">Der Rückgabewert von " **msirecorddatasize** " ist für den Feldtyp sensibel.</span><span class="sxs-lookup"><span data-stu-id="9076a-122">The return value of **MsiRecordDataSize** is sensitive to the field type.</span></span>

 

 



