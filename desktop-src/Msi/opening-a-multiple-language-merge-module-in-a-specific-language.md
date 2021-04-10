---
description: Wenn Sie ein Modul in eine Installations Datenbank zusammenführen, gibt es zwei wichtige Sprachen.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Öffnen eines Multiple-Language Merge-Moduls in einer bestimmten Sprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041868"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a><span data-ttu-id="32273-103">Öffnen eines Multiple-Language Merge-Moduls in einer bestimmten Sprache</span><span class="sxs-lookup"><span data-stu-id="32273-103">Opening a Multiple-Language Merge Module in a Specific Language</span></span>

<span data-ttu-id="32273-104">Wenn Sie ein Modul in eine Installations Datenbank zusammenführen, gibt es zwei wichtige Sprachen.</span><span class="sxs-lookup"><span data-stu-id="32273-104">When merging a module into an installation database, there are two important languages.</span></span> <span data-ttu-id="32273-105">Die erste ist die Sprache des Ziel Installationspakets, das von [**productlanguage**](productlanguage.md) in der [Eigenschaften Tabelle](property-table.md)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="32273-105">The first is the language of the target installation package specified by [**ProductLanguage**](productlanguage.md) in the [Property Table](property-table.md).</span></span> <span data-ttu-id="32273-106">Die zweite ist die Sprache des Mergemoduls, das in der Spalte Sprache der [Tabelle ModuleSignature](modulesignature-table.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="32273-106">The second is the language of the merge module that appears in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="32273-107">Die Sprache des Installationspakets kann vom Mergetool an das Modul übermittelt werden, wenn das Paket für einen Mergevorgang geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="32273-107">The language of the installation package can be passed to the module by the merge tool when the package is opened for a merge.</span></span> <span data-ttu-id="32273-108">Manchmal kann es jedoch notwendig sein, die Sprache des Ziels zu ignorieren und anzufordern, dass das Modul in einer anderen Sprache geöffnet werden soll, z. b. in einem englischen Paket, das sowohl die englischen als auch die deutschen Ressourcen aus dem Modul installiert.</span><span class="sxs-lookup"><span data-stu-id="32273-108">However, sometimes it may be necessary to disregard the language of the target, and request that the module be opened in another language, for example, an English package installing both the English and German resources from the module.</span></span>

<span data-ttu-id="32273-109">Beim Öffnen eines Moduls mit einer sprach Anforderung überprüft das Mergetool die angeforderte Sprache auf die Sprachen, die in der Spalte Sprache der [Tabelle ModuleSignature](modulesignature-table.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="32273-109">When opening a module with a language request, the merge tool checks the requested language against the languages that are specified in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="32273-110">Der folgende Prozess wird verwendet, um zu bestimmen, welche Sprache verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="32273-110">The following process is used to determine which language to use.</span></span>

<span data-ttu-id="32273-111">**So bestimmen Sie die zu verwendende Sprache**</span><span class="sxs-lookup"><span data-stu-id="32273-111">**To determine which language to use**</span></span>

1.  <span data-ttu-id="32273-112">Wenn die Sprache in der [ModuleSignature-Tabelle](modulesignature-table.md) gleich oder allgemeiner als die angeforderte Sprache ist, wird das Modul geöffnet.</span><span class="sxs-lookup"><span data-stu-id="32273-112">If the language in the [ModuleSignature Table](modulesignature-table.md) is equal or more general than the requested language, the module opens.</span></span>
2.  <span data-ttu-id="32273-113">Wenn das Modul die angeforderte Sprache genau unterstützt, wird diese Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="32273-113">If the module supports the exact language requested, that language is used.</span></span>
3.  <span data-ttu-id="32273-114">Wenn das Modul die Sprachgruppe der angeforderten Sprache unterstützt, beispielsweise 9, wenn 1033 angefordert wurde, aber in Schritt 2 nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="32273-114">If the module supports the language group of the language requested that language group is used, for example, check 9 if 1033 was requested but not found in step 2.</span></span>
4.  <span data-ttu-id="32273-115">Überprüfen Sie, ob eine sprach Transformation vorhanden ist, durch die das Modul in neutral geändert wird.</span><span class="sxs-lookup"><span data-stu-id="32273-115">Check if there is a language transform that changes the module to neutral.</span></span>
5.  <span data-ttu-id="32273-116">Wenn keiner der vorherigen Schritte erfolgreich ausgeführt wurde, wird die angeforderte Sprache vom Modul nicht unterstützt, und die Zusammenführung schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="32273-116">If none of the previous steps succeed, the module does not support the requested language and the merge fails.</span></span>

 

 



