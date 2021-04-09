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
# <a name="using-rpc-with-winsock-proxy"></a><span data-ttu-id="8707f-103">Verwenden von RPC mit Winsock-Proxy</span><span class="sxs-lookup"><span data-stu-id="8707f-103">Using RPC with Winsock Proxy</span></span>

<span data-ttu-id="8707f-104">Die Version von Microsoft Internet Access Server enthielt den Winsock-Proxy, eine verbesserte Version der Windows Sockets-API, Version 1,1.</span><span class="sxs-lookup"><span data-stu-id="8707f-104">The release of Microsoft Internet Access Server included Winsock Proxy, an enhanced version of Windows Sockets API version 1.1.</span></span> <span data-ttu-id="8707f-105">Der Winsock-Proxy lässt eine Windows Sockets-Anwendung, die auf einem privaten Netzwerkclient ausgeführt wird, so Verhalten, als ob Sie direkt mit einer Remote-Internet Serveranwendung verbunden wäre.</span><span class="sxs-lookup"><span data-stu-id="8707f-105">Winsock Proxy lets a Windows Sockets application, running on a private network client, behave as if it were directly connected to a remote Internet server application.</span></span> <span data-ttu-id="8707f-106">Der Microsoft-Proxy Server fungiert als Host für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="8707f-106">The Microsoft Proxy Server acts as the host for this connection.</span></span> <span data-ttu-id="8707f-107">Dies bedeutet, dass die gesamte Kommunikation auf Anwendungsebene über einen einzelnen gesicherten Computer geleitet wird – dem Gatewaycomputer, auf dem Microsoft Proxy Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8707f-107">This means that all application-level communications are channeled through a single secured computer—the gateway computer running Microsoft Proxy Server.</span></span>

<span data-ttu-id="8707f-108">Normalerweise umgeht die RPC-Transport-dll bei der Übertragung von Datagramm-Paketen die in Wsock32.dll bereitgestellten Funktionen [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) und [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) und kommuniziert direkt mit dem zugrunde liegenden Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="8707f-108">Ordinarily, for datagram-packet transfers, the RPC transport DLL bypasses the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) functions provided in Wsock32.dll, and communicates directly with the underlying device driver.</span></span> <span data-ttu-id="8707f-109">Dadurch wird die Geschwindigkeit der Paket Übertragungen erhöht, aber die Winsock-Proxy Funktionen sind für die Anwendung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8707f-109">This improves the speed of packet transfers but makes Winsock Proxy features unavailable to the application.</span></span>

<span data-ttu-id="8707f-110">Jedem Netzwerkprotokoll Anbieter muss eine GUID zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="8707f-110">Each network protocol provider to have an associated GUID.</span></span> <span data-ttu-id="8707f-111">Die RPC-Lauf Zeit Bibliothek vergleicht die UDP-und IPX-GUIDs mit den bekannten Microsoft-bezeichnerbezeichner.</span><span class="sxs-lookup"><span data-stu-id="8707f-111">The RPC run-time library compares the UDP and IPX GUIDs to the well known Microsoft identifiers.</span></span> <span data-ttu-id="8707f-112">Wenn Sie nicht identisch sind, verwendet RPC automatisch Winsock.</span><span class="sxs-lookup"><span data-stu-id="8707f-112">If they don't match, RPC automatically uses Winsock.</span></span>

<span data-ttu-id="8707f-113">Eine weitere Funktion des Winsock-Proxys ist die Möglichkeit, das TCP-Transportprotokoll über den Novell SPX-Transport zu emulieren, wenn auf dem SPX-Client Computer TCP nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8707f-113">Another feature of Winsock Proxy is its ability to emulate the TCP transport protocol over the Novell SPX transport when the SPX client computer does not have TCP installed.</span></span> <span data-ttu-id="8707f-114">Wenn Sie dieses Feature mit RPC-Anwendungen verwenden möchten, bearbeiten Sie die Systemregistrierung auf jedem Client Computer, um diesen Eintrag hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="8707f-114">To use this feature with RPC applications, edit the system registry on each client computer to add this entry:</span></span>

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

<span data-ttu-id="8707f-115">Bearbeiten Sie die Registrierung auf jedem Server Computer, um diesen Eintrag hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="8707f-115">Edit the registry on each server computer to add this entry:</span></span>

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

<span data-ttu-id="8707f-116">Weitere Informationen zu RPC-Transportprotokollen finden Sie unter [Angeben von Protokoll Sequenzen](specifying-protocol-sequences.md).</span><span class="sxs-lookup"><span data-stu-id="8707f-116">For more information about RPC transport protocols see [Specifying Protocol Sequences](specifying-protocol-sequences.md).</span></span> <span data-ttu-id="8707f-117">Weitere Informationen zum Winsock-Proxy finden Sie in der Produktdokumentation für Microsoft Internet Access Server.</span><span class="sxs-lookup"><span data-stu-id="8707f-117">For more information about Winsock Proxy, see the product documentation for Microsoft Internet Access Server.</span></span>

<span data-ttu-id="8707f-118">Die Registrierungseinträge **clientprotokolls** und **Server Protokolle** werden von Windows 2000 nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8707f-118">Windows 2000 does not implement the **ClientProtocols** and **ServerProtocols** registry entries.</span></span> <span data-ttu-id="8707f-119">Microsoft stellt alle bekannten Transporte als Teil der Lauf Zeit Bibliothek bereit.</span><span class="sxs-lookup"><span data-stu-id="8707f-119">Microsoft provides all well known transports as part of the run-time library.</span></span> <span data-ttu-id="8707f-120">Daher sind diese Einträge nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8707f-120">Therefore, these entries are not necessary.</span></span>

 

 