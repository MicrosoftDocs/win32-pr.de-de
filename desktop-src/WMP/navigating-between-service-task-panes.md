---
title: Navigieren zwischen Dienstaufgaben Bereichen
description: Navigieren zwischen Dienstaufgaben Bereichen
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player Online Stores, navigieren
- Online Stores, navigieren
- Geben Sie 2 Online Stores ein, navigieren Sie zu
- Windows Media Player Online Stores, Aufgabenbereiche für Dienste
- Online Stores, Aufgabenbereiche für Dienste
- Typ 2 Online Stores, Dienstaufgaben Bereiche
- Windows Media Player Online Stores, Aufgabenbereiche
- Online Stores, Aufgabenbereiche
- Typ 2 Online Stores, Aufgabenbereiche
- Navigieren zu Typ 2 Online Stores
- Aufgabenbereiche für Windows Media Player, Dienste
- Windows Media Player, Aufgabenbereiche
- Aufgabenbereiche für Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035215f822c67bb40c528f141422977efc8653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310031"
---
# <a name="navigating-between-service-task-panes"></a>Navigieren zwischen Dienstaufgaben Bereichen

Um zwischen Dienstaufgaben Bereichen in Windows Media Player zu navigieren, verwenden Sie die **navigatetaskpaneurl** -Methode, die über das **Window. extern** -Objekt verfügbar ist. Wenn Sie diese Methode verwenden, geben Sie Werte für drei Parameter an:

-   *btrekeyname*. Dies ist der Schlüssel Name des Online Stores. Wenn Sie in einem Online Shop navigieren, verwenden Sie den Schlüsselnamen des aktuellen Stores.
-   *bstrautaskpane*. Diese Zeichenfolge enthält den Namen des Aufgabenbereichs Dienst, zu dem Sie navigieren möchten.
-   *bstrinbiams*. Diese Zeichenfolge enthält die Abfrage Zeichenfolgen-Parameter, die Sie an die URL für die Webseite anfügen möchten, die vom Aufgabenbereich Dienst gehostet wird, zu dem Sie navigieren möchten.

Die Navigation wird von einer von Ihnen erstellten Webseite verwaltet, die als Navigationsseite bezeichnet wird. Die URL für die Navigationsseite wird vom **Navigate** -Element im servicinput Info-Dokument angegeben. Wenn Sie **navigatetaskpaneurl** aufzurufen, öffnet Windows Media Player die Navigationsseite und nicht die Webseite, die von den Elementen **ServiceTask1**, **ServiceTask2** oder **ServiceTask3** angegeben wird. Dabei handelt es sich um die Navigationsseite, die die von *bstrinparameams* angegebene Abfrage Zeichenfolge empfängt. Die Navigationsseite sollte die Regeln enthalten, mit denen bestimmt wird, welcher Inhalt nach der Navigation in einem Dienstaufgaben Bereich angezeigt wird.

Angenommen, Sie möchten, dass Benutzer auf einen Link klicken, um von **ServiceTask1** zu **ServiceTask2** zu navigieren. Zum Erstellen des Links können Sie den folgenden HTML-Code verwenden:


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



Wenn der Benutzer auf den Videolink klickt, wechselt Windows Media Player zu **ServiceTask2** und öffnet die Navigationsseite, wobei die folgende Abfrage Zeichenfolge an die zugehörige URL angehängt wird.


```C++
?From=Music&To=2

```



Der from-Parameter identifiziert die Seite, auf der der Benutzer auf den Link geklickt hat, und der to-Parameter gibt die Nummer des Dienstaufgaben Bereichs an, zu dem er navigieren möchte. (Beachten Sie, dass es keine besonderen Informationen zu diesen Parametern gibt. Sie können beliebige Parameter für beliebige Zwecke verwenden, die Sie auswählen möchten.)

Der folgende Beispielcode zeigt z. b. das **Navigate** -Element in einem serviceInfo-Dokument:


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



Die resultierende URL, die mit der Abfrage Zeichenfolge vervollständigt wird, wird im folgenden Beispiel gezeigt:


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



Der vorangehende Code erstellt einfach eine URL und leitet den Browser an ihn weiter. Zuerst ruft der Code Werte aus der URL-Abfrage Zeichenfolge und der Abfrage Zeichenfolge selbst ab. Er verwendet den Wert des to-Parameters, um zu bestimmen, welche Seite angezeigt werden soll. Anschließend wird die ursprüngliche Abfrage Zeichenfolge an die URL angefügt. Zum Schluss navigiert der Browser mit einer URL, die der folgenden ähnelt:


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



Wenn Sie auf diese Weise eine Navigation ausführen, müssen Sie " [extern. selectedtaskpane](external-selectedtaskpane.md) " angeben, um sicherzustellen, dass die Schaltfläche für die korrekte Aufgabe hervorgehoben ist.

-   **Warnung** Achten Sie darauf, wie Sie Abfrage Zeichen folgen Parameter für die Navigation verwenden.

HtmlView-Webseiten können von allen Benutzern bereitgestellt werden, die eine ASX-Wiedergabeliste erstellen. Dies bedeutet, dass böswillige Websites Abfrage Zeichenfolgen-Werte mithilfe von **navigatetaskpaneurl** an Ihren Online Store übergeben können. Sie müssen diese Möglichkeit planen, um den Online Store sicher zu halten. Wenn Ihr Online Store z. b. einfach einen Abfrage Zeichen folgen Wert für den Benutzer anzeigt, könnte eine böswillige Website einen unerwarteten Text anzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Navigate-Element**](navigate-element.md)
</dt> <dt>

[**Navigation für den Typ 2-Online Speicher**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




