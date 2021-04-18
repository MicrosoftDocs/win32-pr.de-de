---
description: In diesem Abschnitt werden Überlegungen zum Bereitstellen der MUI-Anwendung für die optimale Verwendung durch die Anwendungs Lade Logik und das Ressourcen Lade Programm beschrieben.
ms.assetid: 6c10b355-9bdd-4dba-8446-91034d4fe9b8
title: Anwendungsbereitstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2023e5fc2dbde51a6ef996126e7557c9ffce8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366339"
---
# <a name="application-deployment"></a>Anwendungsbereitstellung

In diesem Abschnitt werden Überlegungen zum Bereitstellen der MUI-Anwendung für die optimale Verwendung durch die Anwendungs Lade Logik und das Ressourcen Lade Programm beschrieben.

## <a name="packaging"></a>Verpackung

Die Paket Erstellung für die Anwendung hängt von der Art der bereitgestellten Sprachunterstützung ab, da Windows Sprachpakete auf der Grundlage der Benutzereinstellungen installiert. Wenn Sie sich z. b. für die Unterstützung der System Spracheinstellungen entschieden haben, möchten Sie möglicherweise die gesamte Sprachunterstützung in einem einzelnen Paket bereitstellen, unabhängig von dem vorgesehenen Benutzer.

Wenn die Anwendung und die Ressourcen groß sind, sollten Sie ein Paket pro unterstützter Sprache verwenden. Beispielsweise können Sie diesen Pakettyp verwenden, wenn Ihre Anwendung Benutzer auswählbare Sprachen bereitstellt und der Benutzer das dynamische Hinzufügen und Entfernen von Sprachressourcen benötigt.

## <a name="file-placement-on-windows-vista-and-later"></a>Datei Platzierung unter Windows Vista und höher

In diesem Abschnitt wird die Platzierung von Dateien für eine MUI-Anwendung beschrieben, die nur auf Windows Vista und höher ausgerichtet ist

### <a name="place-the-ln-file"></a>Die LN-Datei platzieren

Eine typische LN-Datei für eine MUI-Anwendung ist eine exe-Datei oder eine DLL-Datei, z. b. BakerDelta.dll. Sie sollten diese Datei im Stamm Ordner platzieren, in dem Ihre Anwendung installiert ist, z. b. X: \\ \\ <somepath> \\BakerDelta.dll.

### <a name="place-language-specific-resource-files"></a>Language-Specific Ressourcen Dateien platzieren

Die sprachspezifischen Ressourcen Dateien müssen vorhersagbare Namen aufweisen, indem Sie ". MUI" an den vollständigen Namen der LN-Datei anhängen, z. b. BakerDelta.dll. MUI. Diese Dateien müssen in Unterordnern abgelegt werden, die nach den entsprechenden [Sprachnamen](language-names.md)benannt sind. Das folgende Beispiel zeigt die Platzierung von Ressourcen für die BakerDelta.dll LN-Datei mit sprachspezifischen Ressourcen Dateien für Englisch (Vereinigtes Königreich), Englisch (USA), neutral Deutsch, Spanisch (Spanien), Spanisch (Mexiko) und neutralem Spanisch:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath> \\ en-GB \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ en-US \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ en \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ es-es \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ es-MX \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ es \\BakerDelta.dll. MUI

Die Ressourcen Dateien müssen bei der Installation der MUI-Anwendung oder eines Sprachpakets an den richtigen Speicherorten abgelegt werden. Es ist wichtig, jede Datei im richtigen Ordner zu platzieren, da der Ressourcen Lader andernfalls nicht ordnungsgemäß funktionieren kann. Im obigen Beispiel untersucht das Ressourcen Lade Modul X: \\ <somepath> \\ en-US \\BakerDelta.dll. MUI für englische Ressourcen (USA). Wenn das Lade Modul in dieser Datei sucht und nur auf spanischsprachige Ressourcen stößt, tritt ein Fehler auf.

## <a name="file-placement-on-a-pre-windows-vista-operating-system"></a>Datei Platzierung unter einem Betriebs System vor Windows Vista

Für eine Anwendung, die unter einem Betriebssystem vor Windows Vista ausgeführt werden soll, kann die Windows Vista-Konvention verwendet werden, um sprachspezifische Ressourcen Dateien in Ordnern auf der Grundlage von Sprachnamen zu platzieren. Alternativ kann die Anwendung einer älteren Konvention entsprechen, die Pfade aus [sprach bezeichnerformularen](language-identifiers.md)bildet. Bei Anwendungen, die nur eine einzige Sprache unterstützen, können Sie einfach die sprachspezifische Ressourcen Datei im Stammverzeichnis der Binärdatei platzieren.

Angenommen, Sie haben eine ln-Datei namens "BakerDelta.dll" mit sprachspezifischen Ressourcen Dateien für Englisch (Vereinigtes Königreich), Englisch (USA), neutralem Englisch, Spanisch (Spanien), Spanisch (Mexiko) und neutralem Spanisch. Bei einer Installation unter einem Betriebssystem vor Windows Vista können diese Dateien wie folgt platziert werden:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath> \\BakerDelta.dll. MUI (optionale MUI-Datei mit Ressourcen in der Sprache des Betriebssystems als endgültiges Fallback)
-   X: \\ \\ <somepath> \\ MUI \\ 0809 \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ MUI \\ 0409 \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ MUI \\ 0209 \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ MUI \\ 040a \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ MUI \\ 080a \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ MUI \\ 0209 \\BakerDelta.dll. MUI

Zusätzlich zu diesen Dateien kann die Anwendung eine ultimative Fall Back sprachspezifische Ressourcen Datei einrichten, die sich im selben Ordner wie die Anwendung selbst befindet. Im obigen Beispiel lautet die Datei X: \\ <somepath> \\BakerDelta.dll. MUI.

## <a name="installation"></a>Installation

Die Installations Logik zum Kopieren und Einrichten von Anwendungs Dateien basiert auf den unterstützten Sprachen und dem Speicherort der Sprachressourcen Dateien an den richtigen Installations Standorten. Die Anwendung muss von einem Installer installiert und eingerichtet werden, damit der Benutzer problemlos Sprachen hinzufügen und entfernen kann.

Wenn die Sprache des Ziel Betriebssystems von Ihrer Anwendung einfach installiert wird, muss das Installationsprogramm die Benutzeroberfläche des Betriebssystems erkennen, um die zu installierenden Anwendungs Ressourcen zu bestimmen. Um die bestmögliche Benutzeroberfläche zu unterstützen, sollte das Installationsprogramm auch die Benutzeroberflächen Sprache erkennen, um eine lokalisierte Benutzeroberfläche für die Installation zu präsentieren.

Es wird empfohlen, zum Erstellen der Installationssoftware Windows Installer (MSI) zu verwenden. Zugehörige Ressourcen sollten in der Ressourcen Datei der Basis Sprache enthalten sein, wie unter [Erstellen der Ressourcen Datei für die Basis Sprache](creating-the-base-language-resource-file.md)beschrieben. Anweisungen zum Verwenden von MSI zum Vorbereiten des Anwendungsinstallations Programms finden Sie unter [Windows Installer](../msi/windows-installer-portal.md).

## <a name="uninstall-program"></a>Programm deinstallieren

Möglicherweise möchten Sie auch ein Deinstallationsprogramm für Ihre MUI-Anwendung einrichten. MSI wird auch für die Erstellung dieses Programms empfohlen. Anweisungen zum Verwenden von MSI zum Vorbereiten der Deinstallations Software finden Sie unter [Windows Installer](../msi/windows-installer-portal.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der mehrsprachigen Benutzeroberfläche](using-multilingual-user-interface.md)
</dt> </dl>

 

 
