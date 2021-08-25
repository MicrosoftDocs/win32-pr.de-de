---
title: RAS-Telefon Books
description: Telefon-Bücher bieten eine Standard methode zum Sammeln und Angeben der Informationen, die der Remotezugriffsserver benötigt Verbindungs-Manager um eine Remoteverbindung herzustellen.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Telefon, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba80b11696df220a904a13685855818b945794c17b9bd4233e9f897592ee7b7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868420"
---
# <a name="ras-phone-books"></a>RAS-Telefon Books

Telefon-Bücher bieten eine Standard methode zum Sammeln und Angeben der Informationen, die der Remotezugriffsserver benötigt Verbindungs-Manager um eine Remoteverbindung herzustellen. Telefon-Bücher ordnen Eintragsnamen Informationen wie Telefonnummern, COM-Ports und Modemeinstellungen zu. Jeder Telefonbucheintrag enthält die Informationen, die zum Herstellen einer RAS-Verbindung erforderlich sind.

Telefon bücher werden in Telefonbuchdateien gespeichert, bei denen es sich um Textdateien handelt, die die Eintragsnamen und die zugehörigen Informationen enthalten. RAS erstellt eine Telefonbuchdatei namens RASPHONE. Pbk. Der Benutzer kann das **Hauptdialogfeld DFÜ-Netzwerk,** um persönliche Telefonbuchdateien zu erstellen. Die RAS-API bietet derzeit keine Unterstützung für das Erstellen einer Telefonbuchdatei. Einige RAS-Funktionen, z. B. die [**RasDial-Funktion,**](/windows/desktop/api/Ras/nf-ras-rasdiala) verfügen über einen Parameter, der eine Telefonbuchdatei angibt. Wenn der Aufrufer keine Phone-Book-Datei ansteuert, verwendet die Funktion die Standarddatei phone-book. Dies  ist die Datei, die der Benutzer im Eigenschaftenblatt Benutzereinstellungen des Dialogfelds DFÜ-Netzwerk ausgewählt hat. 

Windows NT 4.0 stellt die [**Funktionen RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) und [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) bereit, die die integrierte RAS-Benutzeroberfläche anzeigen, mit der Benutzer mit Telefonbüchern und Telefonbucheinträgen arbeiten können.

**Windows 95:** DFÜ-Netzwerke speichern Telefonbucheinträge in der Registrierung und nicht in einer Telefonbuchdatei. Windows 95 unterstützt keine persönlichen Telefonbuchdateien oder Funktionen, die die integrierten RAS-Dialogfelder anzeigen.

 

 




