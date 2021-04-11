---
title: Client Protokollierung (Windows Media-Format 11 SDK)
description: Client Protokollierung
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media-Format-SDK, Client Protokollierung
- Windows Media-Format-SDK, Protokollierung
- Advanced Systems Format (ASF), Client Protokollierung
- ASF (Advanced Systems Format), Client Protokollierung
- Advanced Systems Format (ASF), Protokollierung
- ASF (Advanced Systems Format), Protokollierung
- Client Protokollierung
- Protokollieren von Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856f2df4c2377b94edc40574c3e2efcced34aa81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102630"
---
# <a name="client-logging-windows-media-format-11-sdk"></a>Client Protokollierung (Windows Media-Format 11 SDK)

Wenn das Reader-Objektdaten von einem Server liest, werden Protokollierungs Informationen an den Server gesendet. Inhaltsanbieter verwenden diese Informationen in der Regel, um die Dienst Qualität zu messen, Abrechnungsinformationen zu generieren oder Werbung zu verfolgen. Die Protokollierungs Informationen enthalten keine personenbezogenen Daten.

Die Anwendung kann einige der protokollierten Informationen angeben, indem Sie die [**iwmreaderadvanced:: setClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) -Methode für das Reader-Objekt aufruft. Sie können z. b. die Benutzer-Agent-Zeichenfolge, den Namen der Player Anwendung oder die Webseite angeben, die den Player hostet.

Die Protokollierungs Informationen beinhalten eine GUID, die die Sitzung identifiziert. Standardmäßig generiert der Reader eine anonyme Sitzungs-ID. Optional kann der Reader stattdessen eine ID senden, die den aktuellen Benutzer eindeutig identifiziert. Um dieses Feature zu aktivieren, müssen Sie die [**IWMReaderAdvanced2:: setlogclientid-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) Methode mit dem Wert " **true**" aufrufen.

Sie können das Reader-Objekt so konfigurieren, dass die Protokollierungs Informationen zusätzlich zum ursprünglichen Server an einen anderen Server gesendet werden. Um dies zu tun, wenden Sie die Methode [**iwmreadernetworkconfig:: addloggingurl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) mit der URL des Servers an. Diese URL sollte auf ein Skript oder eine ausführbare Datei verweisen, die HTTP-Get-und Post-Anforderungen verarbeiten kann. Sie können den Multicast-und Protokollierungs Ankündigungs-Agent (wmsiislog.dll) verwenden, oder Sie können ein benutzerdefiniertes ASP-oder CGI-Skript schreiben, um die Protokolldaten zu empfangen.

> [!Note]  
> Sie können dieselbe Funktionalität erzielen, indem Sie eine serverseitige Wiedergabeliste mit einem **LogURL** -Attribut erstellen.

 

Wenn das Reader-Objekt das Protokoll sendet, erfolgt Folgendes:

1.  Sendet eine leere Get-Anforderung an den Server.
2.  Analysiert die Serverantwort für eine der folgenden Zeichen folgen:
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   `<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` Dabei ist "0.0.0.0" eine beliebige gültige Versionsnummer.
3.  Sendet eine Post-Anforderung mit den Protokollinformationen.

Der folgende Code zeigt ein ASP-Beispielskript, mit dem die Protokollierungs Informationen empfangen und in eine Datei geschrieben werden:


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



Sie können mehrere Server angeben, um Protokollierungs Informationen zu empfangen. nennen Sie **addloggingurl** nur einmal mit jeder URL. Um die Liste der Server zu löschen, die Protokolle empfangen, müssen Sie die [**iwmreadernetworkconfig:: resetloggingurllist**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) -Methode aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Netzwerkfunktionen**](implementing-network-functionality.md)
</dt> <dt>

[**Iwmreaderadvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[**IWMReaderAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




