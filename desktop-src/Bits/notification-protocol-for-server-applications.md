---
title: Benachrichtigungsprotokoll für Serveranwendungen
description: BITS verwendet die BITSServerNotificationType-Eigenschaft, um zu bestimmen, wie BITS den Inhalt der Uploaddatei an die Serveranwendung sendet.
ms.assetid: d5193d0c-3ab4-47ab-a570-fea2904a4371
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54e859730acaa1456624e9fa5c2302bc36efd9d085daeecdf234aef8f74729c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004940"
---
# <a name="notification-protocol-for-server-applications"></a>Benachrichtigungsprotokoll für Serveranwendungen

BITS verwendet die [BITSServerNotificationType-Eigenschaft,](bits-iis-extension-properties.md) um zu bestimmen, wie BITS den Inhalt der Uploaddatei an die Serveranwendung sendet. Wenn die BITSServerNotificationType-Eigenschaft auf 1 festgelegt ist, übergibt BITS den Speicherort der Uploaddatei [in einem Header.](#sending-the-location-of-the-upload-file-in-a-header) Wenn die BITSServerNotificationType-Eigenschaft auf 2 festgelegt ist, übergibt BITS den Inhalt der Uploaddatei [im Text der Anforderung.](#sending-the-upload-file-in-the-body-of-the-request)

Weitere Informationen dazu, wie BITS Fehler von der Serveranwendung behandelt, finden Sie unter [Behandeln von Serveranwendungsfehlern.](#handling-server-application-errors)

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a>Senden des Speicherorts der Uploaddatei in einem Header

BITS übergibt den Speicherort der Upload- und Antwortdateien an die Serveranwendung in den Headern, wenn die [BITSServerNotificationType-Eigenschaft](bits-iis-extension-properties.md) auf 1 festgelegt ist. Die Serveranwendung öffnet die Uploaddatei, verarbeitet die Daten und generiert dann die Antwortdatei. Standardmäßig entfernt BITS die Upload- und Antwortdateien vom Server, nachdem die Antwort von der Serveranwendung empfangen wurde. Damit BITS die Uploaddatei an den durch den Remotedateinamen im Auftrag angegebenen Speicherort kopiert, fügen Sie den Bits-Copy-File-To-Destination-Header in die Antwort ein. Wenn Sie den Header nicht angeben und die Upload- und Antwortdateien speichern möchten, müssen Sie die Upload- und Antwortdateien an einen neuen Speicherort kopieren, bevor Sie antworten. Die folgende Tabelle zeigt die Anforderungsheader.



| Anforderungsheader              | BESCHREIBUNG                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| BITS-Original-Request-URL   | Enthält den im Auftrag angegebenen Remotenamen.                                             |
| BITS-Request-DataFile-Name  | Enthält den vollständigen Pfad zu den hochgeladenen Daten.                                               |
| BITS-Response-DataFile-Name | Enthält den vollständigen Pfad zu dem Ort, an dem BITS erwartet, dass die Serveranwendung die Antwort schreibt. |



 

In der folgenden Tabelle sind die Antwortheader aufgeführt.



| Antwortheader               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-Static-Response-URL      | Optional. Enthält die absolute URL (geben Sie keine Relative URL an) in eine statische Datendatei, die als Antwort verwendet werden soll. Der BITS-Client muss auf die statische Datendatei zugriffen können. Wenn Sie diesen Header verwenden, erstellen Sie nicht die Antwortdatei, die im Anforderungsheader BITS-Response-DataFile-Name angegeben ist. Beachten Sie, dass BITS diese Datei nicht für Sie löscht.<br/>                                                                                                           |
| BITS-Copy-File-to-Destination | Optional. Wenn die [BITSServerNotificationType-Eigenschaft](bits-iis-extension-properties.md) standardmäßig auf 1 oder 2 festgelegt ist, kopiert der BITS-Server die Uploaddatei nicht an den Speicherort, der durch den Remotedateinamen im Auftrag angegeben wird. Damit BITS die Datei an den speicherort kopiert, der durch den Remotedateinamen im Auftrag angegeben wird, senden Sie diesen Antwortheader. Sie können einen beliebigen Wert angeben. BITS verwendet den Wert nicht. Beachten Sie, dass die Ordner im Remotedateipfad vorhanden sein müssen. |



 

Die folgende Anforderung zeigt BITS, die den Speicherort der Uploaddatei an die Serveranwendung senden.

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

Das folgende Beispiel zeigt die Antwort der Serveranwendung an BITS. Die Antwort wird in der Datei platziert, die durch den Anforderungsheader BITS-Response-DataFile-Name angegeben wird.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a>Senden der Uploaddatei im Text der Anforderung

BITS sendet die Uploaddatei im Text der Anforderung, wenn die [BITSServerNotificationType-Eigenschaft](bits-iis-extension-properties.md) auf 2 festgelegt ist. Durch das Senden der Uploaddatei im Anforderungsteil können vorhandene Skripts und Anwendungen mit minimalen Änderungen funktionieren. Die Uploaddatei und die Antwortdatei werden in der Anforderung bzw. antwort übergeben. Die folgende Tabelle zeigt den Anforderungsheader.



| Anforderungsheader            | BESCHREIBUNG                                    |
|---------------------------|------------------------------------------------|
| BITS-Original-Request-URL | Enthält den im Auftrag angegebenen Remotenamen. |



 

In der folgenden Tabelle sind die Antwortheader aufgeführt.



| Antwortheader               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-Static-Response-URL      | Optional. Enthält die absolute URL (geben Sie keine Relative URL an) in eine statische Datendatei, die als Antwort verwendet werden soll. Der BITS-Client muss auf die statische Datendatei zugriffen können. Wenn Sie diesen Header verwenden, schließen Sie die Antwort nicht in den Stream ein. Beachten Sie, dass BITS diese Datei nicht für Sie löscht.<br/>                                                                                                                                      |
| BITS-Copy-File-to-Destination | Optional. Wenn die [BITSServerNotificationType-Eigenschaft](bits-iis-extension-properties.md) auf 1 oder 2 festgelegt ist, kopiert der BITS-Server die Uploaddatei nicht an den Speicherort, der durch den Remotedateinamen im Auftrag angegeben wird. Damit BITS die Datei an den durch den Remotedateinamen angegebenen Speicherort kopiert, senden Sie diesen Antwortheader. Sie können einen beliebigen Wert angeben. BITS verwendet den Wert nicht. Beachten Sie, dass die Ordner im Remotedateipfad vorhanden sein müssen. |



 

Die folgende Anforderung zeigt BITS, das die hochgeladene Datei im Text der Anforderung an die Serveranwendung über gibt.

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

Die folgende Antwort zeigt, wie die Serveranwendung die Antwortdaten im Text der Antwort an BITS über gibt.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a>Behandeln von Serveranwendungsfehlern

Weitere Informationen [finden Sie unter Behandeln von Serveranwendungsfehlern.](handling-server-application-errors.md)

 

 





