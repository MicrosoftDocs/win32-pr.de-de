---
description: Zum Aktivieren Windows Installers in Ihrer Anwendung müssen Sie die Installerfunktionen verwenden. Die Tabellen in diesem Thema identifizieren die Funktionen nach Kategorie.
ms.assetid: 05a16915-6b47-4d51-b62a-5a4d92b87e50
title: Referenz zur Installerfunktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ab6a77bd3aa02be85f0d2a3cb11a864861535360f5741c6566f77e9fc1aa11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630545"
---
# <a name="installer-function-reference"></a>Referenz zur Installerfunktion

Zum Aktivieren Windows Installers in Ihrer Anwendung müssen Sie die Installerfunktionen verwenden. Die Tabellen in diesem Thema identifizieren die Funktionen nach Kategorie.

## <a name="user-interface-and-logging-functions"></a>Benutzeroberfläche und Protokollierungsfunktionen



| Name                                                     | Beschreibung                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)             | Aktiviert die interne Benutzeroberfläche des Installationsprogramms.                                 |
| [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)             | Aktiviert einen externen Benutzeroberflächenhandler, der Nachrichten in einem Zeichenfolgenformat empfängt. |
| [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) | Aktiviert einen externen Benutzeroberflächenhandler, der Nachrichten in einem Datensatzformat empfängt. |
| [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)                     | Legt den Protokollmodus für alle Installationen im aufrufenden Prozess fest.                       |



 

## <a name="handle-management-functions"></a>Behandeln von Verwaltungsfunktionen



| Name                                             | Beschreibung                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)         | Schließt ein geöffnetes Installationshand handle.                           |
| [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) | Schließt alle geöffneten Installationshandles. Verwenden Sie nicht für die Bereinigung. |



 

## <a name="installation-and-configuration-functions"></a>Installations- und Konfigurationsfunktionen



| Name                                                                     | Beschreibung                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)                       | Gibt ein Produkt an.                                                                                                                                                                                                        |
| [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)                   | Gibt ein Produkt an.                                                                                                                                                                                                        |
| [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)                         | Kopiert eine Ankündigungsskriptdatei an angegebene Speicherorte.                                                                                                                                                                    |
| [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)                           | Installiert oder entfernt eine Anwendung oder Anwendungssammlung.                                                                                                                                                                     |
| [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)                       | Installiert oder entfernt eine Anwendung oder Anwendungssammlung.                                                                                                                                                                     |
| [**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)                   | Installiert oder entfernt eine Anwendung oder Anwendungssammlung. Eine Produktbefehlszeile kann angegeben werden.                                                                                                                            |
| [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)                       | Installiert oder repariert eine Installation neu.                                                                                                                                                                                       |
| [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)                       | Konfiguriert den installierten Zustand eines Features.                                                                                                                                                                                 |
| [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)                       | Überprüft oder repariert Features.                                                                                                                                                                                               |
| [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)         | Installiert fehlende Komponenten.                                                                                                                                                                                                 |
| [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)                   | Installiert fehlende Dateien.                                                                                                                                                                                                      |
| [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)                         | Benachrichtigt und aktualisiert die internen Informationen Windows Installer mit Änderungen an Benutzer-SIDs. Verfügbar ab Windows Installer 3.1.                                                                                   |
| [**MsiProcessAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiprocessadvertisescripta)           | Verarbeitet eine Ankündigungsskriptdatei an angegebenen Speicherorten.                                                                                                                                                                 |
| [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)                 | Fügt die Quellen eines Patches oder Produkts in einem angegebenen Kontext hinzu oder ordnet sie neu an.                                                                                                                                                   |
| [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)             | Fügt die Quellen eines Patches oder Produkts in einem angegebenen Kontext hinzu oder ordnet sie neu an. Erstellt eine Quellliste für einen Patch, der in einem angegebenen Kontext nicht vorhanden ist. Verfügbar in Windows Installer 3.0.                                |
| [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)             | Entfernt eine vorhandene Quelle für ein Produkt oder einen Patch in einem angegebenen Kontext. Verfügbar in Windows Installer 3.0.                                                                                                               |
| [**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)                   | Entfernt alle vorhandenen Quellen eines bestimmten Quelltyps für eine angegebene Produktinstanz.                                                                                                                                 |
| [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)               | Entfernt alle vorhandenen Quellen eines bestimmten Quelltyps für eine angegebene Produktinstanz. Verfügbar in Windows Installer 3.0.                                                                                            |
| [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)     | Entfernt die Registrierung der aktuellen Quelle des Produkts oder Patches, die als Eigenschaft "LastUsedSource" registriert ist. Diese Funktion wirkt sich nicht auf die liste der registrierten Quellen aus.                                      |
| [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) | Entfernt die Registrierung der aktuellen Quelle des Produkts oder Patches, die als Eigenschaft "LastUsedSource" registriert ist. Diese Funktion wirkt sich nicht auf die liste der registrierten Quellen aus. Verfügbar in Windows Installer 3.0. |
| [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)                     | Ruft Informationen über die Quellliste für ein Produkt oder einen Patch in einem bestimmten Kontext ab.                                                                                                                                    |
| [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)                     | Legt die zuletzt verwendete Quelle für ein Produkt oder einen Patch in einem angegebenen Kontext fest. Verfügbar in Windows Installer 3.0.                                                                                                       |
| [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)       | Listet die Datenträger auf, die für die Medienquelle für einen Patch oder ein Produkt registriert sind. Verfügbar in Windows Installer 3.0.                                                                                                    |
| [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)           | Fügt einen Datenträger der Medienquelle eines registrierten Produkts oder Patches hinzu oder aktualisiert diese. Verfügbar in Windows Installer 3.0.                                                                                                            |
| [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)      | Entfernt einen vorhandenen registrierten Datenträger unter der Medienquelle für ein Produkt oder einen Patch in einem bestimmten Kontext. Verfügbar in Windows Installer 3.0.                                                                                |
| [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)             | Listet die Quellen in der Quellliste eines angegebenen Patches oder Produkts auf. Verfügbar in Windows Installer 3.0.                                                                                                              |



 

## <a name="component-specific-functions"></a>Component-Specific Functions



| Name                                                                     | Beschreibung                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)                         | Installiert den vollständigen Komponentenpfad für eine Assembly und gibt diesen zurück.                                                                                                                                                                 |
| [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)                       | Installiert den vollständigen Komponentenpfad einer Komponente und gibt diesen zurück.                                                                                                                                                                  |
| [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)     | Installiert den vollständigen Komponentenpfad einer qualifizierten Komponente und gibt diesen zurück.                                                                                                                                                        |
| [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) | Installiert den vollständigen Komponentenpfad einer qualifizierten Komponente, die von einem Produkt veröffentlicht wird, und gibt diesen zurück.                                                                                                                         |
| [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)                       | Gibt den vollständigen Pfad oder Registrierungsschlüssel an eine installierte Komponente zurück.                                                                                                                                                              |
| [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)                   | Gibt den vollständigen Pfad oder Registrierungsschlüssel für eine installierte Komponente über Benutzerkonten und Installationskontext hinweg zurück. **[Windows Installer 4.5 und früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt.<br/> |
| [**MsiLocateComponent**](/windows/desktop/api/Msi/nf-msi-msilocatecomponenta)                         | Gibt den vollständigen Pfad zu einer installierten Komponente ohne Produktcode zurück.                                                                                                                                                       |
| [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)                 | Gibt den installierten Zustand für eine Komponente zurück. Kann Komponenten einer Instanz eines Produkts abfragen, das unter anderen Benutzerkonten als dem aktuellen Benutzer installiert ist. Verfügbar in Windows Installer 3.0 oder höher.                        |



 

## <a name="application-only-functions"></a>Application-Only Functions



| Name                                             | BESCHREIBUNG                                                            |
|--------------------------------------------------|------------------------------------------------------------------------|
| [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) | Speichert Benutzerinformationen aus einem Installations-Assistenten.                   |
| [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)           | Erhöht die Nutzungsanzahl für ein Feature und gibt den Installationsstatus an. |
| [**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)       | Erhöht die Nutzungsanzahl für ein Feature und gibt den Installationsstatus an. |
| [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)   | Gibt den Produktcode mithilfe des Komponentencodes zurück.                         |



 

## <a name="system-status-functions"></a>Systemstatusfunktionen



| Name                                                             | BESCHREIBUNG                                                                                                                                                                                                                       |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)                       | Aufzählt angekündigte Produkte.                                                                                                                                                                                                   |
| [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)                   | Durchzählt alle Instanzen von angekündigten oder installierten Produkten in einem angegebenen Kontext. Verfügbar in Windows Installer 3.0 oder höher.                                                                                    |
| [**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)         | Hier werden derzeit installierte Produkte mit einem angegebenen Upgradecode aufzählt.                                                                                                                                                          |
| [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)                       | Enumeriert veröffentlichte Features.                                                                                                                                                                                                    |
| [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)                   | Enumeriert die installierten Komponenten.                                                                                                                                                                                              |
| [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)               | Enumeriert die installierten Komponenten über Benutzerkonten und Installationskontext hinweg. **[Windows Installer 4.5 und früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt.<br/>                                 |
| [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)                         | Enumeriert die Clients einer installierten Komponente.                                                                                                                                                                                 |
| [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)                     | Enumeriert die Clients einer installierten Komponente über Benutzerkonten und Installationskontext hinweg. **[Windows Installer 4.5 und früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt.<br/>                    |
| [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) | Enumeriert die angekündigten Qualifizierer für eine Komponente.                                                                                                                                                                             |
| [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)             | Gibt den installierten Zustand eines Features zurück.                                                                                                                                                                                         |
| [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)         | Gibt den installierten Zustand für ein Produktfeature zurück. Kann Funktionen einer Instanz eines Produkts abfragen, das unter anderen Benutzerkonten als dem aktuellen Benutzer installiert ist. Verfügbar in Windows Installer 3.0 oder höher.                        |
| [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)             | Gibt den installierten Zustand für eine Anwendung oder Anwendungssammlung zurück.                                                                                                                                                              |
| [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)                 | Gibt Nutzungsmetriken für ein Feature zurück.                                                                                                                                                                                              |
| [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)                   | Gibt Produktinformationen für veröffentlichte und installierte Produkte zurück.                                                                                                                                                                 |
| [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)               | Gibt Produktinformationen für angekündigte und installierte Produkte zurück. Kann Informationen zu einer Instanz eines Produkts abrufen, das unter einem anderen Benutzerkonto als dem aktuellen Benutzer installiert ist. Verfügbar in Windows Installer 3.0 oder höher. |
| [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)                         | Gibt registrierte Benutzerinformationen für ein installiertes Produkt zurück.                                                                                                                                                                     |



 

## <a name="product-query-functions"></a>Produktabfragefunktionen



| Name                                                               | BESCHREIBUNG                                                                            |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)                           | Öffnet ein Produkt, das mit den Funktionen verwendet werden soll, die auf die Datenbank zugreifen.                    |
| [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)                           | Öffnet ein Paket, das mit den Funktionen verwendet werden soll, die auf die Datenbank zugreifen.                    |
| [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)                       | Öffnet ein Paket, das mit den Funktionen verwendet werden soll, die auf die Datenbank zugreifen.                    |
| [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)               | Überprüft, ob das Produkt mit erhöhten Rechten installiert ist.                      |
| [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) | Gibt Produktinformationen für eine Installationsskriptdatei zurück.                              |
| [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)             | Ruft Eigenschaften in der Produktdatenbank ab.                                          |
| [**MsiGetShortcutTarget**](/windows/desktop/api/Msi/nf-msi-msigetshortcuttargeta)               | Überprüft eine Verknüpfung und gibt das Produkt, den Featurenamen und die Komponente zurück, falls verfügbar. |
| [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)                     | Gibt beschreibende Informationen für ein Feature zurück.                                         |
| [**MsiVerifyPackage**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)                       | Überprüft, ob eine angegebene Datei ein Installationspaket ist.                             |



 

## <a name="patching-functions"></a>Patchen von Funktionen



| Name                                                                   | BESCHREIBUNG                                                                                                                                                        |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)                                 | Ruft eine Installation auf und wendet ein Patchpaket an.                                                                                                               |
| [**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)                    | Gibt die GUID für jeden Patch zurück, der auf ein Produkt angewendet wird, sowie eine Liste der Transformationen aus jedem Patch, der für das Produkt gilt.                                  |
| [**MsiGetPatchInfo**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoa)                             | Gibt Informationen zu einem Patch zurück.                                                                                                                                 |
| [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)                           | Deinstalliert einen Patch aus einem Produkt. Verfügbar in Windows Installer 3.0.                                                                                             |
| [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)         | Bestimmt die beste Anwendungssequenz für eine Reihe von Patches und Produkten. Verfügbar in Windows Installer 3.0.                                                     |
| [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)             | Wendet ein oder mehrere Patches auf Produkte an. Verfügbar in Windows Installer 3.0.                                                                                       |
| [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)                           | Listet alle Patches auf, die für ein Produkt in einem bestimmten Kontext oder in allen Kontexten angewendet werden. Verfügbar in Windows Installer 3.0.                                   |
| [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)                     | Wenn eine Liste mit MSP-Dateien bereitgestellt wird, ruft diese Funktion die Liste der Dateien ab, die von den Patches für den Targe aktualisiert werden können. Verfügbar in Windows Installer 4.0. |
| [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)                         | Fragt Informationen zur Anwendung eines angegebenen Patches auf ein angegebenes Produkt ab. Verfügbar in Windows Installer 3.0.                                     |
| [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)               | Extrahiert Informationen aus einem Patch. Verfügbar in Windows Installer 3.0.                                                                                             |
| [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) | Bestimmt den besten Satz von Patches, die zum Aktualisieren eines Produkts oder einer Gruppe von Produkten erforderlich sind. Verfügbar in Windows Installer 3.0.                                            |



 

## <a name="file-query-functions"></a>Dateiabfragefunktionen



| Name                                                                     | Beschreibung                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)                                 | Nimmt den Pfad zu einer Datei und gibt einen 128-Bit-Hash dieser Datei zurück.                                           |
| [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa) | Nimmt den Pfad zu einer Datei, die digital signiert wurde, und gibt das Signaturgeberzertifikat und den Hash der Datei zurück. |
| [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona)                           | Gibt die Versionszeichenfolge und die Sprachzeichenfolge zurück.                                                             |



 

## <a name="transaction-management-functions"></a>Transaktionsverwaltungsfunktionen



| Name                                               | Beschreibung                                                                                                                                                                                         |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona) | Startet die Transaktionsverarbeitung einer Installation mit mehreren Paketen und gibt einen Bezeichner für die Transaktion zurück. Diese Funktion ist ab Windows Installer 4.5 verfügbar.                    |
| [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)   | Fordert an, dass der Windows Installer den aktuellen Prozess zum Besitzer der Transaktion macht, die eine Installation mit mehreren Paketen installiert. Diese Funktion ist ab Windows Installer 4.5 verfügbar. |
| [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)     | Führt einen Commit für alle Installationen aus, die zur Transaktion gehören, oder führt ein Rollback aus. Diese Funktion ist ab Windows Installer 4.5 verfügbar.                                                          |



 

## <a name="database-functions"></a>Datenbankfunktionen

Zusätzlich zu den in den vorherigen Tabellen angegebenen Windows Installer-Funktionen können Sie Informationen in der Installationsdatenbank bearbeiten, indem Sie die Im Abschnitt [Datenbankfunktionen](database-functions.md) beschriebenen Datenbankzugriffsfunktionen verwenden.

## <a name="installer-structures"></a>Installerstrukturen

Darüber hinaus werden einige Informationen in der Installationsdatenbank mithilfe der im Abschnitt [Installationsstrukturen](installer-structures.md) beschriebenen Strukturen behandelt.

 

 




