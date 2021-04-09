---
title: WS-Verwaltungsprotokoll
description: Ein öffentlicher Standard für den Remote Austausch von Verwaltungsdaten mit jedem Computer Gerät, das das Protokoll implementiert.
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e01fdc860eeb5510dd78a4127fdc22b30d711a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102306"
---
# <a name="ws-management-protocol"></a>WS-Verwaltungsprotokoll

Das WS-Verwaltungsprotokoll wurde von einer Gruppe von Hardware- und Softwareherstellern als öffentlicher Standard für den Remoteaustausch von Verwaltungsdaten mit beliebigen Geräten entwickelt, die das Protokoll implementieren.

## <a name="standards"></a>Standards

Weitere Informationen zum WS-Management-Protokoll finden Sie unter [Spezifikation der Web Services for Management (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

Der Zweck des Protokolls besteht darin, Konsistenz und Interoperabilität für Verwaltungsvorgänge auf vielen Arten von Geräten (einschließlich Firmware) und Betriebssystemen bereitzustellen. WS-Management Protokoll kann erweitert werden, wenn neue Vorgänge von der IT-Branche identifiziert werden.

Die aktuelle Implementierung des WS-Management Protokolls basiert auf den folgenden Standardspezifikationen: https, SOAP über HTTP (WS-I Profile), SOAP 1,2, WS-Adressierung, WS-Transfer, WS-Enumeration und WS-Eventing. Weitere Informationen zu den WS-Management Standards und XML-Schemas finden Sie unter. <https://dmtf.org/standards/wsman>

## <a name="messages"></a>Meldungen

Das WS-Management-Protokoll stellt einen Standard zum Erstellen von XML- [*Nachrichten*](windows-remote-management-glossary.md) mithilfe verschiedener Webdienst Standards wie [*WS-Adressierung*](windows-remote-management-glossary.md) und [*WS-Transfer*](windows-remote-management-glossary.md)bereit. Diese Standards definieren XML-Schemas für Webdienst Nachrichten. Die Nachrichten verweisen auf eine [*Ressource*](windows-remote-management-glossary.md) , die einen [*Ressourcen-URI*](windows-remote-management-glossary.md)verwendet. Das WS-Management-Protokoll fügt einen Satz von Definitionen für Verwaltungsvorgänge und Werte hinzu. Beispielsweise definiert WS-Transfer die Vorgänge "Get", "Put", "Create" und "Delete" für eine Ressource. WS-Management Protokoll fügt rename, partielle Get und partielle Put hinzu.

Die Nachrichten folgen den Konventionen von [*SOAP (Simple Object Access Protocol)*](windows-remote-management-glossary.md) , die von allen Webdienst Protokollen verwendet werden.

Das folgende Codebeispiel zeigt eine Meldung mit einem Get-Vorgang. Dieses Beispiel wird als Hilfe zum Verständnis der zugrunde liegenden Nachrichten angezeigt. Sie müssen nicht wissen, wie SOAP-Nachrichten erzeugt werden. Die Nachrichten werden von Windows-Remoteverwaltung assembliert, wenn Sie mit dem **WinRM** -Befehlszeilen Tool einen Befehl ausführen oder ein Skript ausführen, das mit der [WinRM-Skript-API](winrm-scripting-api.md)geschrieben wurde.

Die Meldung ist eine Anforderung, die Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) mit der **DeviceID** -Eigenschaft "c:" von einem Server mit dem Namen "Remotecomputer" zu erhalten. Die Anforderung verwendet den HTTP-Transport über Port 80. Das Konto, das die Anforderung sendet, muss sich in der lokalen Gruppe "Administratoren" auf dem Remote Computer befinden.

Die Zeichen vor dem Doppelpunkt am Anfang jedes Tags geben an, welcher Standard das XML-Element definiert. Beispielsweise ` <wsa:To>` gibt an, dass das to-Element durch den WS-Addressing-Standard definiert wird, und `<s:Header>` gibt den Anfang des Header Inhalts in einer SOAP-Nachricht an. Beachten Sie, dass der Großteil der Nachricht aus XML-Elementen besteht, die von SOAP oder WS-Adressierung definiert werden. WS-Management Protokoll fügt MaxEnvelopeSize, Selector und selectorset hinzu.


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

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Remote Hardware Verwaltung](remote-hardware-management.md)
</dt> </dl>

 

 