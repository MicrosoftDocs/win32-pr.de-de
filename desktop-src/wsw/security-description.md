---
title: Sicherheitsbeschreibung
description: Eine Sicherheitsentschlüsselung wird durch eine WS \_ SECURITY \_ DESCRIPTION-Struktur dargestellt, und eine Instanz einer Sicherheitsbeschreibung wird bereitgestellt, wenn Sie die WsCreateChannel-Funktion aufrufen, um einen sicheren Kanal zu erstellen, oder die WsCreateListener-Funktion, um einen Listener zu erstellen.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Webdienste zur Sicherheitsbeschreibung für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a2395e2c1e894968f47fa41e98599ec333f6d2724cf6ffe6cbc5219396bca6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083159"
---
# <a name="security-description"></a>Sicherheitsbeschreibung

Eine Sicherheitsentschlüsselung wird durch eine [**WS \_ SECURITY \_ DESCRIPTION-Struktur**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) dargestellt, und eine Instanz einer Sicherheitsbeschreibung wird bereitgestellt, wenn Sie die [**WsCreateChannel-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) aufrufen, um einen sicheren Kanal zu erstellen, oder die [**WsCreateListener-Funktion,**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) um einen Listener zu erstellen.


## <a name="structure-of-a-security-description"></a>Struktur einer Sicherheitsbeschreibung

Das grundlegende Modell der Kanalsicherheit ist, dass ein Kanal mit einem oder mehreren Sicherheitstoken geschützt wird. In diesem Modell enthält die [**WS \_ SECURITY \_ DESCRIPTION-Struktur**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) eine Liste von Sicherheitsbindungen, die durch [**WS \_ SECURITY \_ BINDING-Strukturen**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) dargestellt werden, und jede Sicherheitsbindung beschreibt, wie ein Sicherheitstoken abgerufen und im Kanal verwendet wird. Die Art der Sicherheit, die auf einem Kanal verwendet wird, wird durch die Auswahl von Sicherheitsbindungsuntertypen bestimmt, die in der Sicherheitsbeschreibung enthalten sind.

Optionale Sicherheitseinstellungen, die für eine Sicherheitsbindung spezifisch sind, werden als [Sicherheitsbindungseinstellungen](security-binding-settings.md) in der Sicherheitsbindungsstruktur angegeben. Kanalweite Einstellungen werden jedoch unabhängig von Sicherheitsbindungen direkt als [Sicherheitskanaleinstellungen](security-channel-settings.md) im **Eigenschaftenfeld** der Sicherheitsbeschreibung selbst angegeben.

![Diagramm, das die Struktur einer Sicherheitsbeschreibung zeigt.](images/securitydescription.png)

Die folgenden API-Elemente werden mit Sicherheitsbeschreibungen verwendet.

| Struktur                                                    | Beschreibung                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_WS-SICHERHEITSBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | Die Struktur der obersten Ebene, mit der die Sicherheitsanforderungen für einen Kanal (clientseitig) oder einen Listener (auf Serverseite) angegeben werden. |



 

 

 




