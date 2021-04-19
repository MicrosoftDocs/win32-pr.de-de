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
# <a name="locale_invariant"></a>Gebiets Schema \_ invariant

**Windows XP:** Das Gebiets Schema, das für Funktionen auf Betriebssystemebene verwendet wird, für die konsistente und Gebiets Schema unabhängige Ergebnisse erforderlich sind. Beispielsweise wird das invariante Gebiets Schema verwendet, wenn eine Anwendung Zeichen folgen mithilfe der [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) -Funktion vergleicht und unabhängig vom Benutzer Gebiets Schema ein konsistentes Ergebnis erwartet. Die Einstellungen des invarianten Gebiets Schemas ähneln denen für Englisch (USA), Sie sollten jedoch nicht zum Anzeigen von formatierten Daten verwendet werden. In der Regel verwendet eine Anwendung keine Gebiets Schema \_ invariante, da Sie erwartet, dass die Ergebnisse einer Aktion von den Regeln abhängen, die für die einzelnen Gebiets Schemas gelten. Der Wert von locale \_ invariant ist 0x007F.

 

 
