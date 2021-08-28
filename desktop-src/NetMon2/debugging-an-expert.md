---
description: Verwenden Sie das folgende Verfahren, um in Microsoft Visual C++ geschriebene Experten zu debuggen.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Debuggen eines Experten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cdd54484d8dc7d36bf1162433fc98d7d72565d9810c7e0ed838e9193510ac88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064140"
---
# <a name="debugging-an-expert"></a>Debuggen eines Experten

Verwenden Sie das folgende Verfahren, um in Microsoft Visual C++ geschriebene Experten zu debuggen.

**Debuggen eines Experten**

1.  Installieren Sie den Experten (DLL-Datei) und die Programmdatenbankdatei (PDB), die beim Kompilieren des Experten am richtigen Speicherort generiert wurden. Weitere Informationen finden Sie unter [Installing an Expert to Netzwerkmonitor 2.1](installing-an-expert-to-network-monitor-2-1.md).
2.  Starten Sie Microsoft Visual C++.
3.  Klicken Sie im Menü **Datei** auf **Öffnen,** und wählen Sie den Namen Ihrer Experten-DLL aus.
4.  Nachdem Microsoft Visual C++ geladen wurde, klicken Sie auf das **Menü Project** und dann auf **Einstellungen**.
5.  Klicken Sie auf **Debuggen.** Geben Sie unter **Ausführbare Datei für Debugsitzung** den vollständigen Pfad von Netmon.exe ein, z. B.:

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  Legen Sie die Breakpoints im Code fest.

 

 



