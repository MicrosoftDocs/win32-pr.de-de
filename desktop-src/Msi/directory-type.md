---
description: Der Verzeichnistyp des semantischen Typs ist einer der Schlüssel Format Typen, der aus einem Fremdschlüssel in der vom Benutzer bereitgestellten Verzeichnis Tabelle besteht.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Verzeichnistyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866336"
---
# <a name="directory-type"></a><span data-ttu-id="19670-103">Verzeichnistyp</span><span class="sxs-lookup"><span data-stu-id="19670-103">Directory Type</span></span>

<span data-ttu-id="19670-104">Der Verzeichnistyp des [semantischen Typs](semantic-types.md) ist einer der [Schlüssel Format Typen](key-format-types.md), der aus einem Fremdschlüssel in der vom Benutzer bereitgestellten [Verzeichnis Tabelle](directory-table.md) besteht.</span><span class="sxs-lookup"><span data-stu-id="19670-104">The Directory Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md), which consists of a foreign key into the [Directory table](directory-table.md) provided by the user.</span></span>

<span data-ttu-id="19670-105">Das Merge-Tool muss einen gültigen Windows Installer [Bezeichner](identifier.md) für Elemente dieses Typs ersetzen.</span><span class="sxs-lookup"><span data-stu-id="19670-105">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="19670-106">Mergemod.dll erzwingt diese Einschränkung nicht, und es liegt an dem Merge-Tool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel für die Verzeichnis Tabelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="19670-106">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Directory table.</span></span>

<span data-ttu-id="19670-107">Ein konfigurierbares Element des Verzeichnis Typs sollte nur das Zielverzeichnis der Installation ändern und das Quell Abbild nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="19670-107">A configurable item of the Directory type should only modify the destination directory of the installation and not modify the source image.</span></span> <span data-ttu-id="19670-108">Ein konfigurierbares Element dieses Typs sollte daher nur Fremdschlüssel in der Verzeichnis Tabelle ändern und die Verzeichnis Tabelle nicht direkt ändern.</span><span class="sxs-lookup"><span data-stu-id="19670-108">A configurable item of this type should therefore only modify foreign keys to the Directory table and not modify the Directory table directly.</span></span>

<span data-ttu-id="19670-109">Da die Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md) nicht auf NULL festgelegt werden kann, ist NULL ein ungültiger Wert für ein konfigurierbares Element dieses Typs, auch wenn die msmconfigitemnonable-Eigenschaft in der Spalte Attribute nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="19670-109">Because the Directory\_ column of the [Component table](component-table.md) is non-nullable, null is an invalid value for a configurable item of this type even if the msmConfigItemNonNullable is not set in the Attributes column.</span></span>

<span data-ttu-id="19670-110">Der Verzeichnistyp kann mit zwei Arten von ContextData verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19670-110">The Directory type may be used with two kinds of ContextData.</span></span>

<span data-ttu-id="19670-111">**Isolationdirectory ContextData**</span><span class="sxs-lookup"><span data-stu-id="19670-111">**IsolationDirectory ContextData**</span></span>

<span data-ttu-id="19670-112">Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, ein Zielverzeichnis für Dateien im Modul bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="19670-112">A configurable merge module may use this type to enable the user to provide a destination directory for files in the module.</span></span> <span data-ttu-id="19670-113">Das Merge-Tool ersetzt den Bezeichner des Verzeichnisses in den Vorlagen in der Value-Spalte der [ModuleSubstitution-Tabelle](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="19670-113">The merge tool substitutes the directory's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="19670-114">Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen des Verzeichnisses in die Spalte Name ein, geben Sie "1" in die Spalte "Format" ein, geben Sie "Directory" in die Spalte "Type" ein, und geben Sie "isolationdirectory" in die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" ein.</span><span class="sxs-lookup"><span data-stu-id="19670-114">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "IsolationDirectory" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="19670-115">**ShortcutLocation ContextData**</span><span class="sxs-lookup"><span data-stu-id="19670-115">**ShortcutLocation ContextData**</span></span>

<span data-ttu-id="19670-116">Ein konfigurierbares Mergemodul kann diesen Typ verwenden, um dem Benutzer zu ermöglichen, ein Zielverzeichnis für Verknüpfungen im Modul bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="19670-116">A configurable merge module may use this type to enable the user to provide a destination directory for shortcuts in the module.</span></span> <span data-ttu-id="19670-117">Das Merge-Tool ersetzt den Bezeichner der Verknüpfung in den Vorlagen in der Value-Spalte der [ModuleSubstitution-Tabelle](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="19670-117">The merge tool substitutes the shortcut's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="19670-118">Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen des Verzeichnisses in die Spalte Name ein, geben Sie "1" in die Spalte "Format" ein, geben Sie "Directory" in die Spalte "Type" ein, und geben Sie "ShortcutLocation" in die Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" ein.</span><span class="sxs-lookup"><span data-stu-id="19670-118">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "ShortcutLocation" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



