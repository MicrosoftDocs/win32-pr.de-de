---
description: Der Bezeichnertyp des semantischen Typs ist einer der Text Format Typen.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Bezeichnertyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131481"
---
# <a name="identifier-type"></a><span data-ttu-id="1f2bc-103">Bezeichnertyp</span><span class="sxs-lookup"><span data-stu-id="1f2bc-103">Identifier Type</span></span>

<span data-ttu-id="1f2bc-104">Der Bezeichnertyp des [semantischen Typs](semantic-types.md) ist einer der [Text Format Typen](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="1f2bc-104">The Identifier Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="1f2bc-105">Dieser Typ besteht aus einer Text Zeichenfolge, die vom Benutzer im Format eines Windows Installer [Bezeichners](identifier.md)bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1f2bc-105">This type consists of an text string provided by the user in the format of a Windows Installer [Identifier](identifier.md).</span></span> <span data-ttu-id="1f2bc-106">Das Merge-Tool ersetzt diese Zeichenfolge in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1f2bc-106">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="1f2bc-107">Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen der Text Zeichenfolge in die Spalte "Name" eingeben, "0" in die Spalte "Format" eingeben, "Identifier" in die Spalte "Type" eingeben und die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" leer lassen. Die Zeichenfolge kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="1f2bc-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Identifier" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="1f2bc-108">Weitere Informationen finden Sie unter [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="1f2bc-108">See [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="1f2bc-109">NULL ist ein gültiger Wert für die Text Zeichenfolge, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der Tabelle ModuleConfiguration enthalten.</span><span class="sxs-lookup"><span data-stu-id="1f2bc-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



