---
description: LOCALE \_ sconsolefallbackname
ms.assetid: 36465a1c-085f-4f80-ad3d-5be6eaefe943
title: LOCALE_SCONSOLEFALLBACKNAME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09536167c68a4ec9156a1558960c48778019ae97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349467"
---
# <a name="locale_sconsolefallbackname"></a>LOCALE \_ sconsolefallbackname

**Windows Vista und höher:** Bevorzugtes Gebiets Schema für die Konsolen Anzeige. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 85, einschließlich eines abschließenden NULL-Zeichens.

> [!Note]  
> Im Allgemeinen sollten Anwendungen keine direkte Verwendung von \_ sconsolefallbackname-Daten für das Gebiets Schema vornehmen. Um zu ermitteln, welche Sprachressourcen in einem Konsolenfenster verwendet werden sollen, sollte eine Anwendung entweder [setthreaduilanguage](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) oder [setthreadpreferreduilanguages](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)aufrufen. Diese Funktionen verwenden die Konsolen Fall Back Daten als Faktor bei der Auswahl einer Sprache, die in der-Konsole lesbar ist, aber nicht die einzige Determinante. Die-Konsole ist insbesondere auf die Anzeige von Zeichen aus einer einzelnen Codepage beschränkt. Beispielsweise ist el-gr für Griechisch (Griechenland) eine gültige Konsolen Sprache, aber wenn die aktuelle Konsolen Codepage Lateinisch-1 (Codepage 1252) ist, zeigt die Konsole den griechischen Text größtenteils als eine Reihe von Zeichen an, die nicht gefunden wurden.

 

Wenn die Sprache, die diesem Gebiets Schema entspricht, in der-Konsole unterstützt wird, ist der Wert identisch mit dem für [locale \_ sname](locale-sname.md), d. h., das Gebiets Schema kann für die Konsolen Anzeige verwendet werden. Die-Konsole kann jedoch keine Sprachen anzeigen, die nur mit [unischreiber](uniscribe.md)gerendert werden können. Beispielsweise können in der-Konsole keine arabischen oder die verschiedenen indic-Sprachen angezeigt werden. Daher unterscheidet sich der Gebiets Schema- \_ sconsolefallbackname-Wert für Gebiets Schemas, die diesen Sprachen entsprechen, von dem Wert für \_ Gebiets Schema sname.

Bei vordefinierten Gebiets Schemata wird der Wert für das neutrale Gebiets Schema verwendet, wenn sich der Fall Back Wert von dem Wert für das Gebiets Schema unterscheidet. Ein bestimmtes Gebiets Schema ist sowohl einer Sprache als auch einem Land/einer Region zugeordnet, während ein neutrales Gebiets Schema einer Sprache zugeordnet ist, aber keinem Land/keiner Region zugeordnet ist. Beispielsweise greift AR-SA auf "en" und nicht auf "en-US" zurück. Diese Richtlinie für die Verwendung neutraler Gebiets Schemas wird für vordefinierte Gebiets Schemata konsistent implementiert und wird für benutzerdefinierte Gebiets Schemas dringend empfohlen Die Richtlinie wird jedoch nicht erzwungen. Für ein benutzerdefiniertes Gebiets Schema kann die Anwendung ein bestimmtes Gebiets Schema anstelle eines neutralen Gebiets Schemas als Fallback verwenden.

> [!Note]  
> Keine der Funktionen, die unter [Aufrufen der "locale Name"-Funktion](calling-the--locale-name--functions.md) beschrieben werden, akzeptiert neutrale Gebiets Schemas als Eingaben. Daher ist die locale \_ sconsolefallbackname-Daten sehr eingeschränkt. Vor allem kann weder [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) noch [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) neutrale Gebiets Schemas als Eingaben akzeptieren.

 

 

 



