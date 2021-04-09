---
description: Der &\# 0034; Bitfield&\# 0034; geben Sie ohne Kontext Anforderungen ein, dass der Benutzer eine ganze Zahl bereitstellt, deren Wert verwendet wird, um ein oder mehrere Bits in einem Bitfeld festzulegen. Dieser Text kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Beliebiger Bitfeldtyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6571b8585c94577927df8cfedaded802a67d125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131496"
---
# <a name="arbitrary-bitfield-type"></a><span data-ttu-id="7a103-104">Beliebiger Bitfeldtyp</span><span class="sxs-lookup"><span data-stu-id="7a103-104">Arbitrary Bitfield Type</span></span>

<span data-ttu-id="7a103-105">Der Bitfield-Typ ohne Kontext Anforderungen, dass der Benutzer eine ganze Zahl bereitstellt, mit deren Wert ein oder mehrere Bits in einem Bitfeld festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7a103-105">The "Bitfield" type with no context requests that the user provide an integer whose value is used to set one or more bits in a bitfield.</span></span> <span data-ttu-id="7a103-106">Dieser Text kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="7a103-106">This text may be in any language compatible with the code page of the database.</span></span>

<span data-ttu-id="7a103-107">Der beliebige Bitfeldtyp des [semantischen Typs](semantic-types.md) ist einer der Bitfield-Typen.</span><span class="sxs-lookup"><span data-stu-id="7a103-107">The Arbitrary Bitfield Type of [semantic type](semantic-types.md) is one of the Bitfield Types.</span></span> <span data-ttu-id="7a103-108">Dieser Typ besteht aus einer vom Benutzer ausgewählten Ganzzahl aus einem Satz von Optionen.</span><span class="sxs-lookup"><span data-stu-id="7a103-108">This type consists of an integer chosen by the user from a set of choices.</span></span> <span data-ttu-id="7a103-109">Das Merge-Tool ersetzt die ausgewählte Ganzzahl in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7a103-109">The merge tool substitutes the selected integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="7a103-110">Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen des Elements in die Spalte Name ein, geben Sie "3" in die Spalte Format ein, lassen Sie die Spalte Typ leer, und geben Sie die Liste möglicher ganzer Zahlen in der Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" ein.</span><span class="sxs-lookup"><span data-stu-id="7a103-110">To specify a configurable item of this type, module authors should enter the name of the item into the Name column, enter "3" into the Format column, leave the Type column blank, and enter the list of possible integers in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="7a103-111">Die Typspalte ist reserviert und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7a103-111">The Type column is reserved and must be null.</span></span> <span data-ttu-id="7a103-112">Der Eintrag in der ContextData-Spalte für alle Bitfield-Format Typen muss das Format aufweisen <mask> .<Name>=</span><span class="sxs-lookup"><span data-stu-id="7a103-112">The entry in the ContextData column for all Bitfield Format types must be in the form "<mask>;<Name>=</span></span><value><span data-ttu-id="7a103-113">;<Name>=</span><span class="sxs-lookup"><span data-stu-id="7a103-113">;<Name>=</span></span><value><span data-ttu-id="7a103-114">.... ", wobei <mask> ein ganzzahliger Wert ist, der die Bits von Interesse angibt, <Name> ist ein Lokalisier barer Anzeige Name für die Auswahl, und</span><span class="sxs-lookup"><span data-stu-id="7a103-114">....", where <mask> is an integer value indicating the bits of interest, <Name> is a localizable display name for the choice, and</span></span> <value> <span data-ttu-id="7a103-115">ist ein ganzzahliger ganzzahliger Wert.</span><span class="sxs-lookup"><span data-stu-id="7a103-115">is a decimal integer value.</span></span> <span data-ttu-id="7a103-116">Die Kontext Spalte verwendet das [spezielle cmsm-Format](cmsm-special-format.md) und für alle Bitfeld-Typen.</span><span class="sxs-lookup"><span data-stu-id="7a103-116">The context column is in use [CMSM Special Format](cmsm-special-format.md) and for all bitfield types.</span></span> <span data-ttu-id="7a103-117">Ein literales Zeichen "=" oder ";" kann im Feld eingegeben werden, <Name> indem es einem umgekehrten Schrägstrich ("") vorangestellt wird \\ .</span><span class="sxs-lookup"><span data-stu-id="7a103-117">A literal "=" or ";" character can be entered in the <Name> field by prefixing it with a backslash ('\\') character.</span></span>

 

 



