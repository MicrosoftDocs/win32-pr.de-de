---
description: Dieses Material richtet sich an Entwickler, die ihre eigenen Setupprogramme schreiben, und Entwickler, die mehr über die Datenbanktabellen des Installationsprogramms erfahren möchten. Allgemeine Informationen zum Installationsprogramm finden Sie unter Informationen Windows Installer.
ms.assetid: 95516437-9708-4f4e-a5c2-7bcd4741c776
title: Datenbankfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6214dadc413a2c4e2d5f257c396438c850446fb9106fb70970bdb971f4653d44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086210"
---
# <a name="database-functions"></a>Datenbankfunktionen

Dieses Material richtet sich an Entwickler, die ihre eigenen Setupprogramme schreiben, und Entwickler, die mehr über die Datenbanktabellen des Installationsprogramms erfahren möchten. Allgemeine Informationen zum Installationsprogramm finden Sie unter [Informationen Windows Installers.](about-windows-installer.md)

Sie können die Installer-Zugriffsfunktionen verwenden, um auf die Datenbank und den Installationsvorgang zuzugreifen. Diese Funktionen sollten nur von benutzerdefinierten Installationsaktionen und Erstellungstools verwendet werden. Einige der Installerzugriffsfunktionen erfordern SQL Abfragezeichenfolgen zum Abfragen der Datenbank. Abfragen müssen dem Installationsprogramm [SQL Syntax](sql-syntax.md)entsprechen.

In diesem Thema werden die Funktionen für den Datenbankzugriff des Installationsprogramms nach Kategorie aufgelistet.

## <a name="general-database-access-functions"></a>Allgemeine Datenbankzugriffsfunktionen



| Funktion                                                             | BESCHREIBUNG                                                                             |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)                       | Committet Änderungen an einer Datenbank.                                                          |
| [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)       | Gibt die Namen aller Primärschlüsselspalten zurück.                                       |
| [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta) | Gibt eine Enumeration zurück, die den Zustand einer Tabelle beschreibt.                                 |
| [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)                   | Bereitet eine Datenbankabfrage vor und erstellt ein Ansichtsobjekt.                                    |
| [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)                 | Gibt die aktive Datenbank für die Installation zurück.                                       |
| [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)                 | Gibt Spaltennamen oder Definitionen zurück.                                                    |
| [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)                           | Öffnet eine Datenbankdatei für den Datenzugriff.                                                  |
| [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)                                 | Gibt das Resultset für eine ausgeführte Sicht frei.                                           |
| [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)                             | Führt die Sichtabfrage aus und stellt die erforderlichen Parameter zur Verfügung.                               |
| [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)                                 | Ruft den nächsten sequenziellen Datensatz aus der Ansicht ab.                                       |
| [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)                           | Gibt den Fehler zurück, der in der [**MsiViewModify-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) aufgetreten ist. |
| [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)                               | Aktualisiert einen abgerufenen Datensatz.                                                               |



 

## <a name="database-management-functions"></a>Datenbankverwaltungsfunktionen



| Funktion                                                               | BESCHREIBUNG                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) | Erstellt Zusammenfassungsinformationen für eine vorhandene Transformation.           |
| [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)         | Wendet eine Transformation auf eine Datenbank an.                               |
| [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)                         | Exportiert eine Tabelle aus einer geöffneten Datenbank in eine Textarchivdatei.    |
| [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)   | Generiert eine Transformationsdatei mit Unterschieden zwischen zwei Datenbanken. |
| [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)                         | Importiert eine Installationstextarchivtabelle in eine geöffnete Datenbank.   |
| [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)                           | Führt zwei Datenbanken zusammen.                                   |
| [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)                     | Gibt den Status der Datenbank zurück.                               |



 

## <a name="record-processing-functions"></a>Datensatzverarbeitungsfunktionen



| Funktion                                                 | BESCHREIBUNG                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------|
| [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)               | Erstellt ein neues Datensatzobjekt mit der angegebenen Anzahl von Feldern.      |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)               | Formatiert Felddaten und Eigenschaften mithilfe einer Formatzeichenfolge. |
| [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)         | Legt alle Felder in einem Datensatz auf NULL fest.                            |
| [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize)           | Gibt die Länge eines Datensatzfelds zurück.                           |
| [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) | Gibt die Anzahl von Feldern in einem Datensatz zurück                       |
| [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)       | Gibt den ganzzahligen Wert aus einem Datensatzfeld zurück.                  |
| [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)         | Gibt den Zeichenfolgenwert eines Datensatzfelds zurück.                     |
| [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)               | Gibt an, ob ein Datensatzfeld NULL ist.                         |
| [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)       | Liest Bytes aus einem Datensatzstreamfeld in einen Puffer.           |
| [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)       | Legt ein Datensatzfeld auf ein ganzzahliges Feld fest.                        |
| [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)         | Legt ein Datensatzdatenstromfeld aus einer Datei fest.                         |
| [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)         | Kopiert eine Zeichenfolge in das angegebene Feld.                      |



 

## <a name="summary-information-property-functions"></a>Eigenschaftenfunktionen für Zusammenfassungsinformationen



| Funktion                                                                 | BESCHREIBUNG                                                            |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)             | Ruft das Handle für den Zusammenfassungsinformationsdatenstrom der Installer-Datenbank ab.    |
| [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)           | Ruft eine einzelne Eigenschaft aus den Zusammenfassungsinformationen ab.                   |
| [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) | Gibt die Anzahl der Eigenschaften im Zusammenfassungsinformationsdatenstrom zurück.        |
| [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist)                   | Schreibt geänderte Zusammenfassungsinformationen zurück in den Zusammenfassungsinformationsdatenstrom. |
| [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)           | Legt eine einzelne Zusammenfassungsinformationseigenschaft fest.                            |



 

## <a name="installer-state-access-functions"></a>Zustandszugriffsfunktionen des Installationsprogramms



| Funktion                                               | BESCHREIBUNG                                                 |
|--------------------------------------------------------|-------------------------------------------------------------|
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)               | Gibt die numerische Sprache der aktuellen Installation zurück.   |
| [**MsiGetLastErrorRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlasterrorrecord) | Gibt den Fehlerdatensatz zurück, der zuletzt für den aufrufenden Prozess zurückgegeben wurde. |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)                       | Gibt einen der booleschen internen Installationszustände zurück.    |
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)               | Ruft den Wert einer Installereigenschaft ab.                    |
| [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)               | Legt den Wert einer Installationseigenschaft fest.                 |
| [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)                       | Legt einen internen booleschen Engine-Zustand fest.                      |



 

## <a name="installer-action-functions"></a>Aktionsfunktionen des Installers



| Funktion                                             | BESCHREIBUNG                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)                   | Führt eine integrierte Aktion, eine benutzerdefinierte Aktion oder eine Benutzeroberflächen-Assistentenaktion aus. |
| [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) | Wertet einen bedingten Ausdruck aus, der Eigenschaftsnamen und -werte enthält.  |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)       | Sendet einen Fehlerdatensatz zur Verarbeitung an das Installationsprogramm.                    |
| [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)                   | Führt eine Aktionssequenz aus.                                              |



 

## <a name="installer-location-functions"></a>Speicherortfunktionen des Installationsprogramms



| Funktion                                     | BESCHREIBUNG                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) | Gibt den vollständigen Quellpfad für einen Ordner in der Directory-Tabelle zurück. |
| [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) | Gibt den vollständigen Zielpfad für einen Ordner in der Directory-Tabelle zurück. |
| [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) | Legt den vollständigen Zielpfad für einen Ordner in der Directory-Tabelle fest.    |



 

## <a name="installer-selection-functions"></a>Auswahlfunktionen des Installers



| Funktion                                                     | BESCHREIBUNG                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [**MsiEnumComponentCosts**](/windows/desktop/api/Msiquery/nf-msiquery-msienumcomponentcostsa)       | Hier wird der Speicherplatz pro Laufwerk aufzählt, der zum Installieren einer Komponente erforderlich ist. |
| [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)         | Erhält den Zustand einer Komponente.                                    |
| [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)               | Gibt den von einem Feature benötigten Speicherplatz zurück.                        |
| [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)             | Ruft den Zustand eines Features ab.                                         |
| [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) | Gibt einen gültigen Installationsstatus zurück.                                  |
| [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)         | Legt eine Komponente auf den angegebenen Zustand fest.                             |
| [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa)   | Ändert die Standardattribute eines Features zur Laufzeit.            |
| [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)             | Legt ein Feature auf einen angegebenen Zustand fest.                                 |
| [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)             | Legt die Installationsebene einer vollständigen Produktinstallation fest.          |
| [**MsiVerifyDiskSpace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)             | Überprüft, ob ausreichend Speicherplatz vorhanden ist.                                    |



 

## <a name="user-interface-functions"></a>Benutzeroberfläche Functions



| Funktion                                           | BESCHREIBUNG                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)   | Aktiviert den Vorschaumodus der Benutzeroberfläche.                             |
| [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) | Zeigt eine Tafel mit dem Hoststeuerfeld im angezeigten Dialogfeld an. |
| [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)       | Zeigt ein Dialogfeld als moduslos und inaktiv an.                         |



 

Alle Funktionen unterstützen sowohl ANSI- als auch Unicode-Aufrufe. Um diese Funktionen zu verwenden, schließen Sie MsiQuery.h ein, und verknüpfen Sie msi.lib.

## <a name="installation-functions"></a>Installationsfunktionen

Zusätzlich zu den oben aufgeführten Datenbankzugriffsfunktionen erstellen Sie ein Installationspaket für eine Anwendung mithilfe der Installerfunktionen, die im Abschnitt Referenz zur [Installerfunktion aufgeführt](installer-function-reference.md) sind.

 

 



