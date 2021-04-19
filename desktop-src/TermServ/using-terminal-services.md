---
title: Verwenden von Remotedesktopdienste
description: Erfahren Sie, wie Sie in der Remotedesktopdienste Umgebung programmieren und Remotedesktopdienste (ehemals Terminaldienstetechnologie) mithilfe Remotedesktop-Webverbindung auf das Web erweitern.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac575a89d1ae8c7c065199aca136f2f0e5fc7459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338192"
---
# <a name="using-remote-desktop-services"></a>Verwenden von Remotedesktopdienste

In den folgenden Abschnitten wird beschrieben, wie Sie in der Remotedesktopdienste Umgebung programmieren und wie Sie Remotedesktopdienste (ehemals Terminaldienstetechnologie) mithilfe Remotedesktop-Webverbindung auf das Web erweitern. Wenn Sie nach Benutzerinformationen für Remotedesktop-Verbindungen suchen, finden Sie weitere Informationen unter [Herstellen einer Verbindung mit einem anderen Computer mithilfe Remotedesktopverbindung](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).

> [!Note]  
> Dieses Thema ist für Softwareentwickler konzipiert.

 

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Erkennen, ob die Remotedesktopdienste Rolle installiert ist](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

C#-Codebeispiel, das eine Methode anzeigt, die **true** zurückgibt, wenn die Remotedesktopdienste Server-Rolle installiert ist und ausgeführt wird oder andernfalls **false** ist, beginnend mit Windows Server 2008.

</dd> <dt>

[Erweitern des Terminal Dienste-Sitzungs Brokers](extending-ts-session-broker.md)
</dt> <dd>

Sie können den TS-Sitzungs Broker mithilfe der COM-Schnittstelle [**iwtssbplugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) erweitern.

</dd> <dt>

[Implementieren eines benutzerdefinierten audioendpunkt-Enumerators](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

Ab Windows Server 2008 R2 können Sie einen benutzerdefinierten remoteaudioendpunkt-Enumerator als Teil eines Remotedesktop Protokoll Anbieters implementieren.

</dd> <dt>

[Sitzungsmoniker](session-monikers.md)
</dt> <dd>

Verteiltes com (DCOM) ermöglicht die Objekt Aktivierung pro Sitzung mithilfe eines vom System bereitgestellten sitzungsmonikers.

</dd> <dt>

[Verwenden der ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

Die Verwaltung Remotedesktopdienste spezifischer Benutzereigenschaften ist möglich, indem die von der ADSI-Erweiterung (Active Directory Service Interfaces) implementierten Methoden verwendet werden, die mit der Dynamic Link Library-Tsuserex.dll verpackt werden.

</dd> <dt>

[Verwenden der Remotedesktopdienste-API](using-the-terminal-services-api.md)
</dt> <dd>

Beschreibt, wie Sie mit der Remotedesktopdienste-API Anwendungen in einer Remotedesktopdienste Umgebung ausführen können.

</dd> <dt>

[Verwenden der Remotedesktop Virtualization-API](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

Entwickler können diese API verwenden, um die Logik anzupassen, die Remotedesktopverbindung Broker (RD-Verbindungsbroker) verwendet, um das beste Ziel für eine eingehende Client Verbindung zu ermitteln.

</dd> <dt>

[WSDL-Schnittstelle für benutzerdefinierte VDI-Lösungen](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

Entwickler können benutzerdefinierte Webdienste erstellen, die VDI-Lösungen (Virtual Desktop Infrastructure) verwalten.

</dd> </dl>

Weitere Informationen finden Sie unter [Remotedesktopdienste-Programmier Richtlinien](terminal-services-programming-guidelines.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Terminal Dienste sind jetzt Remotedesktopdienste](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Erkennen der Remotedesktopdienste Umgebung](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




