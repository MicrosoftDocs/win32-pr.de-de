---
description: .
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Verwenden des Meta-Tags zum Sicherstellen der zukünftigen Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e965711053a7108c69295ac737953a05536a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359617"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a>Verwenden des Meta-Tags zum Sicherstellen der zukünftigen Kompatibilität

Windows Internet Explorer 8 ermöglicht Ihnen, den Dokument Kompatibilitätsmodus zu steuern, damit Sie den Browser anweisen können, Webseiten auf die gleiche Weise wie ältere Browserversionen zu renderieren. Sie können auch auswählen, wann die Webseite aktualisiert werden soll, während Sie weiterhin verwendbar ist und ordnungsgemäß funktioniert.

## <a name="setting-the-meta-element"></a>Festlegen des Meta-Elements

Das **Meta** -Element enthält ein **Inhalts** Attribut, mit dem Sie den Modus angeben können, in dem der Inhalt für die Webseite gerendert wird, wie in der folgenden Tabelle gezeigt.



| Wert | Renderingmodus                                                 |
|-------|----------------------------------------------------------------|
| IE = 9  | Verwenden des Standard-Renderingmodus von Windows Internet Explorer 9   |
| IE = 8  | Verwenden des Standard-Renderingmodus von Internet Explorer 8           |
| IE = 7  | Verwenden des Standard-Renderingmodus von Windows Internet Explorer 7   |
| IE=5  | Verwenden des Standard-Renderingmodus von Microsoft Internet Explorer 5 |



 

Weitere Informationen zur Kompatibilität und zum X-UA-kompatiblen Header finden Sie unter [Definieren der Dokument Kompatibilität](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in der MSDN Library.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie erzwingen können, dass eine Webseite im Internet Explorer 8-Modus gerendert wird.


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

Viele Websites enthalten Tausende (oder Zehntausende) individuelle Webseiten, sodass das Festlegen des **Meta** -Elements für jedes Dokument nicht praktikabel ist. Wenn Sie das **Meta** -Element für alle Seiten oder eine Auflistung von Seiten festlegen möchten, die nach Ordner ausgewählt sind, können Sie stattdessen die Serverkonfiguration anpassen und die X-UA-kompatiblen Metadaten im- [http-Header](/previous-versions/cc817572(v=msdn.10))hinzufügen.

Für Websites, die unterschiedliche **metaelementwerte** für Seiten auf demselben Server benötigen, gibt es mehrere Tools, die automatisch das entsprechende **Meta** -Element generieren und einfügen. Das Hilfsprogramm " [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) " von Aggiorno fügt z. b. das Feature "Kompatibilitäts Kennzeichen für Internet Explorer 8" ein und entfernt es, sodass Ihre Website bestimmte Kompatibilitäts Standards erfüllen kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
