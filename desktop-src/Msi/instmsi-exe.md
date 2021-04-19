---
description: Instmsi.exe ist das verteilbare Paket für die Installation von Windows Installer&\# 160; 2.0 und früheren Versionen Windows Installer. Weitere Informationen finden Sie unter Windows Installer setzungen für die verteilbaren Komponenten für Windows Installer&\# 160; 3.0 und höher.
ms.assetid: 74ea4530-3a73-4169-b0b7-f0272229192d
title: Instmsi.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 229d748cda68731627a6af2af992e321755b5ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353911"
---
# <a name="instmsiexe"></a>Instmsi.exe

Instmsi.exe ist das verteilbare Paket für die Installation von Windows Installer 2,0 und früheren Versionen von Windows Installer. Weitere Informationen finden Sie unter [Windows Installer setzungen](windows-installer-redistributables.md) für die verteilbaren Komponenten für Windows Installer 3,0 und höhere Versionen.

Weitere Informationen dazu, welche Version des Windows Installer mit dem Betriebssystem ausgeliefert wurde, finden Sie unter [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md).

Einige verteilbare Tabellen sollten nicht in bestimmten Versionen des Betriebssystems ausgeführt werden. In der folgenden Tabelle wird beschrieben, welche Instmsi auf welchem Betriebssystem kompatibel ist.



| Wenn Instmsi.exe diese Version des-Windows Installer installiert. | Instmsi.exe können unter diesen Betriebssystemen ausgeführt werden.                    | Instmsi.exe dürfen nicht unter diesen Betriebssystemen ausgeführt werden.                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Windows Installer Version 1,0                                 | Windows 95, Windows 98, Windows NT 4.0 + SP3                           | Windows Me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Installer Version 1,1                                 | Windows 95, Windows 98, Windows NT 4.0 + SP3                           | Windows Me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Installer Version 1,2                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0 + SP3               | Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008             |
| Windows Installer Version 2,0                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0 und höher SP6, Windows 2000 | Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008                           |



 

Eine Anwendung, die Windows Installer Version 1,1 neu verteilt, sollte z. b. überprüfen, ob das Betriebssystem Windows NT 4,0 SP3 oder Windows 98/95 ist, bevor das verteilbare Paket ausgeführt wird. Anwendungen, die das verteilbare Paket verwenden, sollten außerdem sicherstellen, dass die ANSI-Version der Windows Installer unter Windows 98/95 installiert ist und dass die Unicode-Version unter Windows NT oder Windows 2000 installiert ist. Beachten Sie, dass einige Anwendungen die Unicode-Version in Instmsiw umbenennen.

## <a name="syntax"></a>Syntax

**Instmsi** - *Optionen*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Bei den Befehlszeilenoptionen wird Groß-/Kleinschreibung nicht beachtet.



| Option                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /q                         | Zur Verwendung durch Anwendungen, die die Windows Installer als Teil einer Bootstrapping-Anwendung verteilen. Dem Benutzer wird keine Benutzeroberfläche angezeigt. Die Bootstrapping-Anwendung sollte den Rückgabecode überprüfen, um zu bestimmen, ob ein Neustart erforderlich ist, um die Installation des Windows Installer abzuschließen.                                                                                                                                                                                                                          |
| /t                         | Wird nur zu Debugzwecken verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /c: "msiinst/delayreboot"  | Die Option für den verzögerten Neustart. Verhindert, dass Instmsi den Benutzer zur Eingabe eines Neustarts auffordert, auch wenn er Dateien ersetzen musste, die während der Installation verwendet wurden. Wenn Instmsi mit dieser Option aufgerufen wird, wird ein Neustart des Fehler Fehlers zurückgegeben, \_ \_ \_ Wenn die verwendeten Dateien ersetzt werden mussten. Wenn die verwendeten Dateien nicht ersetzt werden mussten, wird die Fehlermeldung "Erfolg" zurückgegeben \_ . Verfügbar mit Instmsi für Windows Installer 2,0 oder höher. Weitere Informationen zu verzögerten Neustarts finden Sie im Abschnitt "Hinweise".<br/> |
| /c: "msiinst/delayrebootq" | Die quiet-Version der Option für verzögertes Neustarten. Dem Benutzer wird keine Benutzeroberfläche angezeigt. Andernfalls ist das Verhalten mit der vorherigen Option identisch. Verfügbar mit Instmsi für Windows Installer 2,0 oder höher. Weitere Informationen zu verzögerten Neustarts finden Sie im Abschnitt "Hinweise".<br/>                                                                                                                                                                                                                           |
| /?                         | Zeigt die Hilfe an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Bemerkungen

Das [Bootstrapping](bootstrapping.md) von Anwendungen, die Instmsi.exe zum Installieren des Windows Installer mit einer anderen Anwendung verwenden, erfordert möglicherweise einen zusätzlichen Systemneustart. Dies ist möglicherweise ein zusätzlicher Neustart zusätzlich zu allen Neustarts, die für die Installation der Anwendung erforderlich sind.

Die Option für den verzögerten Neustart wird nur für Setup Entwickler empfohlen, die einen zusätzlichen Neustart vermeiden möchten, der durch die Verwendung Instmsi.exe mit einer Setup Anwendung verursacht wird, mit der verwendete Dateien installiert werden.

Entwickler sollten in der Setup Anwendung folgende Aktionen ausführen, um die Option für den verzögerten Neustart zu verwenden. Diese Option ist nicht in Instmsi.exe Versionen verfügbar, bei denen Windows Installer-Versionen vor Version 2,0 installiert werden:

**So verwenden Sie die Option für verzögerten Neustart**

1.  Wenden Sie Instmsi.exe mit einer der verzögerten Neustart-Befehlszeilenoptionen an.
2.  Behandeln Sie die Rückgabe eines Fehler \_ Erfolgs oder eines Fehler \_ Erfolgs \_ Neustarts \_ als Bedeutung von Erfolg.
3.  Rufen Sie den Pfad zu dem Ordner ab, der die neu installierten Windows Installer Binärdateien aus dem installerlocation-Wert enthält:

    **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Installer**

    Dieser Wert ist vom Typ **reg \_ SZ**.

4.  Legen Sie das aktuelle Verzeichnis auf den in Schritt 3 erhaltenen Pfad fest.
5.  Rufen Sie msiexec für das Anwendungspaket auf, und führen Sie einen anderen für die Anwendung spezifischen Setup Code aus. Wenn die Setup Anwendung [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)verwendet, muss die Anwendung MSI.DLL aus dem in Schritt 3 erhaltenen Speicherort laden.
    > [!Note]  
    > Anwendungen, die **LoadLibrary** auf dem neuen MSI.DLL an dem in Schritt 3 abzurufenden Speicherort aufzurufen, müssen sicherstellen, dass eine ältere Version von MSI.DLL nicht bereits innerhalb des Prozesses geladen wurde. Wenn eine ältere Version von MSI.DLL innerhalb des Prozesses geladen wurde, muss Sie vor dem **LoadLibrary** -Rückruf für die neue MSI.DLL aus dem Prozess Adressraum entladen werden.

     

6.  Wenn für Schritt (5) kein Neustart erforderlich ist und Instmsi.exe \_ \_ \_ in Schritt (1) einen Fehler beim Neustart des Fehlers zurückgegeben hat, fordern Sie den Benutzer zur Eingabe eines Neustarts auf, um die Einrichtung der Windows Installer Binärdateien auf dem System abzuschließen. Wenn jedoch ein Neustart in Schritt (5) erfolgt, sind keine weiteren Schritte erforderlich.

Instmsi.exe ist in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bootstrapping](bootstrapping.md)
</dt> <dt>

[Internetdownload-Bootstrapping](internet-download-bootstrapping.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> </dl>

 

 




