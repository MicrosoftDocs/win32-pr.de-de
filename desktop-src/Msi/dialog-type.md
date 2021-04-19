---
description: Der Parametertyp des semantischen Typs ist einer der Schlüssel Format Typen. Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten Dialog Feld Tabelle.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Dialogtyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373137"
---
# <a name="dialog-type"></a><span data-ttu-id="a2b63-104">Dialogtyp</span><span class="sxs-lookup"><span data-stu-id="a2b63-104">Dialog Type</span></span>

<span data-ttu-id="a2b63-105">Der Parametertyp des [semantischen Typs](semantic-types.md) ist einer der [Schlüssel Format Typen](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="a2b63-105">The Dialog Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="a2b63-106">Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten [Dialog Feld Tabelle](dialog-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a2b63-106">This type consists of a foreign key into the [Dialog table](dialog-table.md) provided by the user.</span></span>

<span data-ttu-id="a2b63-107">Das Merge-Tool muss einen gültigen Windows Installer [Bezeichner](identifier.md) für Elemente dieses Typs ersetzen.</span><span class="sxs-lookup"><span data-stu-id="a2b63-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="a2b63-108">Mergemod.dll erzwingt diese Einschränkung nicht, und es liegt an dem Merge-Tool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel in der Dialog Tabelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a2b63-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Dialog table.</span></span>

<span data-ttu-id="a2b63-109">NULL ist ein gültiger Wert für diesen Typ, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="a2b63-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="a2b63-110">Der Dialog Typ kann mit den folgenden Arten von ContextData verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2b63-110">The Dialog type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="a2b63-111">**Dialognext ContextData**</span><span class="sxs-lookup"><span data-stu-id="a2b63-111">**DialogNext ContextData**</span></span>

<span data-ttu-id="a2b63-112">Ein konfigurierbares Mergemodul kann diesen Typ verwenden, damit der Benutzer einen Fremdschlüssel in der Dialog Tabelle bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="a2b63-112">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="a2b63-113">Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen des konfigurierbaren Elements in die Spalte "Name" eingeben, "1" in die Spalte "Format" eingeben, "Dialog" in die Spalte "Typ" eingeben und "dialognext" in die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" eingeben.</span><span class="sxs-lookup"><span data-stu-id="a2b63-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogNext" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="a2b63-114">**Dialogprev ContextData**</span><span class="sxs-lookup"><span data-stu-id="a2b63-114">**DialogPrev ContextData**</span></span>

<span data-ttu-id="a2b63-115">Ein konfigurierbares Mergemodul kann diesen Typ verwenden, damit der Benutzer einen Fremdschlüssel in der Dialog Tabelle bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="a2b63-115">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="a2b63-116">Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modul Autoren den Namen des konfigurierbaren Elements in die Spalte "Name" eingeben, "1" in die Spalte "Format" eingeben, "Dialog" in die Spalte "Typ" eingeben und "dialogprev" in die Spalte "ContextData" der Tabelle "ModuleConfiguration" eingeben.</span><span class="sxs-lookup"><span data-stu-id="a2b63-116">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogPrev" into the ContextData column of the ModuleConfiguration table.</span></span>

 

 



