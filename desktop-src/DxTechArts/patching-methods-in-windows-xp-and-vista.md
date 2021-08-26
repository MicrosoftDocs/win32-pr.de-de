---
title: Patchen von Spielsoftware in Windows XP, Windows Vista und Windows 7
description: In diesem Artikel werden einige Methoden zum Patchen untersucht, die in Windows Vista und Windows 7 sowie in Windows XP gut funktionieren.
ms.assetid: 27be805a-bffd-a9f8-2207-2a9a4822ba48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dae9b3bc91c96006f3b2117093962ee485db948fd983191f2db3c7f88fb33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042500"
---
# <a name="patching-game-software-in-windows-xp-windows-vista-and-windows-7"></a>Patchen von Spielsoftware in Windows XP, Windows Vista und Windows 7

Windows Vista und Windows 7 verfügen über eine Reihe von Features, um das Betriebssystem sicherer zu machen. Zusätzliche Sicherheit bedeutet, dass das Anwenden von Patches auf Software nicht so einfach ist wie in der Vergangenheit. In diesem Artikel werden einige Methoden zum Patchen untersucht, die in Windows Vista und Windows 7 sowie in Windows XP gut funktionieren.

Es gibt zwei Hauptkategorien von Spielen, die Patches erfordern:

-   Spiele, die nur gelegentliche Patches erfordern, z. B. die meisten Offline-Spiele.
-   Spiele, die häufig Patches erfordern, z. B. die meisten Onlinespiel.

Dieser Artikel bietet auch eine kurze Einführung in die Benutzerkontensteuerung (User Account Control, UAC), um Hintergrundinformationen zu den Rechten zu erhalten, die Entwickler von Benutzern in Windows Vista und Windows 7 erwarten können.

-   [Benutzerkontensteuerung](#user-account-control)
-   [Spiele, die nur gelegentliche Patches erfordern](#games-that-require-only-occasional-patches)
    -   [Methode 1: Verwenden des Windows Installers für gelegentliche Patches](#method-1-use-windows-installer-for-occasional-patches)
    -   [Methode 2: Administratorrechte zum Anwenden von Patches erforderlich](#method-2-require-administrator-rights-to-apply-patches)
-   [Spiele, die häufige Patches erfordern](#games-that-require-frequent-patches)
    -   [Methode 3: Pro Benutzer installieren](#method-3-install-per-user)
    -   [Methode 4: Installieren an einem allgemeinen Per-Computer Speicherort](#method-4-install-to-a-common-per-computer-location)
    -   [Weitere Möglichkeiten](#other-possibilities)
-   [Zusammenfassung](#summary)

## <a name="user-account-control"></a>Benutzerkontensteuerung

Windows Vista und Windows 7 verfügen über zwei Haupttypen von Benutzerkonten: Standardbenutzer und Administrator. Für ein Standardbenutzerkonto gelten mehrere Zugriffseinschränkungen. Beispielsweise können keine Daten in das Dateisystem in %SystemDrive%-Programmdateien oder in die Registrierung \\ auf dem HKEY \_ LOCAL MACHINE geschrieben \_ werden. Dies hat Auswirkungen auf die Anwendung von Patches auf ein Spiel, wenn es an einem schreibgeschützten Speicherort installiert ist. Im Gegensatz zu Windows XP ist das Standardbenutzerkonto in Windows Vista und Windows 7 viel häufiger. Standardbenutzerkonten sind auch für wichtige Features des Betriebssystems erforderlich, z. B. für Die Jugendschutzkontrollen. Die Jugendschutzkontrollen erfordern, dass das untergeordnete Konto Standardbenutzer ist, und die Erhöhung eines solchen Kontos auf den Administrator für ein Spiel verhindert, dass die Jugendkontrollen mit allen anderen Spielen arbeiten. Daher ist es wichtig, dass Spiele für Standardbenutzer entworfen werden.

Windows Vista und Windows 7 verfügen über ein neueres Modell für Benutzerrechte, um zu verhindern, dass Benutzer Programme ausführen, die versuchen, Vorgänge durchzuführen, die der Benutzer nicht beabsichtigt oder autorisiert. Zu diesem Zweck ermöglicht die Benutzerkontensteuerung (ehemals Benutzerkonto mit den geringsten Berechtigungen oder LUA) Benutzern, den Computer in den meisten Jahren mit geringen Rechten zu betreiben, während anwendungen, die bei Bedarf höhere Rechte erfordern, problemlos ausgeführt werden können. Dies bedeutet, dass Sowohl Standardbenutzerkonten als auch Administratorkonten Anwendungen mit Standardbenutzerrechten ausführen, aber nur Administratorkonten haben die Möglichkeit, Anwendungen erhöhte Rechte zu gewähren. Das Betriebssystem fordert Benutzer mit Administratorkonten zur expliziten Zustimmung auf, bevor eine Anwendung mit erhöhten Rechten ausgeführt wird. Wenn ein Programm, das Administratorrechte erfordert, für ein Standardbenutzerkonto ausgeführt wird, fordert das System zur Genehmigung durch den Administrator auf.

## <a name="games-that-require-only-occasional-patches"></a>Spiele, die nur gelegentliche Patches erfordern

Für einige Spiele sind während ihres gesamten Lebenszyklus nur einige Patches erforderlich. Zwei Methoden, die Sie für diese Patchhäufigkeit verwenden können, sind die Verteilung von Patches als Windows Installer-Pakete, die im Allgemeinen keine Administratorrechte erfordern, oder die Verwendung einer anderen Art von Verteilung, die Spieldateien direkt ändert.

> [!Note]  
> Unabhängig davon, ob ein Spiel häufiges Patchen erfordert, erfordern Anwendungen in der Regel Administratorrechte, um installiert oder entfernt zu werden.

 

### <a name="method-1-use-windows-installer-for-occasional-patches"></a>Methode 1: Verwenden des Windows Installers für gelegentliche Patches

Bei dieser Methode wird ein Windows Installer verwendet, um ein Paket (.msi-Datei) zu installieren, und ein Windows Installer-Patch (MSP-Datei) wird verteilt, um Patches zu installieren. Das Paket muss über eine MsiPatchCertificate-Tabelle verfügen, und der Patch muss von einem Zertifikat in der Tabelle digital signiert werden. Weitere Informationen zum digitalen Signieren finden Sie unter [Authenticode Signing for Game Developers](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

Weitere Informationen und Anforderungen zur Verwendung dieser Patchmethode finden Sie in der Dokumentation Windows Installer:

-   [Patchen und Upgrades](/windows/desktop/Msi/patching-and-upgrades)
-   [Patchen der Benutzerkontensteuerung (User Account Control, UAC)](/windows/desktop/Msi/user-account-control--uac--patching)

Der Nachteil dieser Methode ist, dass das Patchen Administratorrechte erfordert, wenn das Spiel nicht von wechselbaren Medien auf Windows XP installiert wurde. Dies ist jedoch wahrscheinlich nicht zu restriktiv, da die meisten Benutzeradministratoren auf Windows XP und die Einschränkung auf Software, die von Wechselmedien installiert wird, auf Windows Vista nicht vorhanden sind.

Der Hauptvorteil dieser Methode ist, dass Patches von einem Standardbenutzerkonto angewendet werden können, ohne dass eine Aufforderung und Authentifizierung für erhöhte Rechte erforderlich ist. Dies bietet eine bessere Benutzererfahrung, da ein Benutzer mit einem Standardbenutzerkonto zum Spielen eines Spiels keinen Benutzer mit einem Administratorkonto bitten muss, den Patch zu installieren oder dem Standardbenutzerkonto dauerhafte Administratorrechte zu geben.

Es ist möglich, dass diese Methode für Spiele funktioniert, die häufig Patches erfordern, aber der Mehraufwand der Verwendung von Windows Installer-Paketen in Bezug auf die Buildintegration und die Unterstützung einer großen Anzahl von Dateien kann diese Methode weniger wünschenswert machen als andere.

### <a name="method-2-require-administrator-rights-to-apply-patches"></a>Methode 2: Administratorrechte zum Anwenden von Patches erforderlich

Bei dieser Methode benötigt die ausführbare Datei, die den Patch angewendet, Administratorrechte, um ausgeführt zu werden. Mit Administratorrechten kann die ausführbare Patchdatei die Spieldateien direkt ändern, die sich in %SystemDrive% \\ Program Files befinden.

Der Vorteil dieser Methode ist ihre Einfachheit. Diese Methode ist jedoch nicht geeignet, wenn das Spiel häufig Patches benötigt, denn wenn ein Benutzer mit einem Standardbenutzerkonto ein Spiel spielen möchte, das häufig Patches erfordert, wie etwa ein massives Onlinespiel mit mehreren Spielen, hat dieser Benutzer zwei Möglichkeiten:

-   Wenden Sie sich an einen Administrator, um sich zu anmelden und das Spiel zu patchen. Dies kann für beide Parteien unerquent sein.
-   Er muss sein Konto dauerhaft mit Administratorrechten erhöhen.

> [!Note]  
> Die zweite Lösung schwächt nicht nur die Sicherheit des Systems als Ganzes, sondern verhindert auch, dass wichtige Features wie Jugendkontrollen funktionieren.

 

Bei der Implementierung dieser Methode muss sich die ausführbare Datei, die den Patch angewendet, von der ausführbaren Datei des Spiels unterscheiden. Das Manifest der ausführbaren Patchdatei sollte requireAdministrator für requestedExecutionLevel angeben, um sie als Anwendung anzugeben, die Administratorrechte erfordert. Weitere Informationen dazu finden Sie unter Bewährte Methoden und Richtlinien für Entwickler für Anwendungen [in](/previous-versions/dotnet/articles/aa480150(v=msdn.10))einer Umgebung mit geringsten Berechtigungen unter "Anwendungsmanifestschema".

Wenn diese Methode verwendet wird, kann die ausführbare Datei auch mit den Einstellungen im Manifest in zwei Fällen ohne Administratorrechte gestartet werden:

-   Wenn das Betriebssystem auf XP Windows, und das Konto des Benutzers ein eingeschränkter Benutzer ist.
-   Wenn das Betriebssystem Windows Vista oder Windows 7 ist, ist das Benutzerkonto ein Standardbenutzer, und UAC ist deaktiviert.

Beides sind seltene Consumerszenarien. Der Patcher sollte jedoch über das Manifest verfügen, das Administratorrechte erfordert, und [**isUserAnAdmin aufrufen.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin) Wenn diese Funktion FALSE zurückgibt, wird die Fehlermeldung "Administratorrechte sind erforderlich" angezeigt.

Insgesamt ist Methode 1 für Spiele vorzuziehen, die über ihre Lebensdauer nur wenige Patches benötigen.

## <a name="games-that-require-frequent-patches"></a>Spiele, die häufige Patches erfordern

Viele internetbasierte Spiele werden kontinuierlich verbessert und erfordern in der Regel regelmäßige Patches. Für diese Spiele können Patches pro Benutzer oder pro Computer angewendet werden, wie in den folgenden Themen erläutert. Andere mögliche Lösungen sind das Ändern der ACL, die %SystemDrive%-Programmdateien schützt, oder \\ das Erstellen eines benutzerdefinierten Diensts.

### <a name="method-3-install-per-user"></a>Methode 3: Installieren Per-User

Ein empfohlener und einfacher Ansatz ist die Installation des gesamten Spiels in einem Unterordner pro Benutzer des lokalen Anwendungsdatenordners, den Sie finden, indem Sie [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit CSIDL \_ LOCAL \_ APPDATA aufrufen. Ein Beispielpfad ist C: \\ Dokumente und Einstellungen Benutzername Local Einstellungen Application Data \\ \\ \\ \\ ExampleGame. Ein solcher Speicherort ermöglicht einer Anwendung, die mit Standardbenutzerrechten ausgeführt wird, spieldateien direkt zu ändern.

Dieser Ansatz hat jedoch einen Nachteil, wenn ein Computer über mehrere Benutzer verfügt: Jeder Benutzer hat eine Kopie des Spiels installiert, und Patches müssen von jedem Benutzer heruntergeladen und angewendet werden. Dies verschwendet nicht nur Zeit und Speicherplatz auf dem Datenträger der Benutzer, sondern erhöht auch die Nutzung der Netzwerkbandbreite für den Server, der Patches zur Verfügung stellt. Da jede Anwendung mit Standardbenutzerrechten das Spiel ändern kann, sind ausführbare Spieldateien außerdem weniger geschützt. Der Spielhersteller muss entscheiden, ob dies akzeptabel ist.

### <a name="method-4-install-to-a-common-per-computer-location"></a>Methode 4: Installieren an einem allgemeinen Per-Computer Speicherort

Eine weitere Methode besteht in der Installation der nicht ausführbaren Spieldaten in einem Unterverzeichnis des pfads, der von [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) CSIDL COMMON APPDATA angegeben wird. Ein Beispielpfad ist C: Dokumente und Einstellungen Anwendungsdaten für alle Benutzer \_ \_ \\ \\ \\ \\ ExampleGame. Dies ist ein freigegebener Speicherort für alle Benutzer und kann von Anwendungen geändert werden, die mit Standardbenutzerrechten ausgeführt werden. Diese Methode minimiert die Notwendigkeit, große Patches erneut zu installieren, wenn das Spiel von mehr als einem Konto ausgespielt wird. Ausführbare Dateien für das Spiel sollten in %SystemDrive%-Programmdateien gespeichert werden, um das Risiko für andere Konten im \\ System zu minimieren. Die ausführbaren Dateien sollten die Integrität des neuen Inhalts im freigegebenen Verzeichnis überprüfen, da dieser Speicherort von einem Programm oder einer Person mit Standardbenutzerrechten geändert werden kann. Ziehen Sie [**die Verwendung von MapFileAndCheckSum in**](/windows/desktop/api/imagehlp/nf-imagehlp-mapfileandchecksuma) Betracht, um eine Prüfsumme der Dateien zu berechnen.

Diese Methode hat den Vorteil, dass sie sowohl auf Windows XP als auch Windows Vista gleichermaßen gut funktioniert und keine Administratorrechte erfordert.

### <a name="other-possibilities"></a>Weitere Möglichkeiten

Außerhalb der bereits erläuterten Methoden besteht eine weitere Möglichkeit in der Änderung der ACL von %SystemDrive% Program Files Game Folder bei der Installation des Spiels, sodass ein Patchtool direkt in die Dateien des Spiels schreiben kann, auch wenn es mit Standardbenutzerrechten ausgeführt \\ \\ \\ wird. Dies ist zwar nicht schwierig, umgeht jedoch den Sicherheitsschutz, den das System für die Dateien des Spiels bietet, und bietet böswilligen Programmen die Möglichkeit, den Inhalt des Verzeichnisses zu ändern. Dies ist nicht empfehlenswert, und es wird dringend empfohlen, stattdessen eine Alternative zu verwenden.

Eine letzte Möglichkeit besteht im Schreiben eines benutzerdefinierten Diensts. Im Allgemeinen ist das Schreiben eines benutzerdefinierten Diensts zum Patchen von Spielen keine gute Idee, da dies kompliziert und fehleranfällig ist. Es wird empfohlen, das Patchen mithilfe anderer Methoden zu erfolgen, die in diesem Artikel erläutert werden. Ein benutzerdefinierter Dienst kann jedoch erforderlich sein, wenn er mit Anti-Cheat- oder Anti-Cheat-Lösungen kombiniert wird. Ein solcher Dienst sollte eine große Anzahl von Spielen unterstützen und so entworfen werden, dass er nur die Patchdateien herunterladen und nur in das Installationsverzeichnis für das Zielspiel schreiben kann. Es ist wichtig, dass der Dienst klein ist, eine minimale Oberfläche hat, die anfällig für Angriffe ist, und so wenig Systemressourcen wie möglich verwendet, wenn das Spiel nicht ausgeführt wird.

## <a name="summary"></a>Zusammenfassung

Letztendlich liegt es an Ihnen, zu entscheiden, welche Methode implementiert werden soll. Sie müssen die Faktoren abwägen, die für Sie wichtig sind. Sicherheit, Patchhäufigkeit, Benutzerfreundlichkeit, erforderliche Workload, Komplexität der Lösung und Konformität von Plattformfeatures sind die Faktoren, die jeder Entwickler berücksichtigen muss, bevor er sich für eine bestimmte Methode entscheidet.

Weitere Informationen zum Schutz von Benutzerkonten finden Sie unter [Windows Vista Application Development Requirements for User Account Control (UAC).](/previous-versions/aa905330(v=msdn.10))

 

 