---
description: Der beliebige ganzzahlige Typ des semantischen Typs ist einer der ganzzahligen Format Typen.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Beliebiger Integer-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131493"
---
# <a name="arbitrary-integer-type"></a><span data-ttu-id="48066-103">Beliebiger Integer-Typ</span><span class="sxs-lookup"><span data-stu-id="48066-103">Arbitrary Integer Type</span></span>

<span data-ttu-id="48066-104">Der beliebige ganzzahlige Typ des [semantischen Typs](semantic-types.md) ist einer der [ganzzahligen Format Typen](integer-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="48066-104">The Arbitrary Integer Type of [semantic type](semantic-types.md) is one of the [Integer Format Types](integer-format-types.md).</span></span> <span data-ttu-id="48066-105">Diese Art von konfigurier barem Element ist eine vom Benutzer bereitgestellte Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="48066-105">This type of configurable item is an integer provided by the user.</span></span> <span data-ttu-id="48066-106">Das Merge-Tool ersetzt diese Ganzzahl in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="48066-106">The merge tool substitutes this integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="48066-107">Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen der Text Zeichenfolge in die Spalte "Name" eingeben, "2" in die Spalte "Format" eingeben und die Spalten Type und ContextData der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)leer lassen.</span><span class="sxs-lookup"><span data-stu-id="48066-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "2" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="48066-108">Die Spalten "Type" und "ContextData" sind reserviert und müssen NULL sein.</span><span class="sxs-lookup"><span data-stu-id="48066-108">The Type and ContextData columns are reserved and must be null.</span></span>

 

 



