---
title: Remotedesktop Gateway-Schnittstellen
description: Die Remotedesktop Gateway-API (RD-Gateway) unterstützt die folgenden Schnittstellen. Sie können diese Schnittstellen zum Implementieren von Plug-Ins verwenden, die eine angepasste Authentifizierung und Autorisierung bereitstellen.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947445"
---
# <a name="remote-desktop-gateway-interfaces"></a>Remotedesktop Gateway-Schnittstellen

Die Remotedesktop Gateway-API (RD-Gateway) unterstützt die folgenden Schnittstellen. Sie können diese Schnittstellen zum Implementieren von Plug-Ins verwenden, die eine angepasste Authentifizierung und Autorisierung bereitstellen. Es besteht keine Abhängigkeit zwischen dem Authentifizierungs-Plug-in und dem Autorisierungs-Plug-in, und Sie können nur ein einzelnes Plug-in implementieren, wenn Sie auswählen.

Die Authentifizierungs-Plug-ins sind [**itsgauthentiereusersink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) und [**itsgauthenticationengine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).

Die Autorisierungs-Plug-ins sind [**itsgaccountingengine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**itsgauthorizeconnectionsink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**itsgautorizeresourcesink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)und [**itsgpolicyengine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Itsgaccountingengine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

Macht Methoden verfügbar, die Informationen über das Erstellen oder Schließen von Sitzungen für eine Verbindung bereitstellen.

</dd> <dt>

[**Itsgauthentisineusersink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

Macht Methoden verfügbar, die RD-Gateway über Authentifizierungs Ereignisse benachrichtigen.

</dd> <dt>

[**Itsgauthenticationengine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

Macht Methoden verfügbar, die Benutzer für RD-Gateway authentifizieren.

</dd> <dt>

[**Itsgauthorizeconnectionsink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

Macht Methoden verfügbar, die RD-Gateway über das Ergebnis des Versuchs, eine Verbindung zu autorisieren, benachrichtigt werden.

</dd> <dt>

[**Itsgautorizeresourcesink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

Macht Methoden verfügbar, die RD-Gateway über das Ergebnis des Versuchs, eine Ressource zu autorisieren, benachrichtigt werden.

</dd> <dt>

[**Itsgpolicyengine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

Macht Methoden verfügbar, die Verbindungen und Ressourcen autorisieren.

</dd> </dl>

 

 




