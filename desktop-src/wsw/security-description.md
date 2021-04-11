---
title: Sicherheits Beschreibung
description: Eine Sicherheits Beschreibung wird durch eine WS \_ \_ -Sicherheits Beschreibungs Struktur dargestellt, und es wird eine Instanz einer Sicherheits Beschreibung bereitgestellt, wenn Sie die wscreatechannel-Funktion aufrufen, um einen sicheren Kanal zu erstellen, oder die wscreatelistener-Funktion, um einen Listener zu erstellen.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Sicherheits Beschreibung Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104132133"
---
# <a name="security-description"></a>Sicherheits Beschreibung

Eine Sicherheits Beschreibung wird durch eine [**WS- \_ Sicherheits \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) Struktur dargestellt, und es wird eine Instanz einer Sicherheits Beschreibung bereitgestellt, wenn Sie die [**wscreatechannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) -Funktion aufrufen, um einen sicheren Kanal zu erstellen, oder die [**wscreatelistener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) -Funktion, um einen Listener zu erstellen.


## <a name="structure-of-a-security-description"></a>Struktur einer Sicherheits Beschreibung

Das grundlegende Modell der Channelsicherheit ist, dass ein Kanal durch mindestens ein Sicherheits Token geschützt ist. Die [**WS- \_ Sicherheits \_ Beschreibungs**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) Struktur enthält eine Liste von Sicherheits Bindungen, die durch WS- [**\_ \_ sicherheitsbindungs**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) Strukturen dargestellt werden, und jede Sicherheitsbindung beschreibt, wie ein Sicherheits Token abgerufen und auf dem Kanal verwendet wird. Die Art der Sicherheit, die auf einem Kanal verwendet wird, wird durch die Auswahl von sicherheitsbindungs-Untertypen festgelegt, die in der Sicherheits Beschreibung enthalten sind.

Optionale Sicherheitseinstellungen, die für eine Sicherheitsbindung spezifisch sind, werden in der Sicherheits Bindungsstruktur als [sicherheitsbindungs Einstellungen](security-binding-settings.md) angegeben. Allerdings werden Kanal weite Einstellungen unabhängig von Sicherheits Bindungen direkt als [Sicherheits Kanaleinstellungen](security-channel-settings.md) im **Eigenschaften** Feld der Sicherheits Beschreibung selbst angegeben.

![Diagramm, das die Struktur einer Sicherheits Beschreibung anzeigt.](images/securitydescription.png)

Die folgenden API-Elemente werden mit Sicherheits Beschreibungen verwendet.

| Struktur                                                    | BESCHREIBUNG                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS- \_ Sicherheits \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | Die Struktur der obersten Ebene, die verwendet wird, um die Sicherheitsanforderungen für einen Kanal (auf der Clientseite) oder einen Listener (auf der Serverseite) anzugeben. |



 

 

 




