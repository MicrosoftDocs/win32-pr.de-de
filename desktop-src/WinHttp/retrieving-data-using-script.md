---
description: Dieses Thema enthält ein Beispiel für das Schreiben eines Skripts, das Daten über Microsoft Windows HTTP Services (WinHTTP) entweder synchron oder asynchron erhält.
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: Abrufen von Daten mithilfe eines Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e018aa680808feddc021c7c03937d085b0d0f787c3213720cbb5e94a46a85c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133063"
---
# <a name="retrieving-data-using-script"></a>Abrufen von Daten mithilfe eines Skripts

Dieses Thema enthält ein Beispiel für das Schreiben eines Skripts, das Daten über Microsoft Windows HTTP Services (WinHTTP) entweder synchron oder asynchron erhält. Die in diesem Beispiel veranschaulichten Konzepte bilden die Grundlage für das Schreiben von Client- oder Serveranwendungen der mittleren Ebene, die zugriff auf Daten mithilfe des HTTP-Protokolls benötigen.

-   [Voraussetzungen und Anforderungen](#prerequisites-and-requirements)
-   [Synchrones Abrufen von Daten](#retrieving-data-synchronously)
-   [Asynchrones Abrufen von Daten](#retrieving-data-asynchronously)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites-and-requirements"></a>Voraussetzungen und Anforderungen

Zusätzlich zu den Kenntnissen von Microsoft JScript erfordert dieses Beispiel Folgendes:

-   Die aktuelle Version des Microsoft Windows Software Development Kit (SDK).
-   Das Proxykonfigurationstool zum Einrichten der Proxyeinstellungen für Microsoft Windows HTTP Services (WinHTTP), wenn Ihre Verbindung mit dem Internet über einen Proxyserver hergestellt wird. Weitere Informationen finden Sie unter [ProxyCfg.exe, einem Proxykonfigurationstool.](proxycfg-exe--a-proxy-configuration-tool.md)
-   Vertrautheit mit [Netzwerkterminologie](network-terminology.md) und -konzepten.

## <a name="retrieving-data-synchronously"></a>Synchrones Abrufen von Daten

**Gehen Sie wie folgt vor, um ein Skript zu erstellen, das den Text von einer Webseite synchron erhält:**

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
4.  Geben Sie an einer Eingabeaufforderung "cscript Retrieve.js" ein, und drücken Sie die EINGABETASTE.

Sie verfügen jetzt über ein Skript, das ein [**WinHttpRequest-Objekt**](winhttprequest.md) verwendet, um den HTML-Quellcode für die Webseite unter https://www.microsoft.com abzurufen. Möglicherweise müssen Sie einige Sekunden warten, bis der Code angezeigt wird.

Die Anwendung enthält nur eine Funktion, "getText". In der ersten Zeile des Skripts wird das [**WinHttpRequest-Objekt**](winhttprequest.md) erstellt.


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



Wenn die JScript-Engine diese Zeile erkennt, wird eine Instanz dieses Objekts erstellt. Wenn Sie die Fehlermeldung "ActiveX Komponente kann kein Objekt erstellen" erhalten, wurde in dieser Zeile höchstwahrscheinlich der WinHttp.dll nicht ordnungsgemäß registriert oder ist auf dem System nicht vorhanden.

Die nächste Zeile des Skripts ruft die [**Open-Methode auf.**](iwinhttprequest-open.md)


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



Drei Parameter geben an, welches [*HTTP-Verb*](glossary.md) verwendet werden soll, den Namen der Ressource und ob WinHTTP synchron oder asynchron verwendet werden soll. In diesem Beispiel verwendet die -Methode das *HTTP-Verb*"GET", um Daten aus https://www.microsoft.com abzurufen. Die Angabe von **FALSE** für den letzten Parameter bestimmt, dass die Transaktion synchron erfolgt. Die [**Open-Methode**](iwinhttprequest-open.md) stellt keine Verbindung mit der Ressource her, wie der Name möglicherweise impliziert. Stattdessen werden die internen Datenstrukturen initialisiert, die Informationen zur Sitzung, Verbindung und Anforderung verwalten.

Die [**Send-Methode**](iwinhttprequest-send.md) stellt die Anforderungsheader zusammen und sendet die Anforderung. Beim Aufruf im synchronen Modus wartet die [**Send-Methode**](iwinhttprequest-send.md) auch auf eine Antwort, bevor die Anwendung fortgesetzt werden kann.


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



Nach dem Senden der Anforderung gibt das Skript den Wert der [**ResponseText-Eigenschaft**](iwinhttprequest-responsetext.md) des [**WinHttpRequest-Objekts**](winhttprequest.md) zurück. Diese Eigenschaft enthält den Entitätstext der Antwort, in diesem Fall die Quelle eines Dokuments.


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



Die Ausführung des Skripts wird angehalten, während der gesamte Text der Ressource abgerufen wird. Der Ressourcentext wird von der Funktion zurückgegeben und angezeigt.

Das [**WinHttpRequest-Objekt**](winhttprequest.md) stellt sicher, dass alle internen Ressourcen, die für die HTTP-Transaktion zugeordnet sind, freigegeben werden.

## <a name="retrieving-data-asynchronously"></a>Asynchrones Abrufen von Daten

Das asynchrone Abrufen von Daten mit WinHTTP ähnelt dem synchronen Abrufen von Daten. Ändern Sie das Skript aus dem vorherigen Abschnitt, indem Sie zwei kleine Änderungen vornehmen.

1.  Legen Sie den dritten Parameter der [**Open-Methode**](iwinhttprequest-open.md) auf "true" anstelle von "false" fest, um anzugeben, dass WinHTTP-Methoden asynchron ausgeführt werden sollen.
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  Rufen Sie die [**WaitForResponse-Methode**](iwinhttprequest-waitforresponse.md) auf, bevor Sie auf die [**ResponseText-Eigenschaft**](iwinhttprequest-responsetext.md) zugreifen, um sicherzustellen, dass die gesamte Antwort empfangen wurde.
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

Der Hauptvorteil bei der asynchronen Verwendung von WinHTTP im Skript besteht darin, dass die [**Send-Methode**](iwinhttprequest-send.md) sofort zurückgibt. Die Anforderung wird von einem Arbeitsthread vorbereitet und gesendet. Dadurch kann Ihre Anwendung andere Dinge erledigen, während sie auf die Antwort wartet. Bevor Sie versuchen, auf die Antwort zuzugreifen, stellen Sie sicher, dass die gesamte Antwort empfangen wurde, indem Sie die [**WaitForResponse-Methode**](iwinhttprequest-waitforresponse.md) aufrufen. Andernfalls kann ein Fehler auftreten.

Die [**WaitForResponse-Methode**](iwinhttprequest-waitforresponse.md) kann auch verwendet werden, um einen Time out-Wert für die Transaktion anzugeben. Mit einem optionalen Parameter können Sie den Time out-Wert in Sekunden angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[HTTP/1.1-Anforderung für Kommentare (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



