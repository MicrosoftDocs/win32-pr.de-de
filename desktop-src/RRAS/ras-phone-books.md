---
title: RAS-Telefonbücher
description: Telefonbücher stellen eine Standardmethode zum Erfassen und angeben der Informationen dar, die der RAS-Verbindungs-Manager zum Herstellen einer Remote Verbindung benötigt.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Telefonbücher, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037061"
---
# <a name="ras-phone-books"></a>RAS-Telefonbücher

Telefonbücher stellen eine Standardmethode zum Erfassen und angeben der Informationen dar, die der RAS-Verbindungs-Manager zum Herstellen einer Remote Verbindung benötigt. In Telefonbüchern werden Eintrags Namen mit Informationen wie Telefonnummern, com-Ports und Modem Einstellungen verknüpft. Jeder Telefonbucheintrag enthält die Informationen, die zum Herstellen einer RAS-Verbindung erforderlich sind.

Telefonbücher werden in Telefonbuch Dateien gespeichert. dabei handelt es sich um Textdateien, die die Eintrags Namen und die zugehörigen Informationen enthalten. RAS erstellt eine Telefonbuchdatei mit dem Namen RASPHONE. Pbk. Der Benutzer kann das Dialogfeld "hauptdfü **-Netzwerk** " verwenden, um persönliche Telefonbuch Dateien zu erstellen. Die RAS-API bietet derzeit keine Unterstützung für das Erstellen einer Telefonbuchdatei. Einige RAS-Funktionen, wie z. b. die Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) ", verfügen über einen Parameter, der eine Telefonbuchdatei angibt. Wenn der Aufrufer keine Telefonbuchdatei angibt, verwendet die Funktion die standardmäßige Telefonbuchdatei, die vom Benutzer auf dem Eigenschaften Blatt **Benutzereinstellungen** des Dialog Felds DFÜ **-Netzwerke** ausgewählt wird.

Windows NT 4,0 bietet die Funktionen [**rasphonebookdlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) und [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) , die die integrierte RAS-Benutzeroberfläche anzeigen, mit deren Hilfe Benutzer mit Telefonbüchern und Telefonbucheinträgen arbeiten können.

**Windows 95:** Das Einwählnetzwerk speichert Telefonbucheinträge in der Registrierung und nicht in einer Telefonbuchdatei. Windows 95 unterstützt keine persönlichen Telefonbuch Dateien oder Funktionen, die die integrierten RAS-Dialogfelder anzeigen.

 

 




