---
description: Standardmäßig sind die Windows Search-Engine und der-Katalog nicht mit diakritischen Zeichen versehen, bei denen es sich um Akzente zum Ändern der Bedeutung oder Aussprache eines Worts handelt.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Diakritische Empfindlichkeit bei Such Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346497"
---
# <a name="diacritic-sensitivity-in-searches"></a><span data-ttu-id="298ec-103">Diakritische Empfindlichkeit bei Such Vorgängen</span><span class="sxs-lookup"><span data-stu-id="298ec-103">Diacritic Sensitivity in Searches</span></span>

<span data-ttu-id="298ec-104">Standardmäßig sind die Windows Search-Engine und der-Katalog nicht mit diakritischen Zeichen versehen, bei denen es sich um Akzente zum Ändern der Bedeutung oder Aussprache eines Worts handelt.</span><span class="sxs-lookup"><span data-stu-id="298ec-104">By default, the Windows Search engine and catalog are insensitive to diacritics, which are accent marks added to letters to alter a word's meaning or pronunciation.</span></span> <span data-ttu-id="298ec-105">Mithilfe von Windows Search können Sie dies jedoch für Ihren Katalog ändern, indem Sie den [Katalog-Manager](-search-3x-wds-mngidx-catalog-manager.md) verwenden, um die diakritische Empfindlichkeit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="298ec-105">However, Windows Search enables you to change this for your catalog using the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to set diacritic sensitivity.</span></span> <span data-ttu-id="298ec-106">Wenn z. b. die diakritische Sensitivität auf **false** festgelegt ist, würde der Katalog "Resume" und "Resumé" so behandeln, als wären Sie das gleiche Wort.</span><span class="sxs-lookup"><span data-stu-id="298ec-106">For example, with diacritic sensitivity set to **FALSE**, the catalog would treat "resume" and "resumé" as if they were the same word.</span></span>

<span data-ttu-id="298ec-107">Auf der Abfrage Ebene werden Abfrage Begriffe mit Diakritik in fretext-und enthält-Klauseln an die-Engine weitergegeben und dann normalisiert (wie Sie bei der Index Zeit), um Übereinstimmungen abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="298ec-107">At the query layer, query terms with diacritics in FREETEXT and CONTAINS clauses are passed through to the engine and are then normalized (as they would be at index time) for matching.</span></span> <span data-ttu-id="298ec-108">Die Übereinstimmung mit dem Katalog ist immer diakritisch sensibel.</span><span class="sxs-lookup"><span data-stu-id="298ec-108">Matching against the catalog is always diacritic sensitive.</span></span>

> [!Note]  
> <span data-ttu-id="298ec-109">Dies ist für die Zeichen Bereiche 0x2e81-F8FF liegt und 0x1100-0x11ff nicht der Fall.</span><span class="sxs-lookup"><span data-stu-id="298ec-109">This is not the case for the character ranges 0x2e81-f8ff and 0x1100-0x11ff.</span></span>

 

 

 



