---
description: Gebiets Schema- \_ sscripts
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347803"
---
# <a name="locale_sscripts"></a>Gebiets Schema- \_ sscripts

**Windows Vista und höher:** Eine Zeichenfolge, die eine Liste von Skripts mit der in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)verwendeten 4-Zeichen-Notation darstellt. Jeder Skript Name besteht aus vier lateinischen Zeichen, und die Liste wird in alphabetischer Reihenfolge mit den einzelnen Namen angeordnet, gefolgt von einem Semikolon.

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) kann mit *LCTYPE* , festgelegt auf locale \_ sscripts, als Teil einer Strategie aufgerufen werden, um Sicherheitsprobleme im Zusammenhang mit internationalisierten Domänen Namen (IDNs) zu mindern. Im folgenden finden Sie einige Beispiel Werte:



| Gebietsschema                  | Gebiets Schema-/Sprachname | Wert                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| Englisch (USA) | de-DE                | Latn                                                                                                  |
| Hindi (Indien)           | hi-IN                | Vas                                                                                                  |
| Japanisch (Japan)        | ja-JP                | **Windows 7 und höher:** Han Hira; Jpan; Betrieben<br/> **Windows Vista:** Han Hira; Betrieben<br/> |



 

Ein Verbund Skript Wert enthält nicht das lateinische Skript, es sei denn, er ist ein wesentlicher Bestandteil des für das jeweilige Gebiets Schema verwendeten Schreibsystems. Lateinische Zeichen werden häufig im Kontext von Gebiets Schemas verwendet, für die Sie nicht nativ sind, z. b. für einen fremden Geschäftsnamen. Im obigen Beispiel für Hindi in Indien ist der einzige Skript Wert "Deva" (für "Devanagari"), obwohl auch lateinische Zeichen in Hindi-Text vorkommen können. Die Funktion " [verifyscripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) " weist ein spezielles Flag auf, um diesen Fall zu beheben.

 

 




