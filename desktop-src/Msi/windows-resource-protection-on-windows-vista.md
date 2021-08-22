---
description: Windows Das Installationsprogramm befolgt Windows Resource Protection (WRP), wenn wichtige Systemdateien, Ordner und Registrierungsinformationen in Windows Server 2008 und höher und Windows Vista und höher installiert werden.
ms.assetid: 38865ee1-22ef-430b-99ce-1c6983c3b51f
title: Verwenden von Windows Installer und Windows Resource Protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ed70b502754dcc54c0954d21e6213d815ba0fa98927f5a67680700a4dd802
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012638"
---
# <a name="using-windows-installer-and-windows-resource-protection"></a>Verwenden von Windows Installer und Windows Resource Protection

Windows Das Installationsprogramm befolgt Windows Resource Protection (WRP), wenn wichtige Systemdateien, Ordner und Registrierungsinformationen in Windows Server 2008 und höher und Windows Vista und höher installiert werden.

WRP in Windows Server 2008 und Windows Vista ersetzt Windows File Protection (WFP) in Windows Server 2003, Windows XP und Windows 2000. Windows Entwickler des Installationsprogramms sollten die folgenden Änderungen an der Verarbeitung geschützter Ressourcen in Windows Server 2008 und höher und Windows Vista und höher beachten:

-   Bei Ausführung auf Windows Server 2008 und höher oder Windows Vista und höher überspringt der Windows Installer die Installation einer beliebigen Datei, die durch WRP geschützt ist. Das Installationsprogramm gibt eine Warnung in die Protokolldatei ein und fährt mit dem Rest der Installation ohne Fehler fort. In Windows Server 2003, Windows XP und Windows 2000, wenn der Windows Installer eine WFP-geschützte Datei gefunden hat, fordert das Installationsprogramm an, dass WFP die Datei installiert.
-   WRP auf Windows Server 2008 und höher oder Windows Vista und höher kann Registrierungsschlüssel zusätzlich zu Dateien schützen. Wenn der Windows Installer einen WRP-geschützten Registrierungsschlüssel erkennt, überspringt das Installationsprogramm die Installation dieses Registrierungsschlüssels, das Installationsprogramm gibt eine Warnung in die Protokolldatei ein und fährt mit dem Rest der Installation ohne Fehler fort.
-   Beachten Sie Folgendes: Wenn eine Windows Installer-Komponente eine Datei oder einen Registrierungsschlüssel enthält, die durch WRP geschützt ist, muss diese Ressource als KeyPath für die Komponente verwendet werden. In diesem Fall installiert, aktualisiert oder entfernt Windows Installer die Komponente nicht. Sie sollten keine geschützten Ressourcen in ein Installationspaket einschließen. Stattdessen sollten Sie die [unterstützten Ressourcenersetzungsmechanismen](../wfp/supported-file-replacement-mechanisms.md) für [Windows Resource Protection](../wfp/windows-resource-protection-portal.md)verwenden.

Weitere Informationen zu WRP finden Sie unter [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) und informationen, die auf Microsoft [Technet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))bereitgestellt werden.

## <a name="wfp-for-windows-server-2003-and-windows-xp2000"></a>WFP für Windows Server 2003 und Windows XP/2000

Windows Das Installationsprogramm befolgt Windows File Protection (WFP), wenn wichtige Systemdateien auf Windows Server 2003, Windows XP und Windows 2000 installiert werden. Wenn eine geschützte Systemdatei durch eine unbeaufsichtigte Installation einer Anwendung geändert wird, stellt WFP die Datei in der überprüften Dateiversion wieder her.

Windows Das Installationsprogramm versucht nie, eine geschützte Datei zu installieren oder zu ersetzen. Wenn die [InstallFiles-Aktion](installfiles-action.md) oder eine andere vor InstallFiles geplante Aktion versucht, eine Datei zu installieren, die auf Windows Server 2003, Windows XP oder Windows 2000 geschützt ist, ruft das Installationsprogramm WFP mit einer Anforderung zum Installieren oder Ersetzen der geschützten Datei auf. Das Installationsprogramm fordert die Dateiinstallation von WFP sofort nach dem Ausführen der InstallFiles-Aktion an. WFP installiert oder ersetzt die Datei auf dem System des Benutzers durch eine zwischengespeicherte Version der geschützten Datei. Beachten Sie, dass dies nicht garantiert, dass die Version der aus dem Cache installierten Datei die für die Anwendung erforderliche Version ist. Nachdem WFP die Datei installiert hat, bestimmt das Installationsprogramm, ob diese Version mit der Version im Paket übereinstimmt. Wenn die Dateiversion im Paket größer als die installierte Version ist, informiert das Installationsprogramm den Benutzer, dass es das System nicht aktualisieren kann und dass möglicherweise ein Update des Betriebssystems für die Anwendung erforderlich ist.

Wenn eine Aktion, die nach dem Versuch von [InstallFiles](installfiles-action.md) sequenziert wurde, eine geschützte Datei zu installieren oder zu ersetzen, die nicht bereits auf dem System installiert ist, kann das Installationsprogramm WFP nicht aufrufen, um die Datei zu installieren. In diesem Fall informiert das Installationsprogramm den Benutzer, dass es das System nicht aktualisieren kann und dass möglicherweise ein Update des Betriebssystems für die Anwendung erforderlich ist.

Das Installationsprogramm überprüft auch beim Entfernen von Dateien mit WFP und versucht nie, geschützte Systemdateien zu entfernen.

## <a name="component-key-files-protected-by-wfp"></a>Durch WFP geschützte Komponentenschlüsseldateien

Beachten Sie, dass diese Datei als Schlüsselpfad für die Komponente angegeben werden muss, wenn eine Windows Installer-Komponente eine WFP-Datei enthält.

Wenn das Installationsprogramm versucht, die Schlüsseldatei einer Komponente auf Windows Server 2003, Windows XP oder Windows 2000 zu installieren, ruft es zuerst WFP auf, um zu bestimmen, ob die Schlüsseldatei geschützt ist. Wenn die Schlüsseldatei einer Komponente durch WFP geschützt ist und diese Schlüsseldatei bereits installiert ist, aktualisiert das Installationsprogramm die Komponente nur, wenn die Version der Schlüsseldatei im Paket größer als die installierte Version ist. Wenn das Installationspaket angibt, dass eine Komponente installiert werden soll und die Schlüsseldatei der Komponente derzeit nicht installiert ist, installiert das Installationsprogramm die Komponente unabhängig davon, ob die Schlüsseldatei geschützt ist. Sobald eine Komponente mit einer durch WFP geschützten Schlüsseldatei installiert ist, wird sie dauerhaft installiert, und das Installationsprogramm entfernt oder ersetzt die Komponente nie.

## <a name="installation-of-assemblies-by-wfp"></a>Installation von Assemblys durch WFP

WFP für Assemblys unterscheidet sich von WFP für Systemdateien.

WFP schützt Windows Server 2003, Windows XP- und Windows 2000-Systemdateien, indem versucht wird, geschützte Systemdateien zu ersetzen. Dieser Schutz wird ausgelöst, nachdem WFP eine Verzeichnisänderungsbenachrichtigung für eine Datei in einem geschützten Verzeichnis empfangen hat. Wenn WFP diese Benachrichtigung empfängt, wird ermittelt, welche Datei geändert wurde. Wenn die Datei geschützt ist, sucht WFP die Dateisignatur in einer statischen Katalogdatei, um zu ermitteln, ob die neue Datei die richtige Version ist. Wenn die Dateiversion nicht korrekt ist, ersetzt das System die Datei durch die richtige Version aus dem Cache oder dem Verteilungsmedium.

Im Gegensatz dazu ist WFP von Assemblys dynamisch. WFP wird auf Dateien erweitert, da sie dem freigegebenen nebeneinander verwendeten Assemblycache hinzugefügt werden. Wenn eine Assembly beschädigt wird, fordert WFP an, dass das Installationsprogramm die Datei ersetzt. Windows Das Installationsprogramm kann die Datei möglicherweise ersetzen, je nachdem, ob auf das Quellpaket zugegriffen werden kann. Wenn auf das Quellpaket nicht zugegriffen werden kann, wird von WFP ein Dialogfeld mit dem Hinweis angezeigt, dass die Datei nicht wiederhergestellt werden kann.

Beachten Sie, dass nicht verwaltete freigegebene parallele Assemblys, die in %windir% \\ winsxs installiert sind, durch WFP geschützt sind. Nicht verwaltete private Assemblys, die im Anwendungsverzeichnis installiert sind, werden nicht durch WFP geschützt. Verwaltete globale Assemblys, die im Anwendungsverzeichnis oder %windir% Assembly gac installiert \\ \\ sind, werden nicht durch WFP geschützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Ressourcenschutz](../wfp/windows-resource-protection-portal.md)
</dt> </dl>

 

 
