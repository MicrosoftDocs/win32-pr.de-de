---
description: Bezeichner geben die Namen der Spalten (manchmal als Eigenschaften bezeichnet), Kataloge und Aliase an.
ms.assetid: 799afe2c-9217-4006-a4a3-644e5393993c
title: Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df79bd0d70564ea3e87ff4821a1cb59e3d0a5eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128540"
---
# <a name="identifiers"></a><span data-ttu-id="80c38-103">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="80c38-103">Identifiers</span></span>

<span data-ttu-id="80c38-104">Bezeichner geben die Namen der Spalten (manchmal als Eigenschaften bezeichnet), Kataloge und Aliase an.</span><span class="sxs-lookup"><span data-stu-id="80c38-104">Identifiers specify the names of columns (sometimes referred to as properties), catalogs, and aliases.</span></span> <span data-ttu-id="80c38-105">System. ItemName und System. DateCreated sind z. b. die Bezeichner von zwei System definierten Eigenschafts Spalten.</span><span class="sxs-lookup"><span data-stu-id="80c38-105">For example, System.ItemName and System.DateCreated are the identifiers of two system-defined property columns.</span></span> <span data-ttu-id="80c38-106">Literale geben dagegen Zeichen folgen Werte und numerische Werte an.</span><span class="sxs-lookup"><span data-stu-id="80c38-106">Literals, by contrast, specify string and numeric values.</span></span>


<span data-ttu-id="80c38-107">Sie können Bezeichner erstellen, die bis zu 128 Zeichen lang sind, und in einem von zwei Typen, die von den im Bezeichnernamen verwendeten Zeichen unterschieden werden:</span><span class="sxs-lookup"><span data-stu-id="80c38-107">You can create identifiers that are up to 128 characters long, and in one of two types, distinguished by the characters used in the identifier name:</span></span>

-   <span data-ttu-id="80c38-108">**Reguläre** Bezeichner enthalten nur die Zeichen a-z, a-z, 0-9, Unterstrich ( \_ ) und Punkt (.) und beginnen mit einem Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="80c38-108">**Regular identifiers** contain only the characters A-Z, a-z, 0-9, underscore (\_), and dot (.), and they begin with a letter.</span></span> <span data-ttu-id="80c38-109">Sie müssen reguläre Bezeichner nicht in doppelte Anführungszeichen ("") einschließen.</span><span class="sxs-lookup"><span data-stu-id="80c38-109">You do not need to enclose regular identifiers in double quotation marks (" ").</span></span>
-   <span data-ttu-id="80c38-110">**Begrenzungs** Bezeichner können ein beliebiges gültiges Unicode-Zeichen enthalten und müssen in doppelte Anführungszeichen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="80c38-110">**Delimited identifiers** can contain any valid Unicode character and must be enclosed in double quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="80c38-111">In den Freitext-und enthält-Klauseln können Sie das Sternchen ( \* ) als speziellen Spalten Bezeichner verwenden, wenn Sie angeben möchten, dass die Windows-Suche alle indizierten Eigenschaften in der Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="80c38-111">In FREETEXT and CONTAINS clauses, you can use the asterisk (\*) as a special column identifier when you want to specify that Windows Search includes all of the indexed properties in the query.</span></span> <span data-ttu-id="80c38-112">Obwohl es sich nicht um einen regulären Bezeichner handelt, sind keine doppelten Anführungszeichen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="80c38-112">Although it is not a regular identifier, it does not require double quotation marks.</span></span>

 

 

 



