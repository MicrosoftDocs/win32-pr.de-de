---
title: WS-Verwaltungsprotokoll
description: Ein öffentlicher Standard für den Remoteaustausch von Verwaltungsdaten mit jedem Computergerät, das das Protokoll implementiert.
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a20900e77d7d686868e00f7067b23fff644255997a14c9d4c1cbdcf3d1951d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742731"
---
# <a name="ws-management-protocol"></a>WS-Verwaltungsprotokoll

Das WS-Verwaltungsprotokoll wurde von einer Gruppe von Hardware- und Softwareherstellern als öffentlicher Standard für den Remoteaustausch von Verwaltungsdaten mit beliebigen Geräten entwickelt, die das Protokoll implementieren.

## <a name="standards"></a>Standards

Weitere Informationen zu WS-Management Protokoll finden Sie unter [Web Services for Management (WS-Management)-Spezifikation.](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf)

Das Protokoll soll Konsistenz und Interoperabilität für Verwaltungsvorgänge über viele Gerätetypen (einschließlich Firmware) und Betriebssysteme hinweg bereitstellen. WS-Management Protokoll kann erweitert werden, wenn neue Vorgänge von der IT-Branche identifiziert werden.

Die aktuelle Implementierung des WS-Management-Protokolls basiert auf den folgenden Standardspezifikationen: HTTPS, SOAP über HTTP (WS-I-Profil), SOAP 1.2, WS-Adressierung, WS-Transfer, WS-Enumeration und WS-Eventing. Weitere Informationen zu den WS-Management Standards und XML-Schemas finden Sie unter <https://dmtf.org/standards/wsman>

## <a name="messages"></a>Meldungen

Das WS-Management-Protokoll bietet einen Standard zum Erstellen von [*XML-Nachrichten*](windows-remote-management-glossary.md) mithilfe verschiedener Webdienststandards wie [*WS-Adressierung*](windows-remote-management-glossary.md) und [*WS-Transfer.*](windows-remote-management-glossary.md) Diese Standards definieren XML-Schemas für Webdienstnachrichten. Die Nachrichten verweisen mithilfe eines [*Ressourcen-URI*](windows-remote-management-glossary.md)auf eine [*Ressource.*](windows-remote-management-glossary.md) Das WS-Management-Protokoll fügt eine Reihe von Definitionen für Verwaltungsvorgänge und -werte hinzu. Beispielsweise definiert WS-Transfer die Vorgänge Get, Put, Create und Delete für eine Ressource. WS-Management Protokoll fügt Rename, Partial Get und Partial Put hinzu.

Die Nachrichten folgen den Konventionen des [*Simple Object Access Protocol (SOAP),*](windows-remote-management-glossary.md) das von allen Webdienstprotokollen verwendet wird.

Das folgende Codebeispiel zeigt eine Nachricht mit einem Get-Vorgang. Dieses Beispiel wird als Hilfe gezeigt, um zu verstehen, wie die zugrunde liegenden Nachrichten aussehen. Sie müssen nicht wissen, wie SOAP-Nachrichten erzeugt werden. Die Nachrichten werden von Windows Remoteverwaltung zusammengestellt, wenn  Sie einen Befehl mit dem Winrm-Befehlszeilentool ausführen oder ein Skript ausführen, das mit der [WinRM-Skripterstellungs-API](winrm-scripting-api.md)geschrieben wurde.

Die Nachricht ist eine Anforderung, die Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) mit der **DeviceID-Eigenschaft** "c:" von einem Server mit dem Namen RemoteComputer abzurufen. Die Anforderung verwendet den HTTP-Transport über Port 80. Das Konto, das die Anforderung sendet, muss sich in der lokalen Administratorgruppe auf dem Remotecomputer befinden.

Die Zeichen vor dem Doppelpunkt am Anfang jedes Tags geben an, welcher Standard das XML-Element definiert. Gibt beispielsweise ` <wsa:To>` an, dass das To-Element durch den WS-Addressing Standard definiert wird, und `<s:Header>` gibt den Anfang des Headerinhalts in einer SOAP-Nachricht an. Beachten Sie, dass der Großteil der Nachricht aus XML-Elementen besteht, die durch SOAP oder WS-Adressierung definiert werden. WS-Management-Protokoll fügt MaxEnvelopeSize, Selector und SelectorSet hinzu.


```XML
<s:Envelope xmlns:s="https://www.w3.org/2003/05/soap-envelope" 
            xmlns:a="https://schemas.xmlsoap.org/ws/2004/08/addressing" 
            xmlns:w="https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd">
  <s:Header>
    <a:To>https://RemoteComputer:80/wsman</a:To> 
    <w:ResourceURI s:mustUnderstand="true">
      http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_logicaldisk
    </w:ResourceURI> 
    <a:ReplyTo>
    <a:Address s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </a:Address> 
    </a:ReplyTo>
    <a:Action s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </a:Action> 
    <w:MaxEnvelopeSize s:mustUnderstand="true">153600</w:MaxEnvelopeSize> 
    <a:MessageID>uuid:4ED2993C-4339-4E99-81FC-C2FD3812781A</a:MessageID> 
    <w:Locale xml:lang="en-US" s:mustUnderstand="false"/> 
    <w:SelectorSet>
    <w:Selector Name="DeviceId">c:</w:Selector> 
    </w:SelectorSet>
    <w:OperationTimeout>PT60.000S</w:OperationTimeout> 
  </s:Header>
  <s:Body/> 
</s:Envelope>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Remotehardwareverwaltung](remote-hardware-management.md)
</dt> </dl>

 

 