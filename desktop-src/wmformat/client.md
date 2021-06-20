---
title: Clientprotokollierung (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über die Clientprotokollierung für das Windows Media Format 11 SDK. Die Protokollierung bietet dem Medienserver die Möglichkeit, die Aktivität der Clients nachverfolgungen, die eine Verbindung mit ihm herstellen.
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media Format SDK, Clientprotokollierung
- Windows Media Format SDK, Protokollierung
- Advanced Systems Format (ASF), Clientprotokollierung
- ASF (Advanced Systems Format), Clientprotokollierung
- Advanced Systems Format (ASF), Protokollierung
- ASF (Advanced Systems Format), Protokollierung
- Clientprotokollierung
- Protokollieren von Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095e01fcf0730fdec8d06a931a9a988ca79ea77f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406263"
---
# <a name="client-logging-windows-media-format-11-sdk"></a>Clientprotokollierung (Windows Media Format 11 SDK)

Wenn das Readerobjekt Daten von einem Server liest, sendet es Protokollierungsinformationen an den Server. Inhaltsanbieter verwenden diese Informationen in der Regel, um die Dienstqualität zu messen, Abrechnungsinformationen zu generieren oder Werbung nachverfolgungen. Die Protokollierungsinformationen enthalten keine personenbezogenen Daten.

Die Anwendung kann einige der protokollierten Informationen angeben, indem sie die [**IWMReaderAdvanced::SetClientInfo-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) für das Readerobjekt aufruft. Sie können z. B. die Benutzer-Agent-Zeichenfolge, den Namen der Playeranwendung oder die Webseite angeben, die den Player hostet.

Die Protokollierungsinformationen enthalten eine GUID, die die Sitzung identifiziert. Standardmäßig generiert der Leser eine anonyme Sitzungs-ID. Optional kann der Leser stattdessen eine ID senden, die den aktuellen Benutzer eindeutig identifiziert. Um dieses Feature zu aktivieren, rufen Sie [**die IWMReaderAdvanced2::SetLogClientID-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) mit dem Wert **TRUE auf.**

Sie können das Readerobjekt so konfigurieren, dass die Protokollierungsinformationen zusätzlich zum Ursprungsserver an einen anderen Server gesendet werden. Rufen Sie dazu die [**IWMReaderNetworkConfig::AddLoggingUrl-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) mit der URL des Servers auf. Diese URL sollte auf ein Skript oder eine ausführbare Datei verweisen, die HTTP GET- und POST-Anforderungen verarbeiten kann. Sie können den Multicast- und Protokollierungsanmelde-Agent (wmsiislog.dll) verwenden oder ein benutzerdefiniertes ASP- oder CGI-Skript schreiben, um die Protokolldaten zu empfangen.

> [!Note]  
> Sie können die gleiche Funktionalität erhalten, indem Sie eine serverseitige Wiedergabeliste mit einem **logURL-Attribut** erstellen.

 

Wenn das Readerobjekt das Protokoll sendet, führt es Folgendes aus:

1.  Sendet eine leere GET-Anforderung an den Server.
2.  Analysiert die Serverantwort für eine der folgenden Zeichenfolgen:
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   `<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` wobei "0.0.0.0" eine beliebige gültige Versionsnummer ist.
3.  Sendet eine POST-Anforderung mit den Protokollinformationen.

Der folgende Code zeigt ein ASP-Beispielskript, das die Protokollierungsinformationen empfängt und in eine Datei schreibt:


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



Sie können mehrere Server angeben, um Protokollierungsinformationen zu empfangen. Rufen Sie **addLoggingUrl einfach einmal** mit jeder URL auf. Um die Liste der Server zu löschen, die Protokolle empfangen, rufen Sie [**die IWMReaderNetworkConfig::ResetLoggingUrlList-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Netzwerkfunktionen**](implementing-network-functionality.md)
</dt> <dt>

[**IWMReaderAdvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[**IWMReaderAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




