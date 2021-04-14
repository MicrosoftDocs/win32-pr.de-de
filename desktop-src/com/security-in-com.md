---
title: Sicherheit in com
description: Die Sicherheit in com basiert auf der von Windows bereitgestellten Sicherheit und den zugrunde liegenden RPC-Sicherheitsmechanismen.
ms.assetid: c9f6d06c-da24-48ea-908a-2462c33f7ee3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5e462317d85f7c445d4d8a5ae0aa4d9d3ee724
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391077"
---
# <a name="security-in-com"></a>Sicherheit in com

Die Sicherheit in com basiert auf der von Windows bereitgestellten Sicherheit und den zugrunde liegenden RPC-Sicherheitsmechanismen. Die com-Sicherheit basiert auf der *Authentifizierung* (dem Prozess der Überprüfung der Identität eines Aufrufers) und der *Autorisierung* (der Prozess der Bestimmung, ob ein Aufrufer für die Anforderungen autorisiert ist). Es gibt zwei Haupt Sicherheits Typen in com: *Aktivierungs Sicherheit* und *Sicherheits* Einstellungen. Die Aktivierungs Sicherheit bestimmt, ob ein Client überhaupt einen Server starten kann. Nachdem ein Server gestartet wurde, können Sie mithilfe von "callsecurity" den Zugriff auf die Objekte eines Servers steuern.

In diesem Sicherheitsmodell verwalten und schützen Server Objekte, Clients erhalten Zugriff auf Objekte über Server, und Server können versuchen, auf die Identität des Clients zuzugreifen.

Das System implementiert das Kerberos V5-Authentifizierungsprotokoll und das SChannel-Sicherheitspaket. Sie enthält auch Features wie den Identitätswechsel auf delegatebene, die gegenseitige Authentifizierung, die Möglichkeit zum Festlegen von Authentifizierungs Ebenen für eine AppID in der Registrierung und das Cloaking. Mithilfe der com-Sicherheit können Sie Objekte implementieren, die privilegierte Vorgänge ausführen können, ohne die Sicherheit zu beeinträchtigen.

Da eine große Bandbreite an com-Sicherheitsfeatures verfügbar ist, ist es hilfreich, zunächst zu ermitteln, welche Art von Sicherheit die Anwendung benötigt. Bei den meisten Anwendungen kann das Festlegen eines akzeptablen Sicherheitsniveaus ein unkomplizierter Prozess sein, aber Sie können auch com-Sicherheit verwenden, um sehr komplexe Sicherheits Szenarios zu unterstützen.

Sie können die Sicherheit Processwide festlegen, indem Sie entweder Dcomcnfg.exe verwenden, um die Registrierung festzulegen, oder indem Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aufrufen. Zwei primäre Schnittstellen, [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) und [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) (und zugehörige Hilfsfunktionen), ermöglichen es Ihnen, die Sicherheit auf Aufrufebene innerhalb des Programms festzulegen.

Weitere Informationen zur COM-Sicherheit finden Sie in den folgenden Themen:

-   [Bestimmen Ihrer Sicherheitsanforderungen](determining-your-security-needs.md)
-   [COM-Sicherheitsstandards](com-security-defaults.md)
-   [Aktivierungs Sicherheit](activation-security.md)
-   [Sicherheitswerte](security-values.md)
-   [Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
-   [Aktivieren der com-Sicherheit mithilfe von DCOMCNFG](enabling-com-security-using-dcomcnfg.md)
-   [Ausschalten der Sicherheit](turning-off-security.md)
-   [Server seitige Sicherheit](server-side-security.md)
-   [Aushandlung der Sicherheits Pauschale](security-blanket-negotiation.md)
-   [COM-und Sicherheitspakete](com-and-security-packages.md)
-   [DCOM-Sicherheitsverbesserungen in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
-   [Access Control Listen für com](access-control-lists-for-com.md)
-   [Der com-Erhöhungs Moniker.](the-com-elevation-moniker.md)

 

 