---
title: Erweitern des Sitzungsbrokers für Terminaldienste
description: Sie können TS \ 160 erweitern. Sitzungsbroker mithilfe der IWTSSBPlugin-COM-Schnittstelle.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c859320c11a128ab01a719d17abd9927ea96f312e0aa3df5f0be76dcc0226b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737690"
---
# <a name="extending-terminal-services-session-broker"></a>Erweitern des Sitzungsbrokers für Terminaldienste

Terminal Services Session Broker (TS Session Broker) bestimmt, ob ein Benutzer, der eine Verbindung initiiert, bereits eine Sitzung geöffnet hat. In diesem Falle leitet der TS-Sitzungsbroker die eingehende Verbindung mit der vorhandenen Sitzung an den server Remotedesktop-Sitzungshost (RD-Sitzungshost) weiter. Falls nicht, leitet der TS-Sitzungsbroker die eingehende Verbindung mit den wenigsten Sitzungen an den RD-Sitzungshost-Server weiter.

Sie können den TS-Sitzungsbroker mithilfe der [**IWTSSBPlugin-COM-Schnittstelle**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) erweitern. Sie können diese Schnittstelle verwenden, um Verbindungen mit RD-Sitzungshost Servern sowie jede Art von rdp-Verbindung (Remotedesktopprotokoll) zu verwalten, z. B. Verbindungen mit virtuellen Gastcomputern, auf denen Windows Vista Enterprise Centralized Desktop (VECD) auf einem Windows Server 2008 Hyper-V-VM-Host ausgeführt wird.

Die [**IWTSSBPlugin-Schnittstelle**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) bietet mehrere Vorteile:

-   Es ist nicht erforderlich, einen Agent auf dem Client oder dem RD-Sitzungshost-Server zu installieren.
-   Das Plug-In kann nahtlos mit anderen Remotedesktopdienste Rollendiensten interagieren, z. B. Remotedesktop Gateway (RD-Gateway) und sich auf Informationen vom TS-Sitzungsbroker zu Sitzungs- und Computerzuständen verlassen.
-   Sie können das Plug-In verwenden, um Verbindungen mit Client- oder Servergeräten zu verwalten, die RDP 5.2 oder höher unterstützen.
-   Sie können das Plug-In verwenden, um Windows Vista Enterprise Centralized Desktop-Lösungen zu aktivieren.

Beachten Sie beim Implementieren der Methoden dieser Schnittstelle die folgenden Punkte:

-   Der TS-Sitzungsbroker ruft möglicherweise die Methoden dieses COM-Objekts aus mehreren Threads auf.
-   Wenn eine der aufgerufenen Methoden nicht sofort und erfolgreich zurückgegeben wird, ruft der TS-Sitzungsbroker das Plug-In nicht mehr auf und kehrt zu seiner nativen Lastenausgleichslogik zurück. Um Aufrufe des Plug-Ins fortzusetzen, müssen Sie den Sitzungsbrokerdienst für Terminaldienste neu starten.
-   Sie müssen das Plug-In mithilfe von Regsvr32.exe als systemweites COM-Objekt registrieren. Da der Sitzungsbrokerdienst für Terminaldienste unter dem Konto "NetworkService" ausgeführt wird, müssen Sie dem Konto "NetworkService" die erforderlichen Start-, Aktivierungs- und Zugriffsberechtigungen erteilen, indem Sie Dcomcnfg.exe verwenden. Der Sitzungsbrokerdienst für Terminaldienste sucht nach der CLSID des COM-Objekts, das das Plug-In im folgenden Registrierungsunterschlüssel darstellt:

    **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **Tssdis** \\ **Parameters** \\ **ExtensibilityPluginCLSID**

Weitere Informationen zu Dcomcnfg.exe finden Sie unter [Aktivieren der COM-Sicherheit mithilfe von DCOMCNFG.](/windows/desktop/com/enabling-com-security-using-dcomcnfg)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 