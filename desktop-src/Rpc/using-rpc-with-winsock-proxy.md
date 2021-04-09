---
title: Verwenden von RPC mit Winsock-Proxy
description: Verwenden von RPC mit Winsock-Proxy
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5f658cf60d7e530da99ee139dbcdcbb2c89685
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039563"
---
# <a name="using-rpc-with-winsock-proxy"></a>Verwenden von RPC mit Winsock-Proxy

Die Version von Microsoft Internet Access Server enthielt den Winsock-Proxy, eine verbesserte Version der Windows Sockets-API, Version 1,1. Der Winsock-Proxy lässt eine Windows Sockets-Anwendung, die auf einem privaten Netzwerkclient ausgeführt wird, so Verhalten, als ob Sie direkt mit einer Remote-Internet Serveranwendung verbunden wäre. Der Microsoft-Proxy Server fungiert als Host für diese Verbindung. Dies bedeutet, dass die gesamte Kommunikation auf Anwendungsebene über einen einzelnen gesicherten Computer geleitet wird – dem Gatewaycomputer, auf dem Microsoft Proxy Server ausgeführt wird.

Normalerweise umgeht die RPC-Transport-dll bei der Übertragung von Datagramm-Paketen die in Wsock32.dll bereitgestellten Funktionen [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) und [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) und kommuniziert direkt mit dem zugrunde liegenden Gerätetreiber. Dadurch wird die Geschwindigkeit der Paket Übertragungen erhöht, aber die Winsock-Proxy Funktionen sind für die Anwendung nicht verfügbar.

Jedem Netzwerkprotokoll Anbieter muss eine GUID zugeordnet sein. Die RPC-Lauf Zeit Bibliothek vergleicht die UDP-und IPX-GUIDs mit den bekannten Microsoft-bezeichnerbezeichner. Wenn Sie nicht identisch sind, verwendet RPC automatisch Winsock.

Eine weitere Funktion des Winsock-Proxys ist die Möglichkeit, das TCP-Transportprotokoll über den Novell SPX-Transport zu emulieren, wenn auf dem SPX-Client Computer TCP nicht installiert ist. Wenn Sie dieses Feature mit RPC-Anwendungen verwenden möchten, bearbeiten Sie die Systemregistrierung auf jedem Client Computer, um diesen Eintrag hinzuzufügen:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Bearbeiten Sie die Registrierung auf jedem Server Computer, um diesen Eintrag hinzuzufügen:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Weitere Informationen zu RPC-Transportprotokollen finden Sie unter [Angeben von Protokoll Sequenzen](specifying-protocol-sequences.md). Weitere Informationen zum Winsock-Proxy finden Sie in der Produktdokumentation für Microsoft Internet Access Server.

Die Registrierungseinträge **clientprotokolls** und **Server Protokolle** werden von Windows 2000 nicht implementiert. Microsoft stellt alle bekannten Transporte als Teil der Lauf Zeit Bibliothek bereit. Daher sind diese Einträge nicht erforderlich.

 

 