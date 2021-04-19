---
description: Msistuff.exe ist ein Befehlszeilen-Hilfsprogramm, das verwendet werden kann, um die Ressourcen in der ausführbaren Datei Setup.exe Bootstrap anzuzeigen oder zu konfigurieren.
ms.assetid: df79574c-d0e7-45e3-97c1-d62f700260ce
title: Msistuff.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b56d6b183128971501fd3ad8ddb7a88d08cee70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363655"
---
# <a name="msistuffexe"></a>Msistuff.exe

Msistuff.exe ist ein Befehlszeilen-Hilfsprogramm, das verwendet werden kann, um die Ressourcen in der ausführbaren Datei Setup.exe Bootstrap anzuzeigen oder zu konfigurieren.

Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="syntax"></a>Syntax

**msistuff setup.exe** *Option {Value}*

Wenn nach einer Option keine Daten angegeben werden, wird diese Ressource entfernt.

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msistuff.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung. Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden. Wenn eine Option mehrmals aufgeführt ist, wird nur das letzte Vorkommen verwendet.



| Option               | Ressourcen-ID                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| keine Optionen angegeben. |                              | Zeigt konfigurierbare Ressourcen in Setup.exe an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **-u**               | isetuppropname \_ baseurl      | Legen Sie baseurl, den Basis-URL-Speicherort Setup.exe fest. Wenn kein Wert vorhanden ist, wird der Speicherort von Setup.exe standardmäßig auf Wechselmedien eingestellt. Nur URL-basierte Installationen unterliegen einer Prüfung mit [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust). Der nachstehende Schrägstrich für die URL ist optional. Diese Option darf nicht ausgelassen werden.                                                                                                                                                                                                                     |
| **-d**               | isetuppropname- \_ Datenbank     | Legen Sie MSI als Namen für die MSI-Datei fest. Dabei handelt es sich um einen relativen Pfad zur MSI-Datei in Bezug auf den Speicherort des Setup.exe Programms. Diese Option ist erforderlich, wenn die Option-m nicht angegeben ist. Die Optionen-d und-m schließen sich gegenseitig aus. Beide können nicht gleichzeitig angegeben werden.                                                                                                                                                                                                                                                    |
| **-m**               | isetuppropname- \_ Patch        | Legen Sie MSP als Namen für die MSP-Datei fest. Dabei handelt es sich um einen relativen Pfad zur MSP-Datei in Bezug auf den Speicherort des Setup.exe Programms. Diese Option ist erforderlich, wenn die Option-d nicht angegeben ist. Die Optionen-m und-d schließen sich gegenseitig aus. Beide können nicht gleichzeitig angegeben werden.                                                                                                                                                                                                                                                    |
| **-n**               | isetuppropname \_ ProductName  | Legen Sie Product Name, den Namen des Produkts fest. Dies stellt den Namen dar, der im Banner Text für die heruntergeladene Benutzeroberfläche verwendet wird. Diese Option darf nicht ausgelassen werden. Wenn der Wert nicht weggelassen wird, ist der Standardwert "das Produkt".                                                                                                                                                                                                                                                                                                                            |
| **-o**               | isetuppropname- \_ Vorgang    | Geben Sie den Typ des auszuführenden Vorgangs an. Gültige Werte sind "Install", "minpatch", "majpatch" und "installupd". Weitere Informationen zu diesen Optionen finden Sie unter [Internet Download Bootstrapping](internet-download-bootstrapping.md).                                                                                                                                                                                                                                                                                           |
| **-v**               | isetuppropname- \_ MSI (minimal) \_ | Legen Sie mindestens erforderliche MSI-Version fest, die Mindestversion Windows Installer, die auf dem Computer erforderlich ist. Wenn die Mindestversion der Windows Installer auf dem Computer nicht vorhanden ist, wird die entsprechende [Instmsi.exe](instmsi-exe.md) installiert, um die Windows Installer zu aktualisieren. Der Wert dieser Eigenschaft hat das gleiche Format wie der PID- \_ PageCount-Wert. Siehe [**Zusammenfassungs Eigenschaft der Seitenanzahl**](page-count-summary.md) . Der Wert muss mindestens 200 sein. der Wert für die Windows Installer Version 2,0. Diese Option ist erforderlich. |
| **-i**               | isetuppropname- \_ instanzspeicherort | Legen Sie den Speicherort der Instmsi-URL, den Basis-URL-Speicherort Windows Installer ausführbaren Upgradedateien Wenn dieser Wert fehlt, wird der Speicherort der ausführbaren Dateien für das Upgrade standardmäßig auf den Speicherort Setup.exe angewendet. Diese Option darf nicht ausgelassen werden.                                                                                                                                                                                                                                                                                                |
| **-a**               | isetuppropname \_ Instmsia     | Legen Sie Instmsia, den Namen der ANSI-Version Windows Installer ausführbaren Datei für das Upgrade fest. Dies ist ein relativer Pfad zur ANSI-Version von Instmsi.exe relativ zu dem Speicherort, der von isetuppropname \_ instlocation angegeben wird. Diese Option ist erforderlich.                                                                                                                                                                                                                                                                                   |
| **-w**               | isetuppropname \_ Instmsiw     | Legen Sie Instmsiw, den Namen der Unicode-Version Windows Installer ausführbaren Upgradedatei fest. Dabei handelt es sich um einen relativen Pfad zur Unicode-Version von Instmsi.exe relativ zu dem Speicherort, der von isetuppropname \_ instlocation angegeben wird. Diese Option ist erforderlich.                                                                                                                                                                                                                                                                             |
| **-p**               | isetuppropname- \_ Eigenschaften   | Legen Sie die Eigenschaft = Wert-Zeichen folgen fest. Dies sind die Eigenschaft = Wert-Paare, die in der Befehlszeile enthalten sein sollen. Diese Option darf nicht ausgelassen werden. Diese Option kann nicht mehrmals aufgelistet werden, und Sie muss zuletzt in der Befehlszeile aufgeführt werden. Die gesamte Befehlszeile nach "-p" wird als Teil von "{Value}" betrachtet.                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Internetdownload-Bootstrapping](internet-download-bootstrapping.md)
</dt> <dt>

[Ein Beispiel für eine URL-basierte Windows Installer Installation](a-url-based-windows-installer-installation-example.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 
