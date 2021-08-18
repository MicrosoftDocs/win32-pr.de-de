---
description: In diesem Abschnitt werden Überlegungen zur Bereitstellung Ihrer MSI-Anwendung für die optimale Verwendung durch die Logik zum Laden von Anwendungen und das Ressourcenladeprogramm beschrieben.
ms.assetid: 6c10b355-9bdd-4dba-8446-91034d4fe9b8
title: Anwendungsbereitstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb2d7605a2c6a39629749c00d175be4df8a3c66d8b0dc6c870926ec665d9ce6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041610"
---
# <a name="application-deployment"></a>Anwendungsbereitstellung

In diesem Abschnitt werden Überlegungen zur Bereitstellung Ihrer MSI-Anwendung für die optimale Verwendung durch die Logik zum Laden von Anwendungen und das Ressourcenladeprogramm beschrieben.

## <a name="packaging"></a>Verpackung

Die Paketierung für die Anwendung hängt von der Art der bereitgestellten Sprachunterstützung ab, da Windows Language Packs basierend auf den Benutzereinstellungen installiert. Wenn Sie sich beispielsweise für die Unterstützung von Systemspracheinstellungen entschieden haben, sollten Sie unabhängig vom vorgesehenen Benutzer die gesamte Sprachunterstützung in einem einzelnen Paket bereitstellen.

Wenn die Anwendung und die Ressourcen groß sind, sollten Sie ein Paket pro unterstützter Sprache verwenden. Beispielsweise können Sie diesen Pakettyp verwenden, wenn Ihre Anwendung vom Benutzer auswählbare Sprachen vorstellt und der Benutzer dynamisches Hinzufügen und Entfernen von Sprachressourcen benötigt.

## <a name="file-placement-on-windows-vista-and-later"></a>Dateiplatzierung auf Windows Vista und höher

In diesem Abschnitt wird die Dateiplatzierung für eine VISTA-Anwendung beschrieben, die nur auf Windows Vista und höher ausgerichtet ist.

### <a name="place-the-ln-file"></a>Platzieren der LN-Datei

Eine typische LN-Datei für eine CSV-Anwendung ist eine .exe-Datei oder eine .dll-Datei, z. B. BakerDelta.dll. Sie sollten diese Datei im Stammordner platzieren, in dem Ihre Anwendung installiert ist, z. B. X: \\ \\ <somepath> \\BakerDelta.dll.

### <a name="place-language-specific-resource-files"></a>Platzieren Language-Specific Ressourcendateien

Ihre sprachspezifischen Ressourcendateien müssen vorhersagbare Namen aufweisen, die durch Anfügen von ".firm" an den vollständigen Namen der LN-Datei gebildet werden, z.B. BakerDelta.dll.domains. Diese Dateien müssen in Unterordnern platziert werden, die nach den entsprechenden [Sprachnamen](language-names.md)benannt sind. Das folgende Beispiel zeigt die Platzierung von Ressourcen für die BakerDelta.dll LN-Datei mit sprachspezifischen Ressourcendateien für Englisch (Vereinigtes Königreich), Englisch (USA), neutrales Englisch, Spanisch (Spanien), Spanisch (Mexiko) und neutrales Spanisch:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath> \\ en-GB \\BakerDelta.dll.gigabyte
-   X: \\ \\ <somepath> \\ en-US \\BakerDelta.dll.js
-   X: \\ \\ <somepath> \\ en \\BakerDelta.dll.js
-   X: \\ \\ <somepath> \\ es-ES \\BakerDelta.dll.js
-   X: \\ \\ <somepath> \\ es-MX \\BakerDelta.dll.js
-   X: \\ \\ <somepath> \\ es \\BakerDelta.dll.msi

Die Ressourcendateien müssen während der Installation der WEBANWENDUNG oder eines Sprachpakets an den richtigen Speicherorten platziert werden. Es ist wichtig, jede Datei im richtigen Ordner zu platzieren, da das Ressourcenladeprogramm andernfalls nicht ordnungsgemäß ausgeführt werden kann. Im obigen Beispiel untersucht das Ressourcenladeprogramm X: \\ <somepath> \\ en-US \\BakerDelta.dll.english auf englische Ressourcen (USA). Wenn das Ladeprogramm in dieser Datei sucht und nur Ressourcen in spanischer Sprache erkennt, tritt ein Fehler auf.

## <a name="file-placement-on-a-pre-windows-vista-operating-system"></a>Dateiplatzierung auf einem Betriebssystem vor Windows Vista

Eine Anwendung, die auf einem Betriebssystem vor Windows Vista ausgeführt werden soll, kann die Windows Vista-Konvention verwenden, um sprachspezifische Ressourcendateien basierend auf Sprachnamen in Ordnern zu platzieren. Alternativ kann die Anwendung einer älteren Konvention entsprechen, die Pfade aus [Sprachbezeichnern](language-identifiers.md)bildet. Für Anwendungen, die nur eine einzelne Sprache unterstützen, können Sie einfach die sprachspezifische Ressourcendatei mit der Binärdatei im Stammverzeichnis platzieren.

Betrachten Sie beispielsweise eine LN-Datei namens BakerDelta.dll mit sprachspezifischen Ressourcendateien für Englisch (Vereinigtes Königreich), Englisch (USA), neutrales Englisch, Spanisch (Spanien), Spanisch (Mexiko) und neutrales Spanisch. Bei einer Installation auf einem Betriebssystem vor Windows Vista werden diese Dateien möglicherweise wie folgt gespeichert:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath> \\BakerDelta.dll.msi (optionale DATEI ".msi", die Ressourcen in der Sprache des Betriebssystems als endgültiges Fallback enthält)
-   X: \\ \\ <somepath> \\ BEIM \\ 0809 \\BakerDelta.dll.js
-   X: \\ \\ <somepath> \\ MSI \\ 0409 \\BakerDelta.dll.js
-   X: \\ \\ <somepath> \\ MSI \\ 0209 \\BakerDelta.dll.js
-   X: \\ \\ <somepath> \\ MSI \\ 040a \\BakerDelta.dll.js
-   X: \\ \\ <somepath> \\ MSI \\ 080a \\BakerDelta.dll.js
-   X: \\ \\ <somepath> \\ MSI \\ 0209 \\BakerDelta.dll.js

Zusätzlich zu diesen Dateien kann die Anwendung eine endgültige fallbacksprachspezifische Ressourcendatei einrichten, die sich im selben Ordner wie die Anwendung selbst befindet. Im obigen Beispiel ist diese Datei X: \\ <somepath> \\BakerDelta.dll.xx.

## <a name="installation"></a>Installation

Die Installationslogik zum Kopieren und Einrichten von Anwendungsdateien basiert auf den unterstützten Sprachen und dem Speicherort der Sprachressourcendateien an den richtigen Installationsspeicherorten. Ein Installationsprogramm muss die Anwendung installieren und einrichten, damit der Benutzer Sprachen problemlos hinzufügen und entfernen kann.

Wenn Ihre Anwendung einfach die Sprache des Zielbetriebssystems installiert, muss das Installationsprogramm die Benutzeroberfläche des Betriebssystems erkennen, um die zu installierenden Anwendungsressourcen zu bestimmen. Zur Unterstützung der besten Benutzerfreundlichkeit sollte das Installationsprogramm auch die Sprache der Benutzeroberfläche erkennen, um eine lokalisierte Benutzeroberfläche für die Installation selbst zu präsentieren.

Es wird empfohlen, Windows Installer (MSI) zu verwenden, um Ihre Installationssoftware zu erstellen. Zugeordnete Ressourcen sollten in der Ressourcendatei der Basissprache enthalten sein, wie unter [Erstellen der Ressourcendatei der Basissprache](creating-the-base-language-resource-file.md)beschrieben. Anweisungen zur Verwendung von MSI zum Vorbereiten des Anwendungsinstallationsprogramms finden Sie unter [Windows Installer](../msi/windows-installer-portal.md).

## <a name="uninstall-program"></a>Deinstallationsprogramm

Möglicherweise möchten Sie auch ein Deinstallationsprogramm mit Ihrer CSV-Anwendung einrichten. Msi wird auch für die Erstellung dieses Programms empfohlen. Anweisungen zur Verwendung von MSI zum Vorbereiten der Deinstallationssoftware finden Sie unter [Windows Installer](../msi/windows-installer-portal.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von mehrsprachige Benutzeroberfläche](using-multilingual-user-interface.md)
</dt> </dl>

 

 
