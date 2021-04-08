---
title: Erweitern des Terminal Dienste-Sitzungs Brokers
description: Sie können TS \ 160; erweitern. Sitzungs Broker mithilfe der COM-Schnittstelle iwtssbplugin.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729289"
---
# <a name="extending-terminal-services-session-broker"></a>Erweitern des Terminal Dienste-Sitzungs Brokers

Terminal Dienste-Sitzungs Broker (TS-Sitzungs Broker) bestimmt, ob ein Benutzer, der eine Verbindung initiiert, bereits eine Sitzung geöffnet hat. Wenn dies der Fall ist, leitet der TS-Sitzungs Broker die eingehende Verbindung mit der vorhandenen Sitzung an den Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server weiter. Wenn dies nicht der Fall ist, leitet der TS-Sitzungs Broker die eingehende Verbindung mit den wenigsten Sitzungen an den RD-Sitzungshost-Server weiter.

Sie können den TS-Sitzungs Broker mithilfe der COM-Schnittstelle [**iwtssbplugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) erweitern. Sie können diese Schnittstelle verwenden, um Verbindungen mit RD-Sitzungshost Servern sowie eine beliebige Art von Remotedesktopprotokoll (RDP) zu verwalten, z. b. Verbindungen mit virtuellen Gast Computern, auf denen Windows Vista Enterprise zentralisierte Desktop (VECD) auf einem Host für virtuelle Computer mit Windows Server 2008 Hyper-V ausgeführt wird.

Die [**iwtssbplugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) -Schnittstelle bietet mehrere Vorteile:

-   Es ist nicht erforderlich, einen Agent auf dem Client oder auf dem RD-Sitzungshost Server zu installieren.
-   Das Plug-in kann nahtlos mit anderen Remotedesktopdienste Rollen Diensten interagieren, z. b. Remotedesktop Gateway (RD-Gateway), und von den terminaldienstesitzungsbroker Informationen zu Sitzungs-und Computer Zuständen abhängen.
-   Sie können das-Plug-in verwenden, um Verbindungen mit Client-oder Server Geräten zu verwalten, die RDP 5,2 oder höher unterstützen.
-   Sie können das Plug-in verwenden, um Windows Vista Enterprise zentralisierten Desktop-Lösungen zu aktivieren.

Beachten Sie beim Implementieren der Methoden dieser Schnittstelle die folgenden Punkte:

-   Der TS-Sitzungs Broker kann die Methoden dieses COM-Objekts aus mehreren Threads abrufen.
-   Wenn eine der aufgerufenen Methoden nicht sofort und erfolgreich zurückgegeben wird, sendet der TS-Sitzungs Broker keine weiteren Aufrufe an das Plug-in und stellt die systemeigene Lasten Ausgleichs Logik wieder her. Um Aufrufe des Plug-ins fortzusetzen, müssen Sie den Terminal Dienste-Sitzungs Broker Dienst neu starten.
-   Sie müssen das Plug-in als systemweites com-Objekt registrieren, indem Sie Regsvr32.exe verwenden. Da der Terminal Dienste-Sitzungs Broker Dienst unter dem Konto "NetworkService" ausgeführt wird, müssen Sie dem Konto "Network Service" die erforderlichen Berechtigungen zum Starten, aktivieren und zugreifen über Dcomcnfg.exe einräumen. Der Terminal Dienste-Sitzungs Broker Dienst sucht nach der CLSID des COM-Objekts, das das Plug-in im folgenden Registrierungs Unterschlüssel darstellt:

    **HKEY \_ LOCAL \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Tssdis** \\ **Parameters** \\ **extensibilitypluginclsid**

Weitere Informationen zu Dcomcnfg.exe finden Sie unter [Aktivieren der com-Sicherheit mithilfe von DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwtssbplugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 