---
description: Verwenden des Metatags zum Sicherstellen der zukünftigen Kompatibilität
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Verwenden des Metatags zum Sicherstellen der zukünftigen Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a69180470c60dffc772f20fe6c515ba3803cbf2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084168"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a>Verwenden des Metatags zum Sicherstellen der zukünftigen Kompatibilität

Mit Windows Internet Explorer 8 können Sie dokumentkompatibilitätsmodi steuern, sodass Sie den Browser anweisen können, Webseiten auf die gleiche Weise wie ältere Browserversionen zu rendern. Sie können auch auswählen, wann die Webseite aktualisiert werden soll, während sie weiterhin verwendet werden kann und ordnungsgemäß funktioniert.

## <a name="setting-the-meta-element"></a>Festlegen des Metaelements

Das **Metaelement** enthält ein **Inhaltsattribut,** mit dem Sie den Modus angeben können, in dem Der Inhalt für die Webseite gerendert wird, wie in der folgenden Tabelle gezeigt.



| Wert | Renderingmodus                                                 |
|-------|----------------------------------------------------------------|
| IE=9  | Verwenden des Windows Internet Explorer 9-Standardrenderingmodus   |
| IE=8  | Verwenden des Internet Explorer 8-Standardrenderingmodus           |
| IE=7  | Verwenden des Windows Internet Explorer 7-Standardrenderingmodus   |
| IE=5  | Verwenden des Microsoft Internet Explorer 5-Standardrenderingmodus |



 

Weitere Informationen zur Kompatibilität und zum X-UA-kompatiblen Header finden Sie unter [Definieren der Dokumentkompatibilität](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in der MSDN Library.

Im folgenden Codebeispiel wird veranschaulicht, wie sie erzwingen, dass eine Webseite im 8 Internet Explorer gerendert wird.


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a>Verwenden eines HTTP-Headers

Viele Websites enthalten Tausende (oder Zehntausende) einzelner Webseiten, sodass das Festlegen des **Metaelements** für jedes Dokument unpraktisch ist. Wenn Sie das  Metaelement für alle Seiten oder eine Sammlung von Seiten festlegen möchten, die nach Ordner ausgewählt sind, können Sie stattdessen die Serverkonfiguration anpassen und die X-UA-kompatiblen Metadaten im [HTTP-Header hinzufügen.](/previous-versions/cc817572(v=msdn.10))

Für Websites, die unterschiedliche **Metaelementwerte** für Seiten auf demselben Server benötigen, gibt es mehrere Tools, die automatisch das entsprechende **Metaelement** für Sie generieren und einfügen. Beispielsweise fügt das [Hilfsprogramm ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) von Alayrno das Feature Internet Explorer 8-Kompatibilitätstags ein und entfernt es und kann Ihre Website dabei unterstützen, bestimmte Kompatibilitätsstandards zu erfüllen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
