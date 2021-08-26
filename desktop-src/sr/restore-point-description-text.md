---
title: Beschreibungstext des Wiederherstellungspunkts
description: Wenn eine Anwendung die SRSetRestorePoint-Funktion aufruft, kann sie einen beliebigen Text als Beschreibung für den Wiederherstellungspunkt bereitstellen. Die folgende Tabelle enthält jedoch den empfohlenen Beschreibungstext.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd785d143d3eed243e5d80ec261f121817db6187013f70b6f6cc6be0b1c2b790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111249"
---
# <a name="restore-point-description-text"></a>Beschreibungstext des Wiederherstellungspunkts

Wenn eine Anwendung die [**SRSetRestorePoint-Funktion aufruft,**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) kann sie einen beliebigen Text als Beschreibung für den Wiederherstellungspunkt bereitstellen. Die folgende Tabelle enthält jedoch den empfohlenen Beschreibungstext.



| Systemänderung                            | Wiederherstellungspunkttyp      | Beschreibung            |
|------------------------------------------------|-------------------------|------------------------|
| Anwendungsinstallation                       | \_ANWENDUNGSINSTALL    | Installierter *AppName*    |
| Anwendungsänderung (Features hinzufügen/entfernen) | ÄNDERN VON \_ EINSTELLUNGEN        | Konfigurierter *App-Name*   |
| Entfernen von Anwendungen                            | DEINSTALLIEREN VON \_ ANWENDUNGEN  | AppName *entfernt*      |
| Gerätetreiberinstallation                     | GERÄTETREIBER \_ \_ INSTALLIEREN | Installierter *DriverName* |



 

Installationsprogramme wie Windows Installer und InstallShield verwenden diese Konventionen für den Beschreibungstext:

-   Der Produktname folgt dem Verb. Beispiel: Installierter *AppName.*
-   Der Produktname kann allein verwendet werden (*AppName*), oder der Produktname und der Unternehmensname können beide verwendet werden (*MyCompany AppName*).

 

 




