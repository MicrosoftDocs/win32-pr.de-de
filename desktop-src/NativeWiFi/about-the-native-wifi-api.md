---
description: Die Native Wifi-API enthält Funktionen, Strukturen und Enumerationen, die drahtlose Netzwerkkonnektivität und die Verwaltung von Drahtlosprofilen unterstützen.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Informationen zur nativen WLAN-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fafbe65d162668930470712c79637a41fcd0ee0769441b745e68bca156ada4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685460"
---
# <a name="about-the-native-wifi-api"></a>Informationen zur nativen WLAN-API

Die Native Wifi-API enthält Funktionen, Strukturen und Enumerationen, die drahtlose Netzwerkkonnektivität und die Verwaltung von Drahtlosprofilen unterstützen. Die API kann sowohl für Infrastruktur- als auch für Ad-hoc-Netzwerke verwendet werden. Die Drahtlose Ad-hoc-API ist eine vereinfachte objektorientierte Schnittstelle zum Erstellen, Verwalten und Verwenden von Ad-hoc-Netzwerken.

> [!Note]  
> Der Ad-hoc-Modus ist in zukünftigen Versionen von Windows. Verwenden Sie Windows 8.1 und Windows Server 2012 R2 stattdessen [Wi-Fi Direct.](about-the-wi-fi-direct-api.md)

 

Die Implementierung der Ad-hoc-API verwendet die Native Wifi-API. Dies bedeutet, dass Ad-hoc-API-Aufrufe native WLAN-Benachrichtigungen auslösen können und umgekehrt.

Das Kombinieren von Native Wifi-API-Aufrufen und Drahtlosen Ad-hoc-API-Aufrufen wird nicht empfohlen. Entwickler sollten einen Programmieransatz auswählen, bevor sie eine Anwendung entwerfen. Wenn Ihre Anwendung Infrastrukturnetzwerke verwendet oder verwaltet, sollten Sie die Native Wifi-API verwenden. Wenn Ihre Anwendung Profilverwaltungsfunktionen erfordert, sollten Sie die Native Wifi-API verwenden. Andernfalls sollten Sie die Drahtlose Ad-hoc-API verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu nativem WLAN](about-native-wifi.md)
</dt> <dt>

[Native Wifi-API-Unterstützung auf Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[Native WIFI-API-Berechtigungen](native-wifi-api-permissions.md)
</dt> <dt>

[Informationen zur Drahtlosen Ad-hoc-API](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Herunterladen des Windows Vista SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



