---
title: Verwenden von Bits-Benachrichtigungs Anforderung/Antwort-Headern
description: Bits können den Speicherort der Uploaddatei (als Verweis) an Ihre Serveranwendung senden, oder Sie können die Uploaddatei im Anforderungs Text (nach Wert) senden.
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dcbee8b82d96a4f13db0ae4de6441e9df40ce83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206297"
---
# <a name="using-bits-notification-requestresponse-headers"></a>Verwenden von Bits-Benachrichtigungs Anforderung/Antwort-Headern

Bits können den Speicherort der Uploaddatei (als Verweis) an Ihre Serveranwendung senden, oder Sie können die Uploaddatei im Anforderungs Text (nach Wert) senden. Legen Sie die IIS-Metabasiseigenschaft " [**bitsservernotificationtype**](bits-iis-extension-properties.md)" fest, um anzugeben, wie Bits die Uploaddatei an die Serveranwendung sendet. Wenn Sie als Verweis angeben, übergibt Bits den Speicherort der Datei im Header "Bits-Request-DataFile-Name". Um eine Antwort zu senden, erstellen und schreiben Sie die Antwort auf die Datei, die im Header Bits-Response-DataFile-Name angegeben ist.

Server Anwendungen, die dieselbe Antwort an viele Clients senden, sollten als Verweis verwendet werden, sodass nur eine Kopie der Antwort auf dem Server vorhanden ist. Beispielsweise würde der Client in einer Software Update Anwendung seine Softwarekonfiguration in die Serveranwendung hochladen. Die Serveranwendung bestimmt, welches Paket der Client benötigt, und sendet die URL des Pakets an Bits. Bits lädt das Paket dann als Antwort herunter.

Server Anwendungen, die eindeutige Antworten für jeden Client generieren, sollten als Wert verwenden. Beispielsweise muss eine Serveranwendung, die den Erwerb von Musikdateien unterstützt, eine signierte Musikdatei an den Client senden. Da die signierte Musikdatei für den Client eindeutig ist, wird Sie von der Serveranwendung nicht auf dem Server gespeichert. Als Wert ist auch nützlich für eine Anwendung, die bereits geschrieben wurde, um WebClient Daten direkt zu akzeptieren.

Ausführliche Informationen zu den Anforderungs-und Antwort Headern, die zwischen Bits und der Serveranwendung verwendet werden, finden Sie unter [Benachrichtigungs Protokoll für Server Anwendungen](notification-protocol-for-server-applications.md).

Im folgenden JavaScript-Beispiel wird gezeigt, wie Sie auf die Anforderungs-und Antwort Dateien in einer Serveranwendung zugreifen, die per Verweis Benachrichtigung verwendet (Bits übergibt den Speicherort der Dateien in den Headern).


```JavaScript
  var fso = new ActiveXObject ("Scripting.FileSystemObject")
  var requestFileName = Request.ServerVariables ("HTTP_BITS-Request-DataFile-Name")
  var responseFileName = Request.ServerVariables ("HTTP_BITS-Response-DataFile-Name")
  var requestStream
  var responseStream
  var ForReading = 1
  var ForWriting = 2
  var TristateUseDefault = -2

  //Open the upload data file as text stream for reading.
  requestStream = fso.OpenTextFile(requestFileName, ForReading, false, TristateUseDefault);

  //Do something with the uploaded data.

  //Close the upload stream.
  requestStream.Close()

  //Open response data file as text stream for writing.
  responseStream = fso.OpenTextFile(responseFileName, ForWriting, true, TristateUseDefault);

  //Write a response to the response file.

  //Close the response text stream
  responseStream.Close()
```



Wenn Sie eine andere Antwortdatei als die in Bits-Response-DataFile-Name angegebene Antwortdatei verwenden möchten, müssen Sie die Methode **Response. AddHeader** zum Hinzufügen der Bits-static-Response-URL wie im folgenden Beispiel gezeigt verwenden. Wenn Sie eine andere Antwortdatei angeben, erstellen Sie die in Bits-Response-DataFile-Name angegebene Antwortdatei nicht.


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




