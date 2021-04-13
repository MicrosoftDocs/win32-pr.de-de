---
description: In diesem Abschnitt werden die Funktionen der Windows Shell-Registrierungs Behandlung beschrieben. Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.
title: Verarbeitungsfunktionen für die Shellregistrierung
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 12182f56-5bb3-4f70-ae6a-2ef7366287b9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8a3e4f65904fa97635b3ef4dc3abd9f01344f6a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995070"
---
# <a name="shell-registry-handling-functions"></a>Verarbeitungsfunktionen für die Shellregistrierung

In diesem Abschnitt werden die Funktionen der Windows Shell-Registrierungs Behandlung beschrieben. Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                             | BESCHREIBUNG                                                                                                                                                                         |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Assoccreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate)<br/>                     | Gibt einen Zeiger auf ein [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Objekt zurück.<br/>                                                                                         |
| [**"Assocgetwahrnehmvedtype"**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype)<br/> | Ruft den erkannten Datentyp einer Datei basierend auf der Erweiterung ab.<br/>                                                                                                                |
| [**Assozisgefährlich**](/windows/desktop/api/Shlwapi/nf-shlwapi-associsdangerous)<br/>           | Bestimmt, ob ein Dateityp ein potenzielles Sicherheitsrisiko darstellt.<br/>                                                                                                  |
| [**Assocquerykey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerykeya)<br/>                 | Sucht nach einem Schlüssel, der sich auf eine Datei-oder Protokoll Zuordnung aus der Registrierung bezieht, und ruft ihn ab.<br/>                                                                            |
| [**Assocquerystring**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)<br/>           | Sucht nach einer Datei-oder Protokoll Zuordnungs bezogenen Zeichenfolge aus der Registrierung und ruft Sie ab.<br/>                                                                              |
| [**Assocquerystringbykey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringbykeya)<br/> | Sucht und ruft eine Datei Zuordnungs bezogene Zeichenfolge aus der Registrierung ab, beginnend mit einem angegebenen Schlüssel.<br/>                                                            |
| [**Shcopykey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya)<br/>                         | Kopiert die Unterschlüssel und Werte des Quell unter Schlüssels rekursiv in den Ziel Schlüssel. " [**Shcopykey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya) " kopiert nicht die Sicherheits Attribute der Schlüssel.<br/> |
| [**Shdeleteemptykey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeleteemptykeya)<br/>           | Löscht einen leeren Schlüssel.<br/>                                                                                                                                                    |
| [**Shdeletekey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletekeya)<br/>                     | Löscht einen Unterschlüssel und alle untergeordneten Elemente. Diese Funktion entfernt den Schlüssel und alle Schlüsselwerte aus der Registrierung.<br/>                                                      |
| [**Shdeletevalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletevaluea)<br/>                 | Löscht einen benannten Wert aus dem angegebenen Registrierungsschlüssel.<br/>                                                                                                                   |
| [**Shenumkeyex**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumkeyexa)<br/>                     | Listet die Unterschlüssel des angegebenen geöffneten Registrierungsschlüssels auf.<br/>                                                                                                               |
| [**Shenumvalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumvaluea)<br/>                     | Listet die Werte des angegebenen geöffneten Registrierungsschlüssels auf.<br/>                                                                                                                |
| [**Shgetassockeys**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetassockeys)<br/>               | Ruft ein Array von-Klassen unter Schlüsseln ab, die einem [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Objekt zugeordnet sind.<br/>                                                          |
| [**Shgetvalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetvaluea)<br/>                       | Ruft einen Registrierungs Wert ab.<br/>                                                                                                                                              |
| [**SHOpenRegStream2**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstream2a)<br/>           | Öffnet einen Registrierungs Wert und stellt einen Datenstrom bereit, der zum Lesen oder Schreiben des Werts verwendet werden kann. Diese Funktion löst [**shopenregstream**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstreama)aus.<br/>   |
| [**Shqueryinfokey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryinfokeya)<br/>               | Ruft Informationen zu einem angegebenen Registrierungsschlüssel ab.<br/>                                                                                                                    |
| [**Shqueryvalueex**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryvalueexa)<br/>               | Öffnet einen Registrierungsschlüssel und fragt ihn nach einem bestimmten Wert ab.<br/>                                                                                                                |
| [**Shregcloseukey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcloseuskey)<br/>             | Schließt ein Handle für einen benutzerspezifischen Registrierungs Unterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine).<br/>                                             |
| [**Shregkreateuskey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcreateuskeya)<br/>           | Erstellt oder öffnet einen Registrierungs Unterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine).<br/>                                                             |
| [**Shregdeleteemptyukey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteemptyuskeya)<br/> | Löscht einen leeren Registrierungs Unterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine).<br/>                                                               |
| [**Shregdeletestartvalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteusvaluea)<br/>       | Löscht einen Registrierungs Unterschlüssel Wert in einer benutzerspezifischen Unterstruktur (aktueller HKEY \_ - \_ Benutzer oder HKEY- \_ lokaler \_ Computer).<br/>                                                                |
| [**Shregduplialisiehkey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregduplicatehkey)<br/>       | Dupliziert das HKEY-Handle eines Registrierungsschlüssels.<br/>                                                                                                                                 |
| [**Shregenumuskey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumuskeya)<br/>               | Listet die Unterschlüssel eines Registrierungs unter Schlüssels in einer benutzerspezifischen Unterstruktur auf (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine).<br/>                                                    |
| [**Shregenumusvalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumusvaluea)<br/>           | Listet die Werte des angegebenen Registrierungs unter Schlüssels in einer benutzerspezifischen Unterstruktur (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine) auf.<br/>                                         |
| [**Shreggetboolsvalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetboolusvaluea)<br/>     | Ruft einen booleschen Wert aus einem Registrierungs Unterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine) ab.<br/>                                               |
| [**Shreggetintw**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetintw)<br/>                    | Liest einen numerischen Zeichen folgen Wert aus der Registrierung und konvertiert ihn in eine ganze Zahl.<br/>                                                                                            |
| [**Shreggetpath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetpatha)<br/>                   | Ruft einen Dateipfad aus der Registrierung ab und erweitert die Umgebungsvariablen nach Bedarf.<br/>                                                                                      |
| [**Shreggetusvalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetusvaluea)<br/>             | Ruft einen Wert aus einem Registrierungs Unterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine) ab.<br/>                                                       |
| [**Shregopenukey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregopenuskeya)<br/>               | Öffnet einen Registrierungs Unterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine).<br/>                                                                        |
| [**Shregqueryinfouskey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryinfouskeya)<br/>     | Ruft Informationen zu einem angegebenen Registrierungs Unterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine) ab.<br/>                                        |
| [**Shregqueryusvalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryusvaluea)<br/>         | Ruft den Typ und die Daten für einen angegebenen Namen ab, der einem geöffneten Registrierungs Unterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine) zugeordnet ist.<br/>       |
| [**Shregsetpath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetpatha)<br/>                   | Nimmt einen Dateipfad an, ersetzt Ordnernamen durch Umgebungs Zeichenfolgen und platziert die resultierende Zeichenfolge in der Registrierung.<br/>                                                      |
| [**Shregeintewert**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetusvaluea)<br/>             | Legt einen Registrierungs Unterschlüssel Wert in einer benutzerspezifischen Unterstruktur (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine) fest.<br/>                                                                   |
| [**Shregsetvalue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)<br/>                 | Legt einen Registrierungs Wert fest.<br/> Verwenden Sie [**RegSetValue**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) an seiner Stelle.<br/>                                                                                  |
| [**Shregschreitestartwert**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregwriteusvaluea)<br/>         | Schreibt einen Wert in einen Registrierungs Unterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ Current \_ User oder HKEY \_ local \_ Machine).<br/>                                                            |
| [**Shsetvalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetvaluea)<br/>                       | Legt den Wert eines Registrierungsschlüssels fest.<br/>                                                                                                                                        |



 

 

 
