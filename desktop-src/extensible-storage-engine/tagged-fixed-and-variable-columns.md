---
description: 'Weitere Informationen finden Sie unter: markierte, fixierte und Variablen Spalten.'
title: Markierte, fixierte und Variablen Spalten
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484870"
---
# <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="7ad3f-103">Markierte, fixierte und Variablen Spalten</span><span class="sxs-lookup"><span data-stu-id="7ad3f-103">Tagged, Fixed and Variable Columns</span></span>


<span data-ttu-id="7ad3f-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7ad3f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="7ad3f-105">Markierte, fixierte und Variablen Spalten</span><span class="sxs-lookup"><span data-stu-id="7ad3f-105">Tagged, Fixed and Variable Columns</span></span>

<span data-ttu-id="7ad3f-106">Die Spalten "markiert", "Fixed" und "Variable Länge" sind die von ESE unterstützten primären Spaltentypen.</span><span class="sxs-lookup"><span data-stu-id="7ad3f-106">Tagged, fixed, and variable-length columns are the primary column types supported by ESE.</span></span> <span data-ttu-id="7ad3f-107">Markierte Spalten sind nicht in einem Datensatz vorhanden, es sei denn, die Daten werden in der Spalte gespeichert und können eine fest oder eine Variable Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7ad3f-107">Tagged columns are not present in a record unless data is stored in the column, and may be fixed or variable length.</span></span> <span data-ttu-id="7ad3f-108">Markierte Spalten können auch mehrere Werte in einem einzelnen Datensatz enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ad3f-108">Tagged columns can also contain more than one value in a single record.</span></span> <span data-ttu-id="7ad3f-109">Bei Fixed-Spalten wird die gleiche Menge an Speicherplatz in jeder Zeile benötigt, und es ist ein Bit erforderlich, um den NULL-Wert darzustellen.</span><span class="sxs-lookup"><span data-stu-id="7ad3f-109">Fixed columns take the same amount of space in every row, and require 1 bit to represent the NULL value.</span></span> <span data-ttu-id="7ad3f-110">Spalten variabler Länge erfordern 2 Bytes, um die Größe und den NULL-Wert darzustellen, und belegen in jedem Datensatz eine Variable Menge an Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="7ad3f-110">Variable length columns require 2 bytes to represent the size and NULL value, and occupy a variable amount of space in each record.</span></span> <span data-ttu-id="7ad3f-111">Weitere Informationen zu den markierten und fixierten Spalten finden Sie in der Jet_bitColumnTagged-und Jet_bitColumnFixed-Option im **grbit** -Member [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur, die im Befehl [jetaddcolumn](./jetaddcolumn-function.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7ad3f-111">For more information on the tagged and fixed columns, see the Jet_bitColumnTagged, and Jet_bitColumnFixed option in the **grbit** member of [JET_COLUMNDEF](./jet-columndef-structure.md) structure used in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="7ad3f-112">Spalten variabler Länge werden durch den Spaltentyp bestimmt, der im *coltionparameter* im Befehl [jetaddcolumn](./jetaddcolumn-function.md)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7ad3f-112">Variable-length columns are determined by the column type that is set in the *coltyp* parameter in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="7ad3f-113">Abhängig davon, ob die Jet_bitColumnFixed-Option festgelegt ist, können die folgenden Spaltentypen fest oder eine Variable Länge aufweisen:</span><span class="sxs-lookup"><span data-stu-id="7ad3f-113">The following column types may be fixed or variable length depending on whether the Jet_bitColumnFixed option is set:</span></span>

  - <span data-ttu-id="7ad3f-114">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="7ad3f-114">JET_coltypBinary</span></span>

  - <span data-ttu-id="7ad3f-115">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="7ad3f-115">JET_coltypText</span></span>

  - <span data-ttu-id="7ad3f-116">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="7ad3f-116">JET_coltypLongBinary</span></span>

  - <span data-ttu-id="7ad3f-117">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="7ad3f-117">JET_coltypLongText</span></span>

<span data-ttu-id="7ad3f-118">Im Allgemeinen werden die Daten im Datensatz zunächst mit dem festgelegten Bereich, dem Variablen Bereich Next und dem zuletzt gespeicherten markierten Bereich gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7ad3f-118">In general, data in the record is stored with the fixed range first, the variable range next, and the tagged range stored last.</span></span> <span data-ttu-id="7ad3f-119">Das folgende Diagramm zeigt, wie die Datensätze in der-Tabelle gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7ad3f-119">The following diagram shows how the records are stored in the table.</span></span> <span data-ttu-id="7ad3f-120">Wie im Diagramm gezeigt, kann der markierte Bereich Spalten mit mehreren Werten enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ad3f-120">As shown in the diagram, the tagged range may contain columns with multiple values.</span></span>

<span data-ttu-id="7ad3f-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="7ad3f-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
