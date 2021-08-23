---
title: Programmgesteuerte Erweiterung
description: Programmgesteuerte Erweiterungen haben mehrere Vorteile, aber eine Anwendung ist nicht transparent. Der Administrator muss der in der Setupanwendung enthaltenen Dokumentation vertrauen.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Programmgesteuerte Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc8f049eb243dea0bfb8ad1eef4754d3713b9e908a16837abb832bab829b7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025468"
---
# <a name="programmatic-extension"></a>Programmgesteuerte Erweiterung

Der Vorteil einer LDIF-Datei besteht darin, dass der Administrator seine Funktion überprüfen kann. Das Schema kann jedoch auch programmgesteuert erweitert werden. Programmgesteuerte Erweiterungen haben mehrere Vorteile, aber eine Anwendung ist nicht transparent. Der Administrator muss der in der Setupanwendung enthaltenen Dokumentation vertrauen. Die Verwendung programmgesteuerter Schemaerweiterungen kann eine Barriere für die Bereitstellung von Anwendungen sein, die sie verwenden. Eine programmgesteuerte Erweiterung ist invariante Erweiterung. Es handelt sich um eine Windows ausführbare NT-Datei. Die Binärdatei kann im Gegensatz zu einer LDIF- oder .csv-Datei, die versehentlich oder böswillig bearbeitet werden kann, nicht manipuliert werden.

Zu den Vorteilen einer LDIF-Datei gehören:

-   Anwendungen können Fehler erkennen und beheben und Benutzerfeedback bereitstellen.
-   Anwendungen können Unicode verarbeiten, ohne auf Base64-Codierung zurückzugreifen.
-   Anwendungen können Windows Installer-Setup-APIs nutzen.
-   Anwendungen können signiert werden, um Authentizität herzustellen.

 

 




