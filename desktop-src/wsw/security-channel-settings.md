---
title: Sicherheits Kanaleinstellungen
description: Mit den Sicherheits Kanaleinstellungen wird gesteuert, wie die Sicherheit auf einem Kanal angewendet und überprüft wird.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Sicherheits Kanaleinstellungen Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102574"
---
# <a name="security-channel-settings"></a>Sicherheits Kanaleinstellungen

Mit den Sicherheits Kanaleinstellungen wird gesteuert, wie die Sicherheit auf einem Kanal angewendet und überprüft wird. Jede Sicherheits Kanal Einstellung wird durch eine Auflistung von Eigenschaften-Wert-Paaren dargestellt, wobei die Eigenschafts Schlüssel durch die Enumeration [**WS- \_ Sicherheits \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)definiert werden. Jede Eigenschaft in der Auflistung weist einen angemessenen Standardwert auf. Aufgrund dieser Standardwerte ist es möglich, eine Sicherheits Beschreibung zu definieren und zu verwenden, ohne die Sicherheits Kanaleinstellungen anzugeben.


[Sicherheitsbindungs Einstellungen](security-binding-settings.md) enthalten ähnliche Auflistungen von Eigenschafts-Wert-Paaren, deren Schlüssel durch die [**WS- \_ \_ sicherheitsbindungs- \_ Eigenschafts**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) Struktur definiert werden. Der Unterschied zwischen diesen beiden Arten von Einstellungen besteht darin, dass die Sicherheits Kanaleinstellungen auf eine Sicherheits Beschreibung beschränkt sind (d. h., Sie enthalten channelweite Sicherheitseigenschaften), während die sicherheitsbindungs Einstellungen auf eine der Sicherheits Bindungen beschränkt sind und möglicherweise viele Sicherheits Bindungen vorhanden sind. Folglich hat beispielsweise eine benutzerdefinierte Sicherheits Beschreibung, die drei Sicherheits Bindungen enthält, einen Sicherheits Kanal-Einstellungs Behälter für den gesamten Kanal und drei Einstellungen für die sicherheitsbindungs Einstellungen, eine für jede Sicherheitsbindung.

Die folgenden Enumerationen werden mit den Sicherheits Kanaleinstellungen verwendet:

-   [**WS- \_ Schutz \_ Ebene**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [**WS- \_ Anforderungs \_ Sicherheits Token-Eigenschaften- \_ \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [**WS- \_ Sicherheits \_ Algorithmus- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [**Eigenschaften-ID für WS- \_ Sicherheits \_ Algorithmus \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [**WS- \_ Sicherheits \_ Header \_ Layout**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [**WS- \_ Sicherheits \_ Header \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [**WS- \_ Sicherheits \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**WS- \_ Sicherheits \_ Zeitstempel- \_ Verwendung**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [**WS- \_ XML- \_ Sicherheits Token-Eigenschaften- \_ \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

Die folgenden Strukturen werden mit den Sicherheits Kanaleinstellungen verwendet:

-   [**WS- \_ Anforderungs \_ Sicherheits Token ( \_ \_ Eigenschaft)**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [**WS- \_ Sicherheits \_ Algorithmus ( \_ Eigenschaft)**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [**WS \_ - \_ Sicherheitsalgorithmussuite \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [**WS- \_ Sicherheits \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [**WS \_ XML- \_ Sicherheits \_ Token ( \_ Eigenschaft)**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




