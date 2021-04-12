---
title: Wiederherstellungspunkt-Beschreibungs Text
description: Wenn eine Anwendung die SRSetRestorePoint-Funktion aufruft, kann Sie beliebigen Text als Beschreibung für den Wiederherstellungspunkt angeben. in der folgenden Tabelle wird jedoch der empfohlene Beschreibungstext angezeigt.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206861"
---
# <a name="restore-point-description-text"></a>Wiederherstellungspunkt-Beschreibungs Text

Wenn eine Anwendung die [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) -Funktion aufruft, kann Sie beliebigen Text als Beschreibung für den Wiederherstellungspunkt angeben. in der folgenden Tabelle wird jedoch der empfohlene Beschreibungstext angezeigt.



| System Änderung                            | Typ des Wiederherstellungs Punkts      | BESCHREIBUNG            |
|------------------------------------------------|-------------------------|------------------------|
| Anwendungsinstallation                       | Anwendungs \_ Installation    | Installierter *appname*    |
| Anwendungs Änderung (Features hinzufügen/entfernen) | \_Einstellungen ändern        | Konfigurierter *appname*   |
| Entfernen der Anwendung                            | Anwendungs \_ Deinstallation  | *Appname* wurde entfernt.      |
| Gerätetreiber Installation                     | Geräte \_ Treiber \_ Installation | Installierter *DriverName* |



 

Installationsprogramme, z. b. Windows Installer und InstallShield, verwenden diese Konventionen für den Beschreibungstext:

-   Der Produktname folgt dem Verb. Beispiel: installierter *appname*.
-   Der Produktname kann allein (*appname*) oder der Produktname verwendet werden, und der Name des Unternehmens kann jeweils verwendet werden (*MyCompany appname*).

 

 




