---
description: Instmsi.exe ist das verteilbare Paket für die Installation von Windows Installer&\# 160;2.0 und früheren Versionen von Windows Installer. Weitere Windows Installer Redistributables finden Sie unter verteilbare Windows Installer&\# 160;3.0 und höher.
ms.assetid: 74ea4530-3a73-4169-b0b7-f0272229192d
title: Instmsi.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2177fbb145dbfe2817dba2207cff95e5d80b801cc2f442085ba396f461870f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946118"
---
# <a name="instmsiexe"></a>Instmsi.exe

Instmsi.exe ist das verteilbare Paket zum Installieren von Windows Installer 2.0 und früheren Versionen von Windows Installer. Weitere [Windows Installer Redistributables](windows-installer-redistributables.md) finden Sie unter verteilbare Windows Installer 3.0 und höher.

Weitere Informationen dazu, welche Version des Windows Installers im Lieferumfang Ihres Betriebssystems enthalten war, finden Sie unter Veröffentlichte Versionen des Windows [Installers.](released-versions-of-windows-installer.md)

Einige verteilbare Versionen sollten nicht unter bestimmten Versionen des Betriebssystems ausgeführt werden. In der folgenden Tabelle wird beschrieben, welche Instmsi mit welchem Betriebssystem kompatibel ist.



| Wenn Instmsi.exe installiert diese Version des Windows Installers | Instmsi.exe können unter diesen Betriebssystemen ausgeführt werden.                    | Instmsi.exe darf nicht unter diesen Betriebssystemen ausgeführt werden.                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Windows Installationsprogrammversion 1.0                                 | Windows 95, Windows 98, Windows NT 4.0+SP3                           | Windows Me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Installationsprogrammversion 1.1                                 | Windows 95, Windows 98, Windows NT 4.0+SP3                           | Windows Me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Installationsprogrammversion 1.2                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0+SP3               | Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008             |
| Windows Installer, Version 2.0                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0+SP6, Windows 2000 | Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008                           |



 

Beispielsweise sollte eine Anwendung, die Windows Installer Version 1.1 weiterverteilt, überprüfen, ob das Betriebssystem Windows NT 4.0 SP3 oder Windows 98/95 ist, bevor das verteilbare Paket ausgeführt wird. Anwendungen, die das verteilbare Paket verwenden, sollten auch sicherstellen, dass die ANSI-Version des Windows-Installers unter Windows 98/95 installiert ist und dass die Unicode-Version unter Windows NT oder Windows 2000 installiert ist. Beachten Sie, dass einige Anwendungen die Unicode-Version in InstMsiW umbenennen.

## <a name="syntax"></a>Syntax

**instmsi-Optionen** 

## <a name="command-line-options"></a>Befehlszeilenoptionen

Bei den Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet.



| Option                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /q                         | Zur Verwendung durch Anwendungen, die den Windows Installer als Teil einer Bootstrappinganwendung verteilen. Dem Benutzer wird keine Benutzeroberfläche angezeigt. Die Bootstrappinganwendung sollte den Rückgabecode überprüfen, um zu ermitteln, ob ein Neustart erforderlich ist, um die Installation des Windows abzuschließen.                                                                                                                                                                                                                          |
| /t                         | Wird nur zu Debugzwecken verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /c:"msiinst /delayreboot"  | Die Option für den verzögerten Neustart. Verhindert, dass Instmsi den Benutzer zur Eingabe eines Neustarts aufforderung, auch wenn dateien ersetzt werden mussten, die während der Installation verwendet wurden. Wenn Instmsi mit dieser Option aufgerufen wird, wird ERROR SUCCESS REBOOT REQUIRED zurückgegeben, wenn dateien ersetzt werden mussten, die \_ \_ verwendet \_ wurden. Wenn dateien, die verwendet wurden, nicht ersetzt werden mussten, wird ERROR \_ SUCCESS zurückgegeben. Verfügbar mit Instmsi für Windows Installer 2.0 oder höher. Weitere Informationen zu verzögerten Neustarts finden Sie im Abschnitt "Hinweise".<br/> |
| /c:"msiinst /delayrebootq" | Die stille Version der Option für verzögerten Neustart. Dem Benutzer wird keine Benutzeroberfläche angezeigt. Andernfalls ist das Verhalten mit der vorherigen Option identisch. Verfügbar mit Instmsi für Windows Installer 2.0 oder höher. Weitere Informationen zu verzögerten Neustarts finden Sie im Abschnitt "Hinweise".<br/>                                                                                                                                                                                                                           |
| /?                         | Zeigt die Hilfe an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Hinweise

[Bootstrappinganwendungen,](bootstrapping.md) die Instmsi.exe zum Installieren des Windows Installers mit einer anderen Anwendung verwenden, erfordern möglicherweise einen zusätzlichen Systemneustart. Dies ist möglicherweise zusätzlich zu allen Neustarts, die zum Installieren der Anwendung erforderlich sind, ein zusätzlicher Neustart.

Die Option verzögerter Neustart wird nur für Setupentwickler empfohlen, die einen zusätzlichen Neustart vermeiden möchten, der durch die Verwendung von Instmsi.exe mit einer Setupanwendung verursacht wird, die dateien installiert, die verwendet werden.

Entwickler sollten in ihrer Setupanwendung folgende Schritte ausführen, um die Option für verzögerten Neustart zu verwenden. Diese Option ist nicht für Instmsi.exe verfügbar, die Windows Installer-Versionen vor Version 2.0 installieren:

**So verwenden Sie die Option "Verzögerter Neustart"**

1.  Rufen Instmsi.exe mit einer der Befehlszeilenoptionen für verzögerten Neustart auf.
2.  Behandeln Sie die Rückgabe von ERROR \_ SUCCESS oder ERROR SUCCESS \_ \_ REBOOT REQUIRED als \_ Erfolg.
3.  Den Pfad zu dem Ordner, der die neu installierten Binärdateien Windows Installer enthält, finden Sie unter dem Wert InstallerLocation:

    **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion Installer** \\ 

    Dieser Wert ist vom Typ **REG \_ SZ.**

4.  Legen Sie das aktuelle Verzeichnis auf den Pfad fest, den Sie in Schritt 3 erhalten haben.
5.  Rufen Sie Msiexec für das Anwendungspaket auf, und führen Sie anderen Setupcode aus, der für die Anwendung spezifisch ist. Wenn die Setupanwendung [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)verwendet, muss die Anwendung MSI.DLL speicherort laden, der in Schritt 3 ermittelt wurde.
    > [!Note]  
    > Anwendungen, die **LoadLibrary** auf dem neuen MSI.DLL an dem in Schritt 3 erhaltenen Speicherort aufrufen, müssen sicherstellen, dass eine ältere Version von MSI.DLL nicht bereits innerhalb des Prozesses geladen wurde. Wenn eine ältere Version von MSI.DLL innerhalb des Prozesses geladen wurde, muss sie vor dem **LoadLibrary-Aufruf** für den neuen Prozessadressenbereich entladen MSI.DLL.

     

6.  Wenn Schritt (5) keinen Neustart erfordert und Instmsi.exe in Schritt (1) ERROR SUCCESS REBOOT REQUIRED zurückgegeben hat, fordern Sie den Benutzer zur Eingabe eines Neustarts auf, um das Setup der Binärdateien des \_ \_ Windows-Installers auf dem System \_ abzuschließen. Wenn jedoch in Schritt (5) ein Neustart erfolgt, sind keine zusätzlichen Schritte erforderlich.

Instmsi.exe ist in den sdk-Komponenten Windows [für Windows Installer-Entwickler verfügbar.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bootstrapping](bootstrapping.md)
</dt> <dt>

[Internetdownload-Bootstrapping](internet-download-bootstrapping.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows Installer-Entwicklungstools](windows-installer-development-tools.md)
</dt> </dl>

 

 




