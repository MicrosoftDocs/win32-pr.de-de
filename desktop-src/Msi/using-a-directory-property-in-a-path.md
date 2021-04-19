---
description: Die Verzeichnisse in der Verzeichnis Tabelle geben das Layout einer-Installation an.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Verwenden einer Verzeichnis Eigenschaft in einem Pfad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362735"
---
# <a name="using-a-directory-property-in-a-path"></a><span data-ttu-id="511bb-103">Verwenden einer Verzeichnis Eigenschaft in einem Pfad</span><span class="sxs-lookup"><span data-stu-id="511bb-103">Using a Directory Property in a Path</span></span>

<span data-ttu-id="511bb-104">Die Verzeichnisse in der [Verzeichnis Tabelle](directory-table.md) geben das Layout einer-Installation an.</span><span class="sxs-lookup"><span data-stu-id="511bb-104">The directories in the [Directory table](directory-table.md) specify the layout of an installation.</span></span> <span data-ttu-id="511bb-105">Wenn das Windows Installer diese Verzeichnisse während der [costfinalize-Aktion](costfinalize-action.md)auflöst, werden die Schlüssel in der Verzeichnis Tabelle zu [Eigenschaften](properties.md) , die auf Verzeichnispfade festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="511bb-105">When the Windows Installer resolves these directories during the [CostFinalize action](costfinalize-action.md), the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span> <span data-ttu-id="511bb-106">Das Installationsprogramm legt auch immer eine Reihe von Standard [Systemordner-Eigenschaften](property-reference.md) auf Systemordner Pfade fest.</span><span class="sxs-lookup"><span data-stu-id="511bb-106">The installer also always sets a number of standard [System Folder Properties](property-reference.md) to system folder paths.</span></span>

<span data-ttu-id="511bb-107">Es ist garantiert, dass die Werte der [Eigenschaften des System Ordners](property-reference.md) in einem Verzeichnis Trennzeichen enden.</span><span class="sxs-lookup"><span data-stu-id="511bb-107">The values of the [System Folder Properties](property-reference.md) are guaranteed to end in a directory separator.</span></span> <span data-ttu-id="511bb-108">Die Werte aller anderen Eigenschaften, die in der [Verzeichnis Tabelle](directory-table.md) eingegeben werden, werden nur nach dem Ausführen der [Aktion "costfinalize](costfinalize-action.md)" in einem Verzeichnis Trennzeichen garantiert.</span><span class="sxs-lookup"><span data-stu-id="511bb-108">The values of all other properties entered in the [Directory table](directory-table.md) are only guaranteed to end in a directory separator after the installer has run the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="511bb-109">Vor Abschluss der Kosten werden die in der Verzeichnis Tabelle eingegebenen Werte von Eigenschaften, die keine [System Ordnereigenschaften](property-reference.md) sind, möglicherweise nicht mit einem Verzeichnis Trennzeichen enden.</span><span class="sxs-lookup"><span data-stu-id="511bb-109">Before costing has completed, the values of properties entered in the Directory table which are not [System Folder Properties](property-reference.md) may not end in a directory separator.</span></span> <span data-ttu-id="511bb-110">Wenn bei der Installation Verzeichnis Eigenschaften mithilfe von [benutzerdefinierten Aktionen](custom-actions.md) im Paket festgelegt werden, enden die Verweis Werte möglicherweise nicht mit einem Verzeichnis Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="511bb-110">Therefore, if your installation sets directory properties using [custom actions](custom-actions.md) in the package, the values on reference might not end with a directory separator.</span></span>

<span data-ttu-id="511bb-111">Verzeichnis Eigenschaften, die mit einem Verzeichnis Trennzeichen enden, können daher in einer Pfad Zeichenfolge ohne explizites einschließen des Verzeichnis Trennzeichens verwendet werden</span><span class="sxs-lookup"><span data-stu-id="511bb-111">Directory properties ending with a directory separator can therefore be used in a path string without explicitly including the directory separator.</span></span> <span data-ttu-id="511bb-112">Wenn der Wert von Director Property beispielsweise mit einem Verzeichnis Trennzeichen endet, gibt die folgende Zeichenfolge ordnungsgemäß den Pfad zu der *Datei* im *Unterverzeichnis* an.</span><span class="sxs-lookup"><span data-stu-id="511bb-112">For example, if the value of DirectoryProperty ends with a directory separator, the following string correctly specifies the path to *file* in *subdirectory*</span></span>

``` syntax
[DirectoryProperty]subdirectory\file
```

<span data-ttu-id="511bb-113">und die folgende Pfad Zeichenfolge ist falsch.</span><span class="sxs-lookup"><span data-stu-id="511bb-113">and the following path string is incorrect.</span></span>

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



