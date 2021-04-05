---
title: Zugreifen auf das Steuerelement in Webseiten
description: Zugreifen auf das Steuerelement in Webseiten
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a965d73f7277b2b4a62c08a949782488f1e4dba4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725192"
---
# <a name="accessing-the-control-in-web-pages"></a>Zugreifen auf das Steuerelement in Webseiten

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Um von einer Webseite aus auf die Microsoft-Agent-Dienste zuzugreifen, verwenden Sie das HTML- <OBJECT> Tag innerhalb des <HEAD> oder <BODY> -Element der Seite, das die Microsoft CLSID (Klassen Bezeichner) für das-Steuerelement angibt. Verwenden Sie außerdem einen CodeBase-Parameter, um den Speicherort der Installationsdatei des Microsoft-Agents und deren Versionsnummer anzugeben.

Wenn Microsoft Internet Explorer (Version 3,02 oder höher) auf dem System installiert ist, der Microsoft-Agent aber noch nicht installiert ist und der Benutzer auf eine Webseite <OBJECT> mit der Agent-CLSID zugreift, wird vom Browser automatisch versucht, den Agent von der Microsoft-Website herunterzuladen. Anschließend wird der Benutzer gefragt, ob die Installation fortgesetzt werden soll. Wenden Sie sich für andere Browser an den Lieferanten, um Informationen zur Unterstützung oder zum Support von Drittanbietern für ActiveX-Steuerelemente zu erhalten

Im folgenden Beispiel wird veranschaulicht, wie Sie den CodeBase-Parameter verwenden, um die englische Sprachversion 2,0 des Microsoft-Agents automatisch herunterzuladen.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Der-Agent kann auch über ihren eigenen http-Server oder als Teil des Installationsvorgangs einer Anwendung installiert werden. Um die Installation von einem eigenen http-Server zu unterstützen, müssen Sie den Microsoft-Agent selbst installationscab veröffentlichen. Exe-Datei und geben Sie Ihre URL im CodeBase-Tag an.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Um das automatische Herunterladen einer Microsoft-Agent-Sprachkomponente von einer Webseite zu unterstützen, fügen Sie das Objekttag der Sprachkomponente auf der Seite vor dem agentsteuerungsobjekt ein:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

wobei xxxx durch eine Sprach-ID ersetzt wird. Informationen zu den derzeit unterstützten Sprachen finden Sie auf der Website des Microsoft-Agents.

-   Das- <OBJECT> Tag für eine Sprachkomponente muss dem- <OBJECT> Tag für die Microsoft-Agent-Kernkomponente vorangestellt sein.
-   Auf demselben Client können mehrere Sprachen installiert werden.
-   Vor dem Festlegen der [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) eines Zeichens wird empfohlen, dass das Skript überprüft, ob das Gebiets Schema des Browsers, das in der [**UserLanguage**](https://www.bing.com/search?q=**userLanguage**) -Eigenschaft verfügbar ist, mit der Sprache übereinstimmt, die festgelegt wird.

Um andere Sprachversionen des-Agents zu unterstützen, verwenden Sie ein anderes Objekttag, das die Sprachkomponente angibt. Beachten Sie jedoch, dass beim Versuch, mehrere Sprachen gleichzeitig zu installieren, der Benutzer möglicherweise einen Neustart erfordert. Die-Agent-Sprachkomponenten können von der Agent-Website abgerufen werden, indem das gleiche Verfahren wie für die agentkernkomponente verwendet wird. Die Verteilungs Lizenzierung für die Sprachkomponenten wird in der Standard-Agent-Verteilungs Lizenz behandelt. Um mit der Verwendung eines Zeichens zu beginnen, müssen Sie das Zeichen mit der [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) -Methode laden. Ein Zeichen kann aus dem lokalen Speicher des Benutzers oder einem HTTP-Server geladen werden. Weitere Informationen zur Syntax zum Laden eines Zeichens finden Sie unter **Load** -Methode. Nachdem das Zeichen erfolgreich geladen wurde, können Sie die Methoden, Eigenschaften und Ereignisse verwenden, die vom agentsteuerelement verfügbar gemacht werden, um das Zeichen zu programmieren. Sie können auch die Methoden, Eigenschaften und Ereignisse verwenden, die von ihrer Programmiersprache und dem Browser verfügbar gemacht werden, um das Zeichen zu programmieren. beispielsweise, um die Reaktion auf einen Schaltflächen Klick zu programmieren. Sehen Sie sich die Dokumentation für Ihren Browser an, um zu bestimmen, welche Features im Skript Modell verfügbar gemacht werden. Informationen zu Microsoft Internet Explorer finden Sie im Skript Objektmodell, das im ActiveX SDK verfügbar ist.

Die Dienste des Agents bleiben nur dann geladen, wenn mindestens eine Client Anwendung mit einer Verbindung vorhanden ist. Dies bedeutet Folgendes: Wenn ein Benutzer zwischen den Webseiten mit aktiviertem Agent wechselt, wird der-Agent heruntergefahren, und alle geladenen Zeichen werden nicht mehr angezeigt. Erstellen Sie einen weiteren Client, der zwischen Seiten Änderungen geladen bleibt, damit der Agent zwischen den Seiten ausgeführt wird (und damit ein Zeichen sichtbar bleibt). Beispielsweise können Sie ein HTML-Frameset erstellen und ein <OBJECT> Tag für den-Agent im übergeordneten Frame deklarieren. Sie können dann Skripts für die Seiten erstellen, die Sie in den untergeordneten Frame (en) laden, um das übergeordnete Skript aufzurufen. Alternativ dazu können Sie auch ein <OBJECT> Tag auf jeder Seite einschließen, die Sie in den untergeordneten Rahmen laden. Beachten Sie in diesem Fall, dass es sich bei jeder Seite um einen eigenen Client handelt. Möglicherweise müssen Sie die Methode [**aktivieren**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) verwenden, um festzulegen, welcher Client Steuern soll, wenn der Benutzer mit der übergeordneten oder der untergeordneten Seite interagiert.

 

 