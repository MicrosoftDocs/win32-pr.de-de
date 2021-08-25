---
title: Verwenden Remotedesktopdienste
description: Erfahren Sie, wie Sie in der Remotedesktopdienste-Umgebung programmieren und Remotedesktopdienste (früher als Terminaldienste bezeichnet) Technologie mithilfe von Remotedesktop-Webverbindung.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d0af90aef8eed3c8b9dc397f86cb6940a79e8e399af201ff854cbfaba3ff3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868770"
---
# <a name="using-remote-desktop-services"></a>Verwenden Remotedesktopdienste

In den folgenden Abschnitten wird beschrieben, wie Sie in der Remotedesktopdienste-Umgebung programmieren und wie Sie Remotedesktopdienste-Technologie (früher als Terminaldienste bezeichnet) mithilfe von Remotedesktop-Webverbindung. Wenn Sie nach Benutzerinformationen für verbindungen Remotedesktop suchen, finden Sie weitere Informationen unter Herstellen Verbinden verbindung mit einem anderen [Computer mithilfe Remotedesktopverbindung](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).

> [!Note]  
> Dieses Thema ist für Softwareentwickler.

 

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Erkennen, ob die Remotedesktopdienste-Rolle installiert ist](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

C#-Codebeispiel, das eine Methode zeigt, die **True** zurückgibt, wenn die Remotedesktopdienste-Serverrolle installiert ist und ausgeführt wird, **andernfalls** false, beginnend mit Windows Server 2008.

</dd> <dt>

[Erweitern des Sitzungsbrokers für Terminaldienste](extending-ts-session-broker.md)
</dt> <dd>

Sie können den TS-Sitzungsbroker mithilfe der [**COM-Schnittstelle IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) erweitern.

</dd> <dt>

[Implementieren eines benutzerdefinierten Audioendpunkt-Enumerators](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

Ab Windows Server 2008 R2 können Sie einen benutzerdefinierten Remoteaudioendpunkt-Enumerator als Teil eines Remotedesktop implementieren.

</dd> <dt>

[Sitzungsmoniker](session-monikers.md)
</dt> <dd>

Verteiltes COM (DCOM) ermöglicht die Objektaktivierung pro Sitzung mithilfe eines vom System bereitgestellten Sitzungsmonikers.

</dd> <dt>

[Verwenden der ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

Die Verwaltung Remotedesktopdienste benutzerspezifischen Eigenschaften ist möglich, indem die Methoden verwendet werden, die von der AdsI-Erweiterung (Active Directory Service Interfaces) implementiert werden, die mit der Dynamic Link Library-Erweiterung Tsuserex.dll.

</dd> <dt>

[Verwenden der Remotedesktopdienste-API](using-the-terminal-services-api.md)
</dt> <dd>

Beschreibt, wie Sie die Remotedesktopdienste-API verwenden können, um Anwendungen das Ausführen von Aufgaben in einer Remotedesktopdienste ermöglichen.

</dd> <dt>

[Verwenden der Remotedesktop-Virtualisierungs-API](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

Entwickler können diese API verwenden, um die Logik anzupassen, die Remotedesktopverbindung Broker (RD-Verbindungsbroker) verwendet, um das beste Ziel für eine eingehende Clientverbindung zu ermitteln.

</dd> <dt>

[WSDL-Schnittstelle für benutzerdefinierte VDI-Lösungen](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

Entwickler können benutzerdefinierte Webdienste erstellen, die VDI-Lösungen (Virtual Desktop Infrastructure) verwalten.

</dd> </dl>

Weitere Informationen finden Sie unter [Remotedesktopdienste Programming Guidelines (Programmierrichtlinien).](terminal-services-programming-guidelines.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Terminaldienste sind jetzt Remotedesktopdienste](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Erkennen der Remotedesktopdienste Umgebung](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




