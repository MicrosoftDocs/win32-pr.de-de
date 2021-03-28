---
description: Autorun ist eine Funktion des Windows-Betriebssystems.
title: Erstellen einer Autorun-aktivierten CD-ROM-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214444"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>Erstellen einer Autorun-aktivierten CD-ROM-Anwendung

Autorun ist eine Funktion des Windows-Betriebssystems. Es automatisiert die Verfahren zum Installieren und Konfigurieren von Produkten, die für Windows-basierte Plattformen entworfen wurden, die auf CD-ROMs verteilt sind. Wenn Benutzer eine autornicht aktivierte Compact-CD in das CD-ROM-Laufwerk einfügen, führt Autorun automatisch eine Anwendung auf der CD-ROM aus, die das ausgewählte Produkt installiert, konfiguriert oder ausführt.

Autorun kann zum Installieren und Ausführen von CD-ROM-Anwendungen verwendet werden. Obwohl Autorun am häufigsten für Windows-Anwendungen verwendet wird, kann es auch zum Installieren, konfigurieren oder Ausführen von MS-DOS-basierten Anwendungen in einer Windows-MS-DOS-Sitzung verwendet werden. Sie können jede MS-DOS-basierte Anwendung mit einem eigenen eindeutigen Symbol, Config.sys Datei und Autoexec.bat Datei konfigurieren. Windows erstellt die richtigen Konfigurationsdateien für die MS-DOS-basierte Anwendung. Die Start Anwendung startet dann die MS-DOS-basierte Anwendung in einem-Fenster.

> [!Note]  
> Damit Autorun funktioniert, muss das CD-ROM-Laufwerk über 32-oder 64-Bit-Gerätetreiber verfügen, die erkennen, wenn ein Benutzer eine kompakte CD einfügt und das System benachrichtigt.

 

In den folgenden Abschnitten wird erläutert, wie eine Autorun-fähige CD-ROM-Anwendung implementiert wird.

-   [Erstellen einer AutoRun-Enabled Anwendung](autoplay-works.md)
-   [Autorun. inf-Einträge](autorun-cmds.md)
-   [Aktivieren und Deaktivieren von Autorun](autoplay-reg.md)

 

 



