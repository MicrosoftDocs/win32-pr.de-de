---
title: Zugreifen auf das Steuerelement in Webseiten
description: Zugreifen auf das Steuerelement in Webseiten
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3766475dc798f8f61e98b818fc8e71205bbc72c34f2282098f00b5f03ed3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480736"
---
# <a name="accessing-the-control-in-web-pages"></a>Zugreifen auf das Steuerelement in Webseiten

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Verwenden Sie das HTML-Tag in , um von einer Webseite aus auf die Microsoft-Agent-Dienste <OBJECT> zuzugreifen. <HEAD> oder <BODY> -Element der Seite, das die Microsoft CLSID (Klassenbezeichner) für das Steuerelement angibt. Verwenden Sie außerdem einen CODEBASE-Parameter, um den Speicherort der Microsoft-Agent-Installationsdatei und deren Versionsnummer anzugeben.

Wenn Microsoft Internet Explorer (Version 3.02 oder höher) auf dem System installiert ist, der Microsoft-Agent jedoch noch nicht installiert ist und der Benutzer auf eine Webseite mit dem <OBJECT> Tag mit der Agent-CLSID zugreift, versucht der Browser automatisch, den Agent von der Microsoft-Website herunterzuladen. Anschließend wird der Benutzer gefragt, ob die Installation fortgesetzt werden soll. Wenden Sie sich bei anderen Browsern an den Lieferanten, um Informationen zum Support oder zur Unterstützung von Drittanbietern für ActiveX-Steuerelemente zu erhalten.

Im folgenden Beispiel wird veranschaulicht, wie Sie den CODEBASE-Parameter verwenden, um die englischsprachige Version 2.0 des Microsoft-Agents automatisch herunterzuladen.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Der Agent kann auch von Ihrem eigenen HTTP-Server oder im Rahmen des Installationsprozesses einer Anwendung installiert werden. Um die Installation von Ihrem eigenen HTTP-Server zu unterstützen, müssen Sie das selbstinstallierende Cab .Exe-Datei des Microsoft-Agents veröffentlichen und deren URL im CODEBASE-Tag angeben.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Um den automatischen Download einer Microsoft Agent-Sprachkomponente von einer Webseite zu unterstützen, schließen Sie das Objekttag der Sprachkomponente auf der Seite vor dem Objekttag des -Agent-Steuerelements ein:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

, wobei XXXX durch eine Sprach-ID ersetzt wird. Informationen zu den derzeit unterstützten Sprachen finden Sie auf der Microsoft Agent-Website.

-   Das <OBJECT> -Tag für eine Sprachkomponente muss dem <OBJECT> -Tag für die Microsoft Agent-Kernkomponente vorangestellt werden.
-   Auf demselben Client können mehrere Sprachen installiert werden.
-   Bevor Sie die [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) eines Zeichens festlegen, wird empfohlen, dass Ihr Skript überprüft, ob das gebietsschema des Browsers, das in der [**userLanguage-Eigenschaft**](https://www.bing.com/search?q=**userLanguage**) verfügbar ist, mit der sprache übereinstimmt, die festgelegt wird.

Um andere Sprachversionen des -Agents zu unterstützen, verwenden Sie ein anderes Object-Tag, das die Sprachkomponente angibt. Beachten Sie jedoch, dass der Versuch, mehrere Sprachen gleichzeitig zu installieren, den Benutzer möglicherweise neu starten muss. Die Komponenten der Agent-Sprache können von der Agent-Website mit dem gleichen Verfahren wie für die Agent-Kernkomponente abgerufen werden. Die Verteilungslizenzierung für die Sprachkomponenten wird in der Standard-Agent-Verteilungslizenz behandelt. Um mit der Verwendung eines Zeichens zu beginnen, müssen Sie das Zeichen mithilfe der [**Load-Methode**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) laden. Ein Zeichen kann aus dem lokalen Speicher des Benutzers oder einem HTTP-Server geladen werden. Weitere Informationen zur Syntax zum Laden eines  Zeichens finden Sie unter Load-Methode. Nachdem das Zeichen erfolgreich geladen wurde, können Sie die Methoden, Eigenschaften und Ereignisse verwenden, die vom -Agent-Steuerelement verfügbar gemacht werden, um das Zeichen zu programmieren. Sie können auch die Methoden, Eigenschaften und Ereignisse verwenden, die von Ihrer Programmiersprache und dem Browser verfügbar gemacht werden, um das Zeichen zu programmieren. Beispielsweise, um die Reaktion auf einen Schaltflächenklick zu programmieren. Lesen Sie die Dokumentation für Ihren Browser, um zu ermitteln, welche Features im Skriptmodell verfügbar gemacht werden. Informationen zu Microsoft Internet Explorer finden Sie im Skriptobjektmodell, das im ActiveX SDK verfügbar ist.

Die Dienste des Agents bleiben nur geladen, wenn mindestens eine Clientanwendung mit einer Verbindung vorhanden ist. Dies bedeutet, dass der -Agent heruntergefahren wird und alle von Ihnen geladenen Zeichen ausgeblendet werden, wenn ein Benutzer zwischen Webseiten wechselt, für die der Agent aktiviert ist. Erstellen Sie einen weiteren Client, der zwischen Seitenänderungen geladen bleibt, damit der -Agent zwischen Seiten ausgeführt wird (und dadurch ein Zeichen sichtbar bleibt). Beispielsweise können Sie ein HTML-Frameset erstellen und ein <OBJECT> Tag für den -Agent im übergeordneten Frame deklarieren. Anschließend können Sie ein Skript für die Seiten erstellen, die Sie in die untergeordneten Frames laden, um das Skript des übergeordneten Elements aufzurufen. Alternativ können Sie auch ein Tag auf jeder Seite einschließen, <OBJECT> die Sie in den untergeordneten Frame laden. Beachten Sie in diesem Fall, dass jede Seite ein eigener Client ist. Möglicherweise müssen Sie die [**Activate-Methode**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) verwenden, um festzulegen, welcher Client steuern kann, wann der Benutzer mit der übergeordneten oder untergeordneten Seite interagiert.

 

 