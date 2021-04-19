---
description: Der RTF-Typ des semantischen Typs ist einer der Text Format Typen.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: RTF-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81c708183596d794f20e38bf89c073472e3affb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358522"
---
# <a name="rtf-type"></a><span data-ttu-id="a5765-103">RTF-Typ</span><span class="sxs-lookup"><span data-stu-id="a5765-103">RTF Type</span></span>

<span data-ttu-id="a5765-104">Der RTF-Typ des [semantischen Typs](semantic-types.md) ist einer der [Text Format Typen](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="a5765-104">The RTF Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="a5765-105">Dieser Typ besteht aus einer beliebigen Text Zeichenfolge im Rich-Text-Format (RTF) jeder vom Benutzer bereitgestellten Länge.</span><span class="sxs-lookup"><span data-stu-id="a5765-105">This type consists of an arbitrary text string in the Rich Text Format (RTF) of any length provided by the user.</span></span> <span data-ttu-id="a5765-106">Das Merge-Tool ersetzt diese Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a5765-106">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="a5765-107">Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen der Text Zeichenfolge in die Spalte Name ein, geben Sie "0" in die Spalte "Format" ein, geben Sie "RTF" in die Typspalte ein, und lassen Sie die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" leer. Die Zeichenfolge kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="a5765-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "RTF" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="a5765-108">Weitere Informationen finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="a5765-108">See [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="a5765-109">NULL ist ein gültiger Wert für die Text Zeichenfolge, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der Tabelle ModuleConfiguration enthalten.</span><span class="sxs-lookup"><span data-stu-id="a5765-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



