---
description: Windows Installer entspricht Windows-Ressourcenschutz (WRP), wenn wichtige Systemdateien, Ordner und Registrierungsinformationen in Windows Server 2008 und höher sowie in Windows Vista und höher installiert werden.
ms.assetid: 38865ee1-22ef-430b-99ce-1c6983c3b51f
title: Verwenden von Windows Installer und Windows-Ressourcenschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72808184ff11b29bfeb02dda576e9393e34189fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959978"
---
# <a name="using-windows-installer-and-windows-resource-protection"></a>Verwenden von Windows Installer und Windows-Ressourcenschutz

Windows Installer entspricht Windows-Ressourcenschutz (WRP), wenn wichtige Systemdateien, Ordner und Registrierungsinformationen in Windows Server 2008 und höher sowie in Windows Vista und höher installiert werden.

WRP in Windows Server 2008 und Windows Vista ersetzt den Windows-Datei Schutz (WFP) in Windows Server 2003, Windows XP und Windows 2000. Windows Installer Entwickler sollten die folgenden Änderungen beachten, wie das Installationsprogramm geschützte Ressourcen in Windows Server 2008 und höher sowie in Windows Vista und höher behandelt:

-   Bei Ausführung unter Windows Server 2008 und höher oder Windows Vista und höher überspringt das Windows Installer die Installation von Dateien, die durch WRP geschützt sind, der Installer gibt eine Warnung in die Protokolldatei ein und setzt den Rest der Installation ohne Fehler fort. In Windows Server 2003, Windows XP und Windows 2000 konnte das Installationsprogramm die Datei von WFP installieren, wenn das Windows Installer eine durch WFP geschützte Datei gefunden hat.
-   WRP unter Windows Server 2008 und höher oder Windows Vista und höher kann Registrierungsschlüssel zusätzlich zu den Dateien schützen. Wenn in der Windows Installer ein durch WRP geschützter Registrierungsschlüssel gefunden wird, überspringt das Installationsprogramm die Installation dieses Registrierungsschlüssels, der Installer gibt eine Warnung in die Protokolldatei ein und setzt den Rest der Installation ohne Fehler fort.
-   Beachten Sie Folgendes: Wenn eine Windows Installer Komponente eine Datei oder einen Registrierungsschlüssel enthält, die durch WRP geschützt ist, muss diese Ressource als KEYPATH für die Komponente verwendet werden. In diesem Fall wird die Komponente von Windows Installer nicht installiert, aktualisiert oder entfernt. Sie sollten keine geschützten Ressourcen in ein Installationspaket einschließen. Verwenden Sie stattdessen die [unterstützten Mechanismen zur Ressourcen Ersetzung](../wfp/supported-file-replacement-mechanisms.md) für [Windows-Ressourcenschutz](../wfp/windows-resource-protection-portal.md).

Weitere Informationen zu WRP finden Sie unter [Windows-Ressourcenschutz](../wfp/windows-resource-protection-portal.md) und Informationen, die auf [Microsoft TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))bereitgestellt werden.

## <a name="wfp-for-windows-server-2003-and-windows-xp2000"></a>WFP für Windows Server 2003 und Windows XP/2000

Windows Installer befolgt den Windows-Datei Schutz (WFP), wenn wichtige Systemdateien unter Windows Server 2003, Windows XP und Windows 2000 installiert werden. Wenn eine geschützte Systemdatei durch eine unbeaufsichtigte Installation einer Anwendung geändert wird, stellt WFP die Datei in der überprüften Dateiversion wieder her.

Windows Installer versucht nie, eine geschützte Datei zu installieren oder zu ersetzen. Wenn die [InstallFiles](installfiles-action.md) -Aktion oder eine andere Aktion, die vor der Installation von InstallFiles geplant ist, versucht, eine Datei zu installieren, die unter Windows Server 2003, Windows XP oder Windows 2000 geschützt ist, ruft das Installationsprogramm WFP mit einer Anforderung zum Installieren oder Ersetzen der geschützten Datei auf Das Installationsprogramm fordert die Datei Installation von WFP sofort nach dem Ausführen der InstallFiles-Aktion an. WFP installiert oder ersetzt die Datei im System des Benutzers mit einer zwischengespeicherten Version der geschützten Datei. Beachten Sie, dass dies nicht gewährleistet, dass die Version der Datei, die aus dem Cache installiert wurde, die für die Anwendung erforderliche Version ist. Nachdem die Datei von WFP installiert wurde, ermittelt das Installationsprogramm, ob diese Version mit der Version im Paket übereinstimmt. Wenn die Dateiversion im Paket höher als die installierte Version ist, informiert das Installationsprogramm den Benutzer, dass er das System nicht aktualisieren kann und dass möglicherweise ein Update des Betriebssystems für die Anwendung erforderlich ist.

Wenn eine Aktion, die nach [InstallFiles](installfiles-action.md) ausgeführt wird, versucht, eine geschützte Datei zu installieren oder zu ersetzen, die noch nicht auf dem System installiert ist, kann das Installationsprogramm WFP nicht zum Installieren der Datei abrufen. In diesem Fall informiert der Installer den Benutzer, dass er das System nicht aktualisieren kann und dass möglicherweise ein Update des Betriebssystems für die Anwendung erforderlich ist.

Das Installationsprogramm überprüft beim Entfernen von Dateien auch WFP und versucht nie, geschützte Systemdateien zu entfernen.

## <a name="component-key-files-protected-by-wfp"></a>Von WFP geschützte Komponenten Schlüsseldateien

Beachten Sie Folgendes: Wenn eine Windows Installer Komponente eine WFP-Datei enthält, muss diese Datei als Schlüssel Pfad für die Komponente angegeben werden.

Wenn das Installationsprogramm versucht, die Schlüsseldatei einer Komponente unter Windows Server 2003, Windows XP oder Windows 2000 zu installieren, wird zuerst WFP aufgerufen, um zu bestimmen, ob die Schlüsseldatei geschützt ist. Wenn die Schlüsseldatei einer Komponente durch WFP geschützt wird und diese Schlüsseldatei bereits installiert ist, aktualisiert das Installationsprogramm die Komponente nur dann, wenn die Version der Schlüsseldatei im Paket größer als die installierte Version ist. Wenn das Installationspaket angibt, dass eine Komponente installiert ist und die Schlüsseldatei der Komponente zurzeit nicht installiert ist, installiert das Installationsprogramm unabhängig davon, ob die Schlüsseldatei geschützt ist, die Komponente. Wenn eine Komponente mit einer von WFP geschützten Schlüsseldatei installiert ist, wird Sie permanent installiert, und das Installationsprogramm entfernt bzw. ersetzt die Komponente nie.

## <a name="installation-of-assemblies-by-wfp"></a>Installation von Assemblys nach WFP

WFP für Assemblys unterscheidet sich von WFP für Systemdateien.

WFP schützt Windows Server 2003-, Windows XP-und Windows 2000-Systemdateien durch das Erkennen von versuchen, geschützte Systemdateien zu ersetzen. Dieser Schutz wird ausgelöst, nachdem WFP eine Verzeichnis Änderungs Benachrichtigung für eine Datei in einem geschützten Verzeichnis erhalten hat. Wenn WFP diese Benachrichtigung empfängt, wird ermittelt, welche Datei geändert wurde. Wenn die Datei geschützt ist, sucht WFP in einer statischen Katalog Datei nach der Datei Signatur, um zu bestimmen, ob die neue Datei die richtige Version hat. Wenn die Dateiversion nicht korrekt ist, ersetzt das System die Datei durch die richtige Version des Cache-oder Verteilungs Mediums.

Im Gegensatz dazu ist WFP von Assemblys dynamisch. WFP wird auf Dateien erweitert, da Sie dem freigegebenen parallelen Assemblycache hinzugefügt werden. Wenn eine Assembly beschädigt wird, fordert WFP an, dass die Datei durch das Installationsprogramm ersetzt wird. Windows Installer kann die Datei in Abhängigkeit davon ersetzen, ob auf das Quellpaket zugegriffen werden kann. Wenn auf das Quellpaket nicht zugegriffen werden kann, wird von WFP ein Dialogfeld mit der Meldung angezeigt, dass die Datei nicht wieder hergestellt werden kann.

Beachten Sie, dass nicht verwaltete, freigegebene parallele Assemblys, die in% windir% \\ WinSxS installiert sind, durch WFP geschützt werden. Nicht verwaltete private Assemblys, die im Anwendungsverzeichnis installiert sind, werden nicht durch WFP geschützt. Verwaltete globale Assemblys, die im Anwendungsverzeichnis oder% windir% \\ Assembly \\ GAC installiert sind, werden nicht durch WFP geschützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Ressourcenschutz](../wfp/windows-resource-protection-portal.md)
</dt> </dl>

 

 
