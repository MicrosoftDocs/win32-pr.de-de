---
description: ICEM06 prüft auf ungültige direkte Verweise auf Features durch das Modul.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865763"
---
# <a name="icem06"></a><span data-ttu-id="a2fe9-103">ICEM06</span><span class="sxs-lookup"><span data-stu-id="a2fe9-103">ICEM06</span></span>

<span data-ttu-id="a2fe9-104">ICEM06 prüft auf ungültige direkte Verweise auf Features durch das Modul.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-104">ICEM06 checks for invalid direct references to features by the module.</span></span>

<span data-ttu-id="a2fe9-105">Das Mergemodul "ICES" wird in der Datei "Merge Module. Cub" mit dem Namen "Mergemod. Cub" und nicht in der CUB-Datei gespeichert, die die für die Paketüberprüfung verwendeten Verb</span><span class="sxs-lookup"><span data-stu-id="a2fe9-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="a2fe9-106">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="a2fe9-106">Result</span></span>

<span data-ttu-id="a2fe9-107">ICEM06 gibt einen Fehler aus, wenn die Modul Datenbank direkte Verweise auf eine Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-107">ICEM06 posts an error when the module database contains direct references to a feature.</span></span> <span data-ttu-id="a2fe9-108">Funktions Informationen müssen vom Benutzer des Moduls bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-108">Feature information must be provided by the user of the module.</span></span>

## <a name="example"></a><span data-ttu-id="a2fe9-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a2fe9-109">Example</span></span>

<span data-ttu-id="a2fe9-110">ICEM06 gibt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen aus.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-110">ICEM06 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

<span data-ttu-id="a2fe9-111">Verknüpfungs [Tabelle](shortcut-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="a2fe9-111">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="a2fe9-112">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="a2fe9-112">Shortcut</span></span>          | <span data-ttu-id="a2fe9-113">Ziel</span><span class="sxs-lookup"><span data-stu-id="a2fe9-113">Target</span></span>                                 |
|-------------------|----------------------------------------|
| <span data-ttu-id="a2fe9-114">Shortcut1. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="a2fe9-114">Shortcut1.*GUID1*</span></span> | <span data-ttu-id="a2fe9-115">cmd.exe</span><span class="sxs-lookup"><span data-stu-id="a2fe9-115">cmd.exe</span></span>                                |
| <span data-ttu-id="a2fe9-116">Shortcut2. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="a2fe9-116">Shortcut2.*GUID1*</span></span> | <span data-ttu-id="a2fe9-117">\[MyProp\]</span><span class="sxs-lookup"><span data-stu-id="a2fe9-117">\[MyProp\]</span></span>                             |
| <span data-ttu-id="a2fe9-118">Shortcut3. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="a2fe9-118">Shortcut3.*GUID1*</span></span> | {00000000-0000-0000-0000-000000000000} |



 

<span data-ttu-id="a2fe9-119">[Klassen Tabelle](class-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="a2fe9-119">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="a2fe9-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="a2fe9-120">CLSID</span></span>   | <span data-ttu-id="a2fe9-121">Kontext</span><span class="sxs-lookup"><span data-stu-id="a2fe9-121">Context</span></span>       | <span data-ttu-id="a2fe9-122">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="a2fe9-122">Component\_</span></span> | <span data-ttu-id="a2fe9-123">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="a2fe9-123">Feature\_</span></span>                              |
|---------|---------------|-------------|----------------------------------------|
| <span data-ttu-id="a2fe9-124">*GUID1*</span><span class="sxs-lookup"><span data-stu-id="a2fe9-124">*GUID1*</span></span> | <span data-ttu-id="a2fe9-125">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="a2fe9-125">LocalServer32</span></span> | <span data-ttu-id="a2fe9-126">Component1</span><span class="sxs-lookup"><span data-stu-id="a2fe9-126">Component1</span></span>  | {00000000-0000-0000-0000-000000000000} |
| <span data-ttu-id="a2fe9-127">*GUID2*</span><span class="sxs-lookup"><span data-stu-id="a2fe9-127">*GUID2*</span></span> | <span data-ttu-id="a2fe9-128">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="a2fe9-128">LocalServer32</span></span> | <span data-ttu-id="a2fe9-129">Component2</span><span class="sxs-lookup"><span data-stu-id="a2fe9-129">Component2</span></span>  | <span data-ttu-id="a2fe9-130">Myfeature</span><span class="sxs-lookup"><span data-stu-id="a2fe9-130">MyFeature</span></span>                              |



 

<span data-ttu-id="a2fe9-131">ICEM06 meldet den ersten Fehler, da der erste Datensatz in der Verknüpfungs Tabelle über einen Eintrag im Zielfeld verfügt, der keine Eigenschaft oder NULL-GUID ist.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-131">ICEM06 reports the first error because the first record in the Shortcut table has an entry in the Target field that is not a property or a null GUID.</span></span> <span data-ttu-id="a2fe9-132">Ein Modul kann nicht direkt auf eine Funktion verweisen.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-132">A module cannot reference a feature directly.</span></span> <span data-ttu-id="a2fe9-133">Funktions Informationen müssen vom Benutzer des Moduls bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-133">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="a2fe9-134">Um diesen Fehler zu beheben, müssen Verweise auf eine Funktion durch eine NULL-GUID ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-134">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

<span data-ttu-id="a2fe9-135">ICEM06 meldet den zweiten Fehler, da der zweite Datensatz in der Klassen Tabelle über einen Eintrag im Funktionsfeld verfügt, der keine NULL-GUID ist.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-135">ICEM06 reports the second error because the second record in the Class table has an entry in the Feature field that is not a null GUID.</span></span> <span data-ttu-id="a2fe9-136">Ein Modul kann nicht direkt auf eine Funktion verweisen.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-136">A module cannot reference a feature directly.</span></span> <span data-ttu-id="a2fe9-137">Funktions Informationen müssen vom Benutzer des Moduls bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-137">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="a2fe9-138">Um diesen Fehler zu beheben, müssen Verweise auf eine Funktion durch eine NULL-GUID ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a2fe9-138">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2fe9-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a2fe9-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2fe9-140">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="a2fe9-140">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



