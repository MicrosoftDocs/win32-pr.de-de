---
title: Windows Installer für Spieleentwickler
description: Dieser Artikel bietet eine Übersicht über Windows Installer, der speziell für Spieleentwickler gilt. Eine ausführliche Dokumentation zu den in diesem Artikel erwähnten Features und APIs finden Sie im Windows Platform SDK.
ms.assetid: 07401792-b34b-71c9-18f8-a11c916c7d81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc587725ce2a2a675c9db835fabb503bc44ffa62c07ee1ce80578aef9432cf9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290390"
---
# <a name="windows-installer-for-game-developers"></a>Windows Installer für Spieleentwickler

Zeigt, wie Windows Installer verwendet werden kann, um Spiele auf Endbenutzercomputern zu installieren. Windows Das Installationsprogramm bietet vollständige Unterstützung für eine benutzerdefinierte Benutzeroberfläche sowie für Patches.

Microsoft Windows Installer ist die bevorzugte API zum Installieren von Software auf Windows-basierten Computern. Während viele der Features von Windows Installer die Bereitstellung von Geschäftsanwendungen in einer Unternehmensumgebung unterstützen, ist Windows Installer auch vollständig für die Installation von Spielen auf Endbenutzercomputern geeignet. Die Verwendung von Windows Installer für die Spieleinstallation bietet vor allem folgende Vorteile:

-   Zuverlässige Deinstallation
-   Möglichkeit zum Installieren von Inhalten bei Bedarf
-   Unterstützung für vollständig benutzerdefinierte Benutzeroberfläche
-   Effizientes Patchen

Dieser Artikel bietet eine Übersicht über Windows Installer, der speziell für Spieleentwickler gilt. Eine ausführliche Dokumentation zu den in diesem Artikel erwähnten Features und APIs finden Sie im Windows Platform SDK.

-   [Übersicht](#overview)
-   [Wichtige Konzepte Windows Installers](#key-windows-installer-concepts)
    -   [Komponenten](#components)
    -   [Funktionen](#features)
-   [Installationszustände](#install-states)
-   [Bei Bedarf installieren](#install-on-demand)
-   [Benutzerdefinierte Benutzeroberfläche](#custom-user-interface)
-   [Patching](#patching)
-   [Andere Ressourcen](#other-resources)

## <a name="overview"></a>Übersicht

Alle auf dem Installationsprogramm basierenden Setups Windows verwenden eine Installationsdatenbankdatei namens MSI-Datei, um zu beschreiben, wie die Anwendung installiert werden soll. Die MSI-Datei enthält Informationen dazu, welche Dateien, Registrierungsschlüssel, Desktopverknüpfungen, Dateizuordnungen und andere Anwendungselemente installiert werden sollen. Die tatsächlich zu installierenden Dateien können in der MSI-Datei selbst komprimiert, gebündelt und in separaten "Cabfiles" komprimiert oder als einzelne nicht komprimierte Dateien an anderer Stelle auf dem Installationsmedium gespeichert werden. Die MSI-Datei kann auch auf extern implementierte benutzerdefinierte Aktionen verweisen, um Aktionen zuzulassen, die die MSI-Datei nicht nativ zulässt.

Eine MSI-Datei kann optional eine Benutzeroberfläche enthalten, die den Benutzer durch den Installationsvorgang führt. Diese Benutzeroberfläche ist für die meisten Anwendungen geeignet. Es hat jedoch das Aussehen und Gefühl einer regulären Windows Anwendung, und viele Spieleentwickler bevorzugen es, dass ihre Setupanwendung das Aussehen und Das gefühlt des Spiels selbst beibehält, um eine konsistentere Endbenutzererfahrung zu bieten. Zur Unterstützung dieses vollständig benutzerdefinierten Benutzeroberflächenszenarios kann eine Setupanwendung Windows integrierte Benutzeroberfläche des Installers deaktivieren und die gesamte Benutzeroberfläche selbst verarbeiten. Die Windows Installer-API macht einen Rückrufmechanismus verfügbar, mit dem eine benutzerdefinierte Setupbenutzeroberfläche über den Fortschritt der Installation sowie wichtige Ereignisse wie Datenträgeränderungsanforderungen benachrichtigt werden kann.

Windows Das Installationsprogramm ist keine End-to-End-Lösung zum Erstellen von Setups. Es handelt sich nur um eine API, die von einem Setupprogramm für die eigentliche Installation von Dateien, Registrierungsschlüsseln, Desktopverknüpfungen und anderen Elementen der Anwendung verwendet werden kann. Aktuelle Versionen aller wichtigen kommerziellen Setuptools (z. B. InstallShield, WISE und Microsoft Visual Studio) unterstützen Windows Installer. Diese Tools bieten praktische Benutzeroberflächen zum Erstellen des Setups für ein Spiel, aber sie nutzen die Windows Installer-API, um einen Großteil der eigentlichen Installation zu erledigen. Diese Tools können auch nur verwendet werden, um eine MSI-Datenbank mit dem Setuppaket zu erstellen, die dann über eine benutzerdefinierte Setupbenutzeroberfläche installiert werden kann. Als Alternative zu Drittanbietertools bietet die Windows Installer-API alle Funktionen, die zum programmgesteuerten Erstellen und Bearbeiten einer MSI-Datenbank erforderlich sind, und das Windows Platform SDK enthält ein reines MSI-Datenbankbearbeitungstool namens Orca.

## <a name="key-windows-installer-concepts"></a>Wichtige Konzepte Windows Installers

Hier sind die Komponenten und Features des Windows Installers.

### <a name="components"></a>Komponenten

Eine Anwendung besteht aus einer oder mehreren Komponenten, die durch eine GUID-Komponenten-ID identifiziert werden. Eine Komponente ist eine atomare Einheit. Sie ist entweder vollständig oder überhaupt nicht installiert. Eine Komponente kann aus einer einzelnen Datei, mehreren Dateien, Registrierungsschlüsseln, Desktopverknüpfungen oder einer Kombination davon bestehen. Die Ressourcen (Dateien usw.) innerhalb einer Komponente müssen für diese Komponente eindeutig sein– keine zwei Komponenten können dieselbe Ressource enthalten. Eine Komponente wird nie explizit installiert. Sie wird nur als Teil eines Features installiert (siehe unten).

### <a name="features"></a>Features

Ein Feature ist eine Gruppe von Komponenten, die durch eine GUID-Feature-ID identifiziert wird. Im Gegensatz zu Komponenten können mehrere Features dieselbe Komponente enthalten. Eine Komponente, die von mehreren Features gemeinsam genutzt wird, wird installiert, wenn eines dieser Features installiert ist, und wird nur entfernt, wenn alle Features, die auf die Komponente verweisen, deinstalliert wurden. Die Installation eines Features kann automatisch als Teil der Installation eines Produkts oder manuell mithilfe der [**MsiConfigureFeature-API**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) erfolgen.

Obwohl nur wenige Spiele über mehrere "Features" verfügen, die unabhängig voneinander installiert werden können, ist das Windows Installer-Konzept eines Features weiterhin nützlich. Da ein Windows Installer-Feature nur eine Sammlung von Komponenten ist, die zusammen installiert werden können, können Spiele Features verwenden, um den gesamten Inhalt zu gruppieren, der für eine bestimmte Phase des Spiels benötigt wird. Beispielsweise könnte ein ebenenorientiertes Spiel ein Feature pro Ebene definieren, das aus dem gesamten Für diese Ebene erforderlichen Inhalt besteht. Dies würde es dem Spiel ermöglichen, den Inhalt innerhalb des Spiels selbst auf einer Ebene zu installieren, anstatt den gesamten Inhalt für alle Ebenen während der Erstinstallation zu installieren.

## <a name="install-states"></a>Installationszustände

Jede Komponente oder Funktion verfügt über einen zugeordneten Installationsstatus, der bestimmt, ob die Komponente oder das Feature verfügbar ist, und wenn ja, wo die Dateien für die Komponente oder das Feature installiert sind. Die möglichen Installationszustände für ein Feature sind:

<dl> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>Abwesend
</dt> <dd>

Das Feature ist nicht installiert und daher nicht zugänglich.

</dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>lokal
</dt> <dd>

Das Feature ist verfügbar und für die Ausführung auf der lokalen Festplatte installiert.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Quelle
</dt> <dd>

Das Feature ist verfügbar und wird installiert, um von den ursprünglichen Quellmedien (in der Regel eine CD oder DVD) ausgeführt zu werden.

</dd> <dt>

<span id="Advertised"></span><span id="advertised"></span><span id="ADVERTISED"></span>Angekündigt
</dt> <dd>

Das Feature ist nicht installiert, kann aber bei Bedarf mithilfe der [**MsiConfigureFeature-API**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) installiert werden. Wenn das Feature tatsächlich installiert ist, kann es entweder im Lokalen Zustand oder im Quellzustand installiert werden.

</dd> </dl>

Eine Komponente kann einen der oben genannten Zustände aufweisen, mit Ausnahme von "Advertised". Wenn eine Komponente Teil eines angekündigten Features ist, wird die Komponente als "Absent" angezeigt, bis das Feature installiert ist.

## <a name="install-on-demand"></a>Bei Bedarf installieren

Windows Das Installationsprogramm ermöglicht es einer Anwendung, Features als Angekündigt zu markieren. Dies bedeutet, dass das Feature noch nicht installiert ist, aber bei Bedarf zur Laufzeit installiert werden kann. Das Installieren von Features zur Laufzeit wird als "Bei Bedarf installieren" bezeichnet. Spiele können "Install on Demand" verwenden, um den Zeitaufwand für die anfängliche Spieleinrichtung drastisch zu reduzieren, indem die Installation von Spielinhalten so lange zurückgehalten wird, bis sie zur Laufzeit benötigt wird. Die Verzögerung, die für die Installation des Inhalts zur Laufzeit erforderlich ist, kann häufig teilweise oder vollständig ausgeblendet werden, indem die bedarfsorientierte Installation in einem Hintergrundthread erfolgt, während der Benutzer andernfalls mit dem Spiel beschäftigt ist.

## <a name="custom-user-interface"></a>Benutzerdefinierte Benutzeroberfläche

Obwohl Windows Installer eine Standardbenutzeroberfläche bereitstellt, die den Benutzer durch die Installation der Anwendung führt, sieht diese Schnittstelle wie eine Standard-Windows-Anwendung aus. Viele Spieleentwickler bevorzugen, dass ihre Installationsbenutzeroberfläche das gleiche Aussehen und Gefühl wie das Spiel selbst hat, um dem Benutzer einen Eindruck von der Ambiance des Spiels zu geben. Um dies zu unterstützen, lässt Windows Installer die vollständige Deaktivierung der integrierten Benutzeroberfläche zu, sodass der Entwickler eine vollständig benutzerdefinierte Benutzeroberfläche bereitstellen kann.

Das benutzerdefinierte Setupprogramm deaktiviert zunächst Windows integrierte Benutzeroberfläche des Installers mithilfe der [**MsiSetInternalUI-API,**](/windows/desktop/api/msi/nf-msi-msisetinternalui) um die Benutzeroberflächenebene auf INSTALLUILEVEL \_ NONE festzulegen. Anschließend wird die [**MsiSetExternalUI-API**](/windows/desktop/api/msi/nf-msi-msisetexternaluia) aufgerufen, um eine Rückruffunktion anzugeben, die während des Installationsvorgangs aufgerufen wird, um das Setupprogramm über wichtige Ereignisse während der Installation zu benachrichtigen.

Der eigentliche Installationsvorgang wird dann durch Aufrufen der [**MsiInstallProduct-API**](/windows/desktop/api/msi/nf-msi-msiinstallproducta) gestartet. Diese API akzeptiert eine Parameterzeichenfolge, mit der der Aufrufer Werte für benannte Eigenschaften angeben kann. Diese Eigenschaften können in der Installationsdatenbank selbst verwendet werden, um anzupassen, wie die Anwendung installiert werden soll. Diese Eigenschaften können verwendet werden, um Folgendes anzugeben:

-   Das Verzeichnis, in dem die Anwendung installiert werden soll
-   Welche Features lokal installiert werden sollen und welche installiert werden sollen, um von der CD/DVD aus ausgeführt zu werden (z. B. um die Wahl zwischen einer minimalen installation und einer vollständigen Installation zu ermöglichen)
-   Gibt an, ob die Anwendung für alle Benutzer des Computers oder nur für den aktuellen Benutzer installiert werden soll.

Während der Installation verwendet das Setupprogramm die Benachrichtigungsmeldungen, die an die Rückruffunktion gesendet werden, um zu bestimmen, wann die Statusanzeige-Benutzeroberfläche aktualisiert werden soll, wann der Benutzer aufgefordert werden soll, die nächste CD einzufügen, oder wann der Benutzer über einen Fehler im Installationsvorgang benachrichtigt werden soll.

## <a name="patching"></a>Patching

Windows Das Installationsprogramm ermöglicht das Patchen installierter Anwendungen durch Anwenden einer Patchdatei. Eine Patchdatei enthält die neuen Dateien, die vom Patch hinzugefügt werden sollen, die Dateien, die durch den Patch geändert werden, und eine Liste der Änderungen, die an der Installationsdatenbank vorgenommen werden müssen. Um Speicherplatz zu sparen, anstatt den vollständigen Inhalt einer durch den Patch geänderten Datei zu speichern, enthält die Patchdatei tatsächlich nur die Unterschiede zwischen der ursprünglichen Version der Datei und der neuen Version der Datei.

Um einen Patch zu erstellen, benötigen Sie das Setupimage für jede Version der Anwendung, von der der Patch aktualisiert werden soll, sowie das Setupimage für die neue, aktualisierte Version der Anwendung. Ein Setupimage besteht aus der MSI-Datenbank und allen tatsächlichen Datendateien für die Anwendung. Die beste Möglichkeit, ein Setupimage für eine neue Version der Anwendung zu erstellen, besteht darin, das Setupimage aus der vorherigen Version der Anwendung zu kopieren und dann alle erforderlichen Änderungen vorzunehmen, um diese Kopie auf die gepatchte Version zu aktualisieren.

Sobald Sie über alle erforderlichen Setupimages verfügen, können Sie die Patches mit Msimsp.exe erstellen. Dabei handelt es sich um ein Patcherstellungstool, das als Teil des Plattform-SDK verfügbar ist. Das Tool fragt nach den Speicherorten der einzelnen Setupimages und bestimmt dann, wie die Unterschiede zwischen den nachfolgenden Versionen effizient dargestellt werden können. Die Ausgabe des Tools ist die endgültige Patchdatei (identifiziert durch die MSP-Erweiterung). Um den Patch programmgesteuert zu installieren, rufen Sie die [**MsiApplyPatch-API**](/windows/desktop/api/msi/nf-msi-msiapplypatcha) auf. Der Benutzer kann den Patch auch manuell installieren, indem er im Explorer auf die MSP-Datei doppelklickt.

## <a name="other-resources"></a>Weitere Ressourcen

-   Ausführliche Informationen zur Windows Installer-API finden Sie unter [Windows Installer](/windows/desktop/Msi/windows-installer-portal).
-   Informationen zu bewährten Methoden für die Spieleinstallation finden Sie unter [Installation und Wartung von Spielen.](/windows/desktop/DxTechArts/installation-and-maintenance-of-games)

 

 