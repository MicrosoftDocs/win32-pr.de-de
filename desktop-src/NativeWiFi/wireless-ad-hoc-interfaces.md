---
description: Die drahtlose Ad-hoc-Programmierschnittstelle besteht aus den folgenden Schnittstellen.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Drahtlose Ad-hoc-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c486da50a922a893f4378c4d139741953705f0500cfb78484548db933bb285c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800280"
---
# <a name="wireless-ad-hoc-interfaces"></a>Drahtlose Ad-hoc-Schnittstellen

Die drahtlose Ad-hoc-Programmierschnittstelle besteht aus den folgenden Schnittstellen.



| Schnittstellenname                                                                       | BESCHREIBUNG                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | Stellt eine Drahtlose Netzwerkschnittstellenkarte (NIC) dar.                                                    |
| [**IDot11AdHocInterfaceNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | Definiert die von [**IDot11AdHocInterface unterstützten Benachrichtigungen.**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)           |
| [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | Erstellt und verwaltet 802.11 Ad-hoc-Netzwerke.                                                            |
| [**IDot11AdHocManagerNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | Definiert die von der [**IDot11AdHocManager-Schnittstelle unterstützten Benachrichtigungen.**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) |
| [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | Stellt ein verfügbares Ad-hoc-Netzwerkziel innerhalb des Verbindungsbereichs dar.                            |
| [**IDot11AdHocNetworkNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | Definiert die von der [**IDot11AdHocNetwork-Schnittstelle unterstützten Benachrichtigungen.**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) |
| [**IDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | Gibt die Sicherheitseinstellungen für ein Drahtloses Ad-hoc-Netzwerk an.                                         |
| [**IEnumDot11AdHocInterfaces**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | Stellt die Auflistung der derzeit sichtbaren Ad-hoc-Netzwerkschnittstellen 802.11 dar.                       |
| [**IEnumDot11AdHocNetworks**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | Stellt die Auflistung der derzeit sichtbaren 802.11 Ad-hoc-Netzwerke dar.                                 |
| [**IEnumDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | Stellt die Auflistung der Sicherheitseinstellungen dar, die jedem sichtbaren Drahtlosen Ad-hoc-Netzwerk zugeordnet sind.   |



 

> [!Note]  
> Der Ad-hoc-Modus ist in zukünftigen Versionen von Windows. Verwenden Sie Windows 8.1 und Windows Server 2012 R2 stattdessen [Wi-Fi Direct.](about-the-wi-fi-direct-api.md)

 

 

 



