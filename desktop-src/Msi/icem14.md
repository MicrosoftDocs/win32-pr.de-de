---
description: ICEM14 überprüft die Value-Spalte der ModuleSubstitution-Tabelle.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130448"
---
# <a name="icem14"></a><span data-ttu-id="60e09-103">ICEM14</span><span class="sxs-lookup"><span data-stu-id="60e09-103">ICEM14</span></span>

<span data-ttu-id="60e09-104">ICEM14 überprüft die Value-Spalte der [ModuleSubstitution-Tabelle](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="60e09-104">ICEM14 validates the Value Column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="60e09-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="60e09-105">Result</span></span>

<span data-ttu-id="60e09-106">ICEM14 gibt die folgenden Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="60e09-106">ICEM14 posts the following errors.</span></span>



| <span data-ttu-id="60e09-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="60e09-107">Error</span></span>                                                                                                                                                         | <span data-ttu-id="60e09-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60e09-108">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e09-109">Die Ersetzungs Zeichenfolge in der ModuleSubstitution. Value-Spalte in Zeile \[ 1 \] . \[ 2 \] . \[ 3 wurde \] in der Tabelle "ModuleConfiguration" nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="60e09-109">The replacement string in ModuleSubstitution.Value column in row \[1\].\[2\].\[3\] is not found in ModuleConfiguration table.</span></span>                                 | <span data-ttu-id="60e09-110">\[1 \] . \[ 2 \] . \[ 3 \] bezieht sich auf einen *Table. Row. Column* -Primärschlüssel für eine Zeile in der ModuleSubstitution-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="60e09-110">\[1\].\[2\].\[3\] refers to a *table.row.column* primary key for a row in the ModuleSubstitution table.</span></span> <span data-ttu-id="60e09-111">Die Formatierungs Vorlage im Wertfeld dieser Zeile entspricht nicht einer Zeile mit konfigurierbaren Attributen in der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="60e09-111">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                            |
| <span data-ttu-id="60e09-112">In der Tabelle ModuleSubstitution in Zeile \[ 1 \] . \[ 2 \] . \[ 3 \] , in der Tabelle "% s" ist ein konfigurierbares Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="60e09-112">In ModuleSubstitution table in row \[1\].\[2\].\[3\], a configurable item is indicated in the table '%s'.</span></span> <span data-ttu-id="60e09-113">Die '% s '-Tabelle darf keine konfigurierbaren Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="60e09-113">The table '%s' must not contain configurable items.</span></span> | <span data-ttu-id="60e09-114">Eine der folgenden Tabellen ist in der Tabellenspalte der Tabelle ModuleSubstitution aufgeführt: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [moduleausschluss](moduleexclusion-table.md)oder [ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="60e09-114">One of the following tables is listed in the Table column of the ModuleSubstitution table: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md), or [ModuleSignature](modulesignature-table.md).</span></span> <span data-ttu-id="60e09-115">Diese Tabellen können keine konfigurierbaren Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="60e09-115">These tables cannot contain configurable fields.</span></span> |
| <span data-ttu-id="60e09-116">In der Tabelle ModuleSubstitution in Zeile \[ 1 \] . \[ 2 \] . \[ 3 \] , eine leere Ersetzungs Zeichenfolge wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="60e09-116">In ModuleSubstitution table in row \[1\].\[2\].\[3\], an empty replacement string is specified.</span></span>                                                               | <span data-ttu-id="60e09-117">Die Formatierungs Vorlage im Wertfeld dieser Zeile entspricht nicht einer Zeile mit konfigurierbaren Attributen in der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="60e09-117">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="60e09-118">ICEM14 gibt die folgende Warnung aus.</span><span class="sxs-lookup"><span data-stu-id="60e09-118">ICEM14 posts the following warning.</span></span>



| <span data-ttu-id="60e09-119">Warnung</span><span class="sxs-lookup"><span data-stu-id="60e09-119">Warning</span></span>                                                                  | <span data-ttu-id="60e09-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60e09-120">Meaning</span></span>                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="60e09-121">Die ModuleSubstitution-Tabelle ist vorhanden, aber die ModuleConfiguration-Tabelle fehlt.</span><span class="sxs-lookup"><span data-stu-id="60e09-121">ModuleSubstitution table exists but ModuleConfiguration table is missing</span></span> | <span data-ttu-id="60e09-122">Die ModuleConfiguration-Tabelle ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="60e09-122">The ModuleConfiguration table is absent.</span></span> |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="60e09-123">Während der Ausführung verwendete Tabelle</span><span class="sxs-lookup"><span data-stu-id="60e09-123">Table Used During Execution</span></span>

[<span data-ttu-id="60e09-124">ModuleSubstitution-Tabelle</span><span class="sxs-lookup"><span data-stu-id="60e09-124">ModuleSubstitution table</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="60e09-125">ModuleConfiguration-Tabelle</span><span class="sxs-lookup"><span data-stu-id="60e09-125">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)

## <a name="related-topics"></a><span data-ttu-id="60e09-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60e09-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60e09-127">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="60e09-127">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



