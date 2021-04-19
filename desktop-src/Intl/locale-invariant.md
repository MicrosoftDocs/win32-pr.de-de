---
description: Gebiets Schema \_ invariant
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356737"
---
# <a name="locale_invariant"></a><span data-ttu-id="bf2ff-103">Gebiets Schema \_ invariant</span><span class="sxs-lookup"><span data-stu-id="bf2ff-103">LOCALE\_INVARIANT</span></span>

<span data-ttu-id="bf2ff-104">**Windows XP:** Das Gebiets Schema, das für Funktionen auf Betriebssystemebene verwendet wird, für die konsistente und Gebiets Schema unabhängige Ergebnisse erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bf2ff-104">**Windows XP:** The locale used for operating system-level functions that require consistent and locale-independent results.</span></span> <span data-ttu-id="bf2ff-105">Beispielsweise wird das invariante Gebiets Schema verwendet, wenn eine Anwendung Zeichen folgen mithilfe der [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) -Funktion vergleicht und unabhängig vom Benutzer Gebiets Schema ein konsistentes Ergebnis erwartet.</span><span class="sxs-lookup"><span data-stu-id="bf2ff-105">For example, the invariant locale is used when an application compares character strings using the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) function and expects a consistent result regardless of the user locale.</span></span> <span data-ttu-id="bf2ff-106">Die Einstellungen des invarianten Gebiets Schemas ähneln denen für Englisch (USA), Sie sollten jedoch nicht zum Anzeigen von formatierten Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf2ff-106">The settings of the invariant locale are similar to those for English (United States) but should not be used to display formatted data.</span></span> <span data-ttu-id="bf2ff-107">In der Regel verwendet eine Anwendung keine Gebiets Schema \_ invariante, da Sie erwartet, dass die Ergebnisse einer Aktion von den Regeln abhängen, die für die einzelnen Gebiets Schemas gelten.</span><span class="sxs-lookup"><span data-stu-id="bf2ff-107">Typically, an application does not use LOCALE\_INVARIANT because it expects the results of an action to depend on the rules governing each individual locale.</span></span> <span data-ttu-id="bf2ff-108">Der Wert von locale \_ invariant ist 0x007F.</span><span class="sxs-lookup"><span data-stu-id="bf2ff-108">The value of LOCALE\_INVARIANT IS 0x007f.</span></span>

 

 
