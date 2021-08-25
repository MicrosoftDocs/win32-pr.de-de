---
description: Das System erstellt ein Benutzerprofil, wenn sich ein Benutzer zum ersten Mal bei einem Computer anmeldet. Bei nachfolgenden Anmeldungen lädt das System das Profil des Benutzers, und dann konfigurieren andere Systemkomponenten die Umgebung des Benutzers gemäß den Informationen im Profil.
title: Informationen zu Benutzerprofilen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 333f1861-91fe-4796-af13-dd300a5c6ec3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f0463a38623baa427a6ddaf3ea19b47704b90e3ef36cf91dea2469e0cd2baa00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884770"
---
# <a name="about-user-profiles"></a>Informationen zu Benutzerprofilen

Das System erstellt ein Benutzerprofil, wenn sich ein Benutzer zum ersten Mal bei einem Computer anmeldet. Bei nachfolgenden Anmeldungen lädt das System das Profil des Benutzers, und dann konfigurieren andere Systemkomponenten die Umgebung des Benutzers gemäß den Informationen im Profil.

## <a name="types-of-user-profiles"></a>Typen von Benutzerprofilen

-   [Lokale Benutzerprofile.](local-user-profiles.md) Ein lokales Benutzerprofil wird erstellt, wenn sich ein Benutzer zum ersten Mal bei einem Computer anmeldet. Das Profil wird auf der lokalen Festplatte des Computers gespeichert. Änderungen am lokalen Benutzerprofil gelten spezifisch für den Benutzer und den Computer, auf dem die Änderungen vorgenommen werden.
-   [Roamingbenutzerprofile](roaming-user-profiles.md). Ein Roamingbenutzerprofil ist eine Kopie des lokalen Profils, das in eine Serverfreigabe kopiert und auf dieser gespeichert wird. Dieses Profil wird auf jeden Computer heruntergeladen, auf dem sich ein Benutzer in einem Netzwerk anmeldet. Änderungen an einem Roamingbenutzerprofil werden mit der Serverkopie des Profils synchronisiert, wenn sich der Benutzer abmeldet. Der Vorteil von Roamingbenutzerprofilen besteht darin, dass Benutzer nicht auf jedem Computer, den sie in einem Netzwerk verwenden, ein Profil erstellen müssen.
-   [Erforderliche Benutzerprofile.](mandatory-user-profiles.md) Ein obligatorisches Benutzerprofil ist ein Profiltyp, mit dem Administratoren Einstellungen für Benutzer angeben können. Nur Systemadministratoren können Änderungen an obligatorischen Benutzerprofilen vornehmen. Änderungen, die von Benutzern an Desktopeinstellungen vorgenommen werden, gehen verloren, wenn sich der Benutzer abmeldet.
-   [Temporäre Benutzerprofile.](temporary-user-profiles.md) Jedes Mal, wenn eine Fehlerbedingung das Laden des Benutzerprofils verhindert, wird ein temporäres Profil ausgegeben. Temporäre Profile werden am Ende jeder Sitzung gelöscht, und änderungen, die vom Benutzer an Desktopeinstellungen und -dateien vorgenommen werden, gehen verloren, wenn sich der Benutzer abmeldet. Temporäre Profile sind nur auf Computern verfügbar, auf denen Windows 2000 und höher ausgeführt wird.

Ein Benutzerprofil besteht aus den folgenden Elementen:

-   Eine Registrierungsstruktur. Die Registrierungsstruktur ist die Datei NTuser.dat. Die Struktur wird beim Anmelden des Benutzers vom System geladen und dem Registrierungsschlüssel **HKEY \_ CURRENT \_ USER** zugeordnet. Die Registrierungsstruktur des Benutzers verwaltet die registrierungsbasierten Einstellungen und die Konfiguration des Benutzers.
-   Eine Gruppe von Profilordnern, die im Dateisystem gespeichert sind. Benutzerprofildateien werden im Verzeichnis **Profile** auf Benutzerbasis gespeichert. Der Benutzerprofilordner ist ein Container für Anwendungen und andere Systemkomponenten, der mit Unterordnern und benutzerbezogenen Daten wie Dokumenten und Konfigurationsdateien aufgefüllt werden kann. Windows Der Explorer verwendet die Benutzerprofilordner umfassend für Elemente wie Desktop, **Startmenü** und **Ordner Dokumente** des Benutzers.

Benutzerprofile bieten die folgenden Vorteile:

-   Wenn sich der Benutzer bei einem Computer anmeldet, verwendet das System die gleichen Einstellungen, die bei der letzten Abmeldung des Benutzers verwendet wurden.
-   Wenn ein Computer für andere Benutzer freigegeben wird, erhält jeder Benutzer nach der Anmeldung den angepassten Desktop.
-   Einstellungen im Benutzerprofil sind für jeden Benutzer eindeutig. Andere Benutzer können nicht auf die Einstellungen zugreifen. Änderungen am Profil eines Benutzers wirken sich nicht auf die Profile anderer Benutzer oder anderer Benutzer aus.

## <a name="user-profile-tiles-in-windows-7-and-later"></a>Benutzerprofilkacheln in Windows 7 und höher

In Windows 7 oder höher verfügt jedes Benutzerprofil über ein zugeordnetes Bild, das als Benutzerkachel dargestellt wird. Diese Kacheln werden Benutzern auf dem Element **Benutzerkonten** Systemsteuerung und der zugehörigen Unterseite **Konten verwalten** angezeigt. Die Imagedateien für die Standardbenutzerkonten "Gast" und "Standardbenutzer" werden auch hier angezeigt, wenn Sie über Administratorzugriffsrechte verfügen.

> [!Note]  
> Auf die Unterseite **Konten verwalten** wird über den Link Anderes **Konto verwalten** im Element **Benutzerkonten** Systemsteuerung zugegriffen.

 

-   %ProgramData% \\ Microsoft User Account Pictures \\ \\Guest.bmp
-   %ProgramData% \\ Microsoft User Account Pictures \\ \\User.bmp

Das Kachelbild des Benutzers wird als.bmp im Ordner %SystemDrive% \\ Users \\ <username> \\ AppData \\ Local Temp \\ <username> gespeichert. Alle Schrägstriche ( \\ ) werden in Pluszeichen (+) konvertiert. Beispielsweise wird DOMAIN \\ user in DOMAIN+user konvertiert.

Die Bilddatei wird im Ordner **Temp** des Benutzers angezeigt:

-   Nachdem der Benutzer die anfängliche Systemeinrichtung (OOBE) abgeschlossen hat.
-   Wenn der Benutzer zum ersten Mal die **Benutzerkonten** Systemsteuerung Element startet.
-   Wenn der Benutzer zur Unterseite **Konten verwalten** des Elements **Benutzerkonten** Systemsteuerung wechselt. Darüber hinaus werden Kacheln für alle anderen Benutzer auf dem Computer angezeigt.

Diese Instanzen sind die einzigen Fälle, in denen die Bilder erstellt oder aktualisiert werden. Daher müssen sie bei der programmgesteuerten Verwendung des Speicherorts des **Temporären** Ordners einige Einschränkungen beachten:

1.  Es ist nicht garantiert, dass die Kachel des Benutzers vorhanden ist. Wenn der Benutzer die .bmp Datei löscht, z. B. manuell oder über ein Hilfsprogramm, das temporäre Dateien löscht, wird diese Benutzerkachel erst dann automatisch neu erstellt, wenn der Benutzer die Unterseite **Benutzerkonten** Systemsteuerung Element oder **Konten verwalten** startet.

2.  Benutzerkacheln für andere Benutzer auf dem Computer sind möglicherweise nicht im **Temp-Ordner** des derzeit angemeldeten Benutzers vorhanden. Wenn Benutzer A beispielsweise Benutzer B über das Element **Benutzerkonten** Systemsteuerung erstellt, wird die Kachel von Benutzer B im **Temporären** Ordner von Benutzer A erstellt, wenn Windows Benutzer A an die Unterseite **Konten verwalten** sendet. Da die Verzeichnisstruktur für Benutzer B erst erstellt wird, wenn er sich anmeldet, ist der **Ordner Temp** von Benutzer A der einzige Speicherort, an dem die Kachel von Benutzer B gespeichert wird. Wenn sich Benutzer B anmeldet, ist das einzige Image, das im **Temp-Ordner** von Benutzer B gespeichert ist, sein eigenes Image.

    1.  Um alle Benutzerkacheln für Benutzer in einem System abzurufen, müssen Anwendungen möglicherweise im **Temp-Verzeichnis** jedes Benutzers suchen.
    2.  Da die Zugriffssteuerungsliste (Access Control List, ACL) dieser **temporären** Verzeichnisse den Zugriff auf SYSTEM, Administrator und den aktuellen Benutzer zulässt, müssen Anwendungen erhöhte Zugriffsrechte für andere Benutzer verwenden.

3.  Es ist nicht garantiert, dass die Kacheln anderer Benutzer in ihren **Temporären** Ordnern auf dem neuesten Stand sind. Wenn Benutzer B seine Benutzerkachel aktualisiert, wird die Änderung von Benutzer A erst angezeigt, wenn Benutzer A auf die Unterseite **Konten verwalten** zugreift. Wenn Anwendungen daher den **Ordner Temp** von Benutzer A verwenden, um die Kachel von Benutzer B abzurufen, können diese Anwendungen eine veraltete Bilddatei abrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lokale Benutzerprofile](local-user-profiles.md)
</dt> <dt>

[Roamingbenutzerprofile](roaming-user-profiles.md)
</dt> <dt>

[Erforderliche Benutzerprofile](mandatory-user-profiles.md)
</dt> <dt>

[Temporäre Benutzerprofile](temporary-user-profiles.md)
</dt> <dt>

[Profilverzeichnis](profiles-directory.md)
</dt> <dt>

[Benutzerumgebungsvariablen](user-environment-variables.md)
</dt> <dt>

[Schnelle Benutzerumschaltung](fast-user-switching.md)
</dt> </dl>

 

 



