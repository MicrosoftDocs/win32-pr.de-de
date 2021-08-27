---
description: GEBIETSSCHEMA \_ INVARIANT
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c3a4bddaaa51ca72be9d48f273ac0cbd1727e18e5c821e8ce86acaf0f90ec4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106580"
---
# <a name="locale_invariant"></a>GEBIETSSCHEMA \_ INVARIANT

**Windows XP:** Das Gebietsschema, das für Funktionen auf Betriebssystemebene verwendet wird, die konsistente und gebietsschemaunabhängige Ergebnisse erfordern. Beispielsweise wird das invariante Gebietsschema verwendet, wenn eine Anwendung Zeichenfolgen mithilfe der [**CompareString-Funktion**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) vergleicht und unabhängig vom Benutzergebietsschema ein konsistentes Ergebnis erwartet. Die Einstellungen des invarianten Gebietsschemas ähneln denen für Englisch (USA), sollten jedoch nicht zum Anzeigen formatierter Daten verwendet werden. In der Regel verwendet eine Anwendung LOCALE INVARIANT nicht, \_ da sie erwartet, dass die Ergebnisse einer Aktion von den Regeln abhängen, die die einzelnen Gebietsschemas regeln. Der Wert von LOCALE \_ INVARIANT IST 0x007f.

 

 
