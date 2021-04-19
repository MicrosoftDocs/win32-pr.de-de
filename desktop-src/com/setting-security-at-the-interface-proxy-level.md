---
title: Festlegen der Sicherheit auf der Ebene des Schnittstellen Proxys
description: Manchmal benötigt der Client eine präzisere Kontrolle über die Sicherheit bei Aufrufen bestimmter Schnittstellen.
ms.assetid: 72925ca2-78c9-47d9-8760-63f6379326d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b38fe83e8ce8841cc9029808a6947ec67d4eaf4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341559"
---
# <a name="setting-security-at-the-interface-proxy-level"></a>Festlegen der Sicherheit auf der Ebene des Schnittstellen Proxys

Manchmal benötigt der Client eine präzisere Kontrolle über die Sicherheit bei Aufrufen bestimmter Schnittstellen. Beispielsweise kann die Sicherheit auf niedriger Ebene für den Prozess festgelegt werden, aber Aufrufe an eine bestimmte Schnittstelle erfordern möglicherweise eine höhere Authentifizierungs Ebene, z. b. die Verschlüsselung. Mit den Methoden der [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) -Schnittstelle kann der Client die Sicherheitseinstellungen ändern, die den Aufrufen einer bestimmten Schnittstelle zugeordnet sind, indem die Sicherheitseinstellungen auf der Schnittstellen-Proxy Ebene gesteuert werden.

Der Client kann ein vorhandenes Objekt für [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) Abfragen und dann die [**IClientSecurity:: queryblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-queryblanket) -Methode aufzurufen, um herauszufinden, welche der aktuellen Sicherheitseinstellungen für einen bestimmten Schnittstellen Proxy vorhanden sind. Die [**IClientSecurity:: setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) -Methode kann verwendet werden, um die Sicherheitseinstellungen eines einzelnen Schnittstellen Proxys für das Objekt zu ändern, bevor eine der Methoden der Schnittstelle aufgerufen wird. Die neuen Einstellungen gelten für zukünftige Aufrufer dieser speziellen Schnittstelle. Die [**IClientSecurity:: copyproxy**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-copyproxy) -Methode bietet dem Client die Möglichkeit, einen Schnittstellen Proxy zu kopieren, damit nachfolgende Aufrufe von **setblanket** für die Kopie keine Auswirkungen auf Aufrufer des ursprünglichen Proxys haben.

[**Setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) wird häufig verwendet, um die Authentifizierungs Ebene für einen bestimmten Schnittstellen Proxy auf einen höheren Grad an Sicherheitsschutz zu erhöhen. In einigen Situationen kann es jedoch auch hilfreich sein, die Authentifizierungs Ebene für einen bestimmten Schnittstellen Proxy zu verringern. Nehmen wir beispielsweise an, die Standard Authentifizierungs Ebene für den Prozess ist ein anderer Wert als RPC \_ \_ -C-authn \_ -Ebene "None", \_ und der Client und der Server befinden sich in separaten Domänen, die sich nicht gegenseitig vertrauen. In diesem Fall können Aufrufe an den Server nicht ausgeführt werden, es sei denn, der Client ruft **setblanket** auf, um die Authentifizierungs Ebene auf RPC- \_ C- \_ authn- \_ Ebene " \_ None"

Clients, die die vom Proxy-Manager bereitgestellte Standard Implementierung von [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) verwenden, können die Hilfsfunktionen [**coqueryproxyblanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)und [**cocopyproxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) aufrufen, anstatt die **IClientSecurity** -Methoden direkt aufzurufen. Die Hilfsfunktionen vereinfachen den Code, sind aber etwas weniger effizient, als die entsprechenden **IClientSecurity** -Methoden direkt aufrufen.

Die [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) -Schnittstelle wird vom Proxy-Manager lokal für den Client implementiert. Einige benutzerdefinierte gemarshallte Objekte unterstützen **IClientSecurity** möglicherweise nicht.

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) funktioniert mit allen unterstützten Authentifizierungsdiensten (zurzeit NTLMSSP, SChannel und das Kerberos V5-Protokoll).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 