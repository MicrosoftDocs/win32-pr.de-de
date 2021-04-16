---
description: Das System verwendet die Konfigurationsinformationen, um zu bestimmen, wie der Dienst gestartet wird.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Dienstkonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525823"
---
# <a name="service-configuration"></a>Dienstkonfiguration

Das System verwendet die Konfigurationsinformationen, um zu bestimmen, wie der Dienst gestartet wird. Zu den Konfigurationsinformationen zählen auch der Anzeige Name des dienstanens und seine Beschreibung. Für den DHCP-Dienst können Sie z. b. den anzeigen Amen "Dynamic Host Configuration Protocol Service" und die Beschreibung "stellt Internetadressen für Computer in Ihrem Netzwerk bereit" verwenden.

Zum Ändern der Konfigurationsinformationen für ein Dienst Objekt verwendet ein Konfigurationsprogramm die [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) -oder [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) -Funktion. Ein Beispiel finden Sie unter [Ändern einer Dienst Konfiguration](changing-a-service-configuration.md).

Zum Abrufen der Konfigurationsinformationen für ein Dienst Objekt verwendet das Konfigurationsprogramm die Funktion [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) oder [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) . Ein Beispiel finden Sie unter [Abfragen der Konfiguration eines Dienstanbieter](querying-a-service-s-configuration.md).

Die Dienst Konfigurationsfunktionen [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) und [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) unterstützen die Verwendung von Triggern zum Steuern des Dienst Starts.

Zum Ändern der Sicherheits Beschreibung für ein scmanager-Objekt oder ein Dienst Objekt verwendet ein Konfigurationsprogramm die [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) -Funktion. Zum Abrufen einer Kopie der Sicherheits Beschreibung verwendet das Konfigurationsprogramm die Funktion [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren eines Dienstanbieter mit SC](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
