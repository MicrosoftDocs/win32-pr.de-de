---
description: Mergemodule erfordern selten eine Benutzeroberfläche.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Erstellen von Benutzeroberflächen in Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356681"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a><span data-ttu-id="f7775-103">Erstellen von Benutzeroberflächen in Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="f7775-103">Authoring User Interfaces in Merge Modules</span></span>

<span data-ttu-id="f7775-104">Mergemodule erfordern selten eine Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="f7775-104">Merge modules rarely require a user interface.</span></span> <span data-ttu-id="f7775-105">Das Freigeben eines Mergemoduls, das sowohl installierbare Komponenten als auch eine Benutzeroberfläche enthält, schränkt letztendlich die Flexibilität des Modul Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="f7775-105">Releasing a merge module that contains both installable components and a user interface ultimately restricts the flexibility of the module user.</span></span> <span data-ttu-id="f7775-106">Das Kombinieren von Komponenten und Benutzeroberflächen zu einem Modul kann verhindern, dass Entwickler ihre eigene Benutzeroberfläche verwenden oder unbeaufsichtigte Installationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f7775-106">Combining both components and UI into one module can prevent developers from using their own UI or from providing silent installations.</span></span> <span data-ttu-id="f7775-107">Eine bessere Alternative besteht darin, zwei Mergemodule freizugeben, eine, die die Komponenten im Hintergrund installiert, und ein zweites optionales Modul, das die Benutzeroberfläche enthält.</span><span class="sxs-lookup"><span data-stu-id="f7775-107">A better alternative is to release two merge modules, one that silently installs the components and a second optional module that contains the UI.</span></span> <span data-ttu-id="f7775-108">Das Modul mit der Benutzeroberfläche sollte das Komponenten Modul in seiner [moduledepen-Tabelle](moduledependency-table.md)auflisten.</span><span class="sxs-lookup"><span data-stu-id="f7775-108">The module with the UI should list the component module in its [ModuleDependency table](moduledependency-table.md).</span></span> <span data-ttu-id="f7775-109">Mit dieser Methode können Modul Autoren eine Benutzeroberfläche bereitstellen, ohne Sie für Entwickler zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="f7775-109">This method enables module authors to provide a UI without forcing it on developers.</span></span>

<span data-ttu-id="f7775-110">Wenn Benutzeroberflächen Tabellen in Mergemodulen verwendet werden, können Sie auf die gleiche Weise wie alle anderen Tabellen zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f7775-110">When UI tables are used in merge modules they can be merged in the same way as any other tables.</span></span>

 

 



