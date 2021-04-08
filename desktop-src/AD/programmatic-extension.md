---
title: Programmgesteuerte Erweiterung
description: Programmgesteuerte Erweiterungen haben mehrere Vorzüge, eine Anwendung ist jedoch nicht transparent. der Administrator muss der Dokumentation Vertrauen, die in der Setup Anwendung enthalten ist.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Programmgesteuerte Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707583"
---
# <a name="programmatic-extension"></a>Programmgesteuerte Erweiterung

Der Vorteil einer LDIF-Datei besteht darin, dass der Administrator seine Funktion überprüfen kann. Das Schema kann jedoch auch Programm gesteuert erweitert werden. Programmgesteuerte Erweiterungen haben mehrere Vorzüge, aber eine Anwendung ist nicht transparent. der Administrator muss der Dokumentation Vertrauen, die in der Setup Anwendung enthalten ist. Die Verwendung von programmgesteuerten Schema Erweiterungen kann eine Barriere für die Bereitstellung von Anwendungen darstellen, die Sie verwenden. Eine programmgesteuerte Erweiterung ist invariant. Es handelt sich um eine ausführbare Windows NT-Datei. Die Binärdatei kann nicht manipuliert werden, im Gegensatz zu einer LDIF-oder CSV-Datei, die versehentlich oder böswillig bearbeitet werden kann.

Zu den Vorteilen einer LDIF-Datei gehören:

-   Anwendungen können Fehler erkennen und Wiederherstellen und Benutzer Feedback bereitstellen.
-   Anwendungen können Unicode verarbeiten, ohne auf Base64-Codierung zurückzugreifen.
-   Anwendungen können Windows Installer Setup-APIs nutzen.
-   Anwendungen können signiert werden, um Authentizität zu erzielen.

 

 




