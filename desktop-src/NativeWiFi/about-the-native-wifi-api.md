---
description: Die native WiFi-API enthält Funktionen, Strukturen und Enumerationen, die Drahtlos Netzwerk Konnektivität und drahtlose Profilverwaltung unterstützen.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Informationen zur nativen WiFi-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218198"
---
# <a name="about-the-native-wifi-api"></a>Informationen zur nativen WiFi-API

Die native WiFi-API enthält Funktionen, Strukturen und Enumerationen, die Drahtlos Netzwerk Konnektivität und drahtlose Profilverwaltung unterstützen. Die API kann sowohl für Infrastruktur-als auch für Ad-hoc-Netzwerke verwendet werden. Die drahtlose Ad-hoc-API ist eine vereinfachte objektorientierte Schnittstelle zum Erstellen, verwalten und Verwenden von Ad-hoc-Netzwerken.

> [!Note]  
> Der Ad-hoc-Modus ist möglicherweise in zukünftigen Versionen von Windows nicht verfügbar. Beginnen Sie mit Windows 8.1 und Windows Server 2012 R2, und verwenden Sie stattdessen [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .

 

Bei der Implementierung der Ad-hoc-API wird die native WiFi-API verwendet. Dies bedeutet, dass Ad-hoc-API-Aufrufe Native WiFi-Benachrichtigungen und umgekehrt aufrufen können.

Es wird nicht empfohlen, Native WiFi-API-Aufrufe und drahtlose Ad-hoc-API-Aufrufe zu mischen Entwickler sollten einen Programmier Ansatz auswählen, bevor Sie eine Anwendung entwerfen. Wenn Ihre Anwendung Infrastruktur Netzwerke verwendet oder verwaltet, sollten Sie die native WiFi-API verwenden. Wenn für Ihre Anwendung Profil Verwaltungsfunktionen erforderlich sind, sollten Sie die native WiFi-API verwenden. Andernfalls sollten Sie die drahtlose Ad-hoc-API verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu nativem WiFi](about-native-wifi.md)
</dt> <dt>

[Native WiFi-API-Unterstützung unter Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[Native WiFi-API-Berechtigungen](native-wifi-api-permissions.md)
</dt> <dt>

[Informationen zur drahtlosen Ad-hoc-API](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Herunterladen des Windows Vista SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



