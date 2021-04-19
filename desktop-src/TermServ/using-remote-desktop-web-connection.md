---
title: Verwenden des Remotedesktop ActiveX-Steuer Elements
description: So können Sie das Remotedesktop ActiveX-Steuerelement verwenden, um die Remotedesktopdienste Benutzer Darstellung anzupassen.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste mit Remotedesktop ActiveX-Steuerelement
- Remotedesktop-Webverbindung Remotedesktopdienste mit
- Remotedesktopprotokoll Remotedesktopdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339799"
---
# <a name="using-the-remote-desktop-activex-control"></a>Verwenden des Remotedesktop ActiveX-Steuer Elements

Die folgenden Themen enthalten Informationen dazu, wie Sie das Remotedesktop ActiveX-Steuerelement verwenden können, um die Remotedesktopdienste Benutzer Darstellung anzupassen.

Das Remotedesktop ActiveX-Steuerelement ist in den folgenden Formularen verfügbar:

-   **Das Skript fähige-Steuer** Element – implementiert Schnittstellen, die für die Skripterstellung sicher sind. Diese Form des Steuer Elements kann von Webclients oder Skript Erstellungs Hosts (z. b. VBScript) verwendet werden.
-   **Das nicht Scriptable-Steuer** Element – bietet zusätzliche Funktionen, die für die Skripterstellung nicht sicher sind. Diese Form des Steuer Elements kann von System eigenem oder verwaltetem Code verwendet werden. dieses Formular kann jedoch nicht von Webclients oder reinen Skript Hosts verwendet werden.

Die folgende Liste enthält die **CLSID**-e für die verschiedenen Steuerelemente für verschiedene Betriebssystemversionen. Alle **CLSID**-e sind mit neueren Systemversionen kompatibel. Beispielsweise kann die **CLSID** für das Skript fähige-Steuerelement unter Windows Vista in späteren Systemversionen wie Windows 7 verwendet werden.



| System Version                          | Scriptable-Steuerelement-CLSID             | CLSID für nicht Scriptable-Steuerelement          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| Windows 8.1, Windows Server 2012 R2     | 301b94ba-5d25-4a12-bffe-3b6e7a616585 | 8b918b82-7985-4c24-89df-c33ad2bbfbcd |
| Windows 8, Windows Server 2012          | 5f681803-2900-4c43-a1cc-cf405404a676 | A3BC03A0-041D-42E3-AD22-882B7865C9C5 |
| Windows 7, Windows Server 2008          | A9D7038D-B5ED-472E-9C47-94BEA90A5910 | 54d38bf 7-b1ef-4479-9674-1bd6ea465258 |
| Windows Vista mit Service Pack 1 (SP1) | 7390f3d8-0439-4c05-91E3-cf5cb290c3d0 | D2EA46A7-C2BF-426B-AF24-E19C44456399 |
| Windows Vista                           | 4eb89ff4-7f78-4a0f-8b8d-2bf02e94e4b2 | 4eb2f 086-C818-447e-b32c-c51ce2b30d31 |



 

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Einbetten des Remotedesktop ActiveX-Steuer Elements in eine Webseite](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

Beispiel, das die Verwendung der Skript fähigen Schnittstellen veranschaulicht.

</dd> <dt>

[Implementieren von Skript fähigen virtuellen Kanälen mithilfe von Remotedesktop-Webverbindung](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

Code Beispiele, die die Schritte zum Implementieren von Skript fähigen virtuellen Kanälen mit Remotedesktop-Webverbindung veranschaulichen.

</dd> <dt>

[Verwenden des Remotedesktop ActiveX-Steuer Elements mit virtuellen Kanälen](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

Wenn Sie in der Remotedesktopdienste-Bereitstellung eine virtuelle Channels-Anwendung aktiviert haben, können Sie diese Anwendung für Client Computer zur Verfügung stellen.

</dd> <dt>

[Beispiel Webseite, die im Remotedesktop ActiveX-Steuerelement enthalten ist](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

Eine Beispiel Webseite (Default.htm) befindet sich im Verzeichnis, in dem Remotedesktop-Webverbindung installiert ist.

</dd> <dt>

[Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md)
</dt> <dd>

Einige Eigenschaften des Remotedesktop ActiveX-Steuerelement Objekts sind auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt.

</dd> <dt>

[Deaktivieren von Remotedesktopdienste Features](disabling-terminal-services-features.md)
</dt> <dd>

Zur Erhöhung der Sicherheit können Sie Remotedesktopdienste Funktionen deaktivieren.

</dd> </dl>

Weitere Informationen zur Beispiel Webseite, die in der Installation des Remotedesktop ActiveX-Steuer Elements enthalten ist, finden Sie unter [Sample-Webseite, die im Remotedesktop ActiveX-Steuerelement enthalten](sample-web-page-included-with-the-remote-desktop-activex-control.md)ist.

 

 




