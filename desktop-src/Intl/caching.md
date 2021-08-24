---
description: Uniscribe speichert Zuordnungen von Unicode-zu-Glyphen (cmap), Symbolbreiten und OpenType-Skripts zum Gestalten von Tabellen.
ms.assetid: c06c0eaf-41cb-4fd1-9750-a78355217f12
title: Caching (Internationalisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a01d8444fa222c2b6f6c7b03d0e1be70c1e04b1509ab020b8769d87b2b5cbc0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500830"
---
# <a name="caching-internationalization"></a>Caching (Internationalisierung)

Uniscribe speichert Zuordnungen von Unicode-zu-Glyphen (cmap), Symbolbreiten und OpenType-Skripts zum Gestalten von Tabellen. Ein Handle für die Tabellen für eine bestimmte Schriftart einer bestimmten Größe wird als "Skriptcache" bezeichnet. Viele Uniscribe-Funktionen rufen sowohl für einen Handleparameter für den Gerätekontext als auch für einen Zeiger auf eine [**SCRIPT \_ CACHE-Struktur**](script-cache.md) auf. Diese Funktionen suchen zuerst nach Informationen über den Skriptcache und verwenden den Gerätekontext nur, wenn erforderliche Tabellen nicht bereits zwischengespeichert sind. Beim Aufrufen der [**ScriptShape-,**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) [**ScriptPlace-**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)oder [**ScriptTextOut-Funktion**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) muss die Anwendung einen Zeiger auf eine **SCRIPT \_ CACHE-Struktur** übergeben. Das Handle sollte mit NULL initialisiert **werden,** bevor die Anwendung es zum ersten Mal an eine Uniscribe-Funktion übergibt. Die Anwendung sollte nie dasselbe Handle für verschiedene Schriftarten oder Größen übergeben.

Eine Anwendung kann jederzeit einen Skriptcache frei geben. Uniscribe verwaltet Die Verweisanzahl in den Schriftart- und Shapercaches, gibt Schriftartdaten nur frei, wenn alle Schriftgrößen frei werden, und gibt Shaperdaten nur frei, wenn alle schriftarten, die der Shaper unterstützt, frei werden. Wenn die Anwendung mit einem Stil fertig ist, sollte sie die [**ScriptFreeCache-Funktion**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache) aufrufen, um den Skriptcache für den Stil frei zu geben.

Für [**ScriptShape und**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)ist es gültig, dass die Anwendung einen NULL-Gerätekontext übergibt. In den meisten Jahren ist der Aufruf erfolgreich, da die erforderlichen Tabellen bereits zwischengespeichert sind. Wenn die Gestaltung oder Platzierung Zugriff auf einen Gerätekontext erfordert, wird **ScriptShape** oder **ScriptPlace** sofort mit dem Fehlercode E \_ PENDING zurückgegeben. Anschließend muss die Anwendung die Schriftart im Gerätekontext auswählen. Für die meisten Anwendungen hilft dies bei der Leistung, indem die wiederholte Vorbereitung eines Gerätekontexthandpunkts mit Aufrufen von [**SelectObject vermieden wird.**](/windows/win32/api/wingdi/nf-wingdi-selectobject)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
