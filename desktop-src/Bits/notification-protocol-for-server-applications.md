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
# <a name="notification-protocol-for-server-applications"></a>Benachrichtigungs Protokoll für Server Anwendungen

Bits verwendet die [bitsservernotificationtype](bits-iis-extension-properties.md) -Eigenschaft, um zu bestimmen, wie Bits den Inhalt der Uploaddatei an die Serveranwendung sendet. Wenn die Eigenschaft bitsservernotificationtype auf 1 festgelegt ist, [übergibt Bits den Speicherort der Uploaddatei in einem Header](#sending-the-location-of-the-upload-file-in-a-header). Wenn die Eigenschaft bitsservernotificationtype auf 2 festgelegt ist, [übergibt Bits den Inhalt der Uploaddatei im Text der Anforderung](#sending-the-upload-file-in-the-body-of-the-request).

Ausführliche Informationen dazu, wie Bits Fehler von der Serveranwendung behandelt, finden Sie unter [Handling Server Application Errors](#handling-server-application-errors).

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a>Senden des Speicher Orts der Uploaddatei in einem Header

Bits übergibt den Speicherort der Upload-und Antwort Dateien an die Serveranwendung in den Headern, wenn die Eigenschaft [bitsservernotificationtype](bits-iis-extension-properties.md) auf 1 festgelegt ist. Die Serveranwendung öffnet die Uploaddatei, verarbeitet die Daten und generiert dann die Antwortdatei. Standardmäßig entfernt Bits die Upload-und Antwort Dateien vom Server, nachdem die Antwort von der Serveranwendung empfangen wurde. Um Bits die Uploaddatei an den Speicherort zu kopieren, der durch den Remote Dateinamen im Auftrag angegeben ist, fügen Sie den Bits-Copy-File-to-Destination-Header in die Antwort ein. Wenn Sie den-Header nicht einschließen und die Upload-und Antwort Dateien speichern möchten, müssen Sie die Upload-und die Antwort Dateien vor der Antwort an einen neuen Speicherort kopieren. In der folgenden Tabelle werden die Anforderungs Header angezeigt.



| Anforderungsheader              | BESCHREIBUNG                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| Bits-Original-Request-URL   | Enthält den im Auftrag angegebenen Remote Namen.                                             |
| Bits-Request-DataFile-Name  | Enthält den vollständigen Pfad zu den hochgeladenen Daten.                                               |
| Bits-Response-DataFile-Name | Enthält den vollständigen Pfad, in dem Bits von der Serveranwendung erwartet, dass die Antwort geschrieben wird. |



 

In der folgenden Tabelle werden die Antwortheader angezeigt.



| Antwortheader               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bits-static-Response-URL      | Dies ist optional. Enthält die absolute URL (keine relative URL angeben) für eine statische Datendatei, die als Antwort verwendet werden soll. Der BITS-Client muss auf die statische Datendatei zugreifen können. Wenn Sie diesen Header verwenden, erstellen Sie die im Bits-Response-DataFile-Name-Anforderungs Header angegebene Antwortdatei nicht. Beachten Sie, dass diese Datei von Bits nicht für Sie gelöscht wird.<br/>                                                                                                           |
| Bits-Copy-File-to-Destination | Dies ist optional. Wenn die Eigenschaft [bitsservernotificationtype](bits-iis-extension-properties.md) auf 1 oder 2 festgelegt ist, kopiert der BITS-Server standardmäßig die Uploaddatei nicht an den Speicherort, der durch den Remote Dateinamen im Auftrag angegeben wird. Um Bits die Datei an den Speicherort zu kopieren, der durch den Remote Dateinamen im Auftrag angegeben ist, senden Sie diesen Antwortheader. Sie können einen beliebigen Wert angeben. Bits verwendet nicht den Wert. Beachten Sie, dass die Ordner im Remote Datei Pfad vorhanden sein müssen. |



 

Die folgende Anforderung zeigt Bits, die den Speicherort der Uploaddatei an die Serveranwendung senden.

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

Das folgende Beispiel zeigt die Antwort der Serveranwendung an Bits. die Antwort wird in der Datei abgelegt, die durch den Anforderungs Header Bits-Response-DataFile-Name angegeben wird.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a>Die Uploaddatei wird im Text der Anforderung gesendet.

Bits sendet die Uploaddatei im Hauptteil der Anforderung, wenn die Eigenschaft [bitsservernotificationtype](bits-iis-extension-properties.md) auf 2 festgelegt ist. Wenn die Uploaddatei im Hauptteil der Anforderung gesendet wird, können vorhandene Skripts und Anwendungen mit minimalen Änderungen arbeiten. Die Uploaddatei und die Antwortdatei werden in der Anforderung bzw. der Antwort übermittelt. In der folgenden Tabelle wird der-Anforderungs Header angezeigt.



| Anforderungsheader            | BESCHREIBUNG                                    |
|---------------------------|------------------------------------------------|
| Bits-Original-Request-URL | Enthält den im Auftrag angegebenen Remote Namen. |



 

In der folgenden Tabelle werden die Antwortheader angezeigt.



| Antwortheader               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bits-static-Response-URL      | Dies ist optional. Enthält die absolute URL (keine relative URL angeben) für eine statische Datendatei, die als Antwort verwendet werden soll. Der BITS-Client muss auf die statische Datendatei zugreifen können. Wenn Sie diesen Header verwenden, schließen Sie die Antwort nicht in den Stream ein. Beachten Sie, dass diese Datei von Bits nicht für Sie gelöscht wird.<br/>                                                                                                                                      |
| Bits-Copy-File-to-Destination | Dies ist optional. Wenn die Eigenschaft [bitsservernotificationtype](bits-iis-extension-properties.md) auf 1 oder 2 festgelegt ist, kopiert der BITS-Server die Uploaddatei nicht an den Speicherort, der durch den Remote Dateinamen im Auftrag angegeben wird. Um Bits die Datei an den Speicherort zu kopieren, der durch den Remote Dateinamen angegeben ist, senden Sie diesen Antwortheader. Sie können einen beliebigen Wert angeben. Bits verwendet nicht den Wert. Beachten Sie, dass die Ordner im Remote Datei Pfad vorhanden sein müssen. |



 

Die folgende Anforderung zeigt Bits, die die hochgeladene Datei an die Serveranwendung im Anforderungs Text übergeben.

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

Die folgende Antwort zeigt die Serveranwendung, die die Antwortdaten an Bits im Text der Antwort übergibt.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a>Behandeln von Server Anwendungsfehlern

Weitere Informationen finden Sie unter [Handling Server Application Errors](handling-server-application-errors.md).

 

 





