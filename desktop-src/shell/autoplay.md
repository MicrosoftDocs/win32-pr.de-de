---
description: AutoRun ist ein Feature des Windows Betriebssystems.
title: Erstellen einer CD-ROM-Anwendung mit aktivierter automatischer Läufe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b8bc1edad7fe49b996dd8471ae8ce081c36c71b7b7df48ca6296b07f8646ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460930"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>Erstellen einer CD-ROM-Anwendung mit aktivierter automatischer Läufe

AutoRun ist ein Feature des Windows Betriebssystems. Es automatisiert die Verfahren zum Installieren und Konfigurieren von Produkten, die für Windows-basierte Plattformen entwickelt wurden, die auf CD-ROMs verteilt werden. Wenn Benutzer einen AutoRun-fähigen Datenträger in ihr CD-ROM-Laufwerk einfügen, führt AutoRun automatisch eine Anwendung auf der CD-ROM aus, mit der das ausgewählte Produkt installiert, konfiguriert oder ausgeführt wird.

AutoRun kann zum Installieren und Ausführen von CD-ROM-Anwendungen verwendet werden. Obwohl AutoRun am häufigsten für Windows-Anwendungen verwendet wird, kann es auch zum Installieren, Konfigurieren oder Ausführen von MS-DOS-basierten Anwendungen in einer Windows Microsoft MS-DOS-Sitzung verwendet werden. Sie können jede MS-DOS-basierte Anwendung mit einem eigenen eindeutigen Symbol, einer Config.sys und einer Autoexec.bat konfigurieren. Windows erstellt die richtigen Konfigurationsdateien für die MS-DOS-basierte Anwendung. Die Startanwendung startet dann die MS-DOS-basierte Anwendung in einem Fenster.

> [!Note]  
> Damit autoRun funktioniert, muss das CD-ROM-Laufwerk über 32- oder 64-Bit-Gerätetreiber verfügen, die erkennen, wann ein Benutzer einen Datenträger einlegen und das System benachrichtigt.

 

In den folgenden Abschnitten wird erläutert, wie Sie eine CD-ROM-Anwendung mit aktivierter automatischer Läufe implementieren.

-   [Erstellen einer AutoRun-Enabled Anwendung](autoplay-works.md)
-   [Autorun.inf-Einträge](autorun-cmds.md)
-   [Aktivieren und Deaktivieren von AutoRun](autoplay-reg.md)

 

 



