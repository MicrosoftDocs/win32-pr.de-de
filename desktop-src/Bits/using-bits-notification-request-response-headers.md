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
# <a name="using-bits-notification-requestresponse-headers"></a><span data-ttu-id="5233f-103">Verwenden von Bits-Benachrichtigungs Anforderung/Antwort-Headern</span><span class="sxs-lookup"><span data-stu-id="5233f-103">Using BITS Notification Request/Response Headers</span></span>

<span data-ttu-id="5233f-104">Bits können den Speicherort der Uploaddatei (als Verweis) an Ihre Serveranwendung senden, oder Sie können die Uploaddatei im Anforderungs Text (nach Wert) senden.</span><span class="sxs-lookup"><span data-stu-id="5233f-104">BITS can send the location of the upload file (by reference) to your server application or it can send the upload file in the body of the request (by value).</span></span> <span data-ttu-id="5233f-105">Legen Sie die IIS-Metabasiseigenschaft " [**bitsservernotificationtype**](bits-iis-extension-properties.md)" fest, um anzugeben, wie Bits die Uploaddatei an die Serveranwendung sendet.</span><span class="sxs-lookup"><span data-stu-id="5233f-105">To specify how BITS sends the upload file to your server application, set the IIS metabase property, [**BITSServerNotificationType**](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="5233f-106">Wenn Sie als Verweis angeben, übergibt Bits den Speicherort der Datei im Header "Bits-Request-DataFile-Name".</span><span class="sxs-lookup"><span data-stu-id="5233f-106">If you specify by reference, BITS passes the location of the file in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="5233f-107">Um eine Antwort zu senden, erstellen und schreiben Sie die Antwort auf die Datei, die im Header Bits-Response-DataFile-Name angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5233f-107">To send a reply, create and write your response to the file specified in the BITS-Response-DataFile-Name header.</span></span>

<span data-ttu-id="5233f-108">Server Anwendungen, die dieselbe Antwort an viele Clients senden, sollten als Verweis verwendet werden, sodass nur eine Kopie der Antwort auf dem Server vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5233f-108">Server applications that send the same reply to many clients should use by reference, so there is only one copy of the reply on the server.</span></span> <span data-ttu-id="5233f-109">Beispielsweise würde der Client in einer Software Update Anwendung seine Softwarekonfiguration in die Serveranwendung hochladen.</span><span class="sxs-lookup"><span data-stu-id="5233f-109">For example, in a software update application, the client would upload its software configuration to the server application.</span></span> <span data-ttu-id="5233f-110">Die Serveranwendung bestimmt, welches Paket der Client benötigt, und sendet die URL des Pakets an Bits.</span><span class="sxs-lookup"><span data-stu-id="5233f-110">The server application determines which package the client needs and sends the URL of the package to BITS.</span></span> <span data-ttu-id="5233f-111">Bits lädt das Paket dann als Antwort herunter.</span><span class="sxs-lookup"><span data-stu-id="5233f-111">Then, BITS downloads the package as the reply.</span></span>

<span data-ttu-id="5233f-112">Server Anwendungen, die eindeutige Antworten für jeden Client generieren, sollten als Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="5233f-112">Server applications that generate unique replies for each client should use by value.</span></span> <span data-ttu-id="5233f-113">Beispielsweise muss eine Serveranwendung, die den Erwerb von Musikdateien unterstützt, eine signierte Musikdatei an den Client senden.</span><span class="sxs-lookup"><span data-stu-id="5233f-113">For example, a server application that supports the purchase of music files would need to send a signed music file to the client.</span></span> <span data-ttu-id="5233f-114">Da die signierte Musikdatei für den Client eindeutig ist, wird Sie von der Serveranwendung nicht auf dem Server gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5233f-114">Because the signed music file is unique to the client, the server application would not store it on the server.</span></span> <span data-ttu-id="5233f-115">Als Wert ist auch nützlich für eine Anwendung, die bereits geschrieben wurde, um WebClient Daten direkt zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="5233f-115">By value is also useful for an application that is already written to accept web client data directly.</span></span>

<span data-ttu-id="5233f-116">Ausführliche Informationen zu den Anforderungs-und Antwort Headern, die zwischen Bits und der Serveranwendung verwendet werden, finden Sie unter [Benachrichtigungs Protokoll für Server Anwendungen](notification-protocol-for-server-applications.md).</span><span class="sxs-lookup"><span data-stu-id="5233f-116">For details on the request and response headers used between BITS and your server application, see [Notification Protocol for Server Applications](notification-protocol-for-server-applications.md).</span></span>

<span data-ttu-id="5233f-117">Im folgenden JavaScript-Beispiel wird gezeigt, wie Sie auf die Anforderungs-und Antwort Dateien in einer Serveranwendung zugreifen, die per Verweis Benachrichtigung verwendet (Bits übergibt den Speicherort der Dateien in den Headern).</span><span class="sxs-lookup"><span data-stu-id="5233f-117">The following JavaScript example shows how to access the request and response files in a server application that uses by reference notification (BITS passes the location of the files in the headers).</span></span>


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



<span data-ttu-id="5233f-118">Wenn Sie eine andere Antwortdatei als die in Bits-Response-DataFile-Name angegebene Antwortdatei verwenden möchten, müssen Sie die Methode **Response. AddHeader** zum Hinzufügen der Bits-static-Response-URL wie im folgenden Beispiel gezeigt verwenden.</span><span class="sxs-lookup"><span data-stu-id="5233f-118">If you want to use a different response file than the one specified in BITS-Response-DataFile-Name, call the **Response.AddHeader** method to add the BITS-Static-Response-URL as shown in the following example.</span></span> <span data-ttu-id="5233f-119">Wenn Sie eine andere Antwortdatei angeben, erstellen Sie die in Bits-Response-DataFile-Name angegebene Antwortdatei nicht.</span><span class="sxs-lookup"><span data-stu-id="5233f-119">If you specify a different response file, do not create the response file specified in BITS-Response-DataFile-Name.</span></span>


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




