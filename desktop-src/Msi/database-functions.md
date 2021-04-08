---
description: Dieses Material richtet sich an Entwickler, die eigene Setup Programme und Entwickler schreiben, die mehr über die Installer-Datenbanktabellen erfahren möchten. Allgemeine Informationen zum Installationsprogramm finden Sie unter Informationen zu Windows Installer.
ms.assetid: 95516437-9708-4f4e-a5c2-7bcd4741c776
title: Datenbankfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a4233437d24944c8bb7fe5c7de6412e700022b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752800"
---
# <a name="database-functions"></a>Datenbankfunktionen

Dieses Material richtet sich an Entwickler, die eigene Setup Programme und Entwickler schreiben, die mehr über die Installer-Datenbanktabellen erfahren möchten. Allgemeine Informationen zum Installationsprogramm finden Sie unter Informationen [zu Windows Installer](about-windows-installer.md).

Sie können die installerzugriffsfunktionen verwenden, um auf die Datenbank und den Installationsvorgang zuzugreifen. Diese Funktionen sollten nur von benutzerdefinierten Installations Aktionen und Erstellungs Tools verwendet werden. Einige der Installer-Zugriffs Funktionen erfordern SQL-Abfrage Zeichenfolgen zum Abfragen der Datenbank. Abfragen müssen der [SQL-Syntax](sql-syntax.md)des Installers entsprechen.

In diesem Thema werden die Installer-Datenbankzugriffs Funktionen nach Kategorie aufgelistet.

## <a name="general-database-access-functions"></a>Allgemeine Datenbankzugriffs Funktionen



| Funktion                                                             | BESCHREIBUNG                                                                             |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)                       | Führt einen Commit für Änderungen an einer Datenbank aus.                                                          |
| [**Msidatabasegetprimarykeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)       | Gibt die Namen aller Primärschlüssel Spalten zurück.                                       |
| [**Msidatabaseistablepersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta) | Gibt eine Enumeration zurück, die den Status einer Tabelle beschreibt.                                 |
| [**Msidatabaseopenview**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)                   | Bereitet eine Datenbankabfrage vor und erstellt ein Ansichts Objekt.                                    |
| [**Fehler durch MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)                 | Gibt die aktive Datenbank für die Installation zurück.                                       |
| [**Msiviewgetcolumninfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)                 | Gibt Spaltennamen oder-Definitionen zurück.                                                    |
| [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)                           | Öffnet eine Datenbankdatei für den Datenzugriff.                                                  |
| [**Msiviewclose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)                                 | Gibt das Resultset für eine ausgeführte Ansicht frei.                                           |
| [**Msiviewexecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)                             | Führt die Ansichts Abfrage aus und stellt erforderliche Parameter bereit.                               |
| [**Msiviewfetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)                                 | Ruft den nächsten sequenziellen Datensatz aus der Sicht ab.                                       |
| [**Msiviewgeterror**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)                           | Gibt den Fehler zurück, der in der [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) -Funktion aufgetreten ist. |
| [**Msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)                               | Aktualisiert einen abgerufenen Datensatz.                                                               |



 

## <a name="database-management-functions"></a>Daten Bank Verwaltungsfunktionen



| Funktion                                                               | BESCHREIBUNG                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) | Erstellt Zusammenfassungs Informationen für eine vorhandene Transformation.           |
| [**Msidatabaseapplytransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)         | Wendet eine Transformation auf eine Datenbank an.                               |
| [**Msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)                         | Exportiert eine Tabelle aus einer geöffneten Datenbank in eine Textarchiv Datei.    |
| [**Msidatabasegeneratetransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)   | Generiert eine Transformations Datei mit Unterschieden zwischen zwei Datenbanken. |
| [**Msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)                         | Importiert eine Installer-Textarchiv Tabelle in eine geöffnete Datenbank.   |
| [**Msidatabasemerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)                           | Führt zwei Datenbanken zusammen zusammen.                                   |
| [**Msigetdatabasestate**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)                     | Gibt den Status der Datenbank zurück.                               |



 

## <a name="record-processing-functions"></a>Aufzeichnen von Verarbeitungsfunktionen



| Funktion                                                 | BESCHREIBUNG                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------|
| [**Msikreaterecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)               | Erstellt ein neues Datensatz-Objekt mit der angegebenen Anzahl von Feldern.      |
| [**Msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)               | Formatiert Daten von Daten Satz Feldern und Eigenschaften mit einer Format Zeichenfolge. |
| [**Msirecordcleardata**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)         | Legt alle Felder in einem Datensatz auf NULL fest.                            |
| [**Msirecorddatasize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize)           | Gibt die Länge eines Datensatz-Felds zurück.                           |
| [**Msirecordgetfieldcount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) | Gibt die Anzahl von Feldern in einem Datensatz zurück                       |
| [**Msirecordgetinteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)       | Gibt den ganzzahligen Wert aus einem Daten Satz Feld zurück.                  |
| [**Msirecordgetstring**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)         | Gibt den Zeichen folgen Wert eines Datensatz-Felds zurück.                     |
| [**Msirecordisnull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)               | Meldet, ob ein Daten Satz Feld NULL ist.                         |
| [**Msirecordlesstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)       | Liest Bytes aus einem Daten Satz-Datenstrom Feld in einen Puffer.           |
| [**Msirecordsetinteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)       | Legt ein Daten Satz Feld auf ein ganzzahliges Feld fest.                        |
| [**Msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)         | Legt ein Daten Satz-Datenstrom Feld aus einer Datei fest.                         |
| [**Msirecordsetstring**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)         | Kopiert eine Zeichenfolge in das angegebene Feld.                      |



 

## <a name="summary-information-property-functions"></a>Eigenschaften Funktionen für Zusammenfassungs Informationen



| Funktion                                                                 | BESCHREIBUNG                                                            |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Msigetsummaryinformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)             | Ruft das Handle für den Zusammenfassungs Datenstrom der Installer-Datenbank ab.    |
| [**Msisummaryinfogetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)           | Ruft eine einzelne Eigenschaft aus den Zusammenfassungs Informationen ab.                   |
| [**Msisummaryinfogetpropertycount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) | Gibt die Anzahl der Eigenschaften im Zusammenfassungs Informationsdaten Strom zurück.        |
| [**Msisummaryinfopersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist)                   | Schreibt geänderte Zusammenfassungs Informationen zurück in den Zusammenfassungs Datenstrom. |
| [**Msisummaryinfosetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)           | Legt eine einzelne Zusammenfassungs Informations Eigenschaft fest.                            |



 

## <a name="installer-state-access-functions"></a>Installer-Zustands Zugriffs Funktionen



| Funktion                                               | BESCHREIBUNG                                                 |
|--------------------------------------------------------|-------------------------------------------------------------|
| [**Msigetlanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)               | Gibt die numerische Sprache der aktuellen Installation zurück.   |
| [**Msigetlasterrorrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlasterrorrecord) | Gibt den zuletzt zurückgegebenen Fehler Daten Satz für den aufrufenden Prozess zurück. |
| [**Msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)                       | Gibt einen der booleschen internen Installations Zustände zurück.    |
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)               | Ruft den Wert einer installereigenschaft ab.                    |
| [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)               | Legt den Wert einer Installations Eigenschaft fest.                 |
| [**Msisetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)                       | Legt einen booleschen Wert für die interne Engine fest.                      |



 

## <a name="installer-action-functions"></a>Installer-Aktions Funktionen



| Funktion                                             | BESCHREIBUNG                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**Msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)                   | Führt eine integrierte Aktion, eine benutzerdefinierte Aktion oder eine Aktion des Benutzeroberflächen-Assistenten aus. |
| [**Msievaluatecondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) | Wertet einen bedingten Ausdruck aus, der Eigenschaftsnamen und-Werte enthält.  |
| [**Msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)       | Sendet einen Fehler Daten Satz zur Verarbeitung an den Installer.                    |
| [**Msisequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)                   | Führt eine Aktions Sequenz aus.                                              |



 

## <a name="installer-location-functions"></a>Installationsort-Funktionen



| Funktion                                     | BESCHREIBUNG                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**Msigetsourcepath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) | Gibt den vollständigen Quellpfad für einen Ordner in der Verzeichnis Tabelle zurück. |
| [**Msigettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) | Gibt den vollständigen Zielpfad für einen Ordner in der Verzeichnis Tabelle zurück. |
| [**Msisettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) | Legt den vollständigen Zielpfad für einen Ordner in der Verzeichnis Tabelle fest.    |



 

## <a name="installer-selection-functions"></a>Installerauswahlfunktionen



| Funktion                                                     | BESCHREIBUNG                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [**Msienumschlag componentcosts**](/windows/desktop/api/Msiquery/nf-msiquery-msienumcomponentcostsa)       | Listet den Speicherplatz pro Laufwerk auf, der für die Installation einer Komponente erforderlich ist. |
| [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)         | Ruft den Status einer Komponente ab.                                    |
| [**Msigetfeaturecost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)               | Gibt den für eine Funktion erforderlichen Speicherplatz zurück.                        |
| [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)             | Ruft den Status einer Funktion ab.                                         |
| [**Msigetfeaturevalidstates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) | Gibt einen gültigen Installationsstatus zurück.                                  |
| [**Msisetcomponentstate**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)         | Legt eine Komponente auf den angegebenen Zustand fest.                             |
| [**Msisetfeatureattribute**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa)   | Ändert die Standard Attribute eines Features zur Laufzeit.            |
| [**Msisetfeaturestate**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)             | Legt eine Funktion auf einen angegebenen Zustand fest.                                 |
| [**Msisetinstalllevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)             | Legt die Installations Ebene einer vollständigen Produktinstallation fest.          |
| [**Msiverifydiskspace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)             | Prüft auf ausreichenden Speicherplatz                                    |



 

## <a name="user-interface-functions"></a>Benutzeroberflächen Funktionen



| Funktion                                           | BESCHREIBUNG                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**Msienableuipreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)   | Aktiviert den Vorschaumodus der Benutzeroberfläche.                             |
| [**Msipreviewbillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) | Zeigt im angezeigten Dialogfeld ein Billboard mit dem Host Steuerelement an. |
| [**Msipreviewdialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)       | Zeigt ein Dialogfeld als nicht modalem und inaktiv an.                         |



 

Alle-Funktionen unterstützen sowohl ANSI-als auch Unicode-Aufrufe. Um diese Funktionen zu verwenden, schließen Sie msiquery. h ein, und verknüpfen Sie Sie mit MSI. lib.

## <a name="installation-functions"></a>Installationsfunktionen

Zusätzlich zu den oben aufgeführten Datenbankzugriffs Funktionen erstellen Sie ein Installationspaket für eine Anwendung, indem Sie die installerfunktionen verwenden, die im Abschnitt [installationsfunktionsverweis](installer-function-reference.md) aufgeführt sind.

 

 



