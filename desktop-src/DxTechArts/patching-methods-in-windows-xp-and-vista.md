---
title: Patchen von Spiel Software in Windows XP, Windows Vista und Windows 7
description: In diesem Artikel werden einige Methoden zum Patchen erläutert, die in Windows Vista und Windows 7 sowie in Windows XP gut funktionieren.
ms.assetid: 27be805a-bffd-a9f8-2207-2a9a4822ba48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ae0b1455cae61b8372f81e6928977743084c9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341532"
---
# <a name="patching-game-software-in-windows-xp-windows-vista-and-windows-7"></a>Patchen von Spiel Software in Windows XP, Windows Vista und Windows 7

Windows Vista und Windows 7 verfügen über eine Reihe von Features, um das Betriebssystem sicherer zu machen. Hinzugefügte Sicherheit bedeutet, dass das Anwenden von Patches auf Software nicht so einfach ist wie in der Vergangenheit. In diesem Artikel werden einige Methoden zum Patchen erläutert, die in Windows Vista und Windows 7 sowie in Windows XP gut funktionieren.

Es gibt zwei Hauptkategorien von spielen, für die Patches erforderlich sind:

-   Spiele, die nur gelegentliche Patches benötigen, z. b. die meisten Offline Spiele.
-   Spiele, die häufig Patches erfordern, z. b. die meisten Online Spiele.

Dieser Artikel bietet auch eine kurze Einführung in die Benutzerkontensteuerung (User Account Control, UAC), die als Hintergrund der Rechte fungiert, die Entwickler in Windows Vista und Windows 7 erwarten können.

-   [Benutzerkontensteuerung](#user-account-control)
-   [Spiele, die nur gelegentliche Patches erfordern](#games-that-require-only-occasional-patches)
    -   [Methode 1: Verwenden von Windows Installer für gelegentliche Patches](#method-1-use-windows-installer-for-occasional-patches)
    -   [Methode 2: Administrator Rechte zum Anwenden von Patches erforderlich](#method-2-require-administrator-rights-to-apply-patches)
-   [Spiele, die häufig Patches erfordern](#games-that-require-frequent-patches)
    -   [Methode 3: Installation pro Benutzer](#method-3-install-per-user)
    -   [Methode 4: Installieren an einem gemeinsamen Per-Computer Speicherort](#method-4-install-to-a-common-per-computer-location)
    -   [Weitere Möglichkeiten](#other-possibilities)
-   [Zusammenfassung](#summary)

## <a name="user-account-control"></a>Benutzerkontensteuerung

Windows Vista und Windows 7 verfügen über zwei primäre Arten von Benutzerkonten: Standard Benutzer und Administrator. Ein Standard Benutzerkonto weist mehrere Zugriffsbeschränkungen auf: Beispielsweise können keine Daten in das Dateisystem in% System Drive%- \\ Programmdateien oder in die Registrierung auf dem lokalen HKEY-Computer geschrieben werden \_ \_ . Dies hat Auswirkungen auf das Anwenden von Patches auf ein Spiel, wenn es an einem schreibgeschützten Speicherort installiert ist. Anders als in Windows XP ist das Standard Benutzerkonto in Windows Vista und Windows 7 viel häufiger. Standard Benutzerkonten sind auch für wichtige Features des Betriebssystems erforderlich, wie z. b. Jugendschutz. Die Jugendschutz Kontrolle erfordert, dass das untergeordnete Konto ein Standard Benutzer ist, und die Erhöhung eines solchen Kontos auf den Administrator für sogar ein Spiel verhindert, dass Eltern Kontrollen mit allen anderen Spielen arbeiten. Daher ist es wichtig, dass Spiele für Standard Benutzer entwickelt werden.

Windows Vista und Windows 7 verfügen über ein neueres Modell für Benutzerrechte, um Benutzer daran zu hindern, Programme auszuführen, die versuchen, Vorgänge auszuführen, die der Benutzer nicht beabsichtigt oder autorisiert. Zu diesem Zweck ermöglicht die Benutzerkontensteuerung (früher als "Benutzerkonto mit den geringsten Rechten" bezeichnet) Benutzern den Betrieb des Computers in der Regel auf niedriger Ebene, während Sie problemlos Anwendungen ausführen können, die Rechte höherer Ebene erfordern, wenn dies erforderlich ist. Dies bedeutet, dass Standardbenutzer Konten und Administrator Konten beide Anwendungen mit Standard Benutzerrechten ausführen, aber nur Administrator Konten können Anwendungen erweiterte Rechte erteilen. Das Betriebssystem fordert Benutzer mit Administrator Konten zur expliziten Zustimmung auf, bevor eine Anwendung mit erhöhten Rechten ausgeführt wird. Wenn ein Programm, das Administrator Rechte erfordert, auf einem Standard Benutzerkonto ausgeführt wird, fordert das System zur Genehmigung des Administrators auf.

## <a name="games-that-require-only-occasional-patches"></a>Spiele, die nur gelegentliche Patches erfordern

Einige Spiele erfordern nur einige Patches während des gesamten Lebenszyklus. Zwei Methoden, die Sie für diese Häufigkeit von Patchen verwenden können, sind die Verteilung von Patches als Windows Installer Pakete, für die in der Regel keine Administrator Rechte erforderlich sind, oder eine andere Art von Verteilung, mit der Spieldateien direkt geändert werden.

> [!Note]  
> Unabhängig davon, ob ein Spiel ein häufiges Patchen erfordert, benötigen Anwendungen in der Regel Administrator Rechte, um installiert oder entfernt zu werden.

 

### <a name="method-1-use-windows-installer-for-occasional-patches"></a>Methode 1: Verwenden von Windows Installer für gelegentliche Patches

Bei dieser Methode wird ein Windows Installer zum Installieren eines Pakets (MSI-Datei) verwendet, und ein Windows Installer Patch (MSP-Datei) wird zur Installation von Patches verteilt. Das Paket muss über eine MsiPatchCertificate-Tabelle verfügen, und der Patch muss von einem Zertifikat in der Tabelle digital signiert werden. Weitere Informationen zu digitalen Signaturen finden Sie unter [Authenticode-Signierung für Spieleentwickler](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

Weitere Details und Anforderungen zur Verwendung dieser patchmethode finden Sie in der Windows Installer-Dokumentation:

-   [Patchen und Upgrades](/windows/desktop/Msi/patching-and-upgrades)
-   [Patching der Benutzerkontensteuerung (User Account Control, UAC)](/windows/desktop/Msi/user-account-control--uac--patching)

Der Nachteil dieser Methode besteht darin, dass das Patchen Administrator Rechte erfordert, wenn das Spiel nicht von einem Wechselmedium unter Windows XP installiert wurde. Dies ist jedoch wahrscheinlich nicht zu restriktiv, da die meisten Benutzer Administratoren unter Windows XP und die Beschränkung auf Software, die von Wechselmedien installiert wird, nicht unter Windows Vista vorhanden ist.

Der Hauptvorteil dieser Methode besteht darin, dass Patches von einem Standard Benutzerkonto angewendet werden können, ohne dass eine Aufforderung und eine Authentifizierung für erhöhte Rechte erforderlich sind. Dies sorgt für eine bessere Benutzer Leistung, da ein Benutzer mit einem Standard Benutzerkonto nicht jemand mit einem Administrator Konto bitten muss, den Patch zu installieren oder dem Standardbenutzer Konto permanente Administrator Rechte bereitzustellen.

Es ist möglich, dass diese Methode für Spiele funktioniert, die häufig Patches erfordern, aber der Aufwand für die Verwendung von Windows Installer Paketen in Bezug auf die Buildintegration und die Unterstützung einer großen Anzahl von Dateien kann dazu führen, dass diese Methode weniger erwünscht ist als andere.

### <a name="method-2-require-administrator-rights-to-apply-patches"></a>Methode 2: Administrator Rechte zum Anwenden von Patches erforderlich

Bei dieser Methode erfordert die ausführbare Datei, die den Patch anwendet, Administrator Rechte zum Ausführen von. Mit Administrator Rechten kann die ausführbare Datei für das Patchen die Spieldateien, die sich in% System Drive% Program Files befinden, direkt ändern \\ .

Der Vorteil dieser Methode ist die Einfachheit. Diese Methode ist jedoch ungeeignet, wenn das Spiel häufig Patches benötigt, denn wenn ein Benutzer mit einem Standard Benutzerkonto ein Spiel spielen möchte, das häufig Patches erfordert, wie etwa ein Massively Multi-Player-Onlinespiel, bietet dieser Benutzer zwei Möglichkeiten:

-   Holen Sie sich einen Administrator zum Anmelden und Patchen des Spiels, was für beide Parteien unpraktisch sein kann.
-   Lassen Sie sein Konto dauerhaft mit Administrator Rechten herauf.

> [!Note]  
> Die zweite Lösung schwächt nicht nur die Sicherheit des Systems als Ganzes, sondern verhindert, dass wichtige Features, wie z. b. Jugend Kontrollen, funktionieren.

 

Beim Implementieren dieser Methode muss sich die ausführbare Datei, die den Patch anwendet, von der ausführbaren Spieldatei unterscheiden. Das Manifest der ausführbaren Datei für das Patchen sollte für requestedExecutionLevel den Wert requisionministrator angeben, um ihn als Anwendung anzugeben, für die Administrator Rechte erforderlich sind. Weitere Informationen hierzu finden Sie unter [bewährte Methoden für Entwickler und Richtlinien für Anwendungen in einer Umgebung mit geringsten](/previous-versions/dotnet/articles/aa480150(v=msdn.10))Berechtigungen im "Schema des Anwendungs Manifests".

Wenn diese Methode verwendet wird, auch mit den Einstellungen im Manifest, kann die ausführbare Datei in zwei Fällen weiterhin ohne Administrator Rechte gestartet werden:

-   Wenn das Betriebssystem Windows XP ist und das Benutzerkonto ein eingeschränkter Benutzer ist.
-   Wenn das Betriebssystem Windows Vista oder Windows 7 ist, ist das Benutzerkonto ein Standard Benutzer, und UAC ist deaktiviert.

Beides sind seltene Consumerszenarien. Der Patcher sollte jedoch über das Manifest verfügen, das Administrator Rechte erfordert, und es sollte [**isuseranadmin**](/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin); aufgerufen werden. Wenn diese Funktion false zurückgibt, wird die Fehlermeldung "Administrator Rechte sind erforderlich" angezeigt.

Insgesamt ist Methode 1 für Spiele vorzuziehen, die in ihrer Lebensdauer nur wenige Patches benötigen.

## <a name="games-that-require-frequent-patches"></a>Spiele, die häufig Patches erfordern

Viele Internet basierte Spiele werden ständig verbessert und erfordern normalerweise reguläre Patches. Für diese Spiele können Patches pro Benutzer oder pro Computer angewendet werden, wie in den folgenden Themen erläutert. Weitere mögliche Lösungen sind das Ändern der ACL, die% System Drive%- \\ Programmdateien schützt, oder das Erstellen eines benutzerdefinierten Dienstanbieter.

### <a name="method-3-install-per-user"></a>Methode 3: Installieren von Per-User

Ein empfohlener und einfacher Ansatz besteht darin, das gesamte Spiel in einem benutzerspezifischen Unterordner des Ordners "lokale Anwendungsdaten" zu installieren, den Sie durch Aufrufen von " [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) " mit lokalen CSIDL- \_ \_ AppData finden können. Ein Beispiel Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ lokale Einstellungen \\ Anwendungsdaten \\ examplegname. Ein solcher Speicherort ermöglicht es einer Anwendung, die mit Standard Benutzerrechten ausgeführt wird, Spieldateien direkt zu ändern.

Bei diesem Ansatz gibt es jedoch einen Nachteil, wenn ein Computer mehrere Benutzer hat: für jeden Benutzer ist eine Kopie des Spiels installiert, und Patches müssen heruntergeladen und von jedem Benutzer angewendet werden. Dadurch wird nicht nur die Zeit und der Speicherplatz des Benutzers verschwendet, sondern auch die Netzwerkbandbreite auf den Server erhöht, der Patches bereitstellt. Da alle Anwendungen mit Standardbenutzer rechten das Spiel ändern können, sind die ausführbaren Spieldateien weniger geschützt. Es ist für den Spiel Hersteller zu entscheiden, ob dies akzeptabel ist oder nicht.

### <a name="method-4-install-to-a-common-per-computer-location"></a>Methode 4: Installieren an einem gemeinsamen Per-Computer Speicherort

Eine andere Methode besteht darin, die nicht ausführbaren Spieldaten in einem Unterverzeichnis des Pfads zu installieren, der durch [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) CSIDL \_ Common \_ AppData angegeben wird. ein Beispiel Pfad ist C: \\ Dokumente und Einstellungen \\ alle Benutzer \\ Anwendungsdaten \\ examplegname. Dabei handelt es sich um einen freigegebenen Speicherort für alle Benutzer, der von Anwendungen geändert werden kann, die mit Standard Benutzerrechten ausgeführt werden. Diese Methode minimiert die Notwendigkeit, große Patches erneut anzuwenden, wenn das Spiel von mehr als einem Konto wiedergegeben wird. Ausführbare Dateien für das Spiel sollten in% System Drive% Programme aufbewahrt werden \\ , um das Risiko für andere Konten auf dem System zu minimieren. Die ausführbaren Dateien sollten die Integrität des neuen Inhalts im freigegebenen Verzeichnis überprüfen, da der Speicherort von einem Programm oder einer Person mit Standard Benutzerrechten geändert werden kann. Verwenden Sie " [**mapfileandchecksum**](/windows/desktop/api/imagehlp/nf-imagehlp-mapfileandchecksuma) ", um eine Prüfsumme der Dateien zu berechnen.

Diese Methode hat den Vorteil, dass Sie sowohl unter Windows XP als auch unter Windows Vista gleichermaßen gut funktioniert und keine Administrator Rechte erfordert.

### <a name="other-possibilities"></a>Weitere Möglichkeiten

Außerhalb der bereits erörterten Methoden besteht eine weitere Möglichkeit darin, die ACL des% System Drive% \\ Program Files- \\ Spiel Ordners zu ändern, \\ Wenn das Spiel installiert wird, sodass ein Tool zum Patchen direkt in die Spieldateien schreiben kann, auch wenn es mit Standard Benutzerrechten ausgeführt wird. Obwohl dies nicht schwierig ist, wird der Sicherheitsschutz umgangen, den das System für die Dateien des Spiels bietet, und es ist möglich, dass böswillige Programme den Inhalt des Verzeichnisses ändern können. Dies ist nicht empfehlenswert, und es wird dringend empfohlen, stattdessen eine Alternative zu verwenden.

Eine letzte Möglichkeit besteht darin, einen benutzerdefinierten Dienst zu schreiben. Im Allgemeinen ist das Schreiben eines benutzerdefinierten Dienstanbieter in patchspiele keine gute Idee, da dies kompliziert und fehleranfällig ist. Es wird empfohlen, das Patchen mithilfe anderer Methoden durchführen, die in diesem Artikel erläutert werden. Es ist jedoch möglich, dass ein benutzerdefinierter Dienst erforderlich ist, wenn er mit Anticheat-oder Anti-Piraterie-Lösungen kombiniert wird. Ein solcher Dienst sollte eine große Anzahl von Spielen unterstützen und so entworfen werden, dass er nur die Patchdateien herunterladen und nur in das Installationsverzeichnis für das zielspiel schreiben kann. Es ist wichtig, dass der Dienst klein ist, einen minimalen Oberflächen Bereich hat, der anfällig für Angriffe ist, und so wenig Systemressourcen wie möglich verwenden, wenn das Spiel nicht ausgeführt wird.

## <a name="summary"></a>Zusammenfassung

Letztendlich müssen Sie entscheiden, welche Methode implementiert werden soll. Sie müssen die Faktoren abwägen, die für Sie wichtig sind. Die Sicherheit, die Häufigkeit des Patchens, die Benutzerfreundlichkeit durch den Kunden, die für die Implementierung erforderliche Arbeitsauslastung, die Komplexität der Lösung und die Kompatibilität von Platt Form Features sind die Faktoren, die jeder Entwickler berücksichtigen muss, bevor er sich für eine bestimmte Methode entscheidet.

Weitere Informationen zum Schutz von Benutzerkonten finden Sie unter [Windows Vista Anwendungs Entwicklungsanforderungen für die Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905330(v=msdn.10)).

 

 