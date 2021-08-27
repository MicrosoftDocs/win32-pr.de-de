---
description: Folgendes kann sich auf Windows Installer-Installationen auswirken, wenn ein Terminalserver verwendet wird. Setupentwickler sollten immer testen, ob Windows Installer-Paket wie erwartet installiert wird, wenn Benutzer auch einen Terminalserver verwenden.
ms.assetid: deda9efa-a0fc-4b4e-a531-650ac201fd84
title: Verwenden Windows Installers mit einem Terminalserver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aba70bc9430f0bc55c7e234b19764a14b138a4d5053de5c1cc6b9aee37692d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995830"
---
# <a name="using-windows-installer-with-a-terminal-server"></a>Verwenden Windows Installers mit einem Terminalserver

Folgendes kann sich auf Windows Installer-Installationen auswirken, wenn ein Terminalserver verwendet wird. Setupentwickler sollten immer testen, ob Windows Installer-Paket wie erwartet installiert wird, wenn Benutzer auch einen Terminalserver verwenden.

-   Bei Betriebssystemen vor Windows Server 2008 und Windows Vista muss die [Systemrichtlinie EnableAdminTSRemote](enableadmintsremote.md) festgelegt werden, damit Administratoren Installationen in der Clientsitzung ausführen können. Ab Windows Server 2008 und Windows Vista hat die EnableAdminTSRemote-Richtlinie keine Auswirkungen mehr. Unabhängig von der Einstellung können Administratoren und Nichtadministratoren eine Installation in der Clientsitzung oder der Konsolensitzung ausführen. Administratoren und Nichtadministratoren können installationen Windows Installationen des Installationsprogramms immer in der Konsolensitzung ausführen.
-   Der Windows Installer verhindert die Installation im [](installation-context.md) Benutzerinstallationskontext, wenn die [Systemrichtlinie DisableUserInstalls](disableuserinstalls.md)[auf](system-policy.md) 1 festgelegt ist. In diesem Fall ignoriert das Installationsprogramm alle Anwendungen, die als pro Benutzer registriert sind, und sucht nur nach Anwendungen, die pro Computer registriert sind.
-   Wenn ein Administrator eine Installation in einer Clientsitzung eines Terminalservers ausführt, der in Windows 2000 gehostet wird, muss die Installation einen UNC-Pfad und keinen zugeordneten Laufwerkbuchstaben verwenden.

Entwickler sollten die folgenden Richtlinien befolgen, wenn sie eine Windows Installer-Komponente entwickeln, die mit einem Terminalserver verwendet werden kann.

-   Schreiben Sie **alle HKCU-Registrierungsinformationen** in den **HKCU** \\ **Software-Teil** der Registrierung.
-   Das Speichern von Konfigurationsinformationen in INI-Dateien wird nicht empfohlen.
-   Schreiben Sie Benutzerinformationen in die Registrierung, wenn die Anwendung zum ersten Mal und nicht zum Zeitpunkt der Installation ausgeführt wird. Wenn Sie benutzerspezifische Informationen zur Installationszeit in die Registrierung schreiben müssen, trennen Sie die benutzer- und computerspezifischen Informationen in verschiedene Komponenten Windows Installer. Erstellen Sie das Paket so, dass das Installationsprogramm nicht versucht, die Komponenten zu überprüfen und zu reparieren, die benutzerspezifische Informationen enthalten, wenn die Anwendung installiert wird.
-   Ein Paket, das nur für Installationen pro Computer verwendet wird, sollte Umgebungsvariablen in die Umgebung des Computers schreiben, indem es in die Spalte Name der \* [Umgebungstabelle einfing.](environment-table.md) Wenn das Paket für Benutzer- oder Computerinstallationen verwendet werden kann, verwenden Sie zwei Komponenten. Schließen Sie die Komponente pro Benutzer in die [Komponententabelle ein,](condition-table.md) und geben Sie die Benutzereinstellungen in die Umgebungstabelle ein. Schließen Sie die Komponente pro Computer in die Komponententabelle ein, und geben Sie die Computereinstellungen in die Umgebungstabelle ein. Steuern Sie, welche Komponente installiert wird, indem Sie bedingte Anweisungen verwenden, die auf der [**ALLUSERS-Eigenschaft**](allusers.md) im Feld Bedingung der Komponententabelle basieren.
-   Beim Ausführen von Computerinstallationen von einem Terminalserver aus schreibt das Installationsprogramm benutzerspezifische Umgebungsvariablen in **HKCU** \\ **. Standardumgebung** \\ . Da der Terminalserver diesen Abschnitt der Registrierung nicht repliziert, werden bei der Installation nicht die Benutzerumgebungsvariablen festgelegt.
-   Da ein Server konfiguriert werden kann, um zu verhindern, dass Benutzer Anwendungen reparieren, sollte Ihre Anwendung den Fall fehlender Registrierungsschlüssel ordnungsgemäß behandeln.

Folgendes gilt, wenn ein Windows Installer-Paket, das benutzerdefinierte DLL-, EXE- oder [Skriptaktionen](custom-actions.md) verwendet, im Installationskontext pro Computer auf einem Terminalserver installiert wird. In diesem Fall legt das Installationsprogramm die [**TerminalServer-Eigenschaft**](terminalserver.md) fest.

-   Verzögerte benutzerdefinierte Aktionen werden im Kontext des lokalen Systems ausgeführt, es sei denn, die Aktion verfügt über das **Attribut msidbCustomActionTypeTSAware.** Dies gilt auch, wenn die benutzerdefinierte Aktion die Identität des Benutzers auf einem System antändert, das kein Terminalserver ist. Wenn eine benutzerdefinierte Aktion mit dem **MsidbCustomActionTypeTSAware-Attribut** die Registrierung des Benutzers ändert, stellt das Installationsprogramm nicht automatisch sicher, dass diese Änderungen auch in der Registrierung jedes Benutzers auf dem Computer vorgenommen werden.
-   Alle Registrierungsvorgänge in einer verzögerten benutzerdefinierten Aktion, die aus der **HKCU-Registrierungsstruktur** lesen, sehen die Standardregistrierungsstruktur des Systems und nicht die Registrierungsstruktur des aktuellen Benutzers.
-   Alle Registrierungsvorgänge in einer verzögerten benutzerdefinierten Aktion, die in **HKCU** Software schreiben, werden vom Installationsprogramm erkannt und bei der nächsten Anmeldung des Benutzers an jeden Benutzer des \\  Computers kopiert.
-   Alle Registrierungsvorgänge in einer verzögerten benutzerdefinierten Aktion, die in **HKCU** schreiben, sich aber nicht unter dem Registrierungsschlüssel der **HKCU** Software befinden, werden vom Installationsprogramm nicht erkannt oder \\  kopiert.

Weitere Informationen finden Sie unter [Terminaldienste](../termserv/terminal-services-portal.md) im Microsoft Windows Software Development Kit (SDK).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EnableAdminTSRemote](enableadmintsremote.md)
</dt> <dt>

[**TerminalServer-Eigenschaft**](terminalserver.md)
</dt> <dt>

[**RemoteAdminTS(Eigenschaft)**](remoteadmints.md)
</dt> <dt>

[Terminaldienste](../termserv/terminal-services-portal.md)
</dt> </dl>

 

 
