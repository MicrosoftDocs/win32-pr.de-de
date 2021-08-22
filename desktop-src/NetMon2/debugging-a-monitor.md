---
description: Das folgende Verfahren veranschaulicht das Debuggen eines Monitors.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Debuggen eines Monitors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7ce15252470b280a988f81fe221218778a0fa5e4851db0d3e419d1653fbe92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144203"
---
# <a name="debugging-a-monitor"></a>Debuggen eines Monitors

Das folgende Verfahren veranschaulicht das Debuggen eines Monitors.

**So debuggen Sie einen Monitor**

1.  Installieren Sie die Monitor-DLL und die Programmdatenbankdatei (PDB), die beim Kompilieren des Monitors am richtigen Speicherort generiert wurden. Weitere [Informationen finden Sie unter Installing a Monitor to Netzwerkmonitor](installing-a-monitor-to-network-monitor.md) to Netzwerkmonitor (Installieren eines Monitors zum Installieren von Monitoren).
2.  Stellen Sie sicher, dass der Monitor Control Service als Server und nicht als Dienst konfiguriert ist, indem Sie Systemsteuerung, Dienste auswählen.
3.  Öffnen Sie eine Eingabeaufforderung, und wechseln Sie zum Netzwerkmonitor Verzeichnis. Typ:

    **Mcsvc.exe /RegServer**

    Nachdem die Debugsitzung des Monitors abgeschlossen ist, können Sie mcsvc wieder auf die Standardbedingung zurücksetzen, indem Sie Folgendes eingeben:

    **Mcsvc.exe /Service**

4.  Starten Microsoft Visual Studio sie Microsoft Visual C++.
5.  Wählen Sie **in der** **Menüoption** Datei , Öffnen den Namen Ihrer Monitor-DLL aus.
6.  Nachdem Microsoft Visual C++ geladen wurde, klicken Sie **auf Project**, **Einstellungen**.
7.  Klicken Sie unter **Ausführbare Datei** **für** Debugsitzung auf die Registerkarte Debuggen, und geben Sie den vollständigen Pfad der Mcsvc.exe. Beispiel: C: \\ Programme \\ Netmon2 \\Mcsvc.exe.
8.  Legen Sie die Haltepunkte im Code fest.

> [!Note]  
> Verwenden Sie kein Meldungsfeld für das Debuggen von Monitoren. Wenn MCSVC als Dienst ausgeführt wird, wird das Popup nicht angezeigt, und MCSVC scheint zu hängen.

 

 

 



