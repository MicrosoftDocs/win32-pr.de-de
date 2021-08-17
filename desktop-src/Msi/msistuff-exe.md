---
description: Msistuff.exe ist ein Befehlszeilenprogramm, mit dem die Ressourcen in der ausführbaren Bootstrapdatei angezeigt Setup.exe konfiguriert werden können.
ms.assetid: df79574c-d0e7-45e3-97c1-d62f700260ce
title: Msistuff.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a29c3fd904f137679cf1ce42f3718be151e07c3368b03e6f2807dbfc08656ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145623"
---
# <a name="msistuffexe"></a>Msistuff.exe

Msistuff.exe ist ein Befehlszeilenprogramm, mit dem die Ressourcen in der ausführbaren Bootstrapdatei angezeigt Setup.exe konfiguriert werden können.

Dieses Tool ist nur in Windows [SDK-Komponenten für Windows Installer-Entwickler verfügbar.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="syntax"></a>Syntax

**msistuff setup.exe** *option{value}*

Wenn nach einer Option keine Daten angegeben werden, wird diese Ressource entfernt.

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msistuff.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird. Ein Schrägstrichtrennzeichen kann auch statt eines Bindestrichs verwendet werden. Wenn eine Option mehrmals aufgeführt wird, wird nur das letzte Vorkommen verwendet.



| Option               | Ressourcen-ID                  | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine Optionen angegeben |                              | Anzeigen konfigurierbarer Ressourcen in Setup.exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **-u**               | ISETUPPROPNAME \_ BASEURL      | Legen Sie BaseURL fest, den Basis-URL-Speicherort Setup.exe. Wenn kein Wert vorhanden ist, wird der Speicherort Setup.exe standardmäßig auf Wechselmedien festgelegt. Nur URL-basierte Installationen unterliegen einer Überprüfung mit [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust). Der nachgestellte Schrägstrich für die URL ist optional. Diese Option wird möglicherweise weggelassen.                                                                                                                                                                                                                     |
| **-d**               | ISETUPPROPNAME \_ DATABASE     | Legen Sie Msi fest, den Namen der .msi Datei. Dies ist ein relativer Pfad zur .msi datei in Bezug auf den Speicherort des Setup.exe Programm. Diese Option ist erforderlich, wenn die Option -m nicht angegeben ist. Die Optionen -d und -m schließen sich gegenseitig aus. Sie können nicht beide angegeben werden.                                                                                                                                                                                                                                                    |
| **-m**               | ISETUPPROPNAME \_ PATCH        | Legen Sie Msp, den Namen der MSP-Datei, fest. Dies ist ein relativer Pfad zur MSP-Datei in Bezug auf den Speicherort des Setup.exe Programm. Diese Option ist erforderlich, wenn die Option -d nicht angegeben ist. Die Optionen -m und -d schließen sich gegenseitig aus. Sie können nicht beide angegeben werden.                                                                                                                                                                                                                                                    |
| **-n**               | ISETUPPROPNAME \_ PRODUCTNAME  | Legen Sie Produktname, den Namen des Produkts, fest. Dies stellt den Namen bereit, der im Bannertext für die heruntergeladene Benutzeroberfläche verwendet wird. Diese Option wird möglicherweise weggelassen. Wenn nicht angegeben, ist der Standardwert "das Produkt".                                                                                                                                                                                                                                                                                                                            |
| **-o**               | ISETUPPROPNAME-VORGANG \_    | Geben Sie den Typ des durchzuführenden Vorgangs an. Die gültigen Werte sind INSTALL, MINPATCH,PATCH und INSTALLUPD. Weitere Informationen zu diesen Optionen finden Sie unter [Internet Download Bootstrapping](internet-download-bootstrapping.md).                                                                                                                                                                                                                                                                                           |
| **-v**               | MINDESTENS ERFORDERLICHE \_ MSI-DATEI FÜR ISETUPPROPNAME \_ | Legen Sie Msi-Mindestversion fest, die mindestversion Windows Installationsprogramm, die auf dem Computer erforderlich ist. Wenn die Mindestversion des Windows Installers nicht auf dem [](instmsi-exe.md) Computer vorhanden ist, wird die entsprechendeInstmsi.exeinstalliert, um das Windows aktualisieren. Der Wert dieser Eigenschaft hat das gleiche Format wie der \_ PID PAGECOUNT-Wert. Weitere Informationen [**finden Sie unter Eigenschaft "Zusammenfassung der Seitenanzahl".**](page-count-summary.md) Der Wert muss mindestens 200 sein. Dies ist der Wert für Windows Installer-Version 2.0. Diese Option ist erforderlich. |
| **-i**               | ISETUPPROPNAME \_ INSTLOCATION | Legen Sie InstMsi URL Location fest, den Basis-URL-Speicherort Windows Installer upgrade executables. Wenn dieser Wert fehlt, wird der Speicherort der ausführbaren Upgradedateien standardmäßig auf den Speicherort der Setup.exe. Diese Option wird möglicherweise weggelassen.                                                                                                                                                                                                                                                                                                |
| **-a**               | ISETUPPROPNAME \_ INSTMSIE     | Legen Sie InstMsiA fest, den Namen der ANSI-Version der ausführbaren Windows Installer-Upgradedatei. Dies ist ein relativer Pfad zur ANSI-Version von Instmsi.exe relativ zum von ISETUPPROPNAME \_ INSTLOCATION angegebenen Speicherort. Diese Option ist erforderlich.                                                                                                                                                                                                                                                                                   |
| **-w**               | ISETUPPROPNAME \_ INSTMSIW     | Legen Sie InstMsiW fest, den Namen der Unicode-Version der ausführbaren Windows Installer-Upgradedatei. Dies ist ein relativer Pfad zur Unicode-Version von Instmsi.exe relativ zum von ISETUPPROPNAME \_ INSTLOCATION angegebenen Speicherort. Diese Option ist erforderlich.                                                                                                                                                                                                                                                                             |
| **-p**               | ISETUPPROPNAME-EIGENSCHAFTEN \_   | Legen Sie die PROPERTY=VALUE-Zeichenfolgen fest. Dies sind die PROPERTY=VALUE-Paare, die in der Befehlszeile enthalten sein sollen. Diese Option wird möglicherweise weggelassen. Diese Option kann nicht mehrmals aufgeführt werden und muss zuletzt in der Befehlszeile aufgeführt werden. Alle Befehlszeilen, die auf -p folgen, werden als Teil von {value} betrachtet.                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installer-Entwicklungstools](windows-installer-development-tools.md)
</dt> <dt>

[Internetdownload-Bootstrapping](internet-download-bootstrapping.md)
</dt> <dt>

[Beispiel für eine URL-basierte installation Windows Installer](a-url-based-windows-installer-installation-example.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Verteilbare Versionen](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 
