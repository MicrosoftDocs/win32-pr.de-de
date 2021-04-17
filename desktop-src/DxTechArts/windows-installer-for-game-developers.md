---
title: Windows Installer für Spieleentwickler
description: Dieser Artikel bietet eine Übersicht über Windows Installer, die speziell für Spieleentwickler konzipiert ist. Eine ausführliche Dokumentation zu den Features und APIs, die in diesem Artikel erwähnt werden, finden Sie im Windows Platform SDK.
ms.assetid: 07401792-b34b-71c9-18f8-a11c916c7d81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e44227b633f7f9491b8a69bc06aa7945941a154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390569"
---
# <a name="windows-installer-for-game-developers"></a>Windows Installer für Spieleentwickler

Zeigt, wie Windows Installer verwendet werden kann, um Spiele auf Endbenutzer Computern zu installieren. Windows Installer bietet vollständige Unterstützung für eine angepasste Benutzeroberfläche sowie für das Patchen.

Microsoft Windows Installer ist die bevorzugte API zum Installieren von Software auf Windows-basierten Computern. Obwohl viele der Features von Windows Installer entwickelt wurden, um die Bereitstellung von Geschäftsanwendungen in einer Unternehmensumgebung zu unterstützen, ist Windows Installer auch vollständig für die Installation von Spielen auf Endbenutzer Computern geeignet. Die wichtigsten Vorteile der Verwendung von Windows Installer für die Spiele Installation sind:

-   Zuverlässige Deinstallation
-   Möglichkeit zum Installieren von Inhalten nach Bedarf
-   Unterstützung für vollständig benutzerdefinierte Benutzeroberfläche
-   Effizientes Patchen

Dieser Artikel bietet eine Übersicht über Windows Installer, die speziell für Spieleentwickler konzipiert ist. Eine ausführliche Dokumentation zu den Features und APIs, die in diesem Artikel erwähnt werden, finden Sie im Windows Platform SDK.

-   [Übersicht](#overview)
-   [Konzepte der Schlüssel Windows Installer](#key-windows-installer-concepts)
    -   [Komponenten](#components)
    -   [Funktionen](#features)
-   [Installations Zustände](#install-states)
-   [Bedarfs gesteuert installieren](#install-on-demand)
-   [Benutzerdefinierte Benutzeroberfläche](#custom-user-interface)
-   [Patchen](#patching)
-   [Andere Ressourcen](#other-resources)

## <a name="overview"></a>Übersicht

Alle Windows Installer basierten Setups verwenden eine Installationsdaten Bank Datei mit dem Namen MSI-Datei, um zu beschreiben, wie die Anwendung installiert werden soll. Die MSI-Datei enthält Informationen darüber, welche Dateien, Registrierungsschlüssel, Desktop Verknüpfungen, Dateizuordnungen und andere Anwendungs Elemente installiert werden müssen. Die tatsächlich zu installierenden Dateien können innerhalb der MSI-Datei selbst komprimiert, gebündelt und in separate "CAB-Dateien" komprimiert oder an einer anderen Stelle auf dem Installationsmedium als einzelne nicht komprimierte Dateien gespeichert werden. Die MSI-Datei kann auch auf extern implementierte benutzerdefinierte Aktionen verweisen, um Aktionen zuzulassen, für die die MSI-Datei nicht nativ zulässt.

Eine MSI-Datei kann optional eine Benutzeroberfläche enthalten, die den Benutzer durch den Installationsprozess führt. Diese Benutzeroberfläche eignet sich für die meisten Anwendungen. Es verfügt jedoch über das Aussehen und Verhalten einer normalen Windows-Anwendung, und viele Spieleentwickler bevorzugen, dass Ihre Setup Anwendung das Aussehen und Verhalten des Spiels selbst beibehält, um eine konsistentere Benutzererfahrung zu gewährleisten. Zur Unterstützung dieses vollständig benutzerdefinierten Benutzeroberflächen Szenarios kann eine Setup Anwendung die integrierte Benutzeroberfläche Windows Installer deaktivieren und die gesamte Benutzeroberfläche verarbeiten. Die Windows Installer-API stellt einen Rückrufmechanismus bereit, mit dem eine benutzerdefinierte Setup Benutzeroberfläche über den Fortschritt der Installation sowie wichtige Ereignisse, wie z. b. Datenträger Änderungsanforderungen, benachrichtigt werden kann.

Windows Installer ist keine End-to-End-Lösung zum Erstellen von Setups. Es handelt sich hierbei nur um eine API, die von einem Setup Programm verwendet werden kann, um die tatsächliche Installation von Dateien, Registrierungs Schlüsseln, Desktop Verknüpfungen und anderen Elementen der Anwendung durchzuführen. Die neuesten Versionen aller wichtigen kommerziellen Einrichtungs Tools (z. b. InstallShield, Wise und Microsoft Visual Studio) unterstützen Windows Installer. Diese Tools bieten praktische Benutzeroberflächen zum Erstellen des Setups für ein Spiel, aber Sie verlassen sich auf die Windows Installer-API, um einen Großteil der eigentlichen Installation durchzuführen. Diese Tools können auch verwendet werden, um eine MSI-Datenbank zu erstellen, die das Setup Paket enthält, das dann über eine benutzerdefinierte Setup Benutzeroberfläche installiert werden kann. Als Alternative zu Tools von Drittanbietern stellt die Windows Installer-API alle Funktionen bereit, die für die programmgesteuerte Erstellung und Bearbeitung einer MSI-Datenbank erforderlich sind, und das Windows Platform SDK enthält ein bare-The-MSI-Tool zur Datenbankbearbeitung namens Orca.

## <a name="key-windows-installer-concepts"></a>Konzepte der Schlüssel Windows Installer

Im folgenden finden Sie die Windows Installer Komponenten und Features.

### <a name="components"></a>Komponenten

Eine Anwendung besteht aus einer oder mehreren Komponenten, die durch eine GUID-Komponenten-ID identifiziert werden. Eine Komponente ist eine unteilbare Einheit. Es ist entweder vollständig installiert oder überhaupt nicht installiert. Eine Komponente kann aus einer einzelnen Datei, mehreren Dateien, Registrierungs Schlüsseln, Desktop Verknüpfungen oder einer Kombination aus bestehen. Die Ressourcen (Dateien usw.) innerhalb einer Komponente müssen für diese Komponente eindeutig sein. es können keine zwei Komponenten dieselbe Ressource enthalten. Eine Komponente wird nie explizit installiert. Sie wird nur als Teil eines Features installiert (siehe unten).

### <a name="features"></a>Features

Eine Funktion ist eine Gruppe von Komponenten, die durch eine GUID-Funktions-ID identifiziert wird. Im Unterschied zu-Komponenten können mehrere Features dieselbe Komponente enthalten. Eine Komponente, die von mehreren Features gemeinsam verwendet wird, wird installiert, wenn eine dieser Features installiert ist, und Sie wird nur dann entfernt, wenn alle Features, die auf die Komponente verweisen, deinstalliert wurden. Die Installation eines Features kann automatisch im Rahmen der Installation eines Produkts erfolgen, oder es kann manuell mithilfe der [**msikonfigurirefeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) -API ausgeführt werden.

Obwohl einige Spiele mehrere "Features" aufweisen, die unabhängig installiert werden können, ist das Windows Installer Konzept eines Features weiterhin nützlich. Da eine Windows Installer Funktion nicht mehr als eine Auflistung von Komponenten ist, die gleichzeitig installiert werden können, können Spiele Features verwenden, um den gesamten für eine bestimmte Phase des Spiels benötigten Inhalt zu gruppieren. Beispielsweise könnte ein ebenenorientiertes Spiel eine Funktion pro Ebene definieren, die aus dem gesamten für diese Ebene benötigten Inhalt besteht. Dies ermöglicht es dem Spiel, den Inhalt einzeln von innerhalb des Spiels zu installieren, anstatt den gesamten Inhalt für alle Ebenen während der Erstinstallation zu installieren.

## <a name="install-states"></a>Installations Zustände

Jede Komponente oder jedes Feature verfügt über einen zugeordneten Installationsstatus, der bestimmt, ob die Komponente oder das Feature verfügbar ist, und wenn ja, wo die Dateien für die Komponente oder das Feature installiert sind. Die möglichen Installations Zustände für ein Feature lauten:

<dl> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>Enthalten
</dt> <dd>

Die Funktion ist nicht installiert und kann daher nicht aufgerufen werden.

</dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>Nah
</dt> <dd>

Die Funktion ist verfügbar und wird zum Ausführen von der lokalen Festplatte installiert.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Ausgangs
</dt> <dd>

Die-Funktion ist verfügbar und wird zum Ausführen vom ursprünglichen Quell Medium (in der Regel eine CD oder DVD) installiert.

</dd> <dt>

<span id="Advertised"></span><span id="advertised"></span><span id="ADVERTISED"></span>Angekündigte
</dt> <dd>

Die Funktion ist nicht installiert, kann jedoch bei Bedarf mit der [**msikonfigurirefeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) -API installiert werden. Wenn die Funktion tatsächlich installiert ist, kann Sie entweder im lokalen oder im Quell Zustand installiert werden.

</dd> </dl>

Eine Komponente kann über einen der oben genannten Zustände mit Ausnahme von "angekündigt" verfügen. Wenn eine Komponente Teil eines angekündigten Features ist, wird die Komponente so lange als "nicht vorhanden" angezeigt, bis die Funktion installiert ist.

## <a name="install-on-demand"></a>Bedarfs gesteuert installieren

Windows Installer ermöglicht es einer Anwendung, Features als angekündigt zu markieren, was bedeutet, dass das Feature noch nicht installiert ist, aber zur Laufzeit zur Installation zur Verfügung steht. Die Installation von Features zur Laufzeit wird als "Bedarfs gesteuerte Installation" bezeichnet. Spiele können install on Demand verwenden, um die für die anfängliche Spiel Einrichtung erforderliche Zeit drastisch zu verringern, indem die Installation von Spielinhalten verzögert wird, bis Sie zur Laufzeit benötigt wird. Die Verzögerung, die erforderlich ist, um den Inhalt zur Laufzeit zu installieren, kann oft teilweise oder vollständig ausgeblendet werden, indem die Bedarfs gesteuerte Installation in einem Hintergrund Thread ausgeführt wird, während der Benutzer andernfalls mit dem Spiel beschäftigt ist.

## <a name="custom-user-interface"></a>Benutzerdefinierte Benutzeroberfläche

Obwohl Windows Installer eine Standardbenutzer Oberfläche bereitstellt, die den Benutzer durch die Installation der Anwendung führt, sieht diese Schnittstelle wie eine standardmäßige Windows-Anwendung aus. Viele Spieleentwickler bevorzugen, dass die Benutzeroberfläche der Installation das gleiche Aussehen hat wie das Spiel selbst, um dem Benutzer einen Vorgeschmack auf das Spiel zu geben. Um dies zu unterstützen, ermöglicht Windows Installer die vollständige Deaktivierung der integrierten Benutzeroberfläche, sodass der Entwickler eine vollständig benutzerdefinierte Benutzeroberfläche bereitstellen kann.

Das benutzerdefinierte Setup Programm deaktiviert zunächst die integrierte Benutzeroberfläche von Windows Installer mithilfe der [**MsiSetInternalUI**](/windows/desktop/api/msi/nf-msi-msisetinternalui) -API, um die Benutzeroberflächen Ebene auf "installuilevel None" festzulegen \_ . Anschließend wird die [**msisetexternalui**](/windows/desktop/api/msi/nf-msi-msisetexternaluia) -API aufgerufen, um eine Rückruffunktion anzugeben, die während des Installationsvorgangs aufgerufen wird, um das Setup Programm über wichtige Ereignisse während der Installation zu benachrichtigen.

Der tatsächliche Installationsvorgang wird dann durch Aufrufen der [**msiinstallproduct**](/windows/desktop/api/msi/nf-msi-msiinstallproducta) -API gestartet. Diese API akzeptiert eine Parameter Zeichenfolge, die es dem Aufrufer ermöglicht, Werte für benannte Eigenschaften anzugeben. Diese Eigenschaften können in der Installations Datenbank selbst verwendet werden, um anzupassen, wie die Anwendung installiert werden soll. Diese Eigenschaften können verwendet werden, um Folgendes anzugeben:

-   Das Verzeichnis, in dem die Anwendung installiert werden soll.
-   Welche Features lokal installiert werden müssen und welche installiert werden müssen, um von der CD/DVD auszuführen (z. b. um die Auswahl zwischen einer minimalen Installation und einer vollständigen Installation zu ermöglichen)
-   Gibt an, ob die Anwendung für alle Benutzer des Computers oder nur für den aktuellen Benutzer installiert werden soll.

Im Verlauf der Installation verwendet das Setup Programm die Benachrichtigungs Meldungen, die an die Rückruffunktion gesendet werden, um zu bestimmen, wann die Benutzeroberfläche der Statusanzeige aktualisiert werden soll, wann der Benutzer zur Eingabe der nächsten CD aufgefordert werden soll oder ob der Benutzer über einen Fehler im Installationsprozess benachrichtigt werden soll.

## <a name="patching"></a>Patching

Windows Installer ermöglicht das Patchen installierter Anwendungen durch Anwenden einer Patchdatei. Eine Patchdatei enthält die neuen Dateien, die vom Patch hinzugefügt werden sollen, die Dateien, die durch den Patch geändert werden, sowie eine Liste der Änderungen, die an der Installations Datenbank vorgenommen werden sollen. Um Speicherplatz zu sparen, enthält die Patchdatei statt des vollständigen Inhalts einer Datei, die vom Patch geändert wurde, tatsächlich nur die Unterschiede zwischen der ursprünglichen Version der Datei und der neuen Version der Datei.

Zum Erstellen eines Patches benötigen Sie das Setup Abbild für jede Version der Anwendung, von der der Patch aktualisiert werden soll, sowie das Setup Image für die neue aktualisierte Version der Anwendung. Ein Setup Abbild besteht aus der MSI-Datenbank und allen tatsächlichen Datendateien für die Anwendung. Die beste Möglichkeit, ein Setup Abbild für eine neue Version der Anwendung zu erstellen, besteht darin, das Setup Abbild aus der früheren Version der Anwendung zu kopieren und dann alle erforderlichen Änderungen vorzunehmen, um diese Kopie in die gepatchte Version zu aktualisieren.

Nachdem Sie alle erforderlichen Setup Abbilder erstellt haben, können Sie die Patches mithilfe von Msimsp.exe erstellen. dabei handelt es sich um ein Tool zur Patcherstellung, das als Teil des Platform SDK zur Verfügung steht. Das Tool fragt nach den Speicherorten der einzelnen Setup Abbilder und bestimmt dann, wie die Unterschiede zwischen den aufeinander folgenden Versionen effizient dargestellt werden. Die Ausgabe des Tools ist die endgültige Patchdatei (identifiziert durch die Erweiterung msp). Um den Patch Programm gesteuert zu installieren, wenden Sie die [**msiapplypatch**](/windows/desktop/api/msi/nf-msi-msiapplypatcha) -API an. Der Benutzer kann den Patch auch manuell installieren, indem Sie im Explorer auf die MSP-Datei doppelklicken.

## <a name="other-resources"></a>Weitere Ressourcen

-   Ausführliche Informationen zur Windows Installer-API finden Sie unter [Windows Installer](/windows/desktop/Msi/windows-installer-portal).
-   Informationen zu bewährten Methoden für die Spiele Installation finden Sie unter [Installation und Wartung von spielen](/windows/desktop/DxTechArts/installation-and-maintenance-of-games).

 

 