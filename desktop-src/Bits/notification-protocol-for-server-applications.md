---
title: Benachrichtigungs Protokoll für Server Anwendungen
description: Bits verwendet die bitsservernotificationtype-Eigenschaft, um zu bestimmen, wie Bits den Inhalt der Uploaddatei an die Serveranwendung sendet.
ms.assetid: d5193d0c-3ab4-47ab-a570-fea2904a4371
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d35f6f5fec1a1de9ebd5c2c244a55bc1806b06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947459"
---
# <a name="notification-protocol-for-server-applications"></a><span data-ttu-id="da80c-103">Benachrichtigungs Protokoll für Server Anwendungen</span><span class="sxs-lookup"><span data-stu-id="da80c-103">Notification Protocol for Server Applications</span></span>

<span data-ttu-id="da80c-104">Bits verwendet die [bitsservernotificationtype](bits-iis-extension-properties.md) -Eigenschaft, um zu bestimmen, wie Bits den Inhalt der Uploaddatei an die Serveranwendung sendet.</span><span class="sxs-lookup"><span data-stu-id="da80c-104">BITS uses the [BITSServerNotificationType](bits-iis-extension-properties.md) property to determine how BITS sends the contents of the upload file to the server application.</span></span> <span data-ttu-id="da80c-105">Wenn die Eigenschaft bitsservernotificationtype auf 1 festgelegt ist, [übergibt Bits den Speicherort der Uploaddatei in einem Header](#sending-the-location-of-the-upload-file-in-a-header).</span><span class="sxs-lookup"><span data-stu-id="da80c-105">If the BITSServerNotificationType property is set to 1, [BITS passes the location of the upload file in a header](#sending-the-location-of-the-upload-file-in-a-header).</span></span> <span data-ttu-id="da80c-106">Wenn die Eigenschaft bitsservernotificationtype auf 2 festgelegt ist, [übergibt Bits den Inhalt der Uploaddatei im Text der Anforderung](#sending-the-upload-file-in-the-body-of-the-request).</span><span class="sxs-lookup"><span data-stu-id="da80c-106">If the BITSServerNotificationType property is set to 2, [BITS passes the contents of the upload file in the body of the request](#sending-the-upload-file-in-the-body-of-the-request).</span></span>

<span data-ttu-id="da80c-107">Ausführliche Informationen dazu, wie Bits Fehler von der Serveranwendung behandelt, finden Sie unter [Handling Server Application Errors](#handling-server-application-errors).</span><span class="sxs-lookup"><span data-stu-id="da80c-107">For details on how BITS handles errors from the server application, see [Handling server application errors](#handling-server-application-errors).</span></span>

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a><span data-ttu-id="da80c-108">Senden des Speicher Orts der Uploaddatei in einem Header</span><span class="sxs-lookup"><span data-stu-id="da80c-108">Sending the location of the upload file in a header</span></span>

<span data-ttu-id="da80c-109">Bits übergibt den Speicherort der Upload-und Antwort Dateien an die Serveranwendung in den Headern, wenn die Eigenschaft [bitsservernotificationtype](bits-iis-extension-properties.md) auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="da80c-109">BITS passes the location of the upload and reply files to the server application in the headers if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1.</span></span> <span data-ttu-id="da80c-110">Die Serveranwendung öffnet die Uploaddatei, verarbeitet die Daten und generiert dann die Antwortdatei.</span><span class="sxs-lookup"><span data-stu-id="da80c-110">The server application opens the upload file, processes the data, and then generates the reply file.</span></span> <span data-ttu-id="da80c-111">Standardmäßig entfernt Bits die Upload-und Antwort Dateien vom Server, nachdem die Antwort von der Serveranwendung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="da80c-111">By default, BITS removes the upload and reply files from the server after it receives the response from the server application.</span></span> <span data-ttu-id="da80c-112">Um Bits die Uploaddatei an den Speicherort zu kopieren, der durch den Remote Dateinamen im Auftrag angegeben ist, fügen Sie den Bits-Copy-File-to-Destination-Header in die Antwort ein.</span><span class="sxs-lookup"><span data-stu-id="da80c-112">To have BITS copy the upload file to the location specified by the remote file name in the job, include the BITS-Copy-File-To-Destination header in your response.</span></span> <span data-ttu-id="da80c-113">Wenn Sie den-Header nicht einschließen und die Upload-und Antwort Dateien speichern möchten, müssen Sie die Upload-und die Antwort Dateien vor der Antwort an einen neuen Speicherort kopieren.</span><span class="sxs-lookup"><span data-stu-id="da80c-113">If you do not include the header and you want to save the upload and reply files, you must copy the upload and reply files to a new location before responding.</span></span> <span data-ttu-id="da80c-114">In der folgenden Tabelle werden die Anforderungs Header angezeigt.</span><span class="sxs-lookup"><span data-stu-id="da80c-114">The following table shows the request headers.</span></span>



| <span data-ttu-id="da80c-115">Anforderungsheader</span><span class="sxs-lookup"><span data-stu-id="da80c-115">Request header</span></span>              | <span data-ttu-id="da80c-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da80c-116">Description</span></span>                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="da80c-117">Bits-Original-Request-URL</span><span class="sxs-lookup"><span data-stu-id="da80c-117">BITS-Original-Request-URL</span></span>   | <span data-ttu-id="da80c-118">Enthält den im Auftrag angegebenen Remote Namen.</span><span class="sxs-lookup"><span data-stu-id="da80c-118">Contains the remote name specified in the job.</span></span>                                             |
| <span data-ttu-id="da80c-119">Bits-Request-DataFile-Name</span><span class="sxs-lookup"><span data-stu-id="da80c-119">BITS-Request-DataFile-Name</span></span>  | <span data-ttu-id="da80c-120">Enthält den vollständigen Pfad zu den hochgeladenen Daten.</span><span class="sxs-lookup"><span data-stu-id="da80c-120">Contains the full path to the uploaded data.</span></span>                                               |
| <span data-ttu-id="da80c-121">Bits-Response-DataFile-Name</span><span class="sxs-lookup"><span data-stu-id="da80c-121">BITS-Response-DataFile-Name</span></span> | <span data-ttu-id="da80c-122">Enthält den vollständigen Pfad, in dem Bits von der Serveranwendung erwartet, dass die Antwort geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="da80c-122">Contains the full path to where BITS expects the server application to write the response.</span></span> |



 

<span data-ttu-id="da80c-123">In der folgenden Tabelle werden die Antwortheader angezeigt.</span><span class="sxs-lookup"><span data-stu-id="da80c-123">The following table shows the response headers.</span></span>



| <span data-ttu-id="da80c-124">Antwortheader</span><span class="sxs-lookup"><span data-stu-id="da80c-124">Response header</span></span>               | <span data-ttu-id="da80c-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da80c-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da80c-126">Bits-static-Response-URL</span><span class="sxs-lookup"><span data-stu-id="da80c-126">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="da80c-127">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="da80c-127">Optional.</span></span> <span data-ttu-id="da80c-128">Enthält die absolute URL (keine relative URL angeben) für eine statische Datendatei, die als Antwort verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da80c-128">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="da80c-129">Der BITS-Client muss auf die statische Datendatei zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="da80c-129">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="da80c-130">Wenn Sie diesen Header verwenden, erstellen Sie die im Bits-Response-DataFile-Name-Anforderungs Header angegebene Antwortdatei nicht.</span><span class="sxs-lookup"><span data-stu-id="da80c-130">If you use this header, do not create the response file specified in the BITS-Response-DataFile-Name request header.</span></span> <span data-ttu-id="da80c-131">Beachten Sie, dass diese Datei von Bits nicht für Sie gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="da80c-131">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                           |
| <span data-ttu-id="da80c-132">Bits-Copy-File-to-Destination</span><span class="sxs-lookup"><span data-stu-id="da80c-132">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="da80c-133">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="da80c-133">Optional.</span></span> <span data-ttu-id="da80c-134">Wenn die Eigenschaft [bitsservernotificationtype](bits-iis-extension-properties.md) auf 1 oder 2 festgelegt ist, kopiert der BITS-Server standardmäßig die Uploaddatei nicht an den Speicherort, der durch den Remote Dateinamen im Auftrag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="da80c-134">By default, if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="da80c-135">Um Bits die Datei an den Speicherort zu kopieren, der durch den Remote Dateinamen im Auftrag angegeben ist, senden Sie diesen Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="da80c-135">To have BITS copy the file to the location specified by the remote file name in the job, send this response header.</span></span> <span data-ttu-id="da80c-136">Sie können einen beliebigen Wert angeben. Bits verwendet nicht den Wert.</span><span class="sxs-lookup"><span data-stu-id="da80c-136">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="da80c-137">Beachten Sie, dass die Ordner im Remote Datei Pfad vorhanden sein müssen.</span><span class="sxs-lookup"><span data-stu-id="da80c-137">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="da80c-138">Die folgende Anforderung zeigt Bits, die den Speicherort der Uploaddatei an die Serveranwendung senden.</span><span class="sxs-lookup"><span data-stu-id="da80c-138">The following request shows BITS sending the location of the upload file to the server application.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
BITS-Request-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\request
BITS-Response-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\response
Content-Length: 0
```

<span data-ttu-id="da80c-139">Das folgende Beispiel zeigt die Antwort der Serveranwendung an Bits. die Antwort wird in der Datei abgelegt, die durch den Anforderungs Header Bits-Response-DataFile-Name angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="da80c-139">The following shows the server application's reply to BITS; the reply is placed in the file specified by the BITS-Response-DataFile-Name request header.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a><span data-ttu-id="da80c-140">Die Uploaddatei wird im Text der Anforderung gesendet.</span><span class="sxs-lookup"><span data-stu-id="da80c-140">Sending the upload file in the body of the request</span></span>

<span data-ttu-id="da80c-141">Bits sendet die Uploaddatei im Hauptteil der Anforderung, wenn die Eigenschaft [bitsservernotificationtype](bits-iis-extension-properties.md) auf 2 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="da80c-141">BITS sends the upload file in the body of the request if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 2.</span></span> <span data-ttu-id="da80c-142">Wenn die Uploaddatei im Hauptteil der Anforderung gesendet wird, können vorhandene Skripts und Anwendungen mit minimalen Änderungen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="da80c-142">Sending the upload file in the body of the request lets existing scripts and applications work with minimal modifications.</span></span> <span data-ttu-id="da80c-143">Die Uploaddatei und die Antwortdatei werden in der Anforderung bzw. der Antwort übermittelt.</span><span class="sxs-lookup"><span data-stu-id="da80c-143">The upload file and reply file are passed in the request and response, respectively.</span></span> <span data-ttu-id="da80c-144">In der folgenden Tabelle wird der-Anforderungs Header angezeigt.</span><span class="sxs-lookup"><span data-stu-id="da80c-144">The following table shows the request header.</span></span>



| <span data-ttu-id="da80c-145">Anforderungsheader</span><span class="sxs-lookup"><span data-stu-id="da80c-145">Request header</span></span>            | <span data-ttu-id="da80c-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da80c-146">Description</span></span>                                    |
|---------------------------|------------------------------------------------|
| <span data-ttu-id="da80c-147">Bits-Original-Request-URL</span><span class="sxs-lookup"><span data-stu-id="da80c-147">BITS-Original-Request-URL</span></span> | <span data-ttu-id="da80c-148">Enthält den im Auftrag angegebenen Remote Namen.</span><span class="sxs-lookup"><span data-stu-id="da80c-148">Contains the remote name specified in the job.</span></span> |



 

<span data-ttu-id="da80c-149">In der folgenden Tabelle werden die Antwortheader angezeigt.</span><span class="sxs-lookup"><span data-stu-id="da80c-149">The following table shows the response headers.</span></span>



| <span data-ttu-id="da80c-150">Antwortheader</span><span class="sxs-lookup"><span data-stu-id="da80c-150">Response header</span></span>               | <span data-ttu-id="da80c-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da80c-151">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da80c-152">Bits-static-Response-URL</span><span class="sxs-lookup"><span data-stu-id="da80c-152">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="da80c-153">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="da80c-153">Optional.</span></span> <span data-ttu-id="da80c-154">Enthält die absolute URL (keine relative URL angeben) für eine statische Datendatei, die als Antwort verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da80c-154">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="da80c-155">Der BITS-Client muss auf die statische Datendatei zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="da80c-155">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="da80c-156">Wenn Sie diesen Header verwenden, schließen Sie die Antwort nicht in den Stream ein.</span><span class="sxs-lookup"><span data-stu-id="da80c-156">If you use this header, do not include the response in the stream.</span></span> <span data-ttu-id="da80c-157">Beachten Sie, dass diese Datei von Bits nicht für Sie gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="da80c-157">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="da80c-158">Bits-Copy-File-to-Destination</span><span class="sxs-lookup"><span data-stu-id="da80c-158">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="da80c-159">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="da80c-159">Optional.</span></span> <span data-ttu-id="da80c-160">Wenn die Eigenschaft [bitsservernotificationtype](bits-iis-extension-properties.md) auf 1 oder 2 festgelegt ist, kopiert der BITS-Server die Uploaddatei nicht an den Speicherort, der durch den Remote Dateinamen im Auftrag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="da80c-160">If the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="da80c-161">Um Bits die Datei an den Speicherort zu kopieren, der durch den Remote Dateinamen angegeben ist, senden Sie diesen Antwortheader.</span><span class="sxs-lookup"><span data-stu-id="da80c-161">To have BITS copy the file to the location specified by the remote file name, send this response header.</span></span> <span data-ttu-id="da80c-162">Sie können einen beliebigen Wert angeben. Bits verwendet nicht den Wert.</span><span class="sxs-lookup"><span data-stu-id="da80c-162">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="da80c-163">Beachten Sie, dass die Ordner im Remote Datei Pfad vorhanden sein müssen.</span><span class="sxs-lookup"><span data-stu-id="da80c-163">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="da80c-164">Die folgende Anforderung zeigt Bits, die die hochgeladene Datei an die Serveranwendung im Anforderungs Text übergeben.</span><span class="sxs-lookup"><span data-stu-id="da80c-164">The following request shows BITS passing the uploaded file to the server application in the body of the request.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

<span data-ttu-id="da80c-165">Die folgende Antwort zeigt die Serveranwendung, die die Antwortdaten an Bits im Text der Antwort übergibt.</span><span class="sxs-lookup"><span data-stu-id="da80c-165">The following reply shows the server application passing the reply data to BITS in the body of the response.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a><span data-ttu-id="da80c-166">Behandeln von Server Anwendungsfehlern</span><span class="sxs-lookup"><span data-stu-id="da80c-166">Handling server application errors</span></span>

<span data-ttu-id="da80c-167">Weitere Informationen finden Sie unter [Handling Server Application Errors](handling-server-application-errors.md).</span><span class="sxs-lookup"><span data-stu-id="da80c-167">See [Handling Server Application Errors](handling-server-application-errors.md).</span></span>

 

 





