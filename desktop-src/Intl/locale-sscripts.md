---
description: '\_LOCALE-SSCRIPTS'
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aede4d6d1843fd32bdd17ae3a275a364c3a2d4f0bd282302f49d7b4a3b0dd1ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105850"
---
# <a name="locale_sscripts"></a>\_LOCALE-SSCRIPTS

**Windows Vista und höher:** Eine Zeichenfolge, die eine Liste von Skripts mit der in [ISO 15924 verwendeten 4-Zeichen-Notation darstellt.](https://www.unicode.org/iso15924/iso15924-codes.html) Jeder Skriptname besteht aus vier lateinischen Zeichen, und die Liste wird in alphabetischer Reihenfolge mit jedem Namen, einschließlich des letzten, gefolgt von einem Semikolon angeordnet.

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) kann aufgerufen werden, wenn *LCType* im Rahmen einer Strategie zur Entschärfung von Sicherheitsproblemen im Zusammenhang mit internationalisierten Domänennamen (IDNs) auf LOCALE \_ SSCRIPTS festgelegt ist. Hier sind einige Beispielwerte:



| Gebietsschema                  | Locale/language name | Wert                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| Englisch (USA) | de-DE                | Latn;                                                                                                  |
| Hindi (Indien)           | hi-IN                | Deva;                                                                                                  |
| Japanisch (Japan)        | ja-JP                | **Windows 7 und höher:** Hani; Hira; Jpan; Kana;<br/> **Windows Vista:** Hani; Hira; Kana;<br/> |



 

Ein zusammengesetzter Skriptwert enthält das lateinische Skript nur, wenn es ein wesentlicher Bestandteil des Schreibsystems ist, das für das bestimmte Locale verwendet wird. Lateinische Zeichen werden häufig im Kontext von Locales verwendet, für die sie nicht nativ sind, z. B. für einen fremd geschriebenen Geschäftsnamen. Im obigen Beispiel für Hindi in Indien ist der einzige Skriptwert "Deva" (für "Devana sollen"), obwohl lateinische Zeichen auch im Hindi-Text angezeigt werden können. Die [VerifyScripts-Funktion](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) verfügt über ein spezielles Flag, um diesen Fall zu erfüllen.

 

 




