---
description: Wenn ein Modul mehrere Sprachen unterstützt, können Sie es mehrmals in dieselbe Windows Installer Datenbank zusammenführen, aber stellen Sie sicher, dass für jede Zusammenführung eine andere Sprache verwendet wird.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Mehrmals Zusammenführen eines Moduls mit mehreren Sprachen in demselben Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363286"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a><span data-ttu-id="65d21-103">Mehrmals Zusammenführen eines Moduls mit mehreren Sprachen in demselben Paket</span><span class="sxs-lookup"><span data-stu-id="65d21-103">Merging a Multiple Language Module into the Same Package Multiple Times</span></span>

<span data-ttu-id="65d21-104">Wenn ein Modul mehrere Sprachen unterstützt, können Sie es mehrmals in dieselbe Windows Installer Datenbank zusammenführen, aber stellen Sie sicher, dass für jede Zusammenführung eine andere Sprache verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65d21-104">When a module supports multiple languages, you can merge it into the same Windows Installer database multiple times, but make sure that each merge uses a different language.</span></span> <span data-ttu-id="65d21-105">Fordern Sie vor jeder Zusammenführung eine andere Sprache vom Modul an.</span><span class="sxs-lookup"><span data-stu-id="65d21-105">Before each merge, request a different language from the module.</span></span> <span data-ttu-id="65d21-106">Die resultierende MSI-Datenbank hat dann einen Datensatz in der [Tabelle ModuleSignature](modulesignature-table.md) für jede Zusammenführung des Moduls.</span><span class="sxs-lookup"><span data-stu-id="65d21-106">The resulting .msi database then has a record in the [ModuleSignature Table](modulesignature-table.md) for each merge of the module.</span></span> <span data-ttu-id="65d21-107">Komponenten, die von Sprachen gemeinsam genutzt werden, sind nur einmal in der [Component-Tabelle](component-table.md)vorhanden, sind aber jeder Sprache in der [modulecomponents-Tabelle](modulecomponents-table.md)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="65d21-107">Components that are shared between languages exist only one time in the [Component Table](component-table.md), but are associated with each language in the [ModuleComponents Table](modulecomponents-table.md).</span></span>

<span data-ttu-id="65d21-108">Wenn Sie mehrere Sprachen eines Moduls in dasselbe Paket zusammenführen, muss jede Zusammenführung dieselben Einschränkungen für Codepages wie einzelne Sprachmodule erfüllen.</span><span class="sxs-lookup"><span data-stu-id="65d21-108">When merging multiple languages of a module into the same package, each merge must satisfy the same restrictions on code pages as single-language modules.</span></span> <span data-ttu-id="65d21-109">Die Module können keine Zeichen folgen in unterschiedlichen Codepages enthalten.</span><span class="sxs-lookup"><span data-stu-id="65d21-109">The modules cannot contain strings in different code pages.</span></span>

<span data-ttu-id="65d21-110">Wenn Sie ein Modul mehrmals in eine MSI-Datei zusammenführen, müssen Sie ggf. die Reihenfolge der Dateien in der [Dateitabelle](file-table.md) so ändern, dass die vorhandene CAB-Datei direkt in der Installation von dem Modul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65d21-110">When merging a module multiple times into a single .msi file, you may need to modify the order of the files in the [File Table](file-table.md) to use the existing .cab from the module directly in your installation.</span></span> <span data-ttu-id="65d21-111">Die Reihenfolge der Dateien in der Dateitabelle muss mit der Reihenfolge der Dateien in der CAB-Datei identisch sein.</span><span class="sxs-lookup"><span data-stu-id="65d21-111">The order of files in the File Table must match the order of files in the .cab.</span></span> <span data-ttu-id="65d21-112">Wenn Sie ein Modul mehrmals in eine Installations Datenbank zusammenführen, kann die Sequenz geändert werden, da Dateien, die von den Sprachen gemeinsam genutzt werden, möglicherweise bereits aus einer vorherigen Zusammenführung im Modul vorhanden sind und eine andere relative Sequenznummer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="65d21-112">When merging a module multiple times into an installation database the sequence may be modified, because files shared between the languages may already exist in the module from a prior merge, and they have a different relative sequence number.</span></span>

 

 



