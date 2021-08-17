---
description: LOCALE \_ SCONSOLEFALLBACKNAME
ms.assetid: 36465a1c-085f-4f80-ad3d-5be6eaefe943
title: LOCALE_SCONSOLEFALLBACKNAME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4234ea00516f777b4f70adc6127fd7dcf089d687b16ce68df8fbb210057b469b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948495"
---
# <a name="locale_sconsolefallbackname"></a>LOCALE \_ SCONSOLEFALLBACKNAME

**Windows Vista und höher:** Bevorzugtes Für die Konsolenanzeige zu verwendende Locale. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind, beträgt 85, einschließlich eines beendenden NULL-Zeichens.

> [!Note]  
> Im Allgemeinen sollten Anwendungen \_ locale-SCONSOLEFALLBACKNAME-Daten nicht direkt verwenden. Um zu bestimmen, welche Sprachressourcen in einem Konsolenfenster verwendet werden sollen, sollte eine Anwendung [entweder SetThreadUILanguage](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) oder [SetThreadPreferredUILanguages aufrufen.](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) Diese Funktionen verwenden die Fallbackdaten der Konsole als Faktor bei der Auswahl einer Sprache, die in der Konsole lesbar ist, aber nicht die einzige Determinante ist. Insbesondere ist die Konsole auf das Anzeigen von Zeichen aus einer einzelnen Codepage beschränkt. Beispielsweise ist el-GR für Griechisch (Griechisch) eine gültige Konsolensprache, aber wenn die aktuelle Konsolencodepage Latin-1 (Codepage 1252) ist, zeigt die Konsole den lateinischen Text größtenteils als eine Reihe von Symbolen an, die nicht gefunden wurden.

 

If the language corresponding to this locale is supported in the console, the value is the same as that for [LOCALE\_SNAME](locale-sname.md), that is, the locale itself can be used for console display. Die Konsole kann jedoch keine Sprachen anzeigen, die nur mit [Uniscribe gerendert werden können.](uniscribe.md) Beispielsweise kann die Konsole nicht arabisch oder die verschiedenen indischen Sprachen anzeigen. Daher ist der LOCALE SCONSOLEFALLBACKNAME-Wert für die Diesen Sprachen entsprechenden Locales anders als der Wert \_ für LOCALE \_ SNAME.

Für vordefinierte Locales wird der Wert für das neutrale Locale verwendet, wenn sich der Fallbackwert vom Wert für das Locale selbst abtrat. Ein bestimmtes Locale ist sowohl einer Sprache als auch einem Land/einer Region zugeordnet, während ein neutrales Locale einer Sprache zugeordnet ist, aber nicht mit einem Land/einer Region verknüpft ist. Beispielsweise fällt ar-SA auf "en" zurück, nicht auf "en-US". Diese Richtlinie zur Verwendung neutraler Locales wird konsistent für vordefinierte Locales implementiert und wird dringend für benutzerdefinierte Locales empfohlen. Die Richtlinie wird jedoch nicht erzwungen. Für ein benutzerdefiniertes Locale kann Ihre Anwendung ein bestimmtes Locale anstelle eines neutralen Locale als Fallback verwenden.

> [!Note]  
> Keine der unter Aufrufen der [Locale Name-Funktionen](calling-the--locale-name--functions.md) beschriebenen Funktionen akzeptiert neutrale Locales als Eingaben. Daher werden LOCALE \_ SCONSOLEFALLBACKNAME-Daten nur sehr eingeschränkt verwendet. Insbesondere akzeptieren weder [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) noch [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) neutrale Locales als Eingaben.

 

 

 



