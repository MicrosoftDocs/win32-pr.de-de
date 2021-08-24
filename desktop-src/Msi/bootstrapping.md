---
description: Derzeit beginnt jede Installation, die versucht, den Windows-Installer zu verwenden, mit der Überprüfung, ob das Installationsprogramm auf dem Computer des Benutzers vorhanden ist, und wenn es nicht vorhanden ist, ob der Benutzer und der Computer bereit sind, den Windows Installer zu installieren.
ms.assetid: a5174284-2a8c-4510-accf-641fda5be98d
title: Bootstrapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c590d00fa9d6ac63f93caa287f34b9f2bf25357bd36ab9ea3fb9ce87e81291d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145713"
---
# <a name="bootstrapping"></a>Bootstrapping

Derzeit beginnt jede Installation, die versucht, den Windows-Installer zu verwenden, mit der Überprüfung, ob das Installationsprogramm auf dem Computer des Benutzers vorhanden ist, und wenn es nicht vorhanden ist, ob der Benutzer und der Computer bereit sind, den Windows Installer zu installieren. Ein [Setupanwendungs-Instmsi.exe](instmsi-exe.md) steht mit dem Windows Installer SDK zur Verfügung, das die ganze Logik und Funktionalität zum Installieren des Windows enthält. Diese Installation muss jedoch von einer Bootstrappinganwendung verwaltet werden.

Die Bootstrappinganwendung muss zunächst überprüfen, ob Windows Installer installiert ist. Anwendungen können die Derzeit installierte Version des Windows mithilfe von [**DllGetVersion erhalten.**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc) Wenn Windows Installer derzeit nicht installiert ist, muss die Bootstrappinganwendung das Betriebssystem abfragen, um zu ermitteln, welche Version der Instmsi.exe erforderlich ist. Nachdem die Installation des Windows-Installers initiiert wurde, muss die Bootstrappinganwendung Rückgabecodes aus der Instmsi.exe-Anwendung verarbeiten und jeden Neustart verarbeiten, der während der Installation des Windows Installers Windows wird. Weitere Informationen finden Sie unter [Bestimmen der Windows Installerversion.](determining-the-windows-installer-version.md)

Im folgenden Beispiel wird veranschaulicht, wie die Setupanwendung, die Microsoft Office 2000 installiert, das System des Benutzers überprüft und die Installation Windows Installer konfiguriert. Dieses Beispiel wurde speziell für die Installation Office 2000 geschrieben und sollte nur als allgemeiner Verweis verwendet werden.

Wenn ein Benutzer eine Office 2000 CD-ROM auf seinen Computer einfügung, versucht Setup.exe, den Wartungsmodus, die Setupanwendung zu starten, oder führt gemäß den Anforderungen des Benutzers gar nichts aus. Im folgenden Abschnitt wird beschrieben, wie die Office 2000-Setupanwendung mit dem Namen Setup.exe den Benutzer und seinen Computer qualifiziert, eine Befehlszeile erstellt und Windows Installer mithilfe der Msiexec.exe-Anwendung installiert.

## <a name="how-setupexe-bootstraps-the-windows-installer-when-installing-office-2000"></a>Ausführen Setup.exe Bootstraps des Windows Installers bei der Installation Office 2000

1.  Der Benutzer fügt eine Office 2000 CD-ROM auf seinen Computer ein. Das Windows-Betriebssystem initiiert die Setup.exe mithilfe des Schalters /autorun und der Datei Autorun.inf. Die Datei Autorun.inf befindet sich im Stammverzeichnis der Office 2000 CD-ROM und enthält die folgenden Abschnitte:

    \[Autorun\]

     

    \[Office Funktionen\]

     

    \[Produktinformationen\]

     

    \[ServicePack \] .

    Der Abschnitt Autorun enthält eine Befehlszeile, die die Setup.exe-Anwendung und das Symbol zum Anzeigen des Datenträgers sowie Informationen zum Hinzufügen einer Option "Installieren" und einer Option "Konfigurieren" zum Kontextmenü für die \[ \] CD-ROM enthält.

    Der \[ abschnitt Office \] Features enthält eine Liste mit Features und Funktionsnamenpaaren.

    Im \[ Abschnitt \] Produktinformationen werden der Name und die Version der Anwendung angegeben.

    Im \[ Abschnitt ServicePack \] kann ein Netzwerkadministrator die mindestens erforderliche Service Pack-Ebene festlegen. Der Netzwerkadministrator kann diesen Abschnitt verwenden, um den Text einer Warnmeldung zu erstellen, die angezeigt wird, wenn das lokale Betriebssystem nicht über das erforderliche Service Pack verfügt.

    Im Folgenden finden Sie ein Beispiel für Autorun.inf.

    ``` syntax
    [autorun] 
    OPEN=setup.EXE /AUTORUN /KEY:Software\Microsoft\Office\9.0\Common\General\InstallProductID
    ICON=setup.EXE,1
    shell\configure=&Configure
    shell\configure\command=setup.EXE
    shell\install=&Install
    shell\install\command=setup.EXE
    [OfficeFeatures]
    Feature1=ACCESSFiles
    Feature2=OfficeFiles
    Feature3=WORDFiles
    Feature4=EXCELFiles
    Feature5=PPTFiles
    [ProductInformation]
    DisplayName=Microsoft Office 9
    Version=9.0
    ProductCode={product guid}
    [ServicePack]
    MessageText="The operating system does not have a required service pack. Please download and install this from www.microsoft.com."
    SPLevel=3
    ```

2.  Die Setup.exe überprüft den \_ Mutex MsiPromptForCD. Windows Das Installationsprogramm erstellt diesen Mutex, wenn er den Benutzer zum Einfügen der CD-ROM aufgefordert. Das Vorhandensein des Mutex gibt an, dass Windows Installer eine Installation ausgeführt, die die Office 2000 CD-ROM angefordert hat. In diesem Fall wird die Setup.exe sofort beendet, und die Installation Office 2000 wird fortgesetzt. Wenn der Mutex nicht vorhanden ist, wird die Setup.exe-Anwendung in Schritt 3 fortgesetzt, wobei ein Registrierungsschlüssel ausgewertet wird, um zu bestimmen, ob Office 2000 installiert ist.
3.  Die Setup.exe überprüft das Vorhandensein des Office9-Registrierungsschlüssels:

    **HKCU/Software/Microsoft/Office/9.0/Common/General/InstallProductID**

    Wenn dieser Registrierungsschlüssel nicht vorhanden ist, wird die Setup.exe-Anwendung in Schritt 6 fortgesetzt, wobei das Betriebssystem überprüft wird, um zu ermitteln, ob es für die Installation von Office 2000 qualifiziert ist.

4.  Wenn der Office 2000 vorhanden ist, überprüft die Setup.exe Anwendung den aktuellen Installationsstatus durch Aufrufen [**von MsiQueryProductState.**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) Der Rückgabestatus InstallState Default gibt an, dass Office 2000 bereits installiert ist und die Setup.exe-Anwendung in Schritt 5 fortgesetzt wird, wobei Office 2000 auf die Ausführung aus der Quelle überprüft \_ wird.

    Wenn Office 2000 nicht installiert ist, wird die Setup.exe-Anwendung in Schritt 6 fortgesetzt, wobei das Betriebssystem überprüft wird, um zu ermitteln, ob es für die Installation von Office 2000 qualifiziert ist.

5.  Die Setup.exe-Anwendung ruft [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) für jedes der Features im **\[ \] OfficeFeatures-Abschnitt** der Datei Autorun.inf auf. Wenn eines dieser Features INSTALLSTATE SOURCE zurückgibt, deutet dies darauf hin, dass das Feature von der Quelle ausgeführt wird und Setup.exe \_ anwendung sofort beendet wird.

    Wenn keines der Features INSTALLSTATE SOURCE zurückgibt, startet die Setup.exe-Anwendung die Installationsprogrammanwendung Msiexec.exe und zeigt den Wartungsmodus Windows Installer an, bevor sie beendet \_ wird.

6.  Die Setup.exe bestimmt, ob das Betriebssystem für eine Installation von Office 2000 qualifiziert ist. Windows XP ist erforderlich, um Office 2000 zu installieren. Wenn für das Betriebssystem ein Service Pack-Update erforderlich ist, um sich für Office 2000 zu qualifizieren, zeigt die Setup.exe-Anwendung den in der Datei Autorun.inf angegebenen Text an. Wenn das Betriebssystem nicht für Office 2000 oder ein Upgrade von Office 2000 qualifiziert ist, zeigt die Setup.exe-Anwendung eine Meldung an, die den Benutzer daran hindert, fortzuführen.

    Wenn das Betriebssystem für Office 2000 qualifiziert ist, wird die Setup.exe-Anwendung mit Schritt 7 fortgesetzt, der bestimmt, ob der Windows-Installer auf dem Computer des Benutzers installiert ist.

7.  Wenn Windows Installer auf dem Computer des Benutzers vorhanden ist, startet die Setup.exe-Anwendung die Msiexec.exe-Anwendung und übergibt die Office 2000.msi datei an diese.

    Wenn Windows Installer nicht auf dem lokalen Computer installiert ist, wird die Setup.exe-Anwendung mit Schritt 8 fortgesetzt, der bestimmt, ob das Betriebssystem berechtigt ist, Windows Installer installiert zu haben.

8.  Wenn der lokale Computer berechtigt ist, Windows Installer installiert zu haben, führt die Setup.exe-Anwendung die richtige Version der Instmsi.exe-Installationsprogrammanwendung für die Plattform aus. Setup.exe den Befehlszeilenschalter "/q" übergeben, um die Benutzeroberfläche zu unterdrücken und zu verhindern, dass der Benutzer Installationskonfigurationsoptionen ändert.
9.  Die Setup.exe anwendung lädt die neu installierte Msi.dll-Datei und führt einen Aufruf der [**MsiInstallProduct-Funktion**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) aus, um die Anwendung des Benutzers zu installieren.

## <a name="setupexe-command-line-parameters"></a>Setup.exe Befehlszeilenparameter

Mit Setup.exe-Anwendung können Administratoren und Benutzer Befehlszeilenoptionen an die Msiexec.exe übergeben. Weitere Informationen finden Sie unter [Befehlszeilenoptionen.](command-line-options.md) In der folgenden Tabelle sind die Befehlsoptionen aufgeführt, die mit der Setup.exe.



| Option                       | Verwendung                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /autorun                     | setup.exe /autorun                                                                                                                           | Führt die oben beschriebene Datei Autorun.inf aus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| /a                           | setup.exe /a                                                                                                                                 | Initiiert eine Administratorinstallation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| /j                           | \[u \| \] *m-Paket* oder <br/> \[u \| m \] *Package* /t *Transform List*<br/> oder <br/> \[u \| m \] *Package* /g *LanguageID*<br/> | Gibt ein Produkt an. Diese Option ignoriert alle Eigenschaftswerte, die in der Befehlszeile eingegeben werden. u Ankündigung für den aktuellen Benutzer.<br/> m Ankündigung für alle Benutzer des Computers.<br/> g Sprachbezeichner<br/> t Wendet die Transformation auf angekündigtes Paket an.<br/>                                                                                                                                                                                                                        |
| /I                           | setup.exe /I Office9.msi /t ProgramMgmt.mst                                                                                                  | Gibt die .msi datei an, Setup.exe installiert werden soll. Wenn die Option /I nicht enthalten ist, verwendet Setup.exe die Office9.msi Datei.                                                                                                                                                                                                                                                                                                                                                                                 |
| /o< = *Eigenschaftswert*> | setup.exe /o CDKEY=111111-1111                                                                                                               | Legt Eigenschaften in der .msi fest. Setup.exe sie wie geschrieben an msiexec übergibt.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| /q                           | setup.exe /q                                                                                                                                 | Legen Sie die Benutzeroberflächenebene der Installation fest. /q no UI (/qn for msiexec.) /qb basic UI<br/> /qr reduzierte Benutzeroberfläche.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| /m\#                         | setup.exe /m4                                                                                                                                | Unterstützt mehrere Lizenzen in Übereinstimmung mit Select Agreements. Diese Eigenschaft wird in von der benutzerdefinierten Aktion Lizenzüberprüfung verwendet, um das LV-Zertifikat zu schreiben. Auf die Option /m muss die Anzahl der zulässigen Entsperrungen folgen. Der durch die Option /m angegebene Wert sollte als "M"-Eigenschaft in der Office9.msi werden. Wenn kein Wert angegeben wird, aber die Option /m beim Setup verwendet wird, sollte der Wert 0 festgelegt werden. Die Option /m ist erforderlich, um Select customers using a CD or network (Kunden mit einer CD oder einem Netzwerk auswählen) zu unterstützen. |
| /settings                    | setup.exe /settings-mysettings.ini                                                                                                           | Ermöglicht Es Administratoren, eine .ini-Datei anzugeben, die alle benutzerdefinierten Einstellungen enthält, die während Office 2000-Setup übergeben werden sollen. Sehen Sie sich die Beschreibung der .ini Datei unten an.                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="using-an-ini-file"></a>Verwenden einer .ini-Datei

Das Erstellen einer Initialisierungsdatei ist möglicherweise einfacher als das Erstellen einer langen Befehlszeile. Mithilfe der Option /settings liest die Setup.exe Anwendung die angegebene .ini-Datei und erstellt eine Befehlszeile, die an die Msiexec.exe Anwendung übergeben wird. In der datei .ini werden nur Eigenschaften unterstützt, die in der Befehlszeile unterstützt werden. Wenn eine Eigenschaft oder ein Wert sowohl in der .ini-Datei als auch in der Befehlszeile gefunden wird, überschreiben die Befehlszeileneinstellungen die .ini Dateieinstellungen.

Das Format der .ini-Datei lautet:

\[Msi\]

 

\[Mst\]

 

\[options\]

 

\[Display\]

Der \[ \] MSI-Abschnitt der .ini Datei gibt den Pfad zum Installationspaket für die Installation an. Dies entspricht der Option /I in der Befehlszeile.

Der \[ \] mst-Abschnitt der .ini-Datei gibt den Pfad zu transformationen an, der bei dieser Installation verwendet wird. Dies entspricht der Option /j in der Befehlszeile. Mehrere Transformationen werden jeweils in einer anderen Zeile mit MST1 MST(N) angegeben. Bei der Analyse in der Befehlszeile wird die Liste in der datei .ini von links nach rechts geschaltet. Beachten Sie, dass die dem MST(N)-Titel zugeordnete Zahl nur zur Verwaltung eindeutiger Bezeichner vorhanden ist und keine programmgesteuerte Bedeutung hat.

Im \[ \] Abschnitt "Optionen" können Netzwerkadministratoren Eigenschaften in den dateien .msi oder .mst festlegen und überschreiben. Optionen, die in der .ini-Datei festgelegt sind, werden der Befehlszeile mithilfe der Option /o hinzugefügt. Jede Option im Optionsabschnitt muss einen Eigenschaftennamen und einen Wert aufweisen.

Der \[ Abschnitt Anzeigen wird \] verwendet, um die benutzeroberflächenebene festzulegen, die während des Setups verwendet wird. Dies entspricht der Option /q in der Befehlszeile. Gültige Werte sind "none", "basic", "reduced" und "full".

Beispieldatei für .ini

\[MSI\]

 

MSI= \\ \\ sourceshare \\ Office2000 \\Office2000.msi

 

\[Mst\]

 

MST1= \\ \\ sourceshare \\ Office2000 \\ trns1.mst

 

MST2= \\ \\ sourceshare \\ Office2000 \\ trns2.mst

 

\[Optionen\]

 

PUBLICPROPERTY=Ihr Wert

\[Display\]

 

Display=None

 

