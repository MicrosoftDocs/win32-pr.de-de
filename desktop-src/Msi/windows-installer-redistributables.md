---
description: Der Windows Installer Redistributable ist ein Software Update Paket.
ms.assetid: 8491dfa6-b9be-4e37-8a61-a405c8eb0ab0
title: Verteilbare Windows Installer-Dateien
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 9fc175a96ae1d2daed9798981b0dbe679505975e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348087"
---
# <a name="windows-installer-redistributables"></a>Verteilbare Windows Installer-Dateien

Windows Installer 4,5 und früher ist als verteilbares Software Update Paket verfügbar. Lesen Sie den Abschnitt [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md) , um zu bestimmen, welche Produkte Versionen des Windows Installer ausgeliefert haben. Das weitervertreibbare Update Paket für eine Version wird nach der Veröffentlichung des Produkts, das mit einer bestimmten Windows Installer Version ausgeliefert wird, verfügbar gemacht.

> [!NOTE]
> Es ist kein verteilbares für Windows Installer 5,0 vorhanden. Diese Version ist im Betriebssystem in Windows 7, Windows Server 2008 R2 und späteren Client-und Server Releases (einschließlich Windows 10) enthalten.

## <a name="obtaining-the-windows-installer-redistributable-45-and-earlier"></a>Abrufen der weitervertreibbaren Windows Installer (4,5 und früher)

-   Alle verfügbaren Windows Installer verteilbaren Dateien finden Sie im [Microsoft Download Center](https://www.microsoft.com/Downloads/).
-   Den Download für das Verteil [Bare Paket Windows Installer 4,5](https://support.microsoft.com/kb/942288) finden Sie unter: https://go.microsoft.com/fwlink/p/?LinkID=101159 .
-   Der Name der weitervertreibbaren Komponente, mit der Windows Installer 4,5 auf x86-basierten Computern mit Windows Vista, Windows Vista mit Service Pack 1 (SP1) und Windows Server 2008 installiert wird, ist Windows 6.0-KB942288-v2-x86. msu.
-   Der Name der weitervertreibbaren Komponente, die Windows Installer 4,5 auf x64-basierten Computern mit Windows Vista, Windows Vista mit SP1 und Windows Server 2008 installiert, ist Windows 6.0-KB942288-v2-x64. msu.
-   Der Name des verteilbaren verteilbaren Computers, der Windows Installer 4,5 auf Itanium-Based Systems-Computern unter Windows Vista, Windows Vista mit SP1 und Windows Server 2008 installiert, ist Windows 6.0-KB942288-v2-ia64. msu.
-   Der Name der weitervertreibbaren Komponente, mit der Windows Installer 4,5 auf x86-basierten Computern mit Windows XP mit Service Pack 2 (SP2) und Windows XP mit Service Pack 3 (SP3) installiert wird, ist WindowsXP-KB942288-v3-x86.exe.
-   Der Name der weitervertreibbaren Komponente, die Windows Installer 4,5 auf x86-basierten Computern mit Windows Server 2003 mit Service Pack 1 (SP1) und Windows Server 2003 mit Service Pack 2 (SP2) installiert, ist WindowsServer2003-KB942288-v4-x86.exe.
-   Der Name der weitervertreibbaren Komponente, die Windows Installer 4,5 auf x64-basierten Computern mit Windows Server 2003 mit SP1 und Windows Server 2003 mit SP2 installiert, ist WindowsServer2003-KB942288-v4-x64.exe.
-   Der Name der weitervertreibbaren Komponente, mit der Windows Installer 4,5 auf Itanium-Based Systemen installiert wird, auf denen Windows Server 2003 mit SP1 und Windows Server 2003 mit SP2 ausgeführt wird, ist WindowsServer2003-KB942288-v4-ia64.exe.
-   Es ist kein verteilbares Paket vorhanden, das Windows Installer 4,0 installiert. Diese Version des Windows Installer wird mit Windows Vista ausgeliefert.
-   Der Name der verteilbaren Komponente, die Windows Installer 3,1 installiert, ist WindowsInstaller-KB893803-v2-x86.exe. Der Download für das [Windows Installer 3,1 Redistributable (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c) -Paket ist verfügbar unter: https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c .
    > [!Note]  
    > Wenn Sie ein Upgrade auf Windows Installer 3,1 durch Installieren von Windows Server 2003 mit SP1 oder eine frühere Version dieser verteilbaren Version durchgeführt haben, müssen Sie möglicherweise auch das [Update für Windows Server 2003 Service Pack 1 (KB898715)](https://www.microsoft.com/downloads/details.aspx?FamilyID=8b4e6b93-1886-4d47-a18d-35581c42eca0) installieren, um alle in [Windows Installer 3,1 Redistributable (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c)verfügbaren Updates zu erhalten.

     

-   Die verteilbare Komponente, die Windows Installer 3,0 installiert, ist WindowsInstaller-KB884016-v2-x86.exe. Den Download für den [Windows Installer 3,0 Redistributable](https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8) finden Sie unter: https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8 .
-   Der Windows Installer 2,0 hat eine vorherige Benennungs Konvention für die verteilbare: [Instmsi.exe](instmsi-exe.md)verwendet. Die weitervertreibbare Datei für die Installation oder das Upgrade auf Windows Installer 2,0 unter Windows 2000 sollte nicht für die Installation oder Aktualisierung Windows Installer 2,0 unter Windows Server 2003 und Windows XP verwendet werden.

    Der Download für den [Windows Installer 2,0 Redistributable für Windows NT 4,0 und Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f) ist unter verfügbar https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f .

## <a name="installing-the-windows-installer-redistributable-45-and-earlier"></a>Installieren der weitervertreibbaren Windows Installer (4,5 und früher)

Der Windows Installer 4,5 resdistributable wird für Windows Vista-und Windows Server 2008-Betriebssysteme als MSU-Datei bereitgestellt und muss mithilfe des [Windows Update eigenständigen Installers](https://support.microsoft.com/kb/934307/) installiert werden (Wusa.exe.)

Die Windows Installer 4,5 Redistributable für die Betriebssysteme Windows XP und Windows Server 2003 können mithilfe der folgenden Befehlszeilen Syntax und-Optionen installiert werden.

Die Windows Installer 3,1 und Windows Installer 3,0 setzungen können mithilfe der folgenden Befehlszeilen Syntax und-Optionen installiert werden.

### <a name="syntax"></a>Syntax

Verwenden Sie die folgende Syntax, um die verteilbaren Komponenten für Windows Installer 4,5 unter Windows XP und Windows Server 2003 zu installieren.

```CMD
<Name of the Redistributable>\[<options>\]*
```

### <a name="command-line-options"></a>Befehlszeilenoptionen

Die Windows Installer verteilbaren Software Update Pakete verwenden die folgenden Befehlszeilenoptionen ohne Berücksichtigung der Groß-und Kleinschreibung.



| Option     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /norestart | Verhindert, dass das verteilbare Paket den Benutzer zum Neustart auffordert, auch wenn es Dateien ersetzen musste, die während der Installation verwendet wurden. Wenn das Update Paket mit dieser Option aufgerufen wird, wird ein **Fehler \_ beim \_ Neustart \_ des Fehlers** zurückgegeben, wenn die verwendeten Dateien ersetzt wurden.<br/> Wenn die verwendeten Dateien nicht ersetzt werden mussten, wird die **Fehlermeldung " \_ Erfolg**" zurückgegeben. Weitere Informationen zu verzögerten Neustarts finden Sie im Abschnitt "Hinweise".<br/> |
| /quiet     | Zur Verwendung durch Anwendungen, die die Windows Installer als Teil einer Bootstrapping-Anwendung verteilen. Eine Benutzeroberfläche (User Interface, UI) wird dem Benutzer nicht angezeigt. Die Bootstrapping-Anwendung sollte den Rückgabecode überprüfen, um zu bestimmen, ob ein Neustart erforderlich ist, um die Installation des Windows Installer abzuschließen.<br/>                                                                                                                                                |
| /help      | Zeigt die Hilfe zu allen verfügbaren Optionen an.                                                                                                                                                                                                                                                                                                                                                                                                                                     |

### <a name="delayed-restart-on-windows-vista-and-windows-server-2008"></a>Verzögerter Neustart unter Windows Vista und Windows Server 2008

Mit der Befehlszeilenoption/norestart wird verhindert, dass wusa.exe den Computer neu startet. Wenn jedoch eine vom MSU-Paket aktualisierte Datei verwendet wird, wird das Paket erst dann auf den Computer angewendet, wenn der Benutzer den Computer neu startet. Dies bedeutet, dass Anwendungen, die den Windows Installer 4,5 Redistributable für Windows Vista und Windows Server 2008 verwenden, die Windows Installer 4,5-Funktionalität nicht verwenden können, bis der Computer neu gestartet wird.

### <a name="delayed-restart-on-windows-xp-and-windows-server-2003"></a>Verzögerter Neustart unter Windows XP und Windows Server 2003

Es wird empfohlen, den Windows Installer-Dienst bei Verwendung des Update Pakets zu beenden. Wenn das Paket im vollständigen Modus der Benutzeroberfläche ausgeführt wird, wird erkannt, ob der Windows Installer-Dienst ausgeführt wird, und der Benutzer wird aufgefordert, den Dienst zu beenden. Wenn der Benutzer fortgesetzt wird, ohne den Dienst zu beenden, ersetzt das Update Windows Installer.

Das [Bootstrapping](bootstrapping.md) von Anwendungen, die das verteilbare Paket zum Installieren des Windows Installer mit einer anderen Anwendung verwenden, kann zusätzlich zu den Neustarts, die für die Installation der Anwendung erforderlich sind, einen zusätzlichen Systemneustart erfordern. Die Option für den verzögerten Neustart wird nur in Fällen empfohlen, in denen ein zusätzlicher Neustart vermieden werden muss, der durch die Installation von verwendeten Dateien verursacht wird. Entwickler sollten in der Setup Anwendung folgende Aktionen ausführen, um die Option für den verzögerten Neustart zu verwenden.

-   Wenden Sie das verteilbare Paket mit der Befehlszeilenoption/norestart an.
-   Behandeln Sie die Rückgabe eines **Fehler \_ Erfolgs** oder **eines \_ Fehler \_ Erfolgs \_ Neustarts** als Bedeutung von Erfolg.
-   Rufen Sie msiexec für das Anwendungspaket auf, und führen Sie einen anderen für die Anwendung spezifischen Setup Code aus. Wenn die Setup Anwendung [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)verwendet, muss die Anwendung MSI.DLL aus dem System Verzeichnis laden. Wenn kein Neustart erfolgt und die verteilbare Datei einen **Fehler beim \_ \_ Neustart \_ erforderlich** zurückgegeben hat, fordern Sie den Benutzer zur Eingabe eines Neustarts auf, um die Einrichtung der Windows Installer Binärdateien abzuschließen. Wenn ein Neustart auftritt, sind keine weiteren Schritte erforderlich.
    > [!Note]  
    > Anwendungen, die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) auf dem neuen MSI.DLL aufzurufen, nachdem das verteilbare Paket Erfolg zurückgegeben hat, muss sicherstellen, dass eine ältere Version von MSI.DLL nicht bereits innerhalb des Prozesses geladen wurde. Wenn eine ältere Version von MSI.DLL geladen wurde, muss Sie vor dem Aufrufen von **LoadLibrary** für die neue MSI.DLL aus dem Prozess Adressraum entladen werden.

     

Weitere Informationen finden Sie unter [Windows Installer Bootstrapping](windows-installer-bootstrapping.md).

 

 
