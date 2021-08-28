---
title: Zugreifen auf das Steuerelement in Webseiten
description: Zugreifen auf das Steuerelement in Webseiten
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb6476ebdf2d26f1aec12a2f46506b3c4882d06
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882965"
---
# <a name="accessing-the-control-in-web-pages"></a>Zugreifen auf das Steuerelement in Webseiten

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Um über eine Webseite auf die Microsoft Agent-Dienste zu zugreifen, verwenden Sie das HTML &lt; &gt; OBJECT-Tag innerhalb von . <HEAD> oder &lt; das &gt; BODY-Element der Seite unter Angabe der Microsoft CLSID (Klassenbezeichner) für das Steuerelement. Verwenden Sie außerdem einen CODEBASE-Parameter, um den Speicherort der Microsoft Agent-Installationsdatei und deren Versionsnummer anzugeben.

Wenn Microsoft Internet Explorer (Version 3.02 oder höher) auf dem System installiert ist, Microsoft Agent jedoch noch nicht installiert ist und der Benutzer auf eine Webseite mit dem OBJECT-Tag mit der &lt; Agent-CLSID zutritt, versucht der Browser automatisch, den -Agent von der &gt; Microsoft-Website herunterzuladen. Anschließend wird der Benutzer gefragt, ob er mit der Installation fortfahren soll. Wenden Sie sich bei anderen Browsern an den Lieferanten, um Informationen zu deren Support oder Drittanbietersupport für ActiveX erhalten.

Im folgenden Beispiel wird veranschaulicht, wie sie den CODEBASE-Parameter verwenden, um die englischsprachige Version 2.0 von Microsoft Agent automatisch zu laden.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Der Agent kann auch von Ihrem eigenen HTTP-Server oder im Rahmen des Installationsprozesses einer Anwendung installiert werden. Um die Installation von Ihrem eigenen HTTP-Server aus zu unterstützen, müssen Sie die Selbstinstallations-.Exe-Datei von Microsoft Agent veröffentlichen und ihre URL im CODEBASE-Tag angeben.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Um den automatischen Download einer Microsoft Agent-Sprachkomponente von einer Webseite zu unterstützen, fügen Sie das Object-Tag der Sprachkomponente auf der Seite vor dem Objekttag des -Agent-Steuerelements ein:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

Dabei wird XXXX durch eine Sprach-ID ersetzt. Informationen zu den derzeit unterstützten Sprachen finden Sie auf der Microsoft Agent-Website.

-   Das &lt; &gt; OBJECT-Tag für eine Sprachkomponente muss dem &lt; &gt; OBJECT-Tag für die Microsoft Agent-Kernkomponente vorangehenden.
-   Auf demselben Client können mehrere Sprachen installiert werden.
-   Bevor Sie [**die LanguageID eines**](https://www.bing.com/search?q=**LanguageID**) Zeichens festlegen, empfiehlt es sich, dass Ihr Skript überprüft, ob das in der [**userLanguage-Eigenschaft**](https://www.bing.com/search?q=**userLanguage**) verfügbare Locale des Browsers der festgelegten Sprache entspricht.

Um andere Sprachversionen des -Agents zu unterstützen, verwenden Sie ein anderes Object-Tag, das die Sprachkomponente anklickt. Beachten Sie jedoch, dass beim Versuch, mehrere Sprachen gleichzeitig zu installieren, der Benutzer möglicherweise neu gestartet werden muss. Die Komponenten der -Agent-Sprache können von der Agent-Website mit dem gleichen Verfahren wie für die Agent-Kernkomponente ermittelt werden. Die Verteilungslizenzierung für die Sprachkomponenten wird in der Standard-Agent-Verteilungslizenz behandelt. Um mit der Verwendung eines Zeichens zu beginnen, müssen Sie das Zeichen mithilfe der [**Load-Methode**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) laden. Ein Zeichen kann aus dem lokalen Speicher des Benutzers oder einem HTTP-Server geladen werden. Weitere Informationen zur Syntax zum Laden eines Zeichens finden Sie unter der **Load-Methode.** Nachdem das Zeichen erfolgreich geladen wurde, können Sie die Methoden, Eigenschaften und Ereignisse verwenden, die vom -Agent-Steuerelement verfügbar gemacht werden, um das Zeichen zu programmieren. Sie können auch die Methoden, Eigenschaften und Ereignisse verwenden, die von Ihrer Programmiersprache und dem Browser verfügbar gemacht werden, um das Zeichen zu programmieren. Um beispielsweise die Reaktion auf einen Klick auf eine Schaltfläche zu programmieren. Sehen Sie sich die Dokumentation für Ihren Browser an, um zu ermitteln, welche Features im Skriptmodell verfügbar sind. Informationen zu Microsoft Internet Explorer finden Sie im Skriptobjektmodell, das im ActiveX SDK verfügbar ist.

Die Dienste des Agents bleiben nur geladen, wenn mindestens eine Clientanwendung mit einer Verbindung besteht. Dies bedeutet, dass der -Agent heruntergefahren wird und alle von Ihnen geladenen Zeichen nicht mehr angezeigt werden, wenn ein Benutzer zwischen Für den Agent aktivierten Webseiten wechselt. Damit der -Agent zwischen Seiten ausgeführt wird (und dadurch ein Zeichen sichtbar bleibt), erstellen Sie einen weiteren Client, der zwischen den Seitenänderungen geladen bleibt. Beispielsweise können Sie ein HTML-Frameset erstellen und ein &lt; OBJECT-Tag &gt; für den -Agent im übergeordneten Frame deklarieren. Sie können dann Skripts für die Seiten erstellen, die Sie in die untergeordneten Frames laden, um in das Skript des übergeordneten Elements zu rufen. Alternativ können Sie auf jeder Seite, die Sie in den untergeordneten Frame laden, auch ein &lt; &gt; OBJECT-Tag hinzufügen. Denken Sie in diesem Fall daran, dass jede Seite ein eigener Client ist. Möglicherweise müssen Sie mit der [**Activate-Methode**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) festlegen, welcher Client die Kontrolle hat, wenn der Benutzer mit der übergeordneten oder untergeordneten Seite interagiert.

 

 
