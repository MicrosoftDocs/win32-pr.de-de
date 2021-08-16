---
title: Festlegen der Sicherheit auf Schnittstellenproxyebene
description: Manchmal benötigt der Client eine fein abgrenzende Kontrolle über die Sicherheit bei Aufrufen bestimmter Schnittstellen.
ms.assetid: 72925ca2-78c9-47d9-8760-63f6379326d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef969039dcfdc12449b7a8d0a3d63729ab5f84061ade1a743d21a1b6b34331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309095"
---
# <a name="setting-security-at-the-interface-proxy-level"></a>Festlegen der Sicherheit auf Schnittstellenproxyebene

Manchmal benötigt der Client eine fein abgrenzende Kontrolle über die Sicherheit bei Aufrufen bestimmter Schnittstellen. Beispielsweise kann die Sicherheit auf einer niedrigen Ebene für den Prozess festgelegt werden, aber Aufrufe einer bestimmten Schnittstelle erfordern möglicherweise eine höhere Authentifizierungsebene, z. B. Verschlüsselung. Die Methoden der [**IClientSecurity-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) ermöglichen es dem Client, die Sicherheitseinstellungen zu ändern, die Aufrufen einer bestimmten Schnittstelle zugeordnet sind, indem die Sicherheitseinstellungen auf Schnittstellenproxyebene kontrolliert werden.

Der Client kann ein vorhandenes Objekt für [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) abfragen und dann die [**IClientSecurity::QueryBlanket-Methode**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-queryblanket) aufrufen, um herauszufinden, welche Sicherheitseinstellungen für einen bestimmten Schnittstellenproxy aktuell gelten. Die [**IClientSecurity::SetBlanket-Methode**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) kann verwendet werden, um die Sicherheitseinstellungen für einen einzelnen Schnittstellenproxy für das Objekt zu ändern, bevor eine der Methoden der Schnittstelle aufruft. Die neuen Einstellungen gelten für alle zukünftigen Aufrufer dieser bestimmten Schnittstelle. Die [**IClientSecurity::CopyProxy-Methode**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-copyproxy) bietet dem Client die Möglichkeit, einen Schnittstellenproxy zu kopieren, damit nachfolgende Aufrufe von **SetBlanket** für die Kopie keine Aufrufe des ursprünglichen Proxys betreffen.

[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) wird häufig verwendet, um die Authentifizierungsebene für einen bestimmten Schnittstellenproxy auf eine höhere Sicherheitsstufe zu erhöhen. In einigen Situationen kann es jedoch auch hilfreich sein, die Authentifizierungsebene für einen bestimmten Schnittstellenproxy zu senken. Angenommen, die Standardauthentifizierungsebene für den Prozess ist ein anderer Wert als RPC \_ C \_ AUTHN LEVEL NONE, und client und server befinden sich in separaten Domänen, die einander \_ \_ nicht vertrauen. In diesem Fall können Aufrufe des Servers nicht ausgeführt werden, es sei denn, der Client ruft **SetBlanket** auf, um die Authentifizierungsebene auf RPC \_ C \_ AUTHN \_ LEVEL NONE zu \_ senken.

Clients, die die vom Proxy-Manager bereitgestellte Standardimplementierung von [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) verwenden, können die [**Hilfsfunktionen CoQueryProxyBlanket,**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)und [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) aufrufen, anstatt **IClientSecurity-Methoden** direkt auf aufruft. Die Hilfsfunktionen vereinfachen den Code, sind aber etwas weniger effizient als das direkte Aufrufen der entsprechenden **IClientSecurity-Methoden.**

Die [**IClientSecurity-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) wird vom Proxy-Manager lokal für den Client implementiert. Einige benutzerdefinierte gemarshallte Objekte unterstützen **IClientSecurity möglicherweise nicht.**

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) funktioniert mit allen unterstützten Authentifizierungsdiensten (derzeit NTLMSSP, Schannel und dem Kerberos v5-Protokoll).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 