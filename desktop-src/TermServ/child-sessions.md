---
title: Untergeordnete Sitzungen
description: Ab Windows Server 2012 Windows 8 unterstützt Remotedesktop das Konzept einer untergeordneten Sitzung. Dabei handelt es sich um eine spezielle Loopback-Remotedesktop-Sitzung, die an die vorhandene Sitzung eines Benutzers gebunden ist.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d79fa6e18cece69c672b60a65e679441ce986a6cd8a0ad46524440738c3844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010420"
---
# <a name="child-sessions"></a>Untergeordnete Sitzungen

Ab Windows Server 2012 und Windows 8 unterstützt Remotedesktop das Konzept einer untergeordneten Sitzung, bei der es sich um eine spezielle Loopback-Remotedesktop-Sitzung handelt, die an die vorhandene Sitzung eines Benutzers gebunden ist.

Untergeordnete Sitzungen werden unter den folgenden Betriebssystemen nicht unterstützt:

<dl> Windows RT  
Windows Server 2012 Server Core-Installationsoption  
Microsoft Hyper-V Server 2012  
</dl>

Ein System kann zu einem bestimmten Zeitpunkt nur eine aktive und verbundene untergeordnete Sitzung haben.

Die untergeordnete Sitzung kann durch direkte Abmelden beendet werden, oder sie wird beendet, wenn die übergeordnete Sitzung beendet wird.

Bevor untergeordnete Sitzungen auf einem System verwendet werden können, müssen Sie die Funktionalität der untergeordneten Sitzung aktivieren, indem Sie die [**WTSEnableChildSessions-Funktion**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) aufrufen. Sie können auch mithilfe der [**WTSIsChildSessionsEnabled-Funktion**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) ermitteln, ob untergeordnete Sitzungen aktiviert wurden.

Eine untergeordnete Sitzung kann nur innerhalb der Sitzung eines vorhandenen Benutzers erstellt werden, indem das [Remotedesktop ActiveX-Steuerelement](remote-desktop-activex-control.md) verwendet und die ConnectToChildSession-Eigenschaft mit [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md) vor dem Herstellen der Verbindung eingerichtet wird. Wenn die [**IMsTscAx.Verbinden-Methode**](imstscax-connect.md) aufgerufen wird, anmeldet sich das Remotedesktop ActiveX-Steuerelement automatisch bei der untergeordneten Sitzung, ohne anmeldeinformationen einzugeben, es sei denn, der Benutzer wird mithilfe einer Smartcard bei der übergeordneten Sitzung angemeldet. Im Gegensatz zu einer Remotedesktop-Sitzung benötigt ein Benutzer nicht das Remote Interactive-Recht, um sich bei der untergeordneten Sitzung anmelden zu können, da es sich um eine Loopbacksitzung handelt.

Eine untergeordnete Sitzung kann nicht gesperrt werden. Es wird kein Bildschirmschoner und kein Anmeldebildschirm angezeigt. Im Gegensatz zu einer regulären Sitzung wird der Anmeldetext auch nicht in dieser untergeordneten Sitzung angezeigt, wenn die Richtlinie für den WinLogon-Anmeldetext festgelegt ist. Wenn diese Richtlinien festgelegt sind, Remotedesktopverbindung auch keine Auswirkungen von Timeoutgruppenrichtlinien auf die untergeordnete Sitzung.

Die folgenden APIs werden in Verbindung mit untergeordneten Sitzungen verwendet:

-   [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   ConnectToChildSession-Eigenschaft in [ **IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md)

 

 




