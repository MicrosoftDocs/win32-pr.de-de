---
description: Im Folgenden wird beschrieben, wie Sie Ihre Anwendung in Windows Installer-Komponenten organisieren.
ms.assetid: 981a3def-1e59-4703-ad97-c8cd5431375d
title: Definieren von Installerkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83d5fa02182c40fa209453484db23706db2f261f41324cd4d86894d9e78dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979560"
---
# <a name="defining-installer-components"></a>Definieren von Installerkomponenten

Im Folgenden wird beschrieben, wie Sie Ihre Anwendung in Windows Installer-Komponenten organisieren.

**So organisieren Sie eine Anwendung in Komponenten**

1.  Beginnen Sie mit dem Abrufen eines Verzeichnisses und einer Dateistruktur für alle Dateien und anderen Ressourcen, die in Ihrer Anwendung verwendet werden.
2.  Identifizieren Sie alle Dateien, Registrierungsschlüssel, Verknüpfungen oder andere Ressourcen, die anwendungsübergreifend freigegeben sind und von vorhandenen Komponenten bereitgestellt werden können, die als [Mergemodule verfügbar sind.](merge-modules.md) Sie dürfen keine dieser Ressourcen in die komponenten, die Sie erstellen, enthalten. Stattdessen erhalten Sie diese Komponenten, indem Sie die Mergemodule in Ihrem Installationspaket zusammenführen. In den folgenden Schritten wird beschrieben, wie die verbleibenden Ressourcen der Anwendung in Komponenten organisiert werden.
3.  Definieren Sie eine neue Komponente für jede .exe, .dll und OCX-Datei. Bestimmen Sie diese Dateien als Schlüsselpfaddateien ihrer Komponenten. Weisen Sie jeder Komponente eine Komponentencode-GUID zu.
4.  Definieren Sie eine neue Komponente für jede HLP- oder CHM-Hilfedatei. Bestimmen Sie diese Dateien als Schlüsselpfaddateien ihrer Komponenten. Fügen Sie die CNT- oder CHI-Dateien den Komponenten hinzu, die ihre zugeordneten HLP- und CHM-Dateien enthalten. Weisen Sie jeder Komponente eine Komponentencode-GUID zu.
5.  Definieren Sie eine neue Komponente für jede Datei, die als Ziel einer Verknüpfung dient. Bestimmen Sie diese Dateien als Schlüsselpfaddateien ihrer Komponenten. Weisen Sie jeder Komponente eine Komponentencode-GUID zu.
6.  Gruppieren Sie alle verbleibenden Ressourcen in Ordner. Alle Ressourcen in jedem Ordner müssen zusammen liefern. Wenn die Möglichkeit besteht, dass ein Ressourcenpaar in Zukunft separat versenden kann, legen Sie diese in separaten Ordnern ab. Definieren Sie für jeden Ordner eine neue Komponente. Versuchen Sie, die Gesamtzahl der Komponenten niedrig zu halten, um die Leistung zu verbessern. Unterteilen Sie die Anwendung in viele Komponenten, wenn das Installationsprogramm die Gültigkeit der Installation gründlich überprüfen muss. Geben Sie eine beliebige Datei in der Komponente als Schlüsselpfaddatei an. Weisen Sie jeder Komponente eine Komponentencode-GUID zu.
7.  Fügen Sie den Komponenten Registrierungsschlüssel hinzu. Jeder Registrierungsschlüssel, der auf eine Datei verweist, sollte in der Komponente dieser Datei enthalten sein. Andere Registrierungsschlüssel sollten logisch mit den Dateien, die sie erfordern, gruppiert werden.

 

 



