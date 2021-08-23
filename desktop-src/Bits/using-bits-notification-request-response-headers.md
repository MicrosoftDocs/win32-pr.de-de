---
title: Verwenden von BITS-Benachrichtigungsanforderungs-/Antwortheadern
description: BITS kann den Speicherort der Uploaddatei (als Verweis) an Ihre Serveranwendung oder die Uploaddatei im Text der Anforderung (nach Wert) senden.
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 3db568f483468cbc92474f24f830da5bf1be94a2165cbb69a2d1751cc58965dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021068"
---
# <a name="using-bits-notification-requestresponse-headers"></a>Verwenden von BITS-Benachrichtigungsanforderungs-/Antwortheadern

BITS kann den Speicherort der Uploaddatei (als Verweis) an Ihre Serveranwendung oder die Uploaddatei im Text der Anforderung (nach Wert) senden. Um anzugeben, wie BITS die Uploaddatei an Ihre Serveranwendung sendet, legen Sie die IIS-Metabasiseigenschaft [**BITSServerNotificationType fest.**](bits-iis-extension-properties.md) Wenn Sie als Verweis angeben, übergibt BITS den Speicherort der Datei im BITS-Request-DataFile-Name-Header. Um eine Antwort zu senden, erstellen und schreiben Sie Ihre Antwort in die Datei, die im BITS-Response-DataFile-Name-Header angegeben ist.

Serveranwendungen, die dieselbe Antwort an viele Clients senden, sollten als Verweis verwenden, sodass es nur eine Kopie der Antwort auf dem Server gibt. Beispielsweise würde der Client in einer Softwareupdateanwendung seine Softwarekonfiguration in die Serveranwendung hochladen. Die Serveranwendung bestimmt, welches Paket der Client benötigt, und sendet die URL des Pakets an BITS. Bits lädt dann das Paket als Antwort herunter.

Serveranwendungen, die eindeutige Antworten für jeden Client generieren, sollten als Wert verwenden. Beispielsweise müsste eine Serveranwendung, die den Erwerb von Musikdateien unterstützt, eine signierte Musikdatei an den Client senden. Da die signierte Musikdatei für den Client eindeutig ist, wird sie von der Serveranwendung nicht auf dem Server gespeichert. Der Wert ist auch nützlich für eine Anwendung, die bereits geschrieben wurde, um Webclientdaten direkt zu akzeptieren.

Weitere Informationen zu den Anforderungs- und Antwortheadern, die zwischen BITS und Ihrer Serveranwendung verwendet werden, finden Sie unter Notification Protocol for Server Applications ( Benachrichtigungsprotokoll [für Serveranwendungen](notification-protocol-for-server-applications.md)).

Das folgende JavaScript-Beispiel zeigt, wie sie auf die Anforderungs- und Antwortdateien in einer Serveranwendung zugreifen, die als Verweisbenachrichtigung verwendet (BITS übergibt den Speicherort der Dateien in den Headern).


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



Wenn Sie eine andere Antwortdatei als die in BITS-Response-DataFile-Name angegebene datei verwenden möchten, rufen Sie die **Response.AddHeader-Methode** auf, um die BITS-Static-Response-URL hinzuzufügen, wie im folgenden Beispiel gezeigt. Wenn Sie eine andere Antwortdatei angeben, erstellen Sie nicht die in BITS-Response-DataFile-Name angegebene Antwortdatei.


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




