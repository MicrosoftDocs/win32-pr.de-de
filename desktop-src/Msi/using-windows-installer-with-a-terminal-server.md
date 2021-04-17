---
description: Die folgenden Auswirkungen können sich auf Windows Installer Installationen bei Verwendung eines Terminal Servers auswirken. Setup Entwickler sollten immer testen, ob das Windows Installer Paket wie erwartet installiert wird, wenn Benutzer auch einen Terminal Server verwenden.
ms.assetid: deda9efa-a0fc-4b4e-a531-650ac201fd84
title: Verwenden von Windows Installer mit einem Terminal Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d471fa19b4588a01a2730af44fa5e9d978d18859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484659"
---
# <a name="using-windows-installer-with-a-terminal-server"></a>Verwenden von Windows Installer mit einem Terminal Server

Die folgenden Auswirkungen können sich auf Windows Installer Installationen bei Verwendung eines Terminal Servers auswirken. Setup Entwickler sollten immer testen, ob das Windows Installer Paket wie erwartet installiert wird, wenn Benutzer auch einen Terminal Server verwenden.

-   Unter älteren Betriebssystemen als Windows Server 2008 und Windows Vista muss die System Richtlinie [enableadminungremote](enableadmintsremote.md) festgelegt werden, damit Administratoren in der Client Sitzung Installationen ausführen können. Ab Windows Server 2008 und Windows Vista hat die enableadminungsremote-Richtlinie keine Auswirkungen mehr. Unabhängig von der Einstellung können Administratoren und nicht-Administratoren eine Installation in der Client Sitzung oder in der Konsolen Sitzung ausführen. Administratoren und nicht-Administratoren können in der Konsolen Sitzung immer Windows Installer Installationen ausführen.
-   Der-Windows Installer verhindert die Installation im [Installations Kontext](installation-context.md) pro Benutzer, wenn die[System Richtlinie](system-policy.md) " [disableuserinstallationen](disableuserinstalls.md)" auf 1 festgelegt ist. In diesem Fall ignoriert das Installationsprogramm alle Anwendungen, die als pro Benutzer registriert sind, und sucht nur nach Anwendungen, die als Computer bezogen registriert sind.
-   Wenn ein Administrator eine Installation in einer Client Sitzung eines in Windows 2000 gehosteten Terminal Servers durchführt, muss bei der Installation ein UNC-Pfad und kein zugeordneter Laufwerk Buchstabe verwendet werden.

Entwickler sollten die folgenden Richtlinien befolgen, wenn Sie eine Windows Installer Komponente entwickeln, die mit einem Terminal Server verwendet werden kann.

-   Schreiben Sie alle **HKCU** -Registrierungsinformationen in den **HKCU**- \\ **Software** Teil der Registrierung.
-   Das Speichern von Konfigurationsinformationen in INI-Dateien wird nicht empfohlen.
-   Schreiben Sie benutzerspezifische Informationen in die Registrierung, wenn die Anwendung zum ersten Mal ausgeführt wird, und nicht zur Installationszeit. Wenn Sie benutzerspezifische Informationen zur Installationszeit in die Registrierung schreiben müssen, müssen Sie die Benutzer-und computerspezifischen Informationen in verschiedene Windows Installer Komponenten aufteilen. Erstellen Sie das Paket so, dass das Installationsprogramm bei der Installation der Anwendung nicht versucht, die Komponenten zu überprüfen und zu reparieren, die benutzerspezifische Informationen enthalten.
-   Ein Paket, das nur für Installationen pro Computer verwendet wird, sollte Umgebungsvariablen in die Computerumgebung schreiben, indem es \* in die Spalte Name der [Umgebungs Tabelle](environment-table.md)eingeschlossen wird. Wenn das Paket für Installationen pro Benutzer oder pro Computer verwendet werden kann, verwenden Sie zwei Komponenten. Fügen Sie die Komponente "pro Benutzer" in die [Komponenten Tabelle](condition-table.md) ein, und geben Sie die Benutzereinstellungen in der Umgebungs Tabelle ein. Fügen Sie die Komponente pro Computer in die Komponenten Tabelle ein, und geben Sie die Computereinstellungen in der Umgebungs Tabelle ein. Steuern, welche Komponente installiert wird, indem Sie bedingte Anweisungen verwenden, die auf der [**ALLUSERS**](allusers.md) -Eigenschaft im Bedingungs Feld der Komponenten Tabelle basieren.
-   Bei der Durchführung von computerspezifischen Installationen von einem Terminal Server schreibt der Installer Umgebungsvariablen pro Benutzer in **HKCU** \\ **. Standard** \\ **Umgebung**. Da der Terminal Server diesen Abschnitt der Registrierung nicht repliziert, werden bei der Installation die Umgebungsvariablen pro Benutzer nicht festgelegt.
-   Da ein Server konfiguriert werden kann, um zu verhindern, dass Benutzer Anwendungen reparieren, sollte Ihre Anwendung die Groß-/Kleinschreibung fehlender Registrierungsschlüssel behandeln.

Folgendes gilt, wenn ein Windows Installer Paket, das dll-, exe-oder Skript- [benutzerdefinierte Aktionen](custom-actions.md) verwendet, im Installations Kontext pro Computer auf einem Terminal Server installiert wird. In diesem Fall legt der Installer die [**Terminalserver**](terminalserver.md) -Eigenschaft fest.

-   Verzögerte benutzerdefinierte Aktionen werden im Kontext des lokalen Systems ausgeführt, es sei denn, die Aktion verfügt über das **msidbcustomaction typetsaware** -Attribut. Dies gilt auch, wenn die benutzerdefinierte Aktion die Identität des Benutzers auf einem System annimmt, das kein Terminal Server ist. Beachten Sie, dass das Installationsprogramm nicht automatisch sicherstellt, dass diese Änderungen auch in der Registrierung jedes Benutzers auf dem Computer vorgenommen werden, wenn eine benutzerdefinierte Aktion, die über das **msidbcustomaction typetsaware** -Attribut verfügt, die Registrierung des Benutzers ändert.
-   Bei allen Registrierungs Vorgängen in einer verzögerten benutzerdefinierten Aktion, die aus der **HKCU** -Registrierungs Struktur gelesen wird, wird die Standard Registrierungs Struktur des Systems und nicht die Registrierungs Struktur des aktuellen Benutzers angezeigt.
-   Alle Registrierungs Vorgänge in einer verzögerten benutzerdefinierten Aktion, die in **HKCU** \\ -**Software** schreiben, werden vom Installationsprogramm erkannt und bei der nächsten Anmeldung des Benutzers auf jeden Benutzer des Computers kopiert.
-   Alle Registrierungs Vorgänge in einer verzögerten benutzerdefinierten Aktion, die in **HKCU** schreiben, jedoch nicht unter dem Registrierungsschlüssel für die **HKCU**- \\ **Software** vorhanden sind, werden vom Installationsprogramm nicht erkannt oder kopiert.

Weitere Informationen finden Sie unter [Terminal Dienste](../termserv/terminal-services-portal.md) im Microsoft Windows Software Development Kit (SDK).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Enableadminout-Remote](enableadmintsremote.md)
</dt> <dt>

[**Terminalserver (Eigenschaft)**](terminalserver.md)
</dt> <dt>

[**Remoteadmints (Eigenschaft)**](remoteadmints.md)
</dt> <dt>

[Terminaldienste](../termserv/terminal-services-portal.md)
</dt> </dl>

 

 
