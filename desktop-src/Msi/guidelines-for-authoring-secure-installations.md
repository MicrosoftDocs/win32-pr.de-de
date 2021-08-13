---
description: Um eine sichere Umgebung während der Softwareinstallation zu gewährleisten, befolgen Sie diese Richtlinien beim Erstellen des Windows Installer-Pakets.
ms.assetid: 04d91a9b-0528-4acb-8e11-fc817009db1f
title: Richtlinien für die Erstellung sicherer Installationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f796594fe665875f63751d0da4cac5bd7cde621e04b4d1d35585c74755dd719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635798"
---
# <a name="guidelines-for-authoring-secure-installations"></a>Richtlinien für die Erstellung sicherer Installationen

Die Einhaltung der folgenden Richtlinien beim Erstellen eines Windows Installer-Pakets trägt zur Aufrechterhaltung einer sicheren Umgebung während der Installation bei:

-   Administratoren sollten verwaltete Anwendungen in einem Zielinstallationsordner installieren, für den Benutzer ohne Administratorrechte keine Änderungs- oder Änderungsrechte besitzen.
-   Legen Sie jede vom Benutzer festgelegte Eigenschaft als öffentliche Eigenschaft fest. Private Eigenschaften können nicht vom Benutzer geändert werden, der mit der Benutzeroberfläche interagiert. Weitere Informationen finden Sie unter [Informationen zu Eigenschaften.](about-properties.md)
-   Verwenden Sie keine Eigenschaften für Kennwörter oder andere Informationen, die sicher bleiben müssen. Das Installationsprogramm kann den Wert einer Eigenschaft, die in die [Property-Tabelle](property-table.md)geschrieben oder zur Laufzeit erstellt wurde, in ein Protokoll oder die Systemregistrierung schreiben. Weitere Informationen finden Sie unter [Verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden.](preventing-confidential-information-from-being-written-into-the-log-file.md)
-   Wenn für die Installation das Installationsprogramm [*erhöhte*](e-gly.md) Rechte benötigt, verwenden Sie [Eingeschränkte öffentliche Eigenschaften,](restricted-public-properties.md) um die öffentlichen Eigenschaften einzuschränken, die ein Benutzer ändern kann. Einige Einschränkungen sind häufig erforderlich, um eine sichere Umgebung aufrechtzuerhalten, wenn für die Installation das Installationsprogramm *erhöhte* Rechte benötigt.
-   Vermeiden Sie die Installation von Diensten, die die Identität der Berechtigungen eines bestimmten Benutzers annehmen, da dies Sicherheitsdaten in ein Protokoll oder die Systemregistrierung schreiben kann. Dies kann zu einem Sicherheitsproblem, einem Kennwortkonflikt oder dem Verlust von Konfigurationsdaten beim Neustart des Systems kommen. Weitere Informationen finden Sie unter [ServiceInstall-Tabelle.](serviceinstall-table.md)
-   Verwenden Sie die [Tabelle LockPermissions](lockpermissions-table.md) und die [Tabelle MsiLockPermissionsEx,](msilockpermissionsex-table.md) um Dienste, Dateien, Registrierungsschlüssel und erstellte Ordner in einer gesperrten Umgebung zu schützen.
-   Fügen Sie der Installation digitale Signaturen hinzu, um die Integrität der Dateien sicherzustellen. Weitere Informationen finden Sie unter [Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md) und Erstellen einer vollständig [überprüften signierten Installation.](authoring-a-fully-verified-signed-installation.md)
-   Erstellen Sie ihr Windows Installer-Paket so, dass das Setup in einer Weise fehlschlägt, die eine sichere Umgebung aufrechterhält, wenn dem Benutzer der Zugriff auf Ressourcen verweigert wird. Überprüfen Sie die Zugriffsberechtigungen des Benutzers, und ermitteln Sie, ob ausreichend Speicherplatz vorhanden ist, bevor die Installation beginnt. In der Regel sollte das Installationsprogramm nur dann ein Dialogfeld zum Durchsuchen anzeigen, wenn der aktuelle Benutzer Administrator ist oder wenn die Installation keine [*erhöhten*](e-gly.md) Berechtigungen erfordert. Weitere Informationen finden Sie unter [Quellresilienz.](source-resiliency.md)
-   Verwenden Sie [geschützte Transformationen,](secured-transforms.md) um Transformationen lokal auf dem Computer des Benutzers in einem sicheren Dateisystem zu speichern. Dadurch wird verhindert, dass der Benutzer Schreibzugriff auf die Transformation hat.
-   Informationen zum Sichern von Medienquellen verwalteter Anwendungen finden Sie unter [Quellresilienz.](source-resiliency.md)
-   Verwenden Sie die [**Sicherheitszusammenfassungseigenschaft,**](security-summary.md) um anzugeben, ob das Paket schreibgeschützt geöffnet werden soll. Diese Eigenschaft sollte auf schreibgeschützt empfohlen für eine Installationsdatenbank und auf schreibgeschützt für eine Transformation oder einen Patch festgelegt werden.
-   Das Installationsprogramm führt standardmäßig benutzerdefinierte Aktionen mit Benutzerberechtigungen aus, um den Zugriff benutzerdefinierter Aktionen auf das System einzuschränken. Das Installationsprogramm kann benutzerdefinierte Aktionen mit [*erhöhten*](e-gly.md) Rechten ausführen, wenn eine verwaltete Anwendung installiert wird oder wenn die Systemrichtlinie für erhöhte Rechte angegeben wurde. Weitere Informationen finden Sie unter [Benutzerdefinierte Aktionssicherheit.](custom-action-security.md)
-   Verwenden Sie die [Richtlinie DisablePatch,](disablepatch.md) um Sicherheit in Umgebungen bereitzustellen, in denen das Patchen eingeschränkt werden muss.
-   Verwenden Sie die [Tabelle AppId,](appid-table.md) um allgemeine Sicherheits- und Konfigurationseinstellungen für DCOM-Objekte zu registrieren.
-   Weitere Informationen finden Sie unter [Richtlinien zum Sichern von benutzerdefinierten Aktionen.](guidelines-for-securing-custom-actions.md)
-   Weitere Informationen finden Sie unter [Richtlinien zum Sichern von Paketen auf gesperrten Computern.](guidelines-for-securing-packages-on-locked-down-computers.md)
-   Ab Windows Installer 3.0 ermöglicht das Patchen der [Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md) Benutzern ohne Administratorrechte das Patchen von Anwendungen, die im Kontext pro Computer installiert sind. UAC-Patching wird aktiviert, indem ein Signaturzertifikat in der [MsiPatchCertificate-Tabelle](msipatchcertificate-table.md) und Signaturpatches mit demselben Zertifikat zur Verfügung gestellt werden.
-   Die Funktion des Windows Installer 5.0 zum Festlegen von Zugriffsberechtigungen für Dienste, Dateien, erstellte Ordner und Registrierungseinträge kann dazu beitragen, Installationsanwendungen sicherer zu machen. Weitere Informationen finden Sie unter [Sichern von Ressourcen.](securing-resources-.md)

 

 



