---
description: Unischreiber speichert Unicode-zu-Glyphen-Zuordnungen (cmap), Glyphe-breiten und OpenType-Skripts zum Strukturieren von Tabellen.
ms.assetid: c06c0eaf-41cb-4fd1-9750-a78355217f12
title: Caching (Internationalisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf8bf7dd10fe414bc170086ff9b8c34142dc197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350994"
---
# <a name="caching-internationalization"></a>Caching (Internationalisierung)

Unischreiber speichert Unicode-zu-Glyphen-Zuordnungen (cmap), Glyphe-breiten und OpenType-Skripts zum Strukturieren von Tabellen. Ein Handle für die Tabellen für eine bestimmte Schriftart einer bestimmten Größe wird als "Skript Cache" bezeichnet. Viele uniscriefunktionen erfordern sowohl einen Gerätekontext handle-Parameter als auch einen Zeiger auf eine [**Skript \_ Cache**](script-cache.md) Struktur. Diese Funktionen suchen zunächst nach Informationen über den Skript Cache und verwenden den Gerätekontext nur dann, wenn erforderliche Tabellen nicht bereits zwischengespeichert wurden. Wenn die [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)-, [**scriptplace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)-oder [**scripttextout**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) -Funktion aufgerufen wird, muss die Anwendung einen Zeiger auf eine **Skript \_ Cache** Struktur übergeben. Das Handle sollte mit **null** initialisiert werden, bevor es von der Anwendung zum ersten Mal an eine uniscrienfunktion weitergeleitet wird. Die Anwendung sollte niemals dasselbe Handle für verschiedene Schriftarten oder andere Größen übergeben.

Eine Anwendung kann jederzeit einen Skript Cache freigeben. Uniscribeibehält Verweis Anzahlen in den Schriftart-und Shaper-Caches, gibt Schriftart Daten nur frei, wenn alle Größen der Schriftart freigegeben werden, und gibt nur dann Shaper-Daten frei, wenn alle vom Shaper unterstützten Schriftarten freigegeben werden. Wenn die Anwendung mit einem Stil ausgeführt wird, sollte Sie die [**scriptfreecache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache) -Funktion aufrufen, um den Skript Cache für den Stil freizugeben.

Für [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) und [**scriptplace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)ist es zulässig, dass die Anwendung einen NULL-Gerätekontext übergibt. In den meisten Fällen wird der-Vorgang erfolgreich ausgeführt, da erforderliche Tabellen bereits zwischengespeichert wurden. Wenn die Strukturierung oder Platzierung Zugriff auf einen Gerätekontext erfordert, gibt **scriptshape** oder **scriptplace** sofort mit dem Fehlercode "E Pending" zurück \_ . Anschließend muss die Anwendung die Schriftart im Gerätekontext auswählen. Bei den meisten Anwendungen wird dadurch die Leistung verbessert, da die wiederholte Vorbereitung eines Gerätekontext Handles mit Aufrufen von [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject)vermieden wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 
