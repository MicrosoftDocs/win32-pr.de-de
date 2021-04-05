---
description: Der formatierte Typ des semantischen Typs ist einer der Text Format Typen.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Formatierter Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041946"
---
# <a name="formatted-type"></a><span data-ttu-id="8b6ad-103">Formatierter Typ</span><span class="sxs-lookup"><span data-stu-id="8b6ad-103">Formatted Type</span></span>

<span data-ttu-id="8b6ad-104">Der formatierte Typ des [semantischen Typs](semantic-types.md) ist einer der [Text Format Typen](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="8b6ad-104">The Formatted Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="8b6ad-105">Dieser Typ besteht aus einer beliebigen Text Zeichenfolge beliebiger Länge, die vom Benutzer bereitgestellt wird, und im Windows Installer formatierten Textformat.</span><span class="sxs-lookup"><span data-stu-id="8b6ad-105">This type consists of an arbitrary text string of any length provided by the user and in the Windows Installer formatted text format.</span></span> <span data-ttu-id="8b6ad-106">Weitere Informationen finden Sie unter [formatiert](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="8b6ad-106">For details, see [Formatted](formatted.md).</span></span> <span data-ttu-id="8b6ad-107">Das Merge-Tool ersetzt diese Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="8b6ad-107">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="8b6ad-108">Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen der Text Zeichenfolge in die Spalte "Name" eingeben, "0" in die Spalte "Format" eingeben, "formatiert" in die Spalte "Type" eingeben und die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" leer lassen. Die Zeichenfolge kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="8b6ad-108">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Formatted" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="8b6ad-109">Weitere Informationen finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="8b6ad-109">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="8b6ad-110">NULL ist ein gültiger Wert für die Text Zeichenfolge, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der Tabelle ModuleConfiguration enthalten.</span><span class="sxs-lookup"><span data-stu-id="8b6ad-110">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



