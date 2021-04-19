---
description: Im folgenden wird erläutert, wie Sie Ihre Anwendung in Windows Installer Komponenten organisieren.
ms.assetid: 981a3def-1e59-4703-ad97-c8cd5431375d
title: Definieren von Installerkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ade4476fa1bf54a0ab4f64d0d43d72265ac1eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356254"
---
# <a name="defining-installer-components"></a>Definieren von Installerkomponenten

Im folgenden wird erläutert, wie Sie Ihre Anwendung in Windows Installer Komponenten organisieren.

**So organisieren Sie eine Anwendung in Komponenten**

1.  Erwerben Sie zunächst ein Verzeichnis und eine Dateistruktur für alle Dateien und anderen Ressourcen, die in der Anwendung verwendet werden.
2.  Identifizieren Sie alle Dateien, Registrierungsschlüssel, Verknüpfungen oder anderen Ressourcen, die von mehreren Anwendungen gemeinsam genutzt werden und von vorhandenen Komponenten bereitgestellt werden können, die als [Mergemodule](merge-modules.md)verfügbar sind. Sie dürfen diese Ressourcen nicht in die von Ihnen verfasell enden Komponenten einschließen. Rufen Sie stattdessen diese Komponenten durch Zusammenführen der Mergemodule in das Installationspaket ab. In den folgenden Schritten wird beschrieben, wie Sie die verbleibenden Ressourcen der Anwendung in-Komponenten organisieren.
3.  Definieren Sie eine neue-Komponente für jede exe-, dll-und OCX-Datei. Legen Sie diese Dateien als Schlüssel Pfad Dateien Ihrer Komponenten fest. Weisen Sie jeder Komponente eine Komponenten Code-GUID zu.
4.  Definieren Sie eine neue-Komponente für jede HLP-oder CHM-Hilfedatei. Legen Sie diese Dateien als Schlüssel Pfad Dateien Ihrer Komponenten fest. Fügen Sie die CNT-oder. Chi-Dateien den Komponenten hinzu, die die zugehörigen HLP-und CHM-Dateien speichern. Weisen Sie jeder Komponente eine Komponenten Code-GUID zu.
5.  Definieren Sie eine neue-Komponente für jede Datei, die als Ziel einer Verknüpfung dient. Legen Sie diese Dateien als Schlüssel Pfad Dateien Ihrer Komponenten fest. Weisen Sie jeder Komponente eine Komponenten Code-GUID zu.
6.  Gruppieren Sie alle verbleibenden Ressourcen in Ordnern. Alle Ressourcen in jedem Ordner müssen miteinander ausgeliefert werden. Wenn eine Möglichkeit besteht, dass ein paar von Ressourcen in Zukunft separat ausgeliefert werden kann, platzieren Sie diese in separaten Ordnern. Definieren Sie für jeden Ordner eine neue Komponente. Versuchen Sie, die Gesamtzahl der Komponenten niedrig zu halten, um die Leistung zu verbessern. Unterteilen Sie die Anwendung in viele Komponenten, wenn es erforderlich ist, dass das Installationsprogramm die Gültigkeit der Installation gründlich überprüft. Legen Sie eine beliebige Datei in der Komponente als Schlüssel Pfad Datei fest. Weisen Sie jeder Komponente eine Komponenten Code-GUID zu.
7.  Fügen Sie den-Komponenten Registrierungsschlüssel hinzu. Jeder Registrierungsschlüssel, der auf eine Datei verweist, sollte in der Komponente dieser Datei enthalten sein. Andere Registrierungsschlüssel sollten logisch mit den Dateien gruppiert werden, für die Sie erforderlich sind.

 

 



