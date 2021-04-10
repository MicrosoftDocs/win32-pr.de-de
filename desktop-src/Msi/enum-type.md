---
description: Der Enumerationstyp des semantischen Typs ist einer der Text Format Typen.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Aufzählungs Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc582a7f96d8fc91aad66387f579f05f9255346f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959393"
---
# <a name="enum-type"></a><span data-ttu-id="63ae5-103">Aufzählungs Typen</span><span class="sxs-lookup"><span data-stu-id="63ae5-103">Enum Type</span></span>

<span data-ttu-id="63ae5-104">Der Enumerationstyp des [semantischen Typs](semantic-types.md) ist einer der [Text Format Typen](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="63ae5-104">The Enum Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="63ae5-105">Dieser Typ besteht aus einer vom Benutzer ausgewählten Text Zeichenfolge aus einem Satz von Optionen.</span><span class="sxs-lookup"><span data-stu-id="63ae5-105">This type consists of a text string chosen by the user from a set of choices.</span></span> <span data-ttu-id="63ae5-106">Das Merge-Tool ersetzt die ausgewählte ausgewählte Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="63ae5-106">The merge tool substitutes the selected string selected into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="63ae5-107">Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen der Text Zeichenfolge in die Spalte "Name" eingeben, "0" in die Spalte "Format" eingeben, "Enum" in die Spalte "Type" eingeben und die Liste der möglichen Zeichen folgen in der Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" eingeben.</span><span class="sxs-lookup"><span data-stu-id="63ae5-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Enum" into the Type column, and enter the list of possible strings in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="63ae5-108">Die Liste der möglichen Zeichen folgen muss als Liste von Zeichen folgen angegeben werden, die durch Semikolons getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="63ae5-108">The list of possible strings must be provided as a list of strings deliminated by semicolons.</span></span> <span data-ttu-id="63ae5-109">Jede Auswahl muss das Format "Name = Wert" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="63ae5-109">Each choice must be in the form "Name=Value".</span></span> <span data-ttu-id="63ae5-110">Dem Wert kann ein literales Semikolon hinzugefügt werden, indem dem Semikolon ein umgekehrter Schrägstrich vorangestellt wird.</span><span class="sxs-lookup"><span data-stu-id="63ae5-110">A literal semicolon can be added to the value by prefixing the semicolon with a backslash character.</span></span> <span data-ttu-id="63ae5-111">NULL ist ein gültiger Wert, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der Tabelle ModuleConfiguration enthalten.</span><span class="sxs-lookup"><span data-stu-id="63ae5-111">Null is a valid value unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



