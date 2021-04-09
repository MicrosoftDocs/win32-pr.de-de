---
description: Dieses Thema enthält ein Beispiel für das Schreiben eines Skripts, mit dem Daten über Microsoft Windows HTTP-Dienste (WinHTTP) entweder synchron oder asynchron abgerufen werden.
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: Abrufen von Daten mithilfe eines Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734516cf75f92cc43ab4cb15f22bd97aa803ec33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958669"
---
# <a name="retrieving-data-using-script"></a>Abrufen von Daten mithilfe eines Skripts

Dieses Thema enthält ein Beispiel für das Schreiben eines Skripts, mit dem Daten über Microsoft Windows HTTP-Dienste (WinHTTP) entweder synchron oder asynchron abgerufen werden. Die in diesem Beispiel dargestellten Konzepte stellen die Grundlage für das Schreiben von Client-oder Server Anwendungen mittlerer Ebene dar, die über das HTTP-Protokoll Zugriff auf Daten benötigen.

-   [Voraussetzungen und Anforderungen](#prerequisites-and-requirements)
-   [Synchrones Abrufen von Daten](#retrieving-data-synchronously)
-   [Asynchrones Abrufen von Daten](#retrieving-data-asynchronously)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites-and-requirements"></a>Voraussetzungen und Anforderungen

Zusätzlich zu den in Microsoft JScript funktionierenden Kenntnissen erfordert dieses Beispiel Folgendes:

-   Die aktuelle Version des Microsoft Windows Software Development Kit (SDK).
-   Das Proxy Konfigurationstool zum Einrichten der Proxy Einstellungen für Microsoft Windows HTTP-Dienste (WinHTTP), wenn die Internetverbindung über einen Proxy Server erfolgt. Weitere Informationen finden Sie unter [ProxyCfg.exe, einem Proxy Konfigurations Tool](proxycfg-exe--a-proxy-configuration-tool.md).
-   Eine Vertrautheit mit der [Netzwerkterminologie](network-terminology.md) und den Konzepten.

## <a name="retrieving-data-synchronously"></a>Synchrones Abrufen von Daten

**Gehen Sie folgendermaßen vor, um ein Skript zu erstellen, mit dem der Text von einer Webseite synchron abgerufen wird:**

1.  Öffnen Sie einen Text-Editor.
2.  Kopieren Sie den folgenden Code in den Text-Editor.

    ```JScript
    function getText(strURL)
    {
        var strResult;
        
        try
        {
            // Create the WinHTTPRequest ActiveX Object.
            var WinHttpReq = new ActiveXObject(
                                      "WinHttp.WinHttpRequest.5.1");
            
            //  Create an HTTP request.
            var temp = WinHttpReq.Open("GET", strURL, false);

            //  Send the HTTP request.
            WinHttpReq.Send();
            
            //  Retrieve the response text.
            strResult = WinHttpReq.ResponseText;
        }
        catch (objError)
        {
            strResult = objError + "\n"
            strResult += "WinHTTP returned error: " + 
                (objError.number & 0xFFFF).toString() + "\n\n";
            strResult += objError.description;
        }
        
        //  Return the response text.
        return strResult;
    }

    WScript.Echo(getText("https://www.microsoft.com/default.htm"));
    ```

    

3.  Speichern Sie die Datei als "Retrieve.js".
4.  Geben Sie an einer Eingabeaufforderung "Cscript Retrieve.js" ein, und drücken Sie die EINGABETASTE.

Sie verfügen jetzt über ein Skript, das ein [**WinHttpRequest**](winhttprequest.md) -Objekt verwendet, um den HTML-Quellcode für die Webseite unter zu erhalten https://www.microsoft.com . Möglicherweise müssen Sie einige Sekunden warten, bis der Code angezeigt wird.

Die Anwendung enthält nur eine Funktion, "gettext". Die erste Zeile des Skripts erstellt das [**WinHttpRequest**](winhttprequest.md) -Objekt.


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



Wenn die JScript-Engine auf diese Zeile stößt, wird eine Instanz dieses Objekts erstellt. Wenn Sie die Fehlermeldung "ActiveX Component Can Can Create Object" (ActiveX-Komponente kann nicht erstellt werden) erhalten, ist die WinHttp.dll in dieser Zeile höchstwahrscheinlich nicht ordnungsgemäß registriert oder nicht auf dem System vorhanden.

Die nächste Zeile des Skripts Ruft die [**Open**](iwinhttprequest-open.md) -Methode auf.


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



Drei Parameter geben an, welches [*http-Verb*](glossary.md) verwendet werden soll, den Namen der Ressource und ob WinHTTP synchron oder asynchron verwendet werden soll. In diesem Beispiel verwendet die-Methode das *http-Verb*"Get" zum Abrufen von Daten aus https://www.microsoft.com . Wenn Sie für den letzten Parameter **false** angeben, wird festgelegt, dass die Transaktion synchron erfolgt. Die [**Open**](iwinhttprequest-open.md) -Methode stellt keine Verbindung mit der Ressource her, wie der Name vermuten könnte. Stattdessen werden die internen Datenstrukturen initialisiert, die Informationen über die Sitzung, die Verbindung und die Anforderung verwalten.

Die [**Send**](iwinhttprequest-send.md) -Methode assembliert die Anforderungs Header und sendet die Anforderung. Wenn Sie im synchronen Modus aufgerufen wird, wartet die [**Send**](iwinhttprequest-send.md) -Methode auch auf eine Antwort, bevor die Anwendung fortgesetzt werden kann.


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



Nach dem Senden der Anforderung gibt das Skript den Wert der [**responseText**](iwinhttprequest-responsetext.md) -Eigenschaft des [**WinHttpRequest**](winhttprequest.md) -Objekts zurück. Diese Eigenschaft enthält den Entitäts Text der Antwort, in diesem Fall die Quelle eines Dokuments.


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



Die Ausführung des Skripts wird angehalten, während der gesamte Text der Ressource abgerufen wird. Der Ressourcen Text wird von der Funktion zurückgegeben und angezeigt.

Das [**WinHttpRequest**](winhttprequest.md) -Objekt stellt sicher, dass alle internen Ressourcen, die für die HTTP-Transaktion zugeordnet sind, freigegeben werden.

## <a name="retrieving-data-asynchronously"></a>Asynchrones Abrufen von Daten

Das asynchrone Abrufen von Daten mithilfe von WinHTTP ähnelt dem synchronen Abrufen von Daten. Ändern Sie das Skript aus dem vorherigen Abschnitt, indem Sie zwei kleine Änderungen vornehmen.

1.  Legen Sie den dritten Parameter der [**Open**](iwinhttprequest-open.md) -Methode auf "true" anstelle von "false" fest, um anzugeben, dass WinHTTP-Methoden asynchron ausgeführt werden sollen.
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  Rufen Sie die [**WaitForResponse**](iwinhttprequest-waitforresponse.md) -Methode auf, bevor Sie auf die Response [**Text**](iwinhttprequest-responsetext.md) -Eigenschaft zugreifen, um sicherzustellen, dass die gesamte Antwort empfangen wurde.
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

Der Hauptvorteil der asynchronen Verwendung von WinHTTP im Skript besteht darin, dass die [**Send**](iwinhttprequest-send.md) -Methode sofort zurückgegeben wird. Die Anforderung wird von einem Arbeits Thread vorbereitet und gesendet. Dadurch kann Ihre Anwendung andere Aufgaben ausführen, während Sie auf die Antwort wartet. Bevor Sie versuchen, auf die Antwort zuzugreifen, stellen Sie sicher, dass die gesamte Antwort empfangen wurde, indem Sie die [**WaitForResponse**](iwinhttprequest-waitforresponse.md) -Methode aufrufen. Andernfalls kann ein Fehler auftreten.

Die [**WaitForResponse**](iwinhttprequest-waitforresponse.md) -Methode kann auch verwendet werden, um einen Timeout Wert für die Transaktion anzugeben. Mit einem optionalen Parameter können Sie den Timeout Wert in Sekunden angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[HTTP/1.1-Anforderung für Kommentare (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



