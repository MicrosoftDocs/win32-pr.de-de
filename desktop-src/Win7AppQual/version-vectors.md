---
description: Ein Versionsvektor verarbeitet bedingte Kommentare auf einer HTML-Webseite. Versionsvektoren ermöglichen Es Ihnen also, Markup basierend auf der Browserversion zu erstellen.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Versionsvektoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7ba3fb77d13ce6aa08a095f4ae95e88c1ffaecf57251b7d9ad718f51be3326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328606"
---
# <a name="version-vectors"></a>Versionsvektoren

Ein *Versionsvektor* verarbeitet bedingte Kommentare auf einer HTML-Webseite. Versionsvektoren ermöglichen Es Ihnen also, Markup basierend auf der Browserversion zu erstellen.

Betrachten Sie das folgende Codebeispiel.


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



Wenn die Windows Internet Explorer Browserversion in diesem Fall mindestens 5.5 ist, wird der entsprechende Absatz auf der Webseite angezeigt. Obwohl die erste Bedingung in diesem Beispiel die Funktion von bedingten Kommentaren veranschaulicht, werden diese Kommentare in der Regel nicht verwendet, um Markup wie die erste Bedingung anzuzeigen. Stattdessen sind die verbleibenden bedingten Kommentare im vorherigen Beispiel häufiger. In diesen verbleibenden Kommentaren verwenden die bedingten Kommentare ein anderes Stylesheet für jede unterschiedliche Version des Browsers.

Im obigen Codebeispiel wird auch auf Gleichheit für Microsoft Internet Explorer 6 und Windows Internet Explorer 7 überprüft. Für Windows Internet Explorer 8 verwendet das Beispiel jedoch den Gte-Operator (größer als oder gleich). Dieser Operator hilft dabei, das Beispiel für die Zukunft zu sichern, sodass die standardkonformste Version des Stylesheets verwendet wird, wenn eine neue Version des Browsers veröffentlicht wird (anstatt das falsche Stylesheet oder kein Stylesheet zu verwenden). Vorhandene Anwendungen berücksichtigen häufig keine Version von Internet Explorer 7 (oder die neueste Version von Internet Explorer, für die der Standort erstellt wurde). Weitere Informationen zu Versionsvektoren finden Sie unter [Versionsvektoren](/previous-versions/cc817577(v=msdn.10)) in der MSDN Library.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



