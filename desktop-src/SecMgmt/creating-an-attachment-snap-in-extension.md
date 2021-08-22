---
description: Eine Erweiterung für das Anfüge-Snap-In stellt eine Schnittstelle bereit, die Benutzer verwenden können, um dienstspezifische Konfigurationseinstellungen zu ändern.
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: Erstellen einer Erweiterung für das Anfüge-Snap-In
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1a4cd4ccecf7fba6e33062fd2bb4df810316f2d66d42165ca207d855a14f961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894830"
---
# <a name="creating-an-attachment-snap-in-extension"></a>Erstellen einer Erweiterung für das Anfüge-Snap-In

Eine Erweiterung für das Anfüge-Snap-In stellt eine Schnittstelle bereit, die Benutzer verwenden können, um dienstspezifische Konfigurationseinstellungen zu ändern. Die Erweiterung für das Anfüge-Snap-In muss die MMC-Anforderungen erfüllen, um eine gültige Snap-In-Erweiterung zu sein. Weitere Informationen zu diesen Anforderungen [](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) finden Sie in der Microsoft Management Console-Dokumentation.

Zusätzlich zu den schnittstellen, die für MMC erforderlich sind, muss eine Erweiterung für das Anfügen die COM-Schnittstelle [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)implementieren. Die Sicherheitskonfigurations-Snap-Ins rufen Methoden dieser Schnittstelle auf, um zu bestimmen, ob sich die Konfigurationsdaten geändert haben, und wenn ja, um die Sicherheitsdatenbank zu aktualisieren. Das Anlagen-Snap-In muss alle Konfigurationsänderungen speichern, bis die Sicherheitskonfigurations-Snap-Ins diese Daten abrufen.

Eine Erweiterung für das Anfüge-Snap-In muss die folgenden Funktionen bereitstellen:

-   [Anzeigen von Konfigurations- und Analyseinformationen](displaying-configuration-and-analysis-information.md)
-   [Ändern von Konfigurationsinformationen im Benutzeroberfläche](modifying-configuration-information-in-the-user-interface.md)
-   [Ändern von Konfigurationsinformationen in der Sicherheitsdatenbank](modifying-configuration-information-in-the-database.md)

Um Ihre Snap-In-Erweiterung bei der Ausführung dieser Aufgaben zu unterstützen, implementieren die Sicherheitskonfigurations-Snap-Ins eine COM-Schnittstelle [**ISceSvcAttachmentData,**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)die Methoden bereitstellt, die Ihre Snap-In-Erweiterung aufrufen kann, um sich selbst zu initialisieren und Informationen aus der Sicherheitsdatenbank abzufragen.

Nachdem Sie die Erweiterung für das Anfüge-Snap-In erstellt haben, müssen Sie sie mit den Sicherheitskonfigurations-Snap-Ins registrieren, wie unter Registrieren einer Erweiterung für [das Anlagen-Snap-In](registering-an-attachment-snap-in-extension.md)beschrieben.

 

 
