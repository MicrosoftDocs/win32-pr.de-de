---
description: Die drahtlos Schnittstelle für die Ad-hoc-Programmierung besteht aus den folgenden Schnittstellen.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Drahtlose Ad-hoc-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354590"
---
# <a name="wireless-ad-hoc-interfaces"></a>Drahtlose Ad-hoc-Schnittstellen

Die drahtlos Schnittstelle für die Ad-hoc-Programmierung besteht aus den folgenden Schnittstellen.



| Schnittstellenname                                                                       | BESCHREIBUNG                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | Stellt eine drahtlos Netzwerkschnittstellenkarte (NIC) dar.                                                    |
| [**IDot11AdHocInterfaceNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | Definiert die von [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)unterstützten Benachrichtigungen.           |
| [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | Erstellt und verwaltet 802,11 Ad-hoc-Netzwerke.                                                            |
| [**IDot11AdHocManagerNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | Definiert die von der [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) -Schnittstelle unterstützten Benachrichtigungen. |
| [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | Stellt ein verfügbares Ad-hoc-Netzwerk Ziel innerhalb des Verbindungs Bereichs dar.                            |
| [**IDot11AdHocNetworkNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | Definiert die von der [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) -Schnittstelle unterstützten Benachrichtigungen. |
| [**IDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | Gibt die Sicherheitseinstellungen für ein drahtloses Ad-hoc-Netzwerk an.                                         |
| [**IEnumDot11AdHocInterfaces**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | Stellt die Auflistung der derzeit sichtbaren 802,11 Ad-hoc-Netzwerkschnittstellen dar.                       |
| [**IEnumDot11AdHocNetworks**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | Stellt die Auflistung der derzeit sichtbaren 802,11 Ad-hoc-Netzwerke dar.                                 |
| [**IEnumDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | Stellt die Auflistung der Sicherheitseinstellungen dar, die jedem sichtbaren drahtlos-Ad-hoc-Netzwerk zugeordnet sind.   |



 

> [!Note]  
> Der Ad-hoc-Modus ist möglicherweise in zukünftigen Versionen von Windows nicht verfügbar. Beginnen Sie mit Windows 8.1 und Windows Server 2012 R2, und verwenden Sie stattdessen [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .

 

 

 



