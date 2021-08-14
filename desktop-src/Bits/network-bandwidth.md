---
title: Netzwerkbandbreite
description: Hintergrundübertragungen verwenden nur Netzwerkbandbreite im Leerlauf, um die interaktive Benutzererfahrung des Benutzers mit anderen Netzwerkanwendungen wie Internet Explorer beizubehalten.
ms.assetid: c0b92a33-7afc-4250-8549-54cc46013239
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 57b6583a99c16748c027fca1666571fc04d9e9aebe27fd104f7ab1215fa27a60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173361"
---
# <a name="network-bandwidth"></a>Netzwerkbandbreite

Bei Hintergrundübertragungen wird nur die Netzwerkbandbreite im Leerlauf genutzt, um die interaktive Benutzeroberfläche des Benutzers mit anderen Netzwerkanwendungen wie Webbrowsern beizubehalten. BITS passt die Verwendung der Bandbreite an, wenn der Benutzer die Bandbreitennutzung erhöht oder verringert. Beachten Sie, dass BITS bei hoher Netzwerknutzung immer noch eine kleine Datenmenge überträgt, um sicherzustellen, dass BITS-Aufträge fortschritten.

BITS überwacht den Netzwerkdatenverkehr auf dem Internetgatewaygerät (IGD) oder der Netzwerkschnittstellenkarte (Network Interface Card, NIC) des Clients und verwendet nur den Leerlaufteil der Netzwerkbandbreite. BITS aktiviert auch [LEDBAT](https://blogs.technet.microsoft.com/networking/2018/07/25/ledbat/) für HTTP-Verbindungen, um netzwerküberlastet zu werden.

Wenn BITS die Netzwerkschnittstellenkarte zum Messen des Datenverkehrs verwendet und keine Netzwerkanwendungen auf dem Client ausgeführt werden, verbraucht BITS den größten Teil der verfügbaren Bandbreite. Dies bedeutet nicht, dass sich das Netzwerk außerhalb des Clients im Leerlauf befindet. Das Netzwerk kann voll ausgelastet sein.

Dies kann ein Problem sein, wenn der Client über einen schnellen Netzwerkadapter verfügt, die vollständige Internetverbindung jedoch über eine langsame Verbindung (z. B. einen DSL-Router) erfolgt, da BITS um die vollständige Bandbreite konkurrieren wird, anstatt nur die verfügbare Bandbreite für die langsame Verbindung zu verwenden. BITS hat keine Sichtbarkeit des Netzwerkdatenverkehrs über den Client hinaus.

Ein Gatewaygerät, das Indikatoren unterstützt, kann dieses Problem beseitigen, da BITS den Datenverkehr auf der langsamen Verbindung messen und die Bandbreite entsprechend verwenden würde. Wenn das Gerät keine Leistungsindikatoren unterstützt, können Sie die Auswirkungen dieser Art von Verbindung verringern, indem Sie die **MaxInternetBandwidth-Richtlinie** verwenden, um die Bandbreite einzuschränken, die BITS auf dem Clientcomputer verwendet. Weitere Informationen finden Sie unter [Gruppenrichtlinien.](group-policies.md)

Wenn der Computer mehrere Netzwerkschnittstellen enthält, z. B. ein Modem, ein virtuelles privates Netzwerk (VPN) und mehrere Netzwerkschnittstellenkarten (NIC), ruft BITS die IP-Hilfsfunktion [**GetBestInterfaceEx**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterfaceex)auf, um die Schnittstelle zu bestimmen, die die beste Route zur angegebenen IP-Adresse auf hat. BITS überwacht dann die Bandbreitennutzung auf dieser Schnittstelle.

## <a name="using-an-internet-gateway-device-igd-to-determine-usage"></a>Ermitteln der Nutzung mithilfe eines Internetgatewaygeräts (IGD)

Um ein Gatewaygerät zu verwenden, muss das Gerät Bytezähler unterstützen (das Gerät muss auf die Aktionen GetTotalBytesSent und GetTotalBytesReceived reagieren), und universelle Plug & Play (UPnP) muss aktiviert sein.

BITS verwendet die Netzwerkschnittstellenkarte, wenn:

-   Das Gatewaygerät unterstützt die Leistungsindikatoren nicht.
-   UPnP ist nicht aktiviert
-   Der Server befindet sich im selben Subnetz.
-   Das Gatewaygerät gibt die Indikatordaten nicht in weniger als 200 Ticks zurück.

Wenn der Benutzer ein öffentliches Netzwerkprofil verwendet, muss das Profil UPnP zulassen. Standardmäßig lassen die privaten Netzwerkprofile und Domänennetzwerkprofile UPnP zu.

Wenn eine VPN-Verbindung verwendet wird, verwendet BITS das erste Gerät, das UPnP zurückgibt.