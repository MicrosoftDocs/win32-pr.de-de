---
description: Der beliebige Texttyp des semantischen Typs ist einer der Text Format Typen.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Beliebiger Texttyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348343"
---
# <a name="arbitrary-text-type"></a><span data-ttu-id="b25a8-103">Beliebiger Texttyp</span><span class="sxs-lookup"><span data-stu-id="b25a8-103">Arbitrary Text Type</span></span>

<span data-ttu-id="b25a8-104">Der beliebige Texttyp des [semantischen Typs](semantic-types.md) ist einer der [Text Format Typen](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="b25a8-104">The Arbitrary Text Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="b25a8-105">Dieser Typ besteht aus einer beliebigen Text Zeichenfolge mit jeder vom Benutzer bereitgestellten Länge.</span><span class="sxs-lookup"><span data-stu-id="b25a8-105">This type consists of an arbitrary text string of any length provided by the user.</span></span> <span data-ttu-id="b25a8-106">Das Merge-Tool ersetzt diese willkürliche Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b25a8-106">The merge tool substitutes this arbitrary string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="b25a8-107">Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen der Text Zeichenfolge in die Spalte "Name" eingeben, "0" in die Spalte "Format" eingeben und die Spalten Type und ContextData der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)leer lassen. Die beliebige Text Zeichenfolge kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="b25a8-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).The arbitrary text string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="b25a8-108">Weitere Informationen finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="b25a8-108">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="b25a8-109">NULL ist ein gültiger Wert für die Text Zeichenfolge, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der Tabelle ModuleConfiguration enthalten.</span><span class="sxs-lookup"><span data-stu-id="b25a8-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



