---
description: Das System erstellt ein Benutzerprofil, wenn sich ein Benutzer das erste Mal an einem Computer anmeldet. Bei nachfolgenden Anmeldungen lädt das System das Profil des Benutzers, und andere Systemkomponenten konfigurieren die Umgebung des Benutzers gemäß den Informationen im Profil.
title: Informationen zu Benutzerprofilen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 333f1861-91fe-4796-af13-dd300a5c6ec3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bafd5df7d59787104c2904b4e83c734deaf28708
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977417"
---
# <a name="about-user-profiles"></a>Informationen zu Benutzerprofilen

Das System erstellt ein Benutzerprofil, wenn sich ein Benutzer das erste Mal an einem Computer anmeldet. Bei nachfolgenden Anmeldungen lädt das System das Profil des Benutzers, und andere Systemkomponenten konfigurieren die Umgebung des Benutzers gemäß den Informationen im Profil.

## <a name="types-of-user-profiles"></a>Typen von Benutzerprofilen

-   [Lokale Benutzerprofile](local-user-profiles.md). Ein lokales Benutzerprofil wird erstellt, wenn sich ein Benutzer zum ersten Mal an einem Computer anmeldet. Das Profil wird auf der lokalen Festplatte des Computers gespeichert. Änderungen, die am lokalen Benutzerprofil vorgenommen werden, sind für den Benutzer und den Computer, auf dem die Änderungen vorgenommen werden, spezifisch.
-   [Roamingbenutzerprofile](roaming-user-profiles.md) Bei einem Roamingbenutzerprofil handelt es sich um eine Kopie des lokalen Profils, das in eine Server Freigabe kopiert und dort gespeichert wird. Dieses Profil wird auf jeden Computer heruntergeladen, auf dem sich ein Benutzer in einem Netzwerk anmeldet. Änderungen, die an einem Roamingbenutzerprofil vorgenommen werden, werden mit der Server Kopie des Profils synchronisiert, wenn sich der Benutzer abmeldet. Der Vorteil von Roamingbenutzerprofilen besteht darin, dass Benutzer auf jedem Computer, den Sie in einem Netzwerk verwenden, kein Profil erstellen müssen.
-   [Verbindliche Benutzerprofile](mandatory-user-profiles.md). Bei einem obligatorischen Benutzerprofil handelt es sich um einen Profiltyp, den Administratoren verwenden können, um Einstellungen für Benutzer anzugeben. Nur Systemadministratoren können Änderungen an obligatorischen Benutzerprofilen vornehmen. Änderungen, die von Benutzern an den Desktop Einstellungen vorgenommen werden, gehen verloren, wenn sich der Benutzer abmeldet.
-   [Temporäre Benutzerprofile](temporary-user-profiles.md). Jedes Mal, wenn ein Fehlerzustand verhindert, dass das Profil des Benutzers geladen wird, wird ein temporäres Profil ausgegeben. Temporäre Profile werden am Ende jeder Sitzung gelöscht, und Änderungen, die vom Benutzer an Desktop Einstellungen und-Dateien vorgenommen werden, gehen verloren, wenn sich der Benutzer abmeldet. Temporäre Profile sind nur auf Computern verfügbar, auf denen Windows 2000 und höher ausgeführt wird.

Ein Benutzerprofil besteht aus den folgenden Elementen:

-   Eine Registrierungs Struktur. Die Registrierungs Struktur ist die Datei Ntuser. dat. Die Struktur wird vom System bei der Benutzeranmeldung geladen und dem Registrierungsschlüssel **HKEY \_ Current \_ User** zugeordnet. Die Registrierungs Struktur des Benutzers behält die Registrierungs basierten Einstellungen und die Konfiguration des Benutzers bei.
-   Ein Satz von Profil Ordnern, die im Dateisystem gespeichert sind. Benutzerprofil Dateien werden im Verzeichnis **profile** in einem Ordner pro Benutzer gespeichert. Der Benutzerprofil Ordner ist ein Container für Anwendungen und andere Systemkomponenten, die mit Unterordnern aufgefüllt werden sollen, sowie für benutzerspezifische Daten, wie z. b. Dokumente und Konfigurationsdateien. Windows-Explorer verwendet die Benutzerprofil Ordner für Elemente wie den Desktop des Benutzers, das **Startmenü** und den Ordner " **Dokumente** " in großem Umfang.

Benutzerprofile bieten folgende Vorteile:

-   Wenn sich der Benutzer bei einem Computer anmeldet, verwendet das System die gleichen Einstellungen, die beim letzten Abmelden des Benutzers verwendet wurden.
-   Wenn ein Computer für andere Benutzer freigegeben wird, erhält jeder Benutzer seinen angepassten Desktop nach der Anmeldung.
-   Einstellungen im Benutzerprofil sind für jeden Benutzer eindeutig. Andere Benutzer können auf die Einstellungen nicht zugreifen. Änderungen, die an einem Benutzerprofil vorgenommen werden, wirken sich nicht auf andere Benutzer oder andere Benutzerprofile aus.

## <a name="user-profile-tiles-in-windows-7-and-later"></a>Benutzerprofil-Kacheln in Windows 7 und höher

In Windows 7 oder höher hat jedes Benutzerprofil ein zugeordnetes Bild als Benutzer Kachel. Diese Kacheln werden Benutzern im System Steuerungselement **Benutzerkonten** und der Unterseite **Konten verwalten** angezeigt. Die Bilddateien für die standardmäßigen Gast-und Standardbenutzer Konten werden hier auch angezeigt, wenn Sie über Administrator Zugriffsrechte verfügen.

> [!Note]  
> Der Zugriff auf die Unterseite **Konten verwalten** erfolgt über den Link **ein anderes Konto verwalten** im System Steuerungselement **Benutzerkonten** .

 

-   % Program Data% \\ Microsoft- \\ Benutzerkonto Bilder \\Guest.bmp
-   % Program Data% \\ Microsoft- \\ Benutzerkonto Bilder \\User.bmp

Das Kachel Bild des Benutzers wird im lokalen temporären Ordner "% System Drive% \\ Users \\ <username> \\ AppData" \\ \\ als <username> BMP gespeichert. Alle Schrägstriche ( \\ ) werden in Pluszeichen (+) konvertiert. Beispielsweise wird der Domänen \\ Benutzer in Domäne + Benutzer konvertiert.

Die Bilddatei wird im **temporären Ordner des** Benutzers angezeigt:

-   Nachdem der Benutzer die anfängliche Systeminstallation (OOBE) abgeschlossen hat.
-   Wenn der Benutzer das System Steuerungselement " **Benutzerkonten** " erstmalig aufruft.
-   Der Benutzer wechselt zur Unterseite **Konten verwalten** des System Steuerungs Elements **Benutzerkonten** . Außerdem werden Kacheln für alle anderen Benutzer auf dem Computer angezeigt.

Diese Instanzen sind das einzige Mal, dass die Images erstellt oder aktualisiert werden. Daher gibt es mehrere Einschränkungen, die Sie berücksichtigen sollten, wenn **Sie den** Speicherort des temporären Ordners Programm gesteuert verwenden:

1.  Es ist nicht garantiert, dass die Kachel des Benutzers vorhanden ist. Wenn der Benutzer die BMP-Datei z. b. manuell oder über ein Hilfsprogramm löscht, das temporäre Dateien löscht, wird diese Benutzer Kachel erst dann automatisch neu erstellt, wenn der Benutzer das System Steuerungselement " **Benutzerkonten** " oder die Unterseite " **Konten verwalten** " aufruft.

2.  Benutzer Kacheln für andere Benutzer auf dem Computer sind möglicherweise nicht im temporären **Ordner des aktuell** angemeldeten Benutzers vorhanden. Wenn Benutzer a z. b. Benutzer b über das System Steuerungselement **Benutzerkonten** erstellt, wird die Kachel von Benutzer b im **temporären Ordner des** Benutzers a erstellt, wenn Windows Benutzer a an die Unterseite **Konten verwalten** sendet. Da die Verzeichnisstruktur nicht für Benutzer b erstellt wird, bis Sie sich anmeldet, ist der **Temp** -Ordner von User a der einzige Speicherort, an dem die Kachel von Benutzer b gespeichert ist. Wenn sich Benutzer b anmeldet, ist das einzige Image **, das im temporären Ordner von** Benutzer b gespeichert ist, das eigene Image.

    1.  Um alle Benutzer Kacheln für Benutzer auf einem System zu erhalten, müssen Anwendungen möglicherweise im **temporären Verzeichnis jedes** Benutzers suchen.
    2.  Da die Zugriffs Steuerungs Liste (Access Control List, ACL) dieser temporären Verzeichnisse den Zugriff **auf das System** , den Administrator und den aktuellen Benutzer ermöglicht, müssen Anwendungen für andere Benutzer den Zugriff auf den Zugriff erhöhen.

3.  Die Kacheln anderer Benutzer sind **in ihren temporären** Ordnern nicht auf dem neuesten Stand. Wenn Benutzer B seine Benutzer Kachel aktualisiert, wird die Änderung erst dann angezeigt, wenn Benutzer a auf die Unterseite **Konten verwalten** zugreift. Wenn Anwendungen den **Temp** -Ordner von User a zum Abrufen der Kachel von Benutzer B verwenden, können diese Anwendungen daher eine veraltete Bilddatei abrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lokale Benutzerprofile](local-user-profiles.md)
</dt> <dt>

[Roamingbenutzerprofile](roaming-user-profiles.md)
</dt> <dt>

[Verbindliche Benutzerprofile](mandatory-user-profiles.md)
</dt> <dt>

[Temporäre Benutzerprofile](temporary-user-profiles.md)
</dt> <dt>

[Profile-Verzeichnis](profiles-directory.md)
</dt> <dt>

[Benutzer Umgebungsvariablen](user-environment-variables.md)
</dt> <dt>

[Schnelle Benutzerumschaltung](fast-user-switching.md)
</dt> </dl>

 

 



