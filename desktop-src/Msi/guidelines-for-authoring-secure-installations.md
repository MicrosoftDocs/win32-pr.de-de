---
description: Befolgen Sie diese Richtlinien, wenn Sie das Windows Installer Paket erstellen, um eine sichere Umgebung während der Software Installation zu gewährleisten.
ms.assetid: 04d91a9b-0528-4acb-8e11-fc817009db1f
title: Richtlinien für das Erstellen von sicheren Installationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d18e66c38480149ddad9e381c6461ffe50cf0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351767"
---
# <a name="guidelines-for-authoring-secure-installations"></a>Richtlinien für das Erstellen von sicheren Installationen

Beachten Sie beim Erstellen eines Windows Installer Pakets die folgenden Richtlinien, um während der Installation eine sichere Umgebung zu gewährleisten:

-   Administratoren sollten verwaltete Anwendungen in einem Ziel Installationsordner installieren, für den Benutzer ohne Administratorrechte über keine Berechtigungen zum Ändern oder ändern verfügen.
-   Legen Sie eine Eigenschaft fest, die vom Benutzer als öffentliche Eigenschaft festgelegt wird. Private Eigenschaften können vom Benutzer, der mit der Benutzeroberfläche interagiert, nicht geändert werden. Weitere Informationen finden Sie unter Informationen [zu Eigenschaften](about-properties.md).
-   Verwenden Sie keine Eigenschaften für Kenn Wörter oder andere Informationen, die sicher bleiben müssen. Das Installationsprogramm kann den Wert einer Eigenschaft, die in die [Eigenschaften Tabelle](property-table.md)geschrieben oder zur Laufzeit erstellt wurde, in ein Protokoll oder die Systemregistrierung schreiben. Weitere Informationen finden Sie unter [verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden](preventing-confidential-information-from-being-written-into-the-log-file.md).
-   Wenn die Installation erfordert, dass das Installationsprogramm [*erhöhte*](e-gly.md) Rechte verwendet, verwenden Sie [Eingeschränkte öffentliche Eigenschaften](restricted-public-properties.md) , um die öffentlichen Eigenschaften einzuschränken, die ein Benutzer ändern kann. Einige Einschränkungen sind im allgemeinen erforderlich, um eine sichere Umgebung zu verwalten, wenn die Installation erfordert, dass das Installationsprogramm *Erweiterte Berechtigungen verwendet* .
-   Vermeiden Sie die Installation von Diensten, die die Berechtigungen eines bestimmten Benutzers annehmen, da dadurch Sicherheitsdaten in ein Protokoll oder die Systemregistrierung geschrieben werden können. Dadurch entsteht ein mögliches Sicherheitsproblem, ein Kenn Wort Konflikt oder der Verlust von Konfigurationsdaten, wenn das System neu gestartet wird. Weitere Informationen finden Sie unter [servicin Stall Table](serviceinstall-table.md).
-   Verwenden Sie die [Tabelle lockberechtigungs Tabelle](lockpermissions-table.md) und die [Tabelle "msilockpermissionsex](msilockpermissionsex-table.md) ", um Dienste, Dateien, Registrierungsschlüssel und erstellte Ordner in einer gesperrten Umgebung zu sichern.
-   Fügen Sie der Installation eine digitale Signatur hinzu, um die Integrität der Dateien sicherzustellen. Weitere Informationen finden Sie unter [digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md) und [Erstellen einer vollständig überprüften signierten Installation](authoring-a-fully-verified-signed-installation.md).
-   Erstellen Sie das Windows Installer Paket, damit der Zugriff auf Ressourcen nicht möglich ist, wenn dem Benutzer der Zugriff auf Ressourcen verweigert wird. Überprüfen Sie die Zugriffsberechtigungen des Benutzers, und stellen Sie fest, ob ausreichend Speicherplatz vorhanden ist, bevor die Installation beginnt Häufig sollte das Installationsprogramm nur ein Dialogfeld zum Durchsuchen anzeigen, wenn der aktuelle Benutzer ein Administrator ist, oder wenn die Installation keine [*erhöhten*](e-gly.md) Rechte erfordert. Weitere Informationen finden Sie unter [Quellen Resilienz](source-resiliency.md).
-   Verwenden Sie [gesicherte Transformationen](secured-transforms.md) , um Transformationen in einem sicheren Dateisystem lokal auf dem Computer des Benutzers zu speichern. Dadurch wird verhindert, dass der Benutzer Schreibzugriff auf die Transformation hat.
-   Informationen zum Sichern von Medienquellen verwalteter Anwendungen finden Sie unter [Quellen Resilienz](source-resiliency.md).
-   Verwenden Sie die Eigenschaft [**Sicherheits Zusammenfassung**](security-summary.md) , um anzugeben, ob das Paket schreibgeschützt geöffnet werden soll. Diese Eigenschaft sollte auf schreibgeschützt festgelegt werden, um eine-Installations Datenbank zu lesen und für eine Transformation oder einen Patch schreibgeschützt zu erzwingen.
-   Der Installer führt standardmäßig benutzerdefinierte Aktionen mit Benutzerberechtigungen aus, um den Zugriff auf benutzerdefinierte Aktionen auf das System zu beschränken. Der Installer kann benutzerdefinierte Aktionen mit [*erhöhten*](e-gly.md) Rechten ausführen, wenn eine verwaltete Anwendung installiert wird oder wenn die System Richtlinie für erweiterte Berechtigungen angegeben wurde. Weitere Informationen finden Sie unter [Sicherheit für benutzerdefinierte Aktionen](custom-action-security.md).
-   Mithilfe der [disablepatch](disablepatch.md) -Richtlinie können Sie Sicherheit in Umgebungen bereitstellen, in denen das Patchen eingeschränkt werden muss.
-   Verwenden Sie die [AppID-Tabelle](appid-table.md) , um allgemeine Sicherheits-und Konfigurationseinstellungen für DCOM-Objekte zu registrieren.
-   Weitere Informationen finden Sie unter [Richtlinien zum Sichern von benutzerdefinierten Aktionen](guidelines-for-securing-custom-actions.md).
-   Weitere Informationen finden Sie unter [Richtlinien zum Sichern von Paketen auf gesperrten Computern](guidelines-for-securing-packages-on-locked-down-computers.md).
-   Ab Windows Installer 3,0 ermöglicht das [Patchen von Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md) Benutzern, die keine Administratoren sind, das Patchen von Anwendungen, die im computerspezifischen Kontext installiert sind. Das UAC-Patchen wird aktiviert, indem ein Signatur Geber Zertifikat in der [MsiPatchCertificate](msipatchcertificate-table.md) -Tabelle bereitgestellt und Patches mit demselben Zertifikat signiert werden.
-   Die Funktion des Windows Installer 5,0, Zugriffsberechtigungen für Dienste, Dateien, erstellte Ordner und Registrierungseinträge festzulegen, kann dazu beitragen, dass Installationsanwendungen sicherer werden. Weitere Informationen finden Sie unter [Sichern von Ressourcen](securing-resources-.md).

 

 



