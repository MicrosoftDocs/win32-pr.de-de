---
description: Der Symboltyp des semantischen Typs ist einer der Schlüssel Format Typen. Dieser Typ besteht aus einem Schlüssel in der vom Benutzer bereitgestellten Symboltabelle.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Symboltyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7c90de925ff34977e7ff192dffe0b8614e5734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345774"
---
# <a name="icon-type"></a><span data-ttu-id="7fe76-104">Symboltyp</span><span class="sxs-lookup"><span data-stu-id="7fe76-104">Icon Type</span></span>

<span data-ttu-id="7fe76-105">Der Symboltyp des [semantischen Typs](semantic-types.md) ist einer der [Schlüssel Format Typen](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="7fe76-105">The Icon Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="7fe76-106">Dieser Typ besteht aus einem Schlüssel in der vom Benutzer bereitgestellten [Symboltabelle](icon-table.md) .</span><span class="sxs-lookup"><span data-stu-id="7fe76-106">This type consists of a key into the [Icon table](icon-table.md) provided by the user.</span></span>

<span data-ttu-id="7fe76-107">Das Merge-Tool muss einen gültigen Windows Installer [Bezeichner](identifier.md) für Elemente dieses Typs ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7fe76-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="7fe76-108">Mergemod.dll erzwingt diese Einschränkung nicht, und es liegt an dem Merge-Tool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel für die Symboltabelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7fe76-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Icon table.</span></span>

<span data-ttu-id="7fe76-109">NULL ist ein gültiger Wert für diesen Typ, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="7fe76-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="7fe76-110">Der binäre Typ kann mit den folgenden Arten von ContextData verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fe76-110">The Binary type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="7fe76-111">**Shortcuticon ContextData**</span><span class="sxs-lookup"><span data-stu-id="7fe76-111">**ShortcutIcon ContextData**</span></span>

<span data-ttu-id="7fe76-112">Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, einen Fremdschlüssel für eine Zeile in der [Symboltabelle](icon-table.md) bereitzustellen, die ein Bild enthält, das für die Verwendung als Verknüpfungs Symbol geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="7fe76-112">A configurable merge module may use this type to enable the user to provide a foreign key to a row in the [Icon Table](icon-table.md) that contains an image suitable for use as a shortcut icon.</span></span> <span data-ttu-id="7fe76-113">Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen des konfigurierbaren Elements in die Spalte "Name" eingeben, "1" in die Spalte "Format" eingeben, "Symbol" in die Spalte "Type" eingeben und "shorcuticon" in die Spalte "ContextData" der Tabelle "ModuleConfiguration" eingeben.</span><span class="sxs-lookup"><span data-stu-id="7fe76-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Icon" into the Type column, and enter "ShorcutIcon" into the ContextData column of the ModuleConfiguration table.</span></span> <span data-ttu-id="7fe76-114">Dieser Typ ist nicht für die Verwendung in einer Benutzeroberflächen Tabelle geeignet.</span><span class="sxs-lookup"><span data-stu-id="7fe76-114">This type is not appropriate for use in a user interface table.</span></span> <span data-ttu-id="7fe76-115">Informationen zum Ändern eines Schlüssels für die Symboltabelle in diesen Tabellen finden Sie unter "Symbol" ContextData "unter [Binary Type](binary-type.md).</span><span class="sxs-lookup"><span data-stu-id="7fe76-115">To modify a key to the Icon table in these tables see Icon ContextData under [Binary Type](binary-type.md).</span></span>

 

 



