---
title: Navigieren zwischen Dienstaufgabenbereichen
description: Navigieren zwischen Dienstaufgabenbereichen
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player Onlineshops, Navigieren
- Onlineshops, Navigieren
- Geben Sie 2 Onlineshops ein, und navigieren Sie
- Windows Media Player Onlineshops, Dienstaufgabenbereiche
- Onlineshops, Dienstaufgabenbereiche
- Geben Sie 2 Onlineshops, Dienstaufgabenbereiche ein.
- Windows Media Player Onlineshops, Aufgabenbereiche
- Onlineshops, Aufgabenbereiche
- Geben Sie 2 Onlineshops und Aufgabenbereiche ein.
- Navigieren in 2 Onlineshops
- Windows Media Player, Dienstaufgabenbereiche
- Windows Media Player, Aufgabenbereiche
- Dienstaufgabenbereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f54a82f2637fe11b0a2a7703cc241c47e799999a89b56ba8ba19c079b7393de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647580"
---
# <a name="navigating-between-service-task-panes"></a>Navigieren zwischen Dienstaufgabenbereichen

Zum Navigieren zwischen Dienstaufgabenbereichen in Windows Media Player verwenden Sie die **NavigateTaskPaneURL-Methode,** die mit dem **window.external-Objekt** verfügbar ist. Wenn Sie diese Methode verwenden, geben Sie Werte für drei Parameter an:

-   *bstrKeyName*. Dies ist der Schlüsselname des Onlineshops. Verwenden Sie beim Navigieren innerhalb eines Onlineshops den Schlüsselnamen des aktuellen Speichers.
-   *bstrTaskPane*. Diese Zeichenfolge enthält den Namen des Dienstaufgabenbereichs, zu dem Sie navigieren möchten.
-   *bstrParams*. Diese Zeichenfolge enthält die Abfragezeichenfolgenparameter, die Sie an die URL für die Webseite anfügen möchten, die vom Aufgabenbereich des Diensts gehostet wird, zu dem Sie navigieren möchten.

Die Navigation wird von einer Webseite verwaltet, die Sie erstellen, die als Navigationsseite bezeichnet wird. Die URL für die Navigationsseite wird vom **Navigate-Element** im ServiceInfo-Dokument angegeben. Wenn Sie **NavigateTaskPaneURL** aufrufen, öffnet Windows Media Player die Navigationsseite, nicht die Webseite, die von den **Elementen ServiceTask1,** **ServiceTask2** oder **ServiceTask3** angegeben wird. Dies ist die Navigationsseite, die die durch *bstrParams* angegebene Abfragezeichenfolge empfängt. Die Navigationsseite sollte die Regeln enthalten, die bestimmen, welcher Inhalt nach der Navigation in einem Dienstaufgabenbereich angezeigt wird.

Angenommen, Sie möchten, dass Benutzer auf einen Link klicken, um von **ServiceTask1** zu **ServiceTask2** zu navigieren. Sie können den folgenden HTML-Code verwenden, um den Link zu erstellen:


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



Wenn der Benutzer auf den Link Video klickt, wechselt Windows Media Player zu **ServiceTask2,** öffnet die Navigationsseite und fügt die folgende Abfragezeichenfolge an die URL an.


```C++
?From=Music&To=2

```



Der From-Parameter identifiziert die Seite, von der aus der Benutzer auf den Link geklickt hat, und der To-Parameter gibt die Nummer des Dienstaufgabenbereichs an, zu dem er navigieren möchte. (Beachten Sie, dass diese Parameter nichts Besonderes sind. Sie können beliebige Parameter für beliebige Zwecke verwenden.)

Der folgende Beispielcode zeigt beispielsweise das **Navigate-Element** in einem ServiceInfo-Dokument:


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



Die resultierende URL, die mit der Abfragezeichenfolge vollständig ist, wird im folgenden Beispiel gezeigt:


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



Der folgende Beispielcode zeigt die Navigationsseite:


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



Der vorangehende Code erstellt einfach eine URL und leitet den Browser darauf um. Zunächst ruft der Code To-Werte aus der URL-Abfragezeichenfolge und der Abfragezeichenfolge selbst ab. Er verwendet den Wert des To-Parameters, um zu bestimmen, welche Seite angezeigt werden soll. Anschließend wird die ursprüngliche Abfragezeichenfolge an die URL angefügt. Schließlich navigiert er über eine URL, die der folgenden ähnelt:


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



Wenn Sie die Navigation auf diese Weise durchführen, müssen Sie [External.SelectedTaskPane](external-selectedtaskpane.md) angeben, um sicherzustellen, dass die richtige Aufgabenschaltfläche hervorgehoben ist.

-   **Warnung** Achten Sie darauf, wie Sie Abfragezeichenfolgenparameter für die Navigation verwenden.

HTMLView-Webseiten können von allen Personen bereitgestellt werden, die eine ASX-Wiedergabeliste erstellen. Dies bedeutet, dass schädliche Websites mit **NavigateTaskPaneURL** Abfragezeichenfolgenwerte an Ihren Onlineshop übergeben können. Sie müssen diese Möglichkeit einplanen, um den Schutz Ihres Onlineshops zu gewährleisten. Wenn Ihr Onlineshop dem Benutzer beispielsweise einfach einen Abfragezeichenfolgenwert anzeigt, kann eine schädliche Website unerwarteten Text anzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Navigate-Element**](navigate-element.md)
</dt> <dt>

[**Navigation für Onlineshops vom Typ 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




