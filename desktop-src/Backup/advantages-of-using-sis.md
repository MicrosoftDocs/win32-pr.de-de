---
title: Vorteile der Verwendung von SIS
description: 'Die Verwendung von SIS und der SIS-Sicherungs Architektur bietet folgende Vorteile:'
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- SIS-Sicherung (Single Instance Store), Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd1856ce54e817c25830f15f133c7d76c6a80fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036417"
---
# <a name="advantages-of-using-sis"></a>Vorteile der Verwendung von SIS

Die Verwendung von SIS und der SIS-Sicherungs Architektur bietet folgende Vorteile:

-   Die Verbindungen zwischen den SIS-Links und den Unterstützungs Dateien werden automatisch von der SIS-Architektur verwaltet, wenn die Sicherungs Anwendungen die SIS Backup-API-Funktionen aufzurufen.
-   Der Inhalt der SIS-Analyse Punkte ist für Ihre Sicherungs-und Wiederherstellungs Anwendungen nicht transparent. Dadurch wird sichergestellt, dass Upgrades auf die SIS-internale keine Änderungen an der SIS-API oder Ihren Sicherungs-und Wiederherstellungs Anwendungen erfordern, die SIS-API-Funktionen aufzurufen. Sie müssen Ihre Anwendung nur mit einer neuen Version der SIS-dll mit dem Namen Sisbkup.dll neu kompilieren.
-   Da SIS als Dateisystem-Filtertreiber implementiert ist, werden die Verbindungen zwischen den SIS-Links und den Unterstützungs Dateien permanent nachverfolgt. Wenn die Dateien gesichert und wieder hergestellt werden, stellt die SIS-Sicherung sicher, dass nur eine Instanz der Sicherungsdatei gesichert und wieder hergestellt wird, unabhängig von der Anzahl von SIS-Links, die darauf zeigen.

 

 




