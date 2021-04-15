---
description: Im folgenden Verfahren wird veranschaulicht, wie ein Monitor debuggt wird.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Debuggen eines Monitors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529018"
---
# <a name="debugging-a-monitor"></a>Debuggen eines Monitors

Im folgenden Verfahren wird veranschaulicht, wie ein Monitor debuggt wird.

**So debuggen Sie einen Monitor**

1.  Installieren Sie die Monitor-DLL und die Programm Datenbankdatei (. pdb), die bei der Kompilierung des Monitors am richtigen Speicherort generiert wurde. Weitere Informationen finden [Sie unter Installieren eines Monitors zum Netzwerkmonitor](installing-a-monitor-to-network-monitor.md) .
2.  Überprüfen Sie, ob der Überwachungs Steuerungs Dienst als Server anstelle eines Diensts konfiguriert ist, indem Sie die Option Systemsteuerung, Dienste auswählen.
3.  Öffnen Sie eine Eingabeaufforderung, und wechseln Sie zum Netzwerkmonitor Verzeichnis. Typ:

    **Mcsvc.exe/RegServer**

    Nachdem die Debugsitzung des Monitors ausgeführt wurde, können Sie die mcsvc-Datei an die Standard Bedingung zurückgeben, indem Sie Folgendes eingeben:

    **Mcsvc.exe/Service**

4.  Starten Sie Microsoft Visual C++ in Microsoft Visual Studio.
5.  Wählen Sie in der Menüoption **Datei** **Öffnen** den Namen Ihrer Monitor-DLL aus.
6.  Nachdem Microsoft Visual C++ geladen ist, klicken Sie auf **Projekt** und dann auf **Einstellungen**.
7.  Klicken Sie unter **ausführbare Datei** für Debugsitzung auf die Registerkarte **Debuggen** , und geben Sie den voll Mcsvc.exe ständigen Beispiel: C: \\ Program Files \\ Netmon2 \\Mcsvc.exe.
8.  Legen Sie die Breakpoints im Code fest.

> [!Note]  
> Verwenden Sie kein Meldungs Feld zum Debuggen von Monitoren. Wenn der mcsvc als Dienst ausgeführt wird, wird das Popup nicht angezeigt, und mcsvc scheint zu hängen.

 

 

 



