---
description: Der Language-Datentyp ist eine Textzeichenfolge, die mindestens eine gültige numerische Sprach-IDs enthält. Wenn zwei oder mehr Sprach-IDs vorhanden sind, müssen sie durch Kommas getrennt werden.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Sprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b98e24ec0ad4d4b42dfcba02374792e10ea117db474a973eae06336a55834538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013128"
---
# <a name="language"></a>Sprache

Der Language-Datentyp ist eine Textzeichenfolge, die mindestens eine gültige numerische Sprach-IDs enthält. Wenn zwei oder mehr Sprach-IDs vorhanden sind, müssen sie durch Kommas getrennt werden.

Der Language-Datentyp ist ein 16-Bit-Wert, der die Kombination aus einer primären und einer untersprachigen numerischen IDs ist. Die primäre LANGID besteht aus den Bits 0 bis 9, während die subLanguage-ID die Bits 10 bis 15 ist. Eine Liste der numerischen Bezeichner der primären und untergeordneten Sprache finden Sie im Thema [Konstanten und Zeichenfolgen für Sprachbezeichner.](../intl/language-identifier-constants-and-strings.md)

Bei IDs der primären Sprache ist der Bereich, der 0x200 0x3ff ist, benutzerdefinierbar. Der bereich, der 0x1ff 0x000 wird, ist für die Systemverwendung reserviert. Bei Untersprache-IDs kann der Bereich, der 0x3f 0x20 wird, vom Benutzerdefinierbar sein. Der Bereich 0x00, der 0x1f werden soll, ist für die Systemverwendung reserviert.

 

 
