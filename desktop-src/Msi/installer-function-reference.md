---
description: Um Windows Installer in der Anwendung zu aktivieren, müssen Sie die Installer-Funktionen verwenden. In den Tabellen in diesem Thema werden die Funktionen nach Kategorie identifiziert.
ms.assetid: 05a16915-6b47-4d51-b62a-5a4d92b87e50
title: Installationsfunktionsverweis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9261789f21bd559e49c4e5718ef68ce9d0bb41c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958955"
---
# <a name="installer-function-reference"></a>Installationsfunktionsverweis

Um Windows Installer in der Anwendung zu aktivieren, müssen Sie die Installer-Funktionen verwenden. In den Tabellen in diesem Thema werden die Funktionen nach Kategorie identifiziert.

## <a name="user-interface-and-logging-functions"></a>Benutzeroberfläche und Protokollierungsfunktionen



| Name                                                     | BESCHREIBUNG                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)             | Aktiviert die interne Benutzeroberfläche des Installers.                                 |
| [**Msiseeltexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)             | Aktiviert einen externen Benutzerschnittstellen Handler, der Nachrichten in einem Zeichen folgen Format empfängt. |
| [**Msiseeltexternaluirecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) | Aktiviert einen externen Benutzerschnittstellen Handler, der Nachrichten in einem Daten Satz Format empfängt. |
| [**Msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga)                     | Legt den Protokollmodus für alle Installationen im aufrufenden Prozess fest.                       |



 

## <a name="handle-management-functions"></a>Verwalten von Verwaltungsfunktionen



| Name                                             | BESCHREIBUNG                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**Msiclosehandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)         | Schließt ein geöffnetes Installations handle.                           |
| [**Msicloseallhandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) | Schließt alle geöffneten Installations Handles. Verwenden Sie nicht für Cleanup. |



 

## <a name="installation-and-configuration-functions"></a>Installations-und Konfigurationsfunktionen



| Name                                                                     | BESCHREIBUNG                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msiankündigen-Produkt**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)                       | Gibt ein Produkt an.                                                                                                                                                                                                        |
| [**Msiankündigen-productex**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)                   | Gibt ein Produkt an.                                                                                                                                                                                                        |
| [**Msiwerbesescript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)                         | Kopiert eine Ankündigungs Skriptdatei an angegebene Speicherorte.                                                                                                                                                                    |
| [**Msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)                           | Installiert oder entfernt eine Anwendung oder Anwendungssuite.                                                                                                                                                                     |
| [**Msikonfigurireproduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)                       | Installiert oder entfernt eine Anwendung oder Anwendungssuite.                                                                                                                                                                     |
| [**Msikonfigurireproduktions-ctex**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)                   | Installiert oder entfernt eine Anwendung oder Anwendungssuite. Es kann eine Produkt Befehlszeile angegeben werden.                                                                                                                            |
| [**Msireinstallproduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)                       | Installiert oder repariert eine Installation.                                                                                                                                                                                       |
| [**Msikonfigurierfeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)                       | Konfiguriert den installierten Zustand einer Funktion.                                                                                                                                                                                 |
| [**Msireinstallfeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)                       | Überprüft oder repariert Features.                                                                                                                                                                                               |
| [**Msiinstallmissingcomponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)         | Installiert fehlende Komponenten.                                                                                                                                                                                                 |
| [**Msiinstallmissingfile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)                   | Installiert fehlende Dateien.                                                                                                                                                                                                      |
| [**Msinotif ysidchange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)                         | Benachrichtigt und aktualisiert die Windows Installer internen Informationen mit Änderungen an Benutzer-SIDs. Verfügbar ab Windows Installer 3,1.                                                                                   |
| [**Msiprocesswerbung**](/windows/desktop/api/Msi/nf-msi-msiprocessadvertisescripta)           | Verarbeitet eine Ankündigungs Skriptdatei an angegebenen Speicherorten.                                                                                                                                                                 |
| [**Msisourcelistaddsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)                 | Fügt die Quellen eines Patches oder Produkts in einem angegebenen Kontext hinzu oder ordnet sie neu zu.                                                                                                                                                   |
| [**Msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)             | Fügt die Quellen eines Patches oder Produkts in einem angegebenen Kontext hinzu oder ordnet sie neu zu. Erstellt eine Quell Liste für einen Patch, der in einem angegebenen Kontext nicht vorhanden ist. Verfügbar in Windows Installer 3,0.                                |
| [**Msisourcelistclearsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)             | Entfernt eine vorhandene Quelle für ein Produkt oder einen Patch in einem angegebenen Kontext. Verfügbar in Windows Installer 3,0.                                                                                                               |
| [**Msisourcelistclearall**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)                   | Entfernt alle vorhandenen Quellen eines bestimmten Quell Typs für eine angegebene Produkt Instanz.                                                                                                                                 |
| [**Msisourcelistclearallex**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)               | Entfernt alle vorhandenen Quellen eines bestimmten Quell Typs für eine angegebene Produkt Instanz. Verfügbar in Windows Installer 3,0.                                                                                            |
| [**Msisourcelistforceresolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)     | Entfernt die Registrierung der aktuellen Quelle des Produkts oder Patches, die als die Eigenschaft "LastUsedSource" registriert ist. Diese Funktion hat keine Auswirkung auf die registrierte Quell Liste.                                      |
| [**Msisourcelistforceresolutionex**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) | Entfernt die Registrierung der aktuellen Quelle des Produkts oder Patches, die als die Eigenschaft "LastUsedSource" registriert ist. Diese Funktion hat keine Auswirkung auf die registrierte Quell Liste. Verfügbar in Windows Installer 3,0. |
| [**Msisourcelistgetinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)                     | Ruft Informationen zur Quell Liste für ein Produkt oder einen Patch in einem bestimmten Kontext ab.                                                                                                                                    |
| [**Msisourcelisteintinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)                     | Legt die zuletzt verwendete Quelle für ein Produkt oder einen Patch in einem angegebenen Kontext fest. Verfügbar in Windows Installer 3,0.                                                                                                       |
| [**Msisourcelistenumschlag mediadisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)       | Listet die Datenträger auf, die für die Medienquelle für einen Patch oder ein Produkt registriert sind. Verfügbar in Windows Installer 3,0.                                                                                                    |
| [**Msisourcelistaddmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)           | Hiermit wird ein Datenträger der Medienquelle eines registrierten Produkts oder Patches hinzugefügt oder aktualisiert. Verfügbar in Windows Installer 3,0.                                                                                                            |
| [**Msisourcelistclearmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)      | Entfernt einen vorhandenen registrierten Datenträger unter der Medienquelle für ein Produkt oder einen Patch in einem bestimmten Kontext. Verfügbar in Windows Installer 3,0.                                                                                |
| [**Msisourcelistenumschlag Quellen**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)             | Listet die Quellen in der Quell Liste eines angegebenen Patches oder Produkts auf. Verfügbar in Windows Installer 3,0.                                                                                                              |



 

## <a name="component-specific-functions"></a>Component-Specific Funktionen



| Name                                                                     | BESCHREIBUNG                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msiproviabassembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)                         | Installiert den vollständigen Komponenten Pfad für eine Assembly und gibt diesen zurück.                                                                                                                                                                 |
| [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)                       | Installiert den vollständigen Komponenten Pfad einer Komponente und gibt diesen zurück.                                                                                                                                                                  |
| [**Msiprovidequalifiedcomponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)     | Installiert den vollständigen Komponenten Pfad einer qualifizierten Komponente und gibt diesen zurück.                                                                                                                                                        |
| [**Msiprovide qualifiedcomponumtex**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) | Installiert den vollständigen Komponenten Pfad einer qualifizierten Komponente, die von einem Produkt veröffentlicht wird, und gibt diesen zurück.                                                                                                                         |
| [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)                       | Gibt den vollständigen Pfad oder den Registrierungsschlüssel für eine installierte Komponente zurück.                                                                                                                                                              |
| [**Msigetcomponentpathex**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)                   | Gibt den vollständigen Pfad oder den Registrierungsschlüssel für eine installierte Komponente über Benutzerkonten und Installations Kontext hinweg zurück. **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/> |
| [**Msilocatecomponent**](/windows/desktop/api/Msi/nf-msi-msilocatecomponenta)                         | Gibt den vollständigen Pfad zu einer installierten Komponente ohne Produktcode zurück.                                                                                                                                                       |
| [**Msiquerycomponentstate**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)                 | Gibt den installierten Zustand für eine Komponente zurück. Kann Komponenten einer Instanz eines Produkts Abfragen, die unter Benutzerkonten mit Ausnahme des aktuellen Benutzers installiert sind. Verfügbar in Windows Installer 3,0 oder höher.                        |



 

## <a name="application-only-functions"></a>Application-Only Funktionen



| Name                                             | BESCHREIBUNG                                                            |
|--------------------------------------------------|------------------------------------------------------------------------|
| [**Msicollectuserinfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) | Speichert Benutzerinformationen von einem Installations-Assistenten.                   |
| [**Msiusefeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)           | Erhöht die Verwendungs Anzahl für eine Funktion und gibt den Installationsstatus an. |
| [**Msiusefeatureex**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)       | Erhöht die Verwendungs Anzahl für eine Funktion und gibt den Installationsstatus an. |
| [**Msigetproductcode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)   | Gibt den Produktcode mithilfe des Komponenten Codes zurück.                         |



 

## <a name="system-status-functions"></a>System Status Funktionen



| Name                                                             | BESCHREIBUNG                                                                                                                                                                                                                       |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msienumschlag Produkte**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)                       | Listet angekündigte Produkte auf.                                                                                                                                                                                                   |
| [**Msienumschlag**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)                   | Listet alle Instanzen von angekündigten oder installierten Produkten in einem angegebenen Kontext auf. Verfügbar in Windows Installer 3,0 oder höher.                                                                                    |
| [**Msienumrelatedproducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)         | Listet die aktuell installierten Produkte auf, die über einen angegebenen UpgradeCode verfügen.                                                                                                                                                          |
| [**Msienumschlag-Features**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)                       | Listet veröffentlichte Funktionen auf.                                                                                                                                                                                                    |
| [**Msienumschlag Components**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)                   | Listet die installierten Komponenten auf.                                                                                                                                                                                              |
| [**Msienumschlag**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)               | Listet die installierten Komponenten über Benutzerkonten und den Installations Kontext auf. **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/>                                 |
| [**Msienumschlag Clients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)                         | Listet die Clients einer installierten Komponente auf.                                                                                                                                                                                 |
| [**Msienumschlag clientsex**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)                     | Listet die Clients einer installierten Komponente über Benutzerkonten und den Installations Kontext auf. **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/>                    |
| [**Msienumschlag componentqualifizierer**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) | Listet die angekündigten Qualifizierer für eine Komponente auf.                                                                                                                                                                             |
| [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)             | Gibt den installierten Zustand einer Funktion zurück.                                                                                                                                                                                         |
| [**Msiqueryfeaturestateex**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)         | Gibt den installierten Zustand für eine Produkt Funktion zurück. Kann Funktionen einer Instanz eines Produkts Abfragen, die unter Benutzerkonten mit Ausnahme des aktuellen Benutzers installiert ist. Verfügbar in Windows Installer 3,0 oder höher.                        |
| [**Msiqueryproductstate**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)             | Gibt den installierten Zustand für eine Anwendung oder Anwendungs Sammlung zurück.                                                                                                                                                              |
| [**Msigetfeatureusage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)                 | Gibt nutzungsmetriken für eine Funktion zurück.                                                                                                                                                                                              |
| [**Msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)                   | Gibt Produktinformationen für veröffentlichte und installierte Produkte zurück.                                                                                                                                                                 |
| [**Msigetproductinfoex**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)               | Gibt Produktinformationen für angekündigte und installierte Produkte zurück. Kann Informationen zu einer Instanz eines Produkts abrufen, die unter einem anderen Benutzerkonto als dem aktuellen Benutzer installiert ist. Verfügbar in Windows Installer 3,0 oder höher. |
| [**Msigetuserinfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)                         | Gibt registrierte Benutzerinformationen für ein installiertes Produkt zurück.                                                                                                                                                                     |



 

## <a name="product-query-functions"></a>Product Query-Funktionen



| Name                                                               | BESCHREIBUNG                                                                            |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)                           | Öffnet ein Produkt, das mit den Funktionen verwendet werden soll, die auf die Datenbank zugreifen.                    |
| [**Msiopenpackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)                           | Öffnet ein Paket für die Verwendung mit den Funktionen, die auf die Datenbank zugreifen.                    |
| [**Msiopenpackageex**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)                       | Öffnet ein Paket für die Verwendung mit den Funktionen, die auf die Datenbank zugreifen.                    |
| [**Msiisproductelevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)               | Überprüft, ob das Produkt mit erhöhten Rechten installiert ist.                      |
| [**Msigetproductinfofromscript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) | Gibt Produktinformationen für eine Installationsskript Datei zurück.                              |
| [**Msigetproductproperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)             | Ruft Eigenschaften in der Produktdatenbank ab.                                          |
| [**Msigetshortcuttarget**](/windows/desktop/api/Msi/nf-msi-msigetshortcuttargeta)               | Untersucht eine Verknüpfung und gibt, sofern verfügbar, das Produkt, den Funktionsnamen und die Komponente zurück. |
| [**Msigetfeatureinfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)                     | Gibt beschreibende Informationen zu einer Funktion zurück.                                         |
| [**Msiverifypackage**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)                       | Überprüft, ob es sich bei der angegebenen Datei um ein Installationspaket handelt.                             |



 

## <a name="patching-functions"></a>Patching von Funktionen



| Name                                                                   | BESCHREIBUNG                                                                                                                                                        |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)                                 | Ruft eine Installation auf und wendet ein Patchpaket an.                                                                                                               |
| [**Msienumschlag**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)                    | Gibt die GUID für jeden Patch, der auf ein Produkt angewendet wird, und eine Liste der Transformationen aus jedem Patch zurück, die für das Produkt gelten.                                  |
| [**Msigetpatchinfo**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoa)                             | Gibt Informationen zu einem Patch zurück.                                                                                                                                 |
| [**Msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)                           | Deinstalliert einen Patch von einem Produkt. Verfügbar in Windows Installer 3,0.                                                                                             |
| [**Msideterminepatchsequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)         | Bestimmt die beste Anwendungs Sequenz für eine Gruppe von Patches und Produkten. Verfügbar in Windows Installer 3,0.                                                     |
| [**Msiapplymultiplepatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)             | Wendet ein oder mehrere Patches auf Produkte an. Verfügbar in Windows Installer 3,0.                                                                                       |
| [**Msienum patchesex**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)                           | Listet alle Patches auf, die für ein Produkt in einem bestimmten Kontext oder in allen Kontexten angewendet wurden. Verfügbar in Windows Installer 3,0.                                   |
| [**Msigetpatchfilelist**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)                     | Wenn eine Liste von MSP-Dateien bereitgestellt wird, ruft diese Funktion die Liste der Dateien ab, die von den Patches für die Targe aktualisiert werden können. Verfügbar in Windows Installer 4,0. |
| [**Msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)                         | Fragt Informationen über die Anwendung eines angegebenen Patches für ein bestimmtes Produkt ab. Verfügbar in Windows Installer 3,0.                                     |
| [**Msiextractpatchxmldata**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)               | Extrahiert Informationen aus einem Patch. Verfügbar in Windows Installer 3,0.                                                                                             |
| [**Msidetermineapplicablepatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) | Bestimmt den besten Satz von Patches, die zum Aktualisieren eines Produkts oder einer Gruppe von Produkten erforderlich sind. Verfügbar in Windows Installer 3,0.                                            |



 

## <a name="file-query-functions"></a>Datei Abfragefunktionen



| Name                                                                     | BESCHREIBUNG                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**Msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)                                 | Nimmt den Pfad zu einer Datei an und gibt einen 128-Bit-Hash dieser Datei zurück.                                           |
| [**Msigetfilesignatureinformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa) | Nimmt den Pfad zu einer Datei an, die digital signiert wurde, und gibt das Signatur Geber Zertifikat und den Hash der Datei zurück. |
| [**Msigetfileversion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona)                           | Gibt die Versions Zeichenfolge und die Zeichenfolge zurück.                                                             |



 

## <a name="transaction-management-functions"></a>Transaktions Verwaltungsfunktionen



| Name                                               | BESCHREIBUNG                                                                                                                                                                                         |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msibegintransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona) | Startet die Transaktionsverarbeitung einer Installation mit mehreren Paketen und gibt einen Bezeichner für die Transaktion zurück. Diese Funktion ist ab Windows Installer 4,5 verfügbar.                    |
| [**Msijointransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)   | Fordert an, dass die Windows Installer den aktuellen Prozess zum Besitzer der Transaktion machen, die eine Installation mit mehreren Paketen installiert. Diese Funktion ist ab Windows Installer 4,5 verfügbar. |
| [**Msiendtransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)     | Führt einen Commit oder Rollback für alle Installationen aus, die zur Transaktion gehören. Diese Funktion ist ab Windows Installer 4,5 verfügbar.                                                          |



 

## <a name="database-functions"></a>Datenbankfunktionen

Zusätzlich zu den in den vorherigen Tabellen identifizierten Windows Installer Funktionen können Sie Informationen in der Installations Datenbank mithilfe der Datenbankzugriffs Funktionen, die im Abschnitt [Datenbankfunktionen](database-functions.md) beschrieben werden, bearbeiten.

## <a name="installer-structures"></a>Installer-Strukturen

Außerdem werden einige Informationen in der Installations Datenbank mithilfe der im Abschnitt [installerstrukturen](installer-structures.md) beschriebenen Strukturen behandelt.

 

 




