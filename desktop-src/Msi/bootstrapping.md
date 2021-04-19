---
description: Derzeit wird bei jeder Installation, die versucht, den Windows Installer zu verwenden, überprüft, ob der Installer auf dem Computer des Benutzers vorhanden ist, und ob er nicht vorhanden ist, ob der Benutzer und der Computer für die Installation Windows Installer bereit sind.
ms.assetid: a5174284-2a8c-4510-accf-641fda5be98d
title: Bootstrapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff743acbcd2dfc81b0e912e5be84c363f34614ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356114"
---
# <a name="bootstrapping"></a>Bootstrapping

Derzeit wird bei jeder Installation, die versucht, den Windows Installer zu verwenden, überprüft, ob der Installer auf dem Computer des Benutzers vorhanden ist, und ob er nicht vorhanden ist, ob der Benutzer und der Computer für die Installation Windows Installer bereit sind. Eine Setup-Anwendungs [Instmsi.exe](instmsi-exe.md) ist mit dem Windows Installer SDK verfügbar, das sämtliche Logik und Funktionalität für die Installation Windows Installer enthält. Diese Installation muss jedoch von einer Bootstrapping-Anwendung verwaltet werden.

Die Bootstrapping-Anwendung muss zunächst überprüfen, ob Windows Installer aktuell installiert ist. Anwendungen können die Version von Windows Installer, die derzeit mithilfe von [**dllgetversion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc)installiert wird, erhalten. Wenn Windows Installer zurzeit nicht installiert ist, muss die Bootstrapping-Anwendung das Betriebssystem Abfragen, um zu bestimmen, welche Version des Instmsi.exe erforderlich ist. Nachdem die Installation von Windows Installer initiiert wurde, muss die Bootstrapping-Anwendung Rückgabecodes der Instmsi.exe Anwendung behandeln und jeden Neustart durchführen, der während der Windows Installer Installation durchgeführt wird. Weitere Informationen finden Sie unter [bestimmen der Windows Installer Version](determining-the-windows-installer-version.md) .

Im folgenden Beispiel wird veranschaulicht, wie die Setup Anwendung, die Microsoft Office 2000 installiert, das System des Benutzers überprüft und die Windows Installer Installation konfiguriert. Dieses Beispiel wird speziell für die Installation von Office 2000 geschrieben und sollte nur als allgemeine Referenz verwendet werden.

Wenn ein Benutzer eine Office 2000-CD-ROM in seinen Computer einfügt, Setup.exe versucht, den Wartungsmodus oder die Setup Anwendung zu starten, oder es werden keinerlei Aktionen gemäß den Anforderungen des Benutzers ausgeführt. Im folgenden Abschnitt wird beschrieben, wie die Office 2000-Setup Anwendung namens Setup.exe den Benutzer und seinen Computer qualifiziert, eine Befehlszeile erstellt und Windows Installer mithilfe der Msiexec.exe Anwendung installiert.

## <a name="how-setupexe-bootstraps-the-windows-installer-when-installing-office-2000"></a>Setup.exe Bootstrap des Windows Installer bei der Installation von Office 2000

1.  Der Benutzer fügt eine Office 2000-CD-ROM in den Computer ein. Das Windows-Betriebssystem initiiert Setup.exe mithilfe des Schalters/Autorun und der INF-Datei Autorun. Die Datei Autorun. inf befindet sich im Stammverzeichnis der CD-ROM von Office 2000 und enthält die folgenden Abschnitte:

    \[Auto ausführen\]

     

    \[Office-Features\]

     

    \[Produktinformationen\]

     

    \[Servicepack \] .

    Der \[ Abschnitt Autorun \] enthält eine Befehlszeile, die die Setup.exe Anwendung ausführt, das Symbol zum Anzeigen der Festplatte ausführt und Informationen zum Hinzufügen einer Option "Install" und der Option "configure" (konfigurieren) zum Kontextmenü für die CD-ROM enthält.

    Der \[ Abschnitt Office \] -Features enthält eine Liste der Features und Featurename-Paare.

    Der \[ Abschnitt Produktinformationen \] gibt den Namen und die Version der Anwendung an.

    Im \[ Abschnitt Servicepack \] kann ein Netzwerkadministrator die mindestens erforderliche Service Pack Ebene festlegen. Der Netzwerkadministrator kann diesen Abschnitt verwenden, um den Text einer Warnmeldung zu verfassen, die angezeigt wird, wenn das lokale Betriebssystem nicht über die erforderliche Service Pack verfügt.

    Im folgenden finden Sie ein Beispiel für eine Autorun. inf-Datei.

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

2.  Die Setup.exe-Anwendung überprüft den \_ Mutex msipromptforcd. Windows Installer erstellt diesen Mutex, wenn er den Benutzer zum Einfügen der CD-ROM auffordert. Das vorhanden sein des Mutex gibt an, dass Windows Installer eine Installation durchführt, die die Office 2000-CD-ROM angefordert hat. In diesem Fall wird die Setup.exe Anwendung sofort beendet, sodass die Installation von Office 2000 fortgesetzt werden kann. Wenn der Mutex nicht vorhanden ist, wird die Setup.exe Anwendung mit Schritt 3 fortgesetzt, in dem ein Registrierungsschlüssel ausgewertet wird, um zu bestimmen, ob Office 2000 installiert ist.
3.  Die Setup.exe-Anwendung überprüft das vorhanden sein des Registrierungsschlüssels OFFICE9:

    **HKCU/Software/Microsoft/Office/9.0/common/General/installproductid**

    Wenn dieser Registrierungsschlüssel nicht vorhanden ist, wird die Setup.exe Anwendung mit Schritt 6 fortgesetzt, wobei das Betriebssystem überprüft wird, um festzustellen, ob es für die Installation von Office 2000 qualifiziert ist.

4.  Wenn der Registrierungsschlüssel Office 2000 vorhanden ist, prüft die Setup.exe Anwendung den aktuellen Installationsstatus durch Aufrufen von [**msiqueryproductstate**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea). Der Rückgabestatus von InstallState \_ Default gibt an, dass Office 2000 bereits installiert ist und die Setup.exe Anwendung mit Schritt 5 fortgesetzt wird, wobei Office 2000 für die Verwendung von der Quelle überprüft wird.

    Wenn Office 2000 nicht installiert ist, wird die Setup.exe Anwendung mit Schritt 6 fortgesetzt, wobei das Betriebssystem überprüft wird, um festzustellen, ob es für die Installation von Office 2000 qualifiziert ist.

5.  Die Setup.exe-Anwendung ruft für jede der Features im Abschnitt **\[ \] officefeatures** der Datei Autorun. inf den Wert [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) auf. Wenn eine dieser Features InstallState Source zurückgibt \_ , gibt dies an, dass die Funktion aus der Quelle ausgeführt wird und die Setup.exe Anwendung sofort beendet wird.

    Wenn keines der Features die InstallState-Quelle zurückgibt, wird die \_ Setup.exe Anwendung die installeranwendung gestartet, Msiexec.exe, und der Windows Installer Wartungsmodus vor dem Beenden angezeigt.

6.  Die Setup.exe-Anwendung bestimmt, ob das Betriebssystem für eine Installation von Office 2000 qualifiziert ist. Zum Installieren von Office 2000 ist Windows XP erforderlich. Wenn das Betriebssystem ein Service Pack Update erfordert, um sich für Office 2000 zu qualifizieren, wird in der Setup.exe Anwendung der in der Datei "Autorun. inf" angegebene Text angezeigt. Wenn das Betriebssystem nicht für Office 2000 oder ein Upgrade von Office 2000 qualifiziert ist, wird in der Setup.exe Anwendung eine Meldung angezeigt, die verhindert, dass der Benutzer fortfahren kann.

    Wenn das Betriebssystem für Office 2000 qualifiziert ist, wird die Setup.exe Anwendung mit Schritt 7 fortgesetzt, die bestimmt, ob Windows Installer auf dem Computer des Benutzers installiert ist.

7.  Wenn Windows Installer auf dem Computer des Benutzers vorhanden ist, wird die Msiexec.exe Anwendung von der Setup.exe Anwendung gestartet, und die MSI-Datei von Office 2000 wird an die Anwendung weitergeleitet.

    Wenn Windows Installer nicht auf dem lokalen Computer installiert ist, wird die Setup.exe Anwendung mit Schritt 8 fortgesetzt, die bestimmt, ob das Betriebssystem Windows Installer installiert ist.

8.  Wenn auf dem lokalen Computer Windows Installer installiert ist, führt die Setup.exe Anwendung die richtige Version der Instmsi.exe installeranwendung für die Plattform aus. Setup.exe können den Befehls Zeilenschalter "/q" übergeben, um die Benutzeroberfläche zu unterdrücken und den Benutzer daran zu hindern, Installations Konfigurationsoptionen zu ändern.
9.  Die Setup.exe-Anwendung lädt die neu installierte Msi.dll Datei und führt einen Rückruf für die [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) -Funktion aus, um die Anwendung des Benutzers zu installieren.

## <a name="setupexe-command-line-parameters"></a>Setup.exe Befehlszeilenparameter

Mit der Setup.exe-Anwendung können Administratoren und Benutzer Befehlszeilenoptionen an die Msiexec.exe-Anwendung übergeben. Weitere Informationen finden Sie unter [Befehlszeilenoptionen](command-line-options.md). In der folgenden Tabelle sind die Befehlsoptionen aufgeführt, die mit Setup.exe verwendet werden können.



| Option                       | Verwendung                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /autorun                     | setup.exe/Autorun                                                                                                                           | Führt die oben beschriebene Autorun. inf-Datei aus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| /a                           | setup.exe /a                                                                                                                                 | Initiiert eine administrative Installation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| /j                           | \[u \| m- \] *Paket* oder <br/> \[u \| m- \] *Paket* /t *Transformations Liste*<br/> oder <br/> \[u \| m- \] *Paket* /g *LanguageID*<br/> | Gibt ein Produkt an. Diese Option ignoriert alle Eigenschaftswerte, die in der Befehlszeile eingegeben werden. u ankündigen für den aktuellen Benutzer.<br/> m Ankündigung für alle Benutzer des Computers.<br/> g-sprach Bezeichner<br/> t wendet die Transformation auf das angekündigte Paket an.<br/>                                                                                                                                                                                                                        |
| /I                           | setup.exe/I Office9.msi/t Program GMT. MST                                                                                                  | Gibt die MSI-Datei an, die Setup.exe installieren soll. Wenn die/I-Option nicht enthalten ist, verwendet Setup.exe die Office9.msi-Datei.                                                                                                                                                                                                                                                                                                                                                                                 |
| /o<- *Eigenschafts* = *Wert*> | setup.exe/o cdkey = 111111-1111                                                                                                               | Legt Eigenschaften in der MSI-Datei fest. Setup.exe übergibt diese an msiexec wie geschrieben.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| /q                           | setup.exe/q                                                                                                                                 | Legen Sie die Benutzeroberflächen Ebene der Installation fest. /q keine Benutzeroberfläche (/qn für msiexec.)/QB grundlegende Benutzeroberfläche<br/> /QR reduzierte Benutzeroberfläche.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| /m\#                         | setup.exe/M4                                                                                                                                | Unterstützt mehrere Lizenzen in Übereinstimmung mit SELECT-Verträgen. Diese Eigenschaft wird in von der benutzerdefinierten Aktion Lizenz Überprüfung zum Schreiben des LV-Zertifikats verwendet. Auf die/m-Option muss die Anzahl der zulässigen Sperre folgen. Der durch die Option/m angegebene Wert sollte in der Office9.msi Datei als "m"-Eigenschaft festgelegt werden. Wenn kein Wert angegeben wird, aber die Option/m bei der Installation verwendet wird, sollte der Wert 0 festgelegt werden. Die Option/m ist erforderlich, um SELECT-Kunden mithilfe einer CD oder eines Netzwerks zu unterstützen. |
| /Settings                    | setup.exe/Settings mysettings.ini                                                                                                           | Ermöglicht es Administratoren, eine INI-Datei anzugeben, die alle angepassten Einstellungen enthält, die während des Setups von Office 2000 übermittelt werden sollen. Weitere Informationen finden Sie unten in der Beschreibung der INI-Datei.                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="using-an-ini-file"></a>Verwenden einer INI-Datei

Das Erstellen einer Initialisierungsdatei ist möglicherweise einfacher als das Erstellen einer langen Befehlszeile. Mithilfe der Option/Settings liest die Setup.exe Anwendung die angegebene ini-Datei und erstellt eine Befehlszeile, die an die Msiexec.exe Anwendung übergeben werden soll. In der INI-Datei werden nur Eigenschaften unterstützt, die in der Befehlszeile unterstützt werden. Wenn eine Eigenschaft oder ein Wert sowohl in der INI-Datei als auch in der Befehlszeile gefunden wird, überschreiben die Befehlszeilen Einstellungen die INI-Datei Einstellungen.

Das Format der INI-Datei lautet wie folgt:

\[MSI\]

 

\[MST\]

 

\[options\]

 

\[Display\]

Der \[ MSI- \] Abschnitt der INI-Datei gibt den Pfad zum Installationspaket für die Installation an. Dies entspricht der/I-Option in der Befehlszeile.

Der \[ MST- \] Abschnitt der INI-Datei gibt den Pfad zu den Transformationen an, die bei dieser Installation verwendet werden. Dies entspricht der/j-Option in der Befehlszeile. Mehrere Transformationen werden jeweils in einer anderen Zeile angegeben, wobei MST1 MST (N) verwendet wird. Wenn die Liste in der Befehlszeile analysiert wird, wird die Liste in der INI-Datei von links nach rechts angezeigt. Beachten Sie, dass die dem MST (N)-Titel zugeordnete Nummer nur vorhanden ist, um eindeutige Bezeichner zu verwalten, und keine programmatische Bedeutung hat.

Im \[ \] Abschnitt Optionen können Netzwerkadministratoren Eigenschaften in den MSI-oder MST-Dateien festlegen und überschreiben. Die in der INI-Datei festgelegten Optionen werden mithilfe der/o-Option der Befehlszeile hinzugefügt. Jede Option im Options Abschnitt muss einen Eigenschaftsnamen und einen-Wert aufweisen.

Der \[ Anzeige \] Abschnitt wird verwendet, um die Benutzeroberflächen Ebene festzulegen, die während des Setups verwendet wird. Dies entspricht der/q-Option in der Befehlszeile. Gültige Werte sind None, Basic, Reduced und Full.

Datei "Sample. ini"

\[MSI\]

 

MSI = \\ \\ sourceshare \\ Office2000 \\Office2000.msi

 

\[MST\]

 

MST1 = \\ \\ sourceshare \\ Office2000 \\ trns1. MST

 

MST2 = \\ \\ sourceshare \\ Office2000 \\ trns2. MST

 

\[Optionen\]

 

PublicProperty = ihr Wert

\[Display\]

 

Display = None

 

