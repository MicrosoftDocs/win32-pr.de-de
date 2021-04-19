---
description: Verwenden Sie das folgende Verfahren, um in Microsoft Visual C++ geschriebene Experten zu debuggen.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Debuggen eines Experten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349498"
---
# <a name="debugging-an-expert"></a>Debuggen eines Experten

Verwenden Sie das folgende Verfahren, um in Microsoft Visual C++ geschriebene Experten zu debuggen.

**Debuggen eines Experten**

1.  Installieren Sie den Experten (DLL-Datei) und die Programm Datenbankdatei (. pdb), die bei der Kompilierung des Experten am richtigen Speicherort generiert wurden. Weitere Informationen finden Sie unter [Installieren eines Experten in Netzwerkmonitor 2,1](installing-an-expert-to-network-monitor-2-1.md).
2.  Starten Sie Microsoft Visual C++.
3.  Klicken Sie im Menü **Datei** auf **Öffnen** , und wählen Sie den Namen ihrer Experten-dll aus.
4.  Nachdem Microsoft Visual C++ geladen ist, klicken Sie auf das Menü **Projekt** , und klicken Sie dann auf **Einstellungen**.
5.  Klicken Sie auf **Debug**. Geben Sie unter **ausführbare Datei für Debugsitzung** den vollständigen Pfad Netmon.exe ein, z. b.:

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  Legen Sie die Breakpoints im Code fest.

 

 



