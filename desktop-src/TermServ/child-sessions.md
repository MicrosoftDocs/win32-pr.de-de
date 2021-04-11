---
title: Untergeordnete Sitzungen
description: Ab Windows Server 2012 und Windows 8 unterstützt Remotedesktop das Konzept einer untergeordneten Sitzung, bei der es sich um eine spezielle Loopback Remotedesktop Sitzung handelt, die an die vorhandene Sitzung eines Benutzers gebunden ist.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206295"
---
# <a name="child-sessions"></a>Untergeordnete Sitzungen

Ab Windows Server 2012 und Windows 8 unterstützt Remotedesktop das Konzept einer untergeordneten *Sitzung*, bei der es sich um eine spezielle Loopback Remotedesktop Sitzung handelt, die an die vorhandene Sitzung eines Benutzers gebunden ist.

Untergeordnete Sitzungen werden unter den folgenden Betriebssystemen nicht unterstützt:

<dl> Windows RT  
Windows Server 2012 Server Core-Installationsoption  
Microsoft Hyper-V Server 2012  
</dl>

Ein System kann zu einem bestimmten Zeitpunkt nur eine aktive und verbundene untergeordnete Sitzung haben.

Die untergeordnete Sitzung kann beendet werden, indem Sie sich direkt von ihr abmelden, oder Sie wird beendet, wenn die übergeordnete Sitzung beendet wird.

Bevor untergeordnete Sitzungen in einem System verwendet werden können, müssen Sie die Funktion der untergeordneten Sitzung aktivieren, indem Sie die [**wtsenablechildsessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) -Funktion aufrufen. Mithilfe der [**wtsischildsessionsenabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) -Funktion können Sie auch feststellen, ob untergeordnete Sitzungen aktiviert wurden.

Eine untergeordnete Sitzung kann nur aus einer vorhandenen Benutzersitzung erstellt werden, indem das [Remotedesktop ActiveX-Steuer](remote-desktop-activex-control.md) Element verwendet wird und die Eigenschaft "connectdechildsession" mit [**imsrdpextendedsettings. Property**](imsrdpextendedsettings-property.md) vor dem Herstellen der Verbindung festgelegt wird. Wenn die [**imstscax. Connect**](imstscax-connect.md) -Methode aufgerufen wird, meldet sich das Remotedesktop ActiveX-Steuerelement automatisch bei der untergeordneten Sitzung an, ohne zur Eingabe von Anmelde Informationen aufgefordert zu werden, es sei denn, der Benutzer ist über eine Smartcard bei der übergeordneten Sitzung angemeldet. Anders als bei einer regulären Remotedesktop Sitzung benötigt ein Benutzer nicht das interaktive Remote Recht, um sich bei der untergeordneten Sitzung anzumelden, da es sich um eine Loopback Sitzung handelt.

Eine untergeordnete Sitzung kann nicht gesperrt werden. Sie verfügt über keinen Bildschirmschoner und keinen Anmeldebildschirm. Anders als bei einer regulären Sitzung wird der Anmelde Text in dieser untergeordneten Sitzung nicht angezeigt, wenn die Winlogon-Anmelde Text Richtlinie festgelegt ist. Außerdem werden Remotedesktopverbindung Timeout-Gruppenrichtlinien in der untergeordneten Sitzung nicht wirksam, wenn diese Richtlinien festgelegt sind.

Die folgenden APIs werden in Verbindung mit untergeordneten Sitzungen verwendet:

-   [**Wtsenablechildsessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [**Wtsischildsessionsenabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [**Wout getchildsessionid**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   Eigenschaft "connectdechildsession" in [ **imsrdpextendedsettings. Property**](imsrdpextendedsettings-property.md)

 

 




