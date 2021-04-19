---
description: Das Beispiel PUASample.msi ist ein Beispiel für ein Paket mit zwei Zweck Windows Installer 5,0, das entweder im Benutzer-oder computerspezifischen Installations Kontext unter Windows Server 2008 R2 und Windows 7 installiert werden kann.
ms.assetid: be018e8a-ca5f-4135-a019-970ec4173f23
title: Beispiel für eine einmalige Paket Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0ed56b8d7aaf8793416ba3ecab24c1f2a48ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356282"
---
# <a name="single-package-authoring-example"></a>Beispiel für eine einmalige Paket Erstellung

Das Beispiel PUASample.msi ist ein Beispiel für ein Paket mit zwei Zweck Windows Installer 5,0, das entweder im Benutzer-oder computerspezifischen [Installations Kontext](installation-context.md) unter Windows Server 2008 R2 und Windows 7 installiert werden kann. Dieses Beispiel Paket folgt den Entwicklungs Richtlinien, die unter [Erstellung eines einzelnen Pakets](single-package-authoring.md)beschrieben werden.

## <a name="obtaining-a-copy-of-the-sample"></a>Abrufen einer Kopie des Beispiels

Eine Kopie dieses Beispiels und eine Windows Installer Datenbanktabellen-Editor Orca.exe finden Sie in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md). Der Beispiel-und Tabellen-Editor wird mit dem Windows Software Development Kit für Windows Server 2008 R2 und Windows 7 als Windows Installer Installationsdateien PUASample1.msi und Orca.msi bereitgestellt.

## <a name="system-requirements"></a>Systemanforderungen

Der-Daten Bank Editor ( [Orca.exe](orca-exe.md)) erfordert Windows Server 2008 R2 und früher sowie Windows 7 und früher. Das Dual-Purpose-Paket (PUASample1.msi) kann entweder im Computer-oder benutzerspezifischen [Installations Kontext](installation-context.md) unter Windows Server 2008 R2 und Windows 7 installiert werden. PUASample1.msi können nur im Einzel Computer Kontext auf Windows Server 2008 und früher sowie in Windows Vista und früher installiert werden. Sie können den Daten Bank Editor installieren, um die Inhalte PUASample1.msi zu untersuchen, ohne das Beispiel zu installieren. Stellen Sie sicher, dass die [DisableMSI](disablemsi.md) -Richtlinie nicht auf einen Wert festgelegt ist, der Anwendungs Installationen blockiert, um die Beispiel-oder Editor Pakete zu installieren.

## <a name="identifying-a-dual-purpose-package"></a>Identifizieren eines Dual-Purpose Pakets

Pakete mit zwei Zweck sollten den Wert der [**msiinstallperuser**](msiinstallperuser.md) -Eigenschaft auf 1 initialisieren. Dadurch wird festgelegt, dass das Paket entweder im Computer-oder benutzerspezifischen Kontext unter Windows Server 2008 R2 und Windows 7 installiert werden konnte. Legen Sie die **msiinstallperuser** -Eigenschaft im Paket nur dann fest, wenn Sie gemäß den in [Single Package Authoring](single-package-authoring.md) beschriebenen Entwicklungs Richtlinien geschrieben wurde, und wenn Sie Benutzern die Möglichkeit geben möchten, das Paket entweder im Benutzer-oder computerspezifischen Kontext zu installieren. Ein Paket mit zwei Zwecken sollte auch den Wert der Eigenschaft " [**ALLUSERS**](allusers.md) " auf "2" initialisieren. Hiermit wird pro Benutzer als Standard Installations Kontext für die Anwendung angegeben. Wenn der Wert der **ALLUSERS** -Eigenschaft ein anderer Wert als 2 ist, ignoriert Windows Installer die **msiinstallperuser** -Eigenschaft.

Verwenden Sie einen Windows Installer Datenbank-Editor, z. b. [Orca.exe](orca-exe.md), um den Inhalt von PUASample1.msi zu überprüfen. Die [Eigenschaften](property-table.md) Tabelle im Beispiel Paket enthält die folgenden zwei Einträge.

[Eigenschaft](property-table.md) Tabelle (teilweise)

| Eigenschaft          | Wert |
|-------------------|-------|
| ALLUSERS          | 2     |
| Msiinstallperuser | 1     |



 

## <a name="custom-dialog-box-for-installation-context"></a>Benutzerdefiniertes Dialog Feld für den Installations Kontext

Die [Benutzeroberfläche](user-interface.md) des Beispiel Pakets enthält ein Beispiel für ein benutzerdefiniertes Dialogfeld, "verifyleseydialog", das es Benutzern ermöglicht, während der Installation entweder den Einzelbenutzer-oder computerspezifischen Installations Kontext auszuwählen. Die [Dialog](dialog-table.md) Feld Tabelle enthält einen Datensatz, der das Dialogfeld verifyread ydialog beschreibt. Der im Feld Attribute eingegebene Wert ist 39, weil in diesem Dialogfeld die Felder msidbdialogattributesvisible (1), msidbdialogattributesmodal (2), msidbdialogattributesminimum (4) und msidbdialogattributestrackdiskspace (32) [Dialogfelder](dialog-style-bits.md)verwendet werden. In der Titelleiste des Dialog Felds wird ein Titel angezeigt, der durch den Wert der [**ProductName**](productname.md) -Eigenschaft angegeben wird.

[Dialog](dialog-table.md) Feld Tabelle (teilweise) 

| Dialog            | Hcentering | Vcentering | Breite | Höhe | Attribute | Titel           | \_Zuerst Steuern | Standard Steuerelement \_ | Abbrechen von Steuerelementen \_ |
|-------------------|------------|------------|-------|--------|------------|-----------------|----------------|------------------|-----------------|
| Verifyleserdialog | 50         | 50         | 480   | 280    | 39         | \[ProductName\] | Installperuser | Nächste             | Abbrechen          |



 

Die [Steuer](control-table.md) Element Tabelle enthält Einträge für die Steuer [Elemente](controls.md) , die im Dialogfeld verifylesdialog angezeigt werden. Das Dialogfeld zeigt [PUSHBUTTON](pushbutton-control.md) -Steuerelemente und ein [Text](text-control.md) Steuerelement an. Alle-Steuerelemente verwenden das msidbcontrolattributesaktivierte-Attribut (2) und das msidbcontrolattributesvisible (1)- [Steuer](control-attributes.md)Element. Das installpermachine-Steuerelement verwendet auch das [elevationshield](elevationshield-attribute.md) -Steuerelement Attribut msidbcontrolattributeselevationshield (8388608). Dieses Steuerelement fügt dem installpermachine-Steuerelement das Symbol für die Rechte Erweiterung der [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) hinzu und informiert den Benutzer darüber, dass die UAC-Anmelde Informationen erforderlich sind, um die Anwendung im computerspezifischen Kontext zu installieren. Der Wert im Textfeld der Steuerelement Tabelle ist der Text Stil und der Text, der vom Steuerelement angezeigt wird. Weitere Informationen zum Hinzufügen von Text zu einem Steuerelement mithilfe vordefinierter Stile finden Sie in der Beschreibung des Textfelds im Thema Control Table.

[Steuer](control-table.md) Element Tabelle (teilweise)

| Dialog\_          | Control           | type       | attribute | Text                                                   | Nächstes Steuerelement \_     |
|-------------------|-------------------|------------|-----------|--------------------------------------------------------|-------------------|
| Verifyleserdialog | Abbrechen            | PUSHBUTTON | 3         | { \\ Tahoma10} &Abbrechen                                    | Nächste              |
| Verifyleserdialog | Vorherige          | PUSHBUTTON | 3         | { \\ Tahoma10} <<&vorherige                          | Abbrechen            |
| Verifyleserdialog | Nächste              | PUSHBUTTON | 3         | { \\ Tahoma10} &nächste >>                             | Installperuser    |
| Verifyleserdialog | Text2             | Text       | 3         | Sind Sie bereit, die angehaltene Installation abzuschließen? |                   |
| Verifyleserdialog | Installperuser    | PUSHBUTTON | 3         | { \\ Tahoma10} nur für &Me installieren                       | Installpermachine |
| Verifyleserdialog | Installpermachine | PUSHBUTTON | 8388611   | { \\ Tahoma10} Installation für &alle                      | Vorherige          |
| Verifyleserdialog | Abbrechen            | PUSHBUTTON | 3         | { \\ Tahoma10} &Abbrechen                                    | Nächste              |



 

Die [ControlEvent](controlevent-table.md) -Tabelle gibt die [ControlEvents](control-events.md)oder Aktionen an, die das Installationsprogramm ausführt, wenn der Benutzer mit einem-Steuerelement interagiert. Wenn ein Benutzer die PUSHBUTTON-Taste von installperuser aktiviert, zeigt die Benutzeroberfläche ein Dialogfeld für den outefdisk an, wenn die [**outefdiskspace**](outofdiskspace.md) -Eigenschaft den Wert 1 aufweist, den Wert der Eigenschaft " [**msiinstallperuser**](msiinstallperuser.md) " auf 1 festlegt, den Wert der Eigenschaft " [**ALLUSERS**](allusers.md) " auf "2" festlegt, die Eigenschaft " [**msifastinstall**](msifastinstall.md) " Da die **msifastinstall** -Eigenschaft festgelegt ist, wird kein System Wiederherstellungspunkt für die Installation generiert. Wenn ein Benutzer die PUSHBUTTON-Taste von installpermachine aktiviert, zeigt die Benutzeroberfläche ein Dialogfeld für das outefdisk an, wenn die **ouesfdiskspace** -Eigenschaft den Wert 1 aufweist, den Wert der **ALLUSERS** -Eigenschaft auf 1 festgelegt und zurückgegeben wird.

[ControlEvent](controlevent-table.md) Tabelle (teilweise) 

| Dialog\_          | Steuerelement\_         | Ereignis                 | Argument  | Bedingung                 | Auftrag |
|-------------------|-------------------|-----------------------|-----------|---------------------------|-------|
| Verifyleserdialog | Installperuser    | Spawndialog           | Outo-Disk | Ausgabebereich = 1        | 1     |
| Verifyleserdialog | Installperuser    | EndDialog             | Rückgabewert    | Ouesf Disk Space <> 1 | 5     |
| Verifyleserdialog | Installperuser    | \[Msiinstallperuser\] | 1         | 1                         | 2     |
| Verifyleserdialog | Installperuser    | \[ALLUSERS\]          | 2         | 1                         | 3     |
| Verifyleserdialog | Installpermachine | Spawndialog           | Outo-Disk | Ausgabebereich = 1        | 1     |
| Verifyleserdialog | Installpermachine | EndDialog             | Rückgabewert    | Ouesf Disk Space <> 1 | 3     |
| Verifyleserdialog | Installpermachine | \[ALLUSERS\]          | 1         | 1                         | 2     |
| Verifyleserdialog | Installperuser    | \[Msifastinstall\]    | 1         | 1                         | 4     |



 

Das installperuser-Steuerelement sollte von der Benutzeroberfläche einer beliebigen Installation mithilfe einer Windows Installer Version vor Windows Installer Windows Installer 5,0 entfernt werden. Die Tabelle [ControlCondition](controlcondition-table.md) im Beispiel Paket enthält vier Einträge, die das installperuser-Steuerelement deaktivieren und ausblenden, wenn die aktuelle Version kleiner als Windows Installer 5,0 ist. Die Tabelle verwendet den Wert der [**versionmsi**](versionmsi.md) -Eigenschaft und die [Syntax der bedingten Anweisung](conditional-statement-syntax.md) , um diese Bedingung zu definieren. Die im Feld "Aktion" angegebene Aktion wird nur ausgeführt, wenn die Anweisung im Feld "Bedingung" den Wert "true" hat.

[ControlCondition](controlcondition-table.md) Tabelle (teilweise)

| Dialog\_          | Steuerelement\_      | Aktion  | Bedingung               |
|-------------------|----------------|---------|-------------------------|
| Verifyleserdialog | Installperuser | Aktivieren  | Versionmsi->= "5,00" |
| Verifyleserdialog | Installperuser | Deaktivieren | Versionmsi-< "5,00"  |
| Verifyleserdialog | Installperuser | Anzeigen    | Versionmsi->= "5,00" |
| Verifyleserdialog | Installperuser | Ausblenden    | Versionmsi-< "5,00"  |



 

## <a name="specifying-directory-structure"></a>Angeben der Verzeichnisstruktur

Verwenden Sie den Datenbank-Editor, um die [Verzeichnis](directory-table.md) Tabelle PUASample1.msi zu überprüfen. Der Datensatz der Verzeichnis Tabelle mit einer leeren Zeichenfolge im übergeordneten Verzeichnis des Verzeichnisses \_ stellt das Stammverzeichnis der Quell-und Zielverzeichnis Strukturen dar. Wenn die [**TARGETDIR**](targetdir.md) -Eigenschaft nicht definiert ist, legt das Installationsprogramm den Wert zum Zeitpunkt der Installation auf den Wert der [**ROOTDRIVE**](rootdrive.md) -Eigenschaft fest. Wenn die [**SourceDir**](sourcedir.md) -Eigenschaft nicht definiert ist, legt der Installer den Wert auf den Speicherort des Verzeichnisses fest, das das Windows Installer Paket (MSI-Datei) enthält. Die Verzeichnisnamen werden mit dem kurzen \| langen Format angegeben.

[Verzeichnis](directory-table.md) Tabelle (teilweise)

| Verzeichnis          | Über \_ geordnetes Verzeichnis  | DefaultDir               |
|--------------------|--------------------|--------------------------|
| TARGETDIR          |                    | SourceDir                |
| ProgramFilesFolder | TARGETDIR          | .                        |
| Programmmenufolder  | TARGETDIR          | .                        |
| INSTALLLOCATION    | Myvendor           | Sample1 \| MSDN-PUASample1 |
| Myvendor           | ProgramFilesFolder | MSFT \| Microsoft          |



 

An der Quelle wird diese [Verzeichnis](directory-table.md) Tabelle in die folgenden Verzeichnispfade aufgelöst.

<dl> \[SourceDir \] \\ MSFT \\ sample1  
\[SourceDir\]  
</dl>

Am Ziel wird die [Verzeichnis](directory-table.md) Tabelle in die Pfade in der folgenden Tabelle aufgelöst. Der Installer legt die Werte der Eigenschaften [**ProgramFilesFolder**](programfilesfolder.md) und [**ProgramMenuFolder**](programmenufolder.md) auf Positionen fest, die vom [Installations Kontext](installation-context.md) abhängen, und ob es sich um die 32-Bit-oder die 64-Bit-Version von Windows Server 2008 R2 und Windows 7 handelt. Die Pfade zu den Ziel Ordnern hängen davon ab, ob der Benutzer eine Installation pro Benutzer oder pro Computer auswählt.

| Installations Kontext | System                                                                              | Beispiel Pfade                                                                                                                    |
|----------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows 2008 R2 und Windows Server 7<br/> 32-Bit-Version<br/>           | % Program Files% \\ MSFT \\ sample1<br/> % ALLUSERSPROFILE% \\ Microsoft \\ Windows- \\ Startmenü \\ Programme<br/>                  |
| Per-Machine          | Windows 2008 R2 und Windows Server 7<br/> 64-Bit-Version<br/>           | % Program Files (x86)% \\ MSFT \\ sample1<br/> % ALLUSERSPROFILE% \\ Microsoft \\ Windows- \\ Startmenü \\ Programme<br/>             |
| Per-User             | Windows 2008 R2 und Windows Server 7<br/> 32-Bit-oder 64-Bit-Version<br/> | % User Profile% \\ AppData \\ lokale \\ Programme \\ MSFT \\ sample1<br/> % APPDATA% \\ Microsoft \\ Windows- \\ Startmenü \\ Programme<br/> |



 

Anwendungen pro Benutzer sollten in Unterordnern unter dem Ordner "Programme" gespeichert werden, der durch den Wert der [**ProgramFilesFolder**](programfilesfolder.md) -Eigenschaft angegeben wird. In der Regel hat der Pfad zur Anwendung die folgende Form.

% LocalAppData% \\ Programme \\ *ISV Name* \\ *appname*.

Benutzerspezifische Konfigurationsdaten sollten im Ordner "Programme" gespeichert werden, der durch den Wert der [**ProgramMenuFolder**](programmenufolder.md) -Eigenschaft angegeben wird. In der Regel befindet sich dieser Ordner im folgenden Pfad.

% APPDATA% \\ Microsoft \\ Windows- \\ Startmenü \\ Programme

Wenn Sie [32-Bit-Windows Installer Paket](32-bit-windows-installer-packages.md) Komponenten installieren, verwenden Sie die [**ProgramFilesFolder**](programfilesfolder.md) -Eigenschaft und die [**CommonFilesFolder**](commonfilesfolder.md) -Eigenschaft in der [Verzeichnis](directory-table.md) Tabelle. Verwenden Sie die Eigenschaften [**ProgramFiles64Folder**](programfiles64folder.md) und [**CommonFiles64Folder**](commonfiles64folder.md) , wenn Sie [64-Bit-Windows Installer Paket](64-bit-windows-installer-packages.md) Komponenten installieren. Wenn Ihre Anwendung 32-Bit-und 64-Bit-Versionen derselben Komponente mit dem gleichen Namen enthält, stellen Sie sicher, dass diese Versionen in verschiedenen Verzeichnissen gespeichert werden, oder weisen Sie Ihnen unterschiedliche Namen zu.

In der folgenden [Verzeichnis](directory-table.md) Tabelle finden Sie ein Beispiel für ein Verzeichnis Layout, das mit einem-Paket kompatibel ist, das 32-Bit-und 64-Bit-Komponenten enthält und einige Komponenten umfasst, die Anwendungs übergreifend gemeinsam genutzt werden.

| Verzeichnis            | Über \_ geordnetes Verzeichnis    | DefaultDir                        |
|----------------------|----------------------|-----------------------------------|
| TARGETDIR            |                      | SourceDir                         |
| ProgramFilesFolder   | TARGETDIR            | .:P rog32                          |
| ProgramFiles64Folder | TARGETDIR            | .:P rog64                          |
| CommonFilesFolder    | TARGETDIR            | .:Share32                         |
| CommonFiles64Folder  | TARGETDIR            | .:Share64                         |
| Programmmenufolder    | TARGETDIR            | .: Sample1 \| MSDN-PUASample1        |
| INSTALLLOCATION      | Myvendor             | Sample1 \| MSDN-PUASample1          |
| INSTALLLOCATIONX64   | Vendorx64            | Sample1 \| MSDN-PUASample1          |
| Sharedlocation       | Shvendor             | Sample1 \| MSDN-PUASample1          |
| SHAREDLOCATIONX64    | ShVendorx64          | Sample1 \| MSDN-PUASample1          |
| Myvendor             | ProgramFilesFolder   | MSFT \| Microsoft                   |
| Vendorx64            | ProgramFiles64Folder | MSFT \| Microsoft                   |
| Shvendor             | CommonFilesFolder    | MSFT \| Microsoft                   |
| ShVendorx64          | CommonFiles64Folder  | MSFT \| Microsoft                   |
| Shrx86               | Sharedlocation       | x32 \| 32-Bit-Komponenten            |
| Shrx64               | SHAREDLOCATIONX64    | x64 \| 64-Bit-Komponenten            |
| Binx86               | INSTALLLOCATION      | x32 \| 32-Bit-Komponenten            |
| Binx64               | INSTALLLOCATIONX64   | x64 \| 64-Bit-Komponenten            |
| App32                | Binx86               | \|nicht freigegebene MyApp-32-Bit-Komponenten |
| App64                | Binx64               | \|nicht freigegebene MyApp-64-Bit-Komponenten |
| Share32              | Shrx86               | \|freigegebene freigegebene 32-Bit-Komponenten  |
| Share64              | Shrx64               | \|freigegebene freigegebene 64-Bit-Komponenten  |



 

An der Quelle wird diese [Verzeichnis](directory-table.md) Tabelle in die folgenden Verzeichnispfade aufgelöst.

<dl> \[SourceDir \] Prog32 \\ MSFT \\ sample1 \\ x32 \\ myapp  
\[SourceDir \] Share32 \\ Allgemeine Dateien \\ MSFT \\ sample1 \\ x32 \\ Shared  
\[SourceDir \] Prog64 \\ MSFT \\ sample1 \\ x64 \\ myapp  
\[SourceDir \] Share64 \\ Allgemeine Dateien \\ MSFT \\ sample1 \\ x64 \\ Shared  
\[SourceDir \] sample1  
</dl>

Am Ziel wird diese [Verzeichnis](directory-table.md) Tabelle in die folgenden Verzeichnispfade aufgelöst. Die Zielpfade hängen vom [Installations Kontext](installation-context.md) und dem System ab.

| Installations Kontext | System                                                                              | Beispiel Pfade                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows 2008 R2 und Windows Server 7<br/> 32-Bit-Version<br/>           | % Program Files% \\ MSFT \\ sample1 \\ x32 \\ myapp<br/> % Program Files% \\ Allgemeine Dateien \\ MSFT \\ sample1 \\ x32 \\ Shared<br/> % Program Files (x86)% \\ MSFT \\ sample1 \\ x64 \\ myapp<br/> % Program Files (x86)% \\ Allgemeine Dateien \\ MSFT \\ sample1 \\ x64 \\ Shared<br/> % Program Data% \\ Microsoft \\ Windows- \\ Startmenü \\ Programme \\ sample1<br/>               |
| Per-Machine          | Windows 2008 R2 und Windows Server 7<br/> 64-Bit-Version<br/>           | % Program Files (x86)% \\ MSFT \\ sample1 \\ x32 \\ myapp<br/> % Program Files (x86)% \\ Allgemeine Dateien \\ MSFT \\ sample1 \\ x32 \\ Shared<br/> % Program Files% \\ MSFT \\ sample1 \\ x64 \\ myapp<br/> % Program Files% \\ Allgemeine Dateien \\ MSFT \\ sample1 \\ x64 \\ Shared<br/> % Program Data% \\ Microsoft \\ Windows- \\ Startmenü \\ Programme \\ sample1<br/>               |
| Per-User             | Windows 2008 R2 und Windows Server 7<br/> 32-Bit-oder 64-Bit-Version<br/> | % LocalAppData% \\ Programme \\ MSFT \\ sample1 \\ x32 \\ myapp<br/> % LocalAppData% \\ Programme \\ Common \\ MSFT \\ sample1 \\ x32 \\ Shared<br/> % LocalAppData% \\ Programme \\ MSFT \\ sample1 \\ x64 \\ myapp<br/> % LocalAppData% \\ Programme \\ Common \\ MSFT \\ sample1 \\ x64 \\ Shared<br/> % APPDATA% \\ Microsoft \\ Windows- \\ Startmenü \\ Programme \\ sample1<br/> |



 

## <a name="application-registration"></a>Anwendungs Registrierung

Der PUASample.msi fügt dem Registrierungsschlüssel für die APP-Pfade einen Unterschlüssel für die Anwendung hinzu und führt Registrierungen durch, mit denen die Anwendungsinformationen in der Registrierung unter diesem Schlüssel gespeichert werden können. Weitere Informationen zu app-Pfaden und zur Anwendungs Registrierung finden Sie im Abschnitt zur [shellerweiterbarkeit](https://msdn.microsoft.com/library/bb762762.aspx) des [Shell-Entwickler Handbuchs](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85))im Abschnitt zum Anzeigen von Daten [Typen, systemfilezuordnungen und Anwendungs](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)) Registrierung. Zum Installations Zeitpunkt trifft der Benutzer die Entscheidung, die Anwendung entweder im Benutzer-oder computerspezifischen Installations Kontext zu installieren. Zum Zeitpunkt der Erstellung des Pakets mit zwei Zweck kann der Paket Entwickler nicht wissen, ob die Registrierungen unter den aktuellen HKEY- \_ Computern \_ oder aktuellen HKEY \_ - \_ Benutzer Schlüsseln durchgeführt werden sollen.

Der Paket Entwickler definiert den Datei Bezeichner für die ausführbare Datei der Anwendung im Feld Datei der [Datei](file-table.md) Tabelle.

[Datei](file-table.md) Tabelle (teilweise) 

| File      | Komponente\_      | FileName                     | FileSize | Version | Sprache | Attribute | Sequenz |
|-----------|------------------|------------------------------|----------|---------|----------|------------|----------|
| Myappfile | Productcomponent | PUASAMP1.EXE\|PUASample1.exe | 81920    |         |          | 0          | 1        |



 

Werte, die in der Registrierung gespeichert werden sollen, können im Wertfeld der [Registrierungs](registry-table.md) Tabelle als [formatierte](formatted.md) Zeichenfolge angegeben werden. Verwenden Sie den Datei Bezeichner, der im Feld Datei der [Datei](file-table.md) Tabelle definiert ist, und die \[ \# *filekey* - \] Konvention des formatierten Typs, um den Standardwert für den Registrierungsschlüssel für App-Pfade anzugeben. Die [Installations](install-action.md) Aktion der obersten Ebene führt die Aktionen in der [InstallExecuteSequence](installexecutesequence-table.md) -Tabelle aus. Nachdem die Aktionen " [costinitialize](costinitialize-action.md)", " [filecost](filecost-action.md)" und " [InstallFinalize](installfinalize-action.md) " in dieser Tabelle abgeschlossen wurden, ersetzt die Windows Installer die formatierte Teil Zeichenfolge " \[ \# myappfile" \] in der Registrierungs Tabelle durch den vollständigen Pfad zur Anwendungsdatei.

Das Beispiel definiert eine benutzerdefinierte Eigenschaft (regroot), die den Speicherort des Stamm Schlüssels enthält, und verwendet eine benutzerdefinierte Aktion, um den Eigenschafts Wert zurückzusetzen, wenn der Benutzer eine Installation pro Computer auswählt. Verwenden Sie die benutzerdefinierte Eigenschaft regroot in allen formatierten Zeichen folgen Werten, die auf den Stamm Speicherort verweisen. In der [Eigenschafts](property-table.md) Tabelle definiert das PUASample.msi Paket die benutzerdefinierte Eigenschaft und legt den Wert von regroot auf HKCU fest. Dies initialisiert den Wert der-Eigenschaft für den pro-Benutzer-Installations Kontext, den empfohlenen Standardkontext für Pakete mit zwei Zweck.

[Eigenschaft](property-table.md) Tabelle (teilweise)

| Eigenschaft | Wert |
|----------|-------|
| Regroot  | HKCU  |



 

In der Tabelle [CustomAction](customaction-table.md) definiert das Paket eine benutzerdefinierte Aktion namens Set \_ regroot \_ HKLM. Der Wert im type-Feld identifiziert dies als [benutzerdefinierte Action Type 51](custom-action-type-51.md) -Standardaktion. Die Bedeutung der Quell-und Zielfelder in der Tabelle "CustomAction" hängt vom benutzerdefinierten Aktionstyp ab. Weitere Informationen zu den Standardtypen von benutzerdefinierten Aktionen finden Sie unter [benutzerdefinierte Aktions Typen](summary-list-of-all-custom-action-types.md). Das Quellfeld für die \_ benutzerdefinierte Aktion Set regroot \_ HKLM gibt an, dass der Wert der regroot-Eigenschaft ist. Wenn das Installationsprogramm die \_ benutzerdefinierte Aktion "Set regroot \_ HKLM" ausführt, wird der Wert der Eigenschaft regroot auf HKLM zurückgesetzt.

[CustomAction](customaction-table.md) Tabelle (teilweise)

| Aktion             | type | `Source`      | Ziel |
|--------------------|------|-------------|--------|
| Festlegen von \_ regroot \_ HKLM | 51   | \[Regroot\] | HKLM   |



 

Die [Installations](install-action.md) Aktion der obersten Ebene führt die Aktionen in der [InstallExecuteSequence](installexecutesequence-table.md) -Tabelle in der Sequenz aus, die im Sequenz Feld der Tabelle angegeben ist. Der Wert, der im Sequenz Feld für die \_ benutzerdefinierte Aktion "Set regroot \_ HKLM" (1501) erstellt wurde, gibt an, dass diese benutzerdefinierte Aktion nach der [installinitialisierungs](installinitialize-action.md) Aktion (1500) und vor der [processcomponents](processcomponents-action.md) -Aktion (1600.) ausgeführt wird. Durch diese Sequenz wird sichergestellt, dass der Datensatz für die \_ benutzerdefinierte Aktion "Set regroot \_ HKLM" zur Installationszeit ausgewertet wird. Weitere Informationen zur empfohlenen Sequenz von Aktionen in der InstallExecuteSequence-Tabelle finden Sie im Thema [Empfohlene InstallExecuteSequence](suggested-installexecutesequence.md) -Tabelle. Die im Bedingungs Feld erstellte [bedingte Anweisungs Syntax](conditional-statement-syntax.md) gibt an, dass die Set \_ regroot \_ HKLM-Aktion nur ausgeführt werden soll, wenn der Wert der [**ALLUSERS**](allusers.md) -Eigenschaft zum Zeitpunkt 1 zur Installation ausgewertet wird. Der Wert 1 der **ALLUSERS** -Eigenschaft gibt eine Installation pro Computer an.

[InstallExecuteSequence](installexecutesequence-table.md) Tabelle (teilweise)

| Aktion             | Bedingung  | Sequenz |
|--------------------|------------|----------|
| Festlegen von \_ regroot \_ HKLM | ALLUSERS = 1 | 1501     |



 

Die folgenden Datensätze in der [Registrierungs](registry-table.md) Tabelle führen die Registrierungen aus, wenn die productcomponent-Komponente installiert ist. Der Wert "-1" im Feld "root" ist erforderlich, um die Registrierung unter HKEY \_ local \_ Machine für eine Installation pro Benutzer und unter HKEY \_ Current \_ User für eine Installation pro Benutzer auszuführen. Der Datensatz mit einer leeren Zeichenfolge im Registrierungs Feld fügt dem Registrierungsschlüssel apppaths einen Unterschlüssel für die Anwendung hinzu und legt den Wert "(Standard)" auf den vollständigen Pfad der ausführbaren Datei der Anwendung fest. Die myapppathalias-Registrierung ordnet die ausführbare Datei einem Anwendungsalias zu und ermöglicht das Starten der Anwendung, wenn der Benutzer den Alias "puapct" an einer Eingabeaufforderung eingibt. Die myapppathregistration-Registrierung ordnet den Namen der ausführbaren Datei dem vollständigen Pfad der Datei zu.



| Registrierung              | Root | Schlüssel                                                                     | Name | Wert                                                                            | Komponente        |
|-----------------------|------|-------------------------------------------------------------------------|------|----------------------------------------------------------------------------------|------------------|
|                       | -1   | Software \\ Microsoft \\ myapppathregistrationlocation                      |      | \[Regroot \] \\ Software \\ Microsoft \\ Windows \\ CurrentVersion- \\ App-Pfade \\PUAPCT.exe | Productcomponent |
| Myapppathalias        | -1   | Software \\ Pfade der Microsoft \\ Windows \\ CurrentVersion- \\ App \\PUAPCT.exe     |      | \[\#Myappfile\]                                                                  | Productcomponent |
| Myapppathregistration | -1   | Software \\ Pfade der Microsoft \\ Windows \\ CurrentVersion- \\ App \\PUASample1.exe |      | \[\#Myappfile\]                                                                  | Productcomponent |



 

## <a name="autoplay-cancel-registration"></a>Automatische AutoPlay-Registrierung

Der PUASample.msi führt Registrierungen durch, mit denen der Anwendungs Benutzer verhindern kann, dass die automatische Wiedergabe von [Hardware](/previous-versions/windows/desktop/legacy/cc144210(v=vs.85)) für ausgewählte Geräte gestartet wird. Informationen zum Registrieren eines Handlers zum Abbrechen von AutoPlay als Reaktion auf ein Ereignis finden Sie im Abschnitt " [Vorbereiten der Hardware und Software für die Verwendung mit](/previous-versions//cc144208(v=vs.85)) der automatischen Verwendung" im Abschnitt zur [shellerweiterbarkeit](https://msdn.microsoft.com/library/bb762762.aspx) des [shellentwicklerhandbuchs](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). Der folgende Datensatz registriert den Handler, der im Feld "Name" angegeben ist, wenn die productcomponent-Komponente installiert ist. Der Wert "-1" im Feld "root" ist erforderlich, um Windows Installer anzugeben, dass die Registrierung an einen Speicherort umgeleitet werden soll, der vom Installations Kontext abhängig ist.

[Registrierung](registry-table.md) Glaub 

| Registrierung                     | Root | Schlüssel                                                                                             | Name                                 | Wert | Komponente        |
|------------------------------|------|-------------------------------------------------------------------------------------------------|--------------------------------------|-------|------------------|
| Myautoplaycancelregistration | -1   | Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ autoplayhandlers \\ cancelautoplay \\ CLSID | 66a32fe6-229d-427b-A608-d273f 40c034c |       | Productcomponent |



 

## <a name="preview-handler-registration"></a>Vorschau der Handlerregistrierung

Der PUASample.msi führt Registrierungen aus, die für die Installation eines [Vorschau Handlers](../shell/preview-handlers.md) erforderlich sind, der eine schreibgeschützte Vorschau von. Pua-Dateien ermöglicht, ohne die Anwendung zu starten. Informationen zum Registrieren von Vorschau Handlern finden Sie im Thema zum [Registrieren von Vorschau Handlern](../shell/how-to-register-a-preview-handler.md) im Abschnitt [shellerweiterbarkeit](https://msdn.microsoft.com/library/bb762762.aspx) des [Shell-Entwickler Handbuchs](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). Die folgenden Datensätze in der [Registrierungs](registry-table.md) Tabelle registrieren den Handler, wenn die productcomponent-Komponente installiert ist. Der Wert "-1" im Feld "root" ist erforderlich, um Windows Installer anzugeben, dass die Registrierung an einen Speicherort umgeleitet werden soll, der vom Installations Kontext abhängig ist.

[Registrierung](registry-table.md) Glaub

| Registrierung                       | Root | Schlüssel                                                                              | Name                                   | Wert                                        | Komponente        |
|--------------------------------|------|----------------------------------------------------------------------------------|----------------------------------------|----------------------------------------------|------------------|
| MyPreviewHandlerRegistration1  | -1   | Software \\ Klassen \\ . Pua                                                          |                                        | puafile                                      | Productcomponent |
| MyPreviewHandlerRegistration2  | -1   | Software \\ Microsoft \\ Windows \\ CurrentVersion \\ PreviewHandlers                    | {1531d583-8375-4d3f-b5fb-d23bbd169 F22} | Microsoft Windows Pua-Test Vorschau Handler   | Productcomponent |
| MyPreviewHandlerRegistration3  | -1   | Software \\ Klassen \\ puafile \\ shellex \\ {8895b1c6-b41f -4c1c-A562-0d564250836f}      |                                        | {1531d583-8375-4d3f-b5fb-d23bbd169 F22}       | Productcomponent |
| MyPreviewHandlerRegistration4  | -1   | Software \\ Klassen \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169 F22}                 |                                        | Per-User Application Sample 1-Vorschau Handler | Productcomponent |
| MyPreviewHandlerRegistration5  | -1   | Software \\ Klassen \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169 F22}                 | AppID                                  | {6d2b5079-2F 0B-48dd-ab7f -97cec514d30b}       | Productcomponent |
| MyPreviewHandlerRegistration6  | -1   | Software \\ Klassen \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169 F22}                 | DisplayName                            | @shell32,-38242                              | Productcomponent |
| MyPreviewHandlerRegistration7  | -1   | Software \\ Klassen \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169 F22}                 | Symbol                                   | notepad.exe, 2                                | Productcomponent |
| MyPreviewHandlerRegistration8  | -1   | Software \\ Klassen \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169 F22} \\ InProcServer32 | ThreadingModel                         | Apartment                                    | Productcomponent |
| MyPreviewHandlerRegistration9  | -1   | Software \\ Klassen \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169 F22} \\ InProcServer32 |                                        | \#%% Systemroot% \\ system32 \\shell32.dll       | Productcomponent |
| MyPreviewHandlerRegistration10 | -1   | Software \\ Klassen \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169 F22} \\ InProcServer32 | ProgID                                 | puafile                                      | Productcomponent |



 

 

 
