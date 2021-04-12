---
title: Virtuelle Kanäle Remotedesktopdienste
description: Virtuelle Kanäle sind Software Erweiterungen, die verwendet werden können, um einer Remotedesktopdienste Anwendung funktionale Verbesserungen hinzuzufügen.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309891"
---
# <a name="remote-desktop-services-virtual-channels"></a>Virtuelle Kanäle Remotedesktopdienste

*Virtuelle Kanäle* sind Software Erweiterungen, die verwendet werden können, um einer Remotedesktopdienste Anwendung funktionale Verbesserungen hinzuzufügen. Beispiele für funktionale Verbesserungen: Unterstützung für spezielle Typen von Hardware, Audiodaten oder andere Ergänzungen der Kernfunktionen, die von der Remotedesktopdienste [Remotedesktopprotokoll](remote-desktop-protocol.md) (RDP) bereitgestellt werden. Das RDP-Protokoll ermöglicht die Multiplex Verwaltung mehrerer virtueller Kanäle.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Verwenden von Remotedesktopdienste virtuellen Kanälen](using-terminal-services-virtual-channels.md)
</dt> <dd>

Zum Implementieren eines virtuellen Kanals stellen Sie die Server-und Client Module der Anwendung eines virtuellen Kanals bereit.

</dd> <dt>

[Referenz zu dynamischen virtuellen Kanälen](dynamic-virtual-channels-reference.md)
</dt> <dd>

DVC-Client Schnittstellen (Dynamic Virtual Channel) werden von Remotedesktopdienste unterstützt.

</dd> <dt>

[Referenz für virtuelle Grafik Kanäle](graphics-virtual-channels-reference.md)
</dt> <dd>

Die Referenz für virtuelle Grafik Kanäle enthält Programmier Elemente, mit denen Sie einen virtuellen Grafik Kanal erstellen können.

</dd> </dl>

Eine virtuelle Kanal Anwendung besteht aus zwei Teilen: einem Client Modul und einem Servermodul. Das Servermodul ist ein ausführbares Programm, das auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) ausgeführt wird. Das Client Modul ist eine DLL, die beim Ausführen des RDC-Client Programms (Remotedesktopverbindung) in den Arbeitsspeicher auf dem Client Computer geladen werden muss.

Virtuelle Kanäle können einem Remotedesktopverbindung-Client (RDC) unabhängig vom RDP-Protokoll funktionale Verbesserungen hinzufügen. Durch die Unterstützung virtueller Kanäle können neue Funktionen hinzugefügt werden, ohne dass die Client-oder Server Software oder das RDP-Protokoll aktualisiert werden muss.

Es wurden vier Hauptklassen von Benutzern von virtuellen Kanälen identifiziert:

-   Allgemeine Kernelmodustreiber, z. b. serielle oder Druckertreiber.
-   Dateisystem Umleitung (Hierbei handelt es sich nur um einen Sonderfall eines allgemeinen Kernelmodustreibers).
-   Benutzermodusanwendungen, z. b. Remote Ausschneiden und einfügen.
-   Audiogeräte.

Weitere Informationen finden Sie unter [Verwenden von Remotedesktopdienste virtuellen Kanälen](using-terminal-services-virtual-channels.md).

Wenn Sie in der Remotedesktopdienste-Bereitstellung eine virtuelle Channels-Anwendung aktiviert haben, können Sie die Anwendung auf Client Computern verfügbar machen, die über das Remotedesktop Microsoft ActiveX-Steuerelement auf den RD-Sitzungshost Server zugreifen. Weitere Informationen finden Sie unter [Skript fähige virtuelle Kanäle](scriptable-virtual-channels.md) und [Verwenden des Remotedesktop ActiveX-Steuer Elements mit virtuellen Kanälen](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 




