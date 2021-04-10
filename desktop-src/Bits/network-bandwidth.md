---
title: Netzwerkbandbreite
description: Bei Hintergrund Übertragungen wird nur die Netzwerkbandbreite im Leerlauf verwendet, um die interaktive Benutzererfahrung mit anderen Netzwerkanwendungen, wie z. b. Internet Explorer, zu erhalten.
ms.assetid: c0b92a33-7afc-4250-8549-54cc46013239
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 39a38a0efd5f2caea432fc9d13f7a958b6bcd407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039225"
---
# <a name="network-bandwidth"></a>Netzwerkbandbreite

Bei Hintergrund Übertragungen wird nur die Netzwerkbandbreite im Leerlauf verwendet, um die interaktive Benutzererfahrung mit anderen Netzwerkanwendungen wie Webbrowsern beizubehalten. Bits passt die Verwendung der Bandbreite an, wenn der Benutzer die Bandbreite erhöht oder verringert. Beachten Sie, dass Bits während einer hohen Netzwerk Verwendung weiterhin eine kleine Menge von Daten überträgt, um sicherzustellen, dass BITS-Aufträge Fortschritte machen.

Bits überwacht den Netzwerk Datenverkehr auf dem Internet Gateway-Gerät (IGD) oder der Netzwerkschnittstellenkarte (NIC) des Clients und verwendet nur den Leerlauf Bereich der Netzwerkbandbreite. Bits aktiviert auch [ledbat](https://blogs.technet.microsoft.com/networking/2018/07/25/ledbat/) auf http-Verbindungen, um die Überlastung des Netzwerks zu unterstützen.

Wenn BITS den Datenverkehr mithilfe der Netzwerkschnittstellenkarte misst und keine Netzwerkanwendungen auf dem Client ausgeführt werden, verbraucht Bits die meiste verfügbare Bandbreite. Dies bedeutet nicht, dass sich das Netzwerk über dem Client im Leerlauf befindet. das Netzwerk kann eine vollständige Kapazität aufweisen.

Dies kann ein Problem sein, wenn der Client über einen schnellen Netzwerkadapter verfügt, die vollständige Internetverbindung jedoch über eine langsame Verbindung (z. b. einen DSL-Router) erfolgt, da Bits für die vollständige Bandbreite konkurriert, anstatt nur die verfügbare Bandbreite auf der langsamen Verbindung zu verwenden. Bits hat keinen Einblick in den Netzwerk Datenverkehr, der über den Client hinausgeht.

Ein Gatewaygerät, das Leistungsindikatoren unterstützt, kann dieses Problem vermeiden, weil Bits den Datenverkehr auf der langsamen Verbindung messen und die Bandbreite entsprechend verwenden würde. Wenn das Gerät keine Leistungsindikatoren unterstützt, können Sie die Auswirkung dieses Verbindungs Typs verringern, indem Sie die **MaxInternetBandwidth** -Richtlinie verwenden, um die Bandbreite zu begrenzen, die Bits auf dem Client Computer verwendet. Weitere Informationen finden Sie unter [Gruppenrichtlinien](group-policies.md).

Wenn der Computer mehrere Netzwerkschnittstellen enthält, z. b. ein Modem, ein virtuelles privates Netzwerk (VPN) und mehrere Netzwerkschnittstellenkarten (NIC), ruft Bits die IP-Hilfsfunktion [**getbestinterfaceex**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterfaceex)auf, um die Schnittstelle zu ermitteln, die die beste Route zu der angegebenen IP-Adresse hat. Bits überwacht dann die Bandbreitennutzung für diese Schnittstelle.

## <a name="using-an-internet-gateway-device-igd-to-determine-usage"></a>Verwenden eines Internet Gateway-Geräts (IGD) zum Bestimmen der Verwendung

Damit ein Gatewaygerät verwendet werden kann, muss das Gerät Byte Zähler unterstützen (das Gerät muss auf die Aktionen gettotalbytess und gettotalbytescount reagieren), und Universal Plug & Play (UPnP) muss aktiviert sein.

Bits verwendet die Netzwerkschnittstellenkarte, wenn Folgendes gilt:

-   Die Leistungsindikatoren werden vom Gatewaygerät nicht unterstützt.
-   UPnP ist nicht aktiviert.
-   Der Server befindet sich im gleichen Subnetz.
-   Das Gatewaygerät gibt die Zählers Daten nicht in weniger als 200 Ticks zurück.

Wenn der Benutzer ein öffentliches Netzwerk Profil verwendet, muss das Profil UPnP zulassen. Standardmäßig lassen die privaten und Domänen-Netzwerk Profile UPnP zu.

Wenn eine VPN-Verbindung verwendet wird, verwendet Bits das erste von UPnP zurückgegebene Gerät.