---
description: In diesem Abschnitt werden die Windows Shell-Registrierungsfunktionen beschrieben. Die in dieser Dokumentation erläuterten Programmierelemente werden von Shlwapi.dll exportiert und in Shlwapi.h und Shlwapi.lib definiert.
title: Shell Registry Handling Functions
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 12182f56-5bb3-4f70-ae6a-2ef7366287b9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7bd7204ada31db6791d3cb78d1a11087d19eae45f0cacbfdf6ae6e032ae66a04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676499"
---
# <a name="shell-registry-handling-functions"></a>Shell Registry Handling Functions

In diesem Abschnitt werden die Windows Shell-Registrierungsfunktionen beschrieben. Die in dieser Dokumentation erläuterten Programmierelemente werden von Shlwapi.dll exportiert und in Shlwapi.h und Shlwapi.lib definiert.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                             | Beschreibung                                                                                                                                                                         |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate)<br/>                     | Gibt einen Zeiger auf ein [**IQueryAssociations-Objekt**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) zurück.<br/>                                                                                         |
| [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype)<br/> | Ruft den wahrgenommenen Typ einer Datei basierend auf ihrer Erweiterung ab.<br/>                                                                                                                |
| [**AssocIsDangerous**](/windows/desktop/api/Shlwapi/nf-shlwapi-associsdangerous)<br/>           | Bestimmt, ob ein Dateityp als potenzielles Sicherheitsrisiko angesehen wird.<br/>                                                                                                  |
| [**AssocQueryKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerykeya)<br/>                 | Sucht nach einem Schlüssel, der sich auf eine Datei- oder Protokollzuordnung in der Registrierung bezieht, und ruft diesen ab.<br/>                                                                            |
| [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)<br/>           | Sucht nach einer datei- oder protokollzuordnungsbezogenen Zeichenfolge in der Registrierung und ruft diese ab.<br/>                                                                              |
| [**AssocQueryStringByKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringbykeya)<br/> | Sucht nach einer dateizuordnungsbezogenen Zeichenfolge aus der Registrierung und ruft sie ab einem angegebenen Schlüssel ab.<br/>                                                            |
| [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya)<br/>                         | Kopiert rekursiv die Unterschlüssel und Werte des Quellunterschlüssels in den Zielschlüssel. [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya) kopiert die Sicherheitsattribute der Schlüssel nicht.<br/> |
| [**SHDeleteEmptyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeleteemptykeya)<br/>           | Löscht einen leeren Schlüssel.<br/>                                                                                                                                                    |
| [**SHDeleteKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletekeya)<br/>                     | Löscht einen Unterschlüssel und alle seine Nachfolger. Diese Funktion entfernt den Schlüssel und alle Schlüsselwerte aus der Registrierung.<br/>                                                      |
| [**SHDeleteValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletevaluea)<br/>                 | Löscht einen benannten Wert aus dem angegebenen Registrierungsschlüssel.<br/>                                                                                                                   |
| [**SHEnumKeyEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumkeyexa)<br/>                     | Listet die Unterschlüssel des angegebenen geöffneten Registrierungsschlüssels auf.<br/>                                                                                                               |
| [**SHEnumValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumvaluea)<br/>                     | Listet die Werte des angegebenen offenen Registrierungsschlüssels auf.<br/>                                                                                                                |
| [**SHGetAssocKeys**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetassockeys)<br/>               | Ruft ein Array von Klassenunterschlüsseln ab, die einem [**IQueryAssociations-Objekt**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) zugeordnet sind.<br/>                                                          |
| [**SHGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetvaluea)<br/>                       | Ruft einen Registrierungswert ab.<br/>                                                                                                                                              |
| [**SHOpenRegStream2**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstream2a)<br/>           | Öffnet einen Registrierungswert und stellt einen Stream bereit, mit dem aus dem Wert gelesen oder in diesen geschrieben werden kann. Diese Funktion ersetzt [**SHOpenRegStream.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstreama)<br/>   |
| [**SHQueryInfoKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryinfokeya)<br/>               | Ruft Informationen zu einem angegebenen Registrierungsschlüssel ab.<br/>                                                                                                                    |
| [**SHQueryValueEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryvalueexa)<br/>               | Öffnet einen Registrierungsschlüssel und fragt ihn nach einem bestimmten Wert ab.<br/>                                                                                                                |
| [**SHRegCloseUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcloseuskey)<br/>             | Schließt ein Handle für einen benutzerspezifischen Registrierungsunterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>                                             |
| [**SHRegCreateUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcreateuskeya)<br/>           | Erstellt oder öffnet einen Registrierungsunterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>                                                             |
| [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteemptyuskeya)<br/> | Löscht einen leeren Registrierungsunterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>                                                               |
| [**SHRegDeleteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteusvaluea)<br/>       | Löscht einen Registrierungsunterschlüsselwert in einer benutzerspezifischen Unterstruktur (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>                                                                |
| [**SHRegDuplicateHKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregduplicatehkey)<br/>       | Dupliziert das HKEY-Handle eines Registrierungsschlüssels.<br/>                                                                                                                                 |
| [**SHRegEnumUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumuskeya)<br/>               | Listet die Unterschlüssel eines Registrierungsunterschlüssels in einer benutzerspezifischen Unterstruktur auf (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>                                                    |
| [**SHRegEnumUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumusvaluea)<br/>           | Listet die Werte des angegebenen Registrierungsunterschlüssels in einer benutzerspezifischen Unterstruktur auf (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>                                         |
| [**SHRegGetBoolUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetboolusvaluea)<br/>     | Ruft einen booleschen Wert aus einem Registrierungsunterschlüssel in einer benutzerspezifischen Unterstruktur ab (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>                                               |
| [**SHRegGetIntW**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetintw)<br/>                    | Liest einen numerischen Zeichenfolgenwert aus der Registrierung und konvertiert ihn in eine ganze Zahl.<br/>                                                                                            |
| [**SHRegGetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetpatha)<br/>                   | Ruft einen Dateipfad aus der Registrierung ab und erweitert nach Bedarf Umgebungsvariablen.<br/>                                                                                      |
| [**SHRegGetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetusvaluea)<br/>             | Ruft einen Wert aus einem Registrierungsunterschlüssel in einer benutzerspezifischen Unterstruktur ab (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>                                                       |
| [**SHRegOpenUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregopenuskeya)<br/>               | Öffnet einen Registrierungsunterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>                                                                        |
| [**SHRegQueryInfoUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryinfouskeya)<br/>     | Ruft Informationen zu einem angegebenen Registrierungsunterschlüssel in einer benutzerspezifischen Unterstruktur ab (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>                                        |
| [**SHRegQueryUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryusvaluea)<br/>         | Ruft den Typ und die Daten für einen angegebenen Namen ab, der einem geöffneten Registrierungsunterschlüssel in einer benutzerspezifischen Unterstruktur zugeordnet ist (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>       |
| [**SHRegSetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetpatha)<br/>                   | Übernimmt einen Dateipfad, ersetzt Ordnernamen durch Umgebungszeichenfolgen und platziert die resultierende Zeichenfolge in der Registrierung.<br/>                                                      |
| [**SHRegSetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetusvaluea)<br/>             | Legt einen Registrierungsunterschlüsselwert in einer benutzerspezifischen Unterstruktur (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE) fest.<br/>                                                                   |
| [**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)<br/>                 | Legt einen Registrierungswert fest.<br/> Verwenden Sie [**Statt regSetValue.**](/windows/win32/api/winreg/nf-winreg-regsetvaluea)<br/>                                                                                  |
| [**SHRegWriteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregwriteusvaluea)<br/>         | Schreibt einen Wert in einen Registrierungsunterschlüssel in einer benutzerspezifischen Unterstruktur (HKEY \_ CURRENT \_ USER oder HKEY LOCAL \_ \_ MACHINE).<br/>                                                            |
| [**SHSetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetvaluea)<br/>                       | Legt den Wert eines Registrierungsschlüssels fest.<br/>                                                                                                                                        |



 

 

 
