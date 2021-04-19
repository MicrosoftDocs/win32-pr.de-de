---
description: Eine Anlage-Snap-in-Erweiterung bietet eine Schnittstelle, mit der Benutzer Dienst spezifische Konfigurationseinstellungen ändern können.
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: Erstellen einer Anlagen-Snap-in-Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513c982acc7e5285f3b4d1510f18b7eb6c9fe1d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347712"
---
# <a name="creating-an-attachment-snap-in-extension"></a>Erstellen einer Anlagen-Snap-in-Erweiterung

Eine Anlage-Snap-in-Erweiterung bietet eine Schnittstelle, mit der Benutzer Dienst spezifische Konfigurationseinstellungen ändern können. Die Erweiterungs-Snap-in-Erweiterung muss die MMC-Anforderungen erfüllen, damit Sie eine gültige Snap-in-Erweiterung ist. Weitere Informationen zu diesen Anforderungen finden Sie in der Dokumentation zur [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

Zusätzlich zu den von der MMC benötigten Schnittstellen muss die COM-Schnittstelle " [**iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)" implementiert werden. Mit den Sicherheits Konfigurations-Snap-Ins werden Methoden dieser Schnittstelle aufgerufen, um zu bestimmen, ob die Konfigurationsdaten geändert wurden, und wenn ja, um die Sicherheitsdatenbank zu aktualisieren. Das Anlagen-Snap-in muss alle Konfigurationsänderungen speichern, bis die Sicherheits Konfigurations-Snap-ins diese Daten abrufen.

Eine Anlage-Snap-in-Erweiterung muss die folgenden Funktionen bereitstellen:

-   [Konfigurations-und Analyse Informationen anzeigen](displaying-configuration-and-analysis-information.md)
-   [Ändern der Konfigurationsinformationen in der Benutzeroberfläche](modifying-configuration-information-in-the-user-interface.md)
-   [Ändern der Konfigurationsinformationen in der Sicherheitsdatenbank](modifying-configuration-information-in-the-database.md)

Um Ihre Snap-in-Erweiterung bei der Ausführung dieser Aufgaben zu unterstützen, implementieren die Sicherheitskonfigurations-Snap-Ins eine COM-Schnittstelle, [**iscesvasetachmentdata**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), die Methoden bereitstellt, die Ihre Snap-in-Erweiterung zum Initialisieren und Abfragen von Informationen aus der Sicherheitsdatenbank aufruft.

Nachdem Sie die Erweiterungs-Snap-in-Erweiterung erstellt haben, müssen Sie Sie mit den Snap-Ins für die Sicherheitskonfiguration registrieren, wie unter [Registrieren einer Anlage-Snap-in-Erweiterung](registering-an-attachment-snap-in-extension.md)beschrieben.

 

 
