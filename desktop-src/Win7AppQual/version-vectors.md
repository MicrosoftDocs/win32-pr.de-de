---
description: Ein Versions Vektor verarbeitet bedingte Kommentare in einer HTML-Webseite. Das heißt, dass Versions Vektoren es Ihnen ermöglichen, Markup basierend auf der Browserversion zu erstellen.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Versionsvektoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350548"
---
# <a name="version-vectors"></a>Versionsvektoren

Ein *Versions Vektor* verarbeitet bedingte Kommentare in einer HTML-Webseite. Das heißt, dass Versions Vektoren es Ihnen ermöglichen, Markup basierend auf der Browserversion zu erstellen.

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



Wenn in diesem Fall die Windows Internet Explorer-Browserversion mindestens 5,5 ist, wird der entsprechende Absatz auf der Webseite angezeigt. Obwohl die erste Bedingung in diesem Beispiel die Funktion von bedingten Kommentaren veranschaulicht, werden diese Kommentare in der Regel nicht verwendet, um Markup wie die erste Bedingung anzuzeigen. Stattdessen sind die verbleibenden bedingten Kommentare im vorherigen Beispiel häufiger. In diesen übrigen Kommentaren verwenden die bedingten Kommentare ein anderes Stylesheet für jede andere Version des Browsers.

Im vorangehenden Codebeispiel wird außerdem überprüft, ob Microsoft Internet Explorer 6 und Windows Internet Explorer 7 gleich sind. Für Windows Internet Explorer 8 verwendet das Beispiel den GTE-Operator (größer als oder gleich). Dieser Operator unterstützt in Zukunft das Beispiel, sodass die standardkonforme Version des Stylesheets verwendet wird, wenn eine neue Version des Browsers freigegeben wird (anstatt das falsche Stylesheet oder kein Stylesheet zu verwenden). Vorhandene Anwendungen sind häufig nicht in der Lage, eine Version von Internet Explorer in der Vergangenheit 7 (oder die neueste Version von Internet Explorer, für die die Website erstellt wurde) zu verwenden. Weitere Informationen zu Versions Vektoren finden Sie unter [Versions Vektoren](/previous-versions/cc817577(v=msdn.10)) in der MSDN Library.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



