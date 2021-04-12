---
description: Im folgenden finden Sie die Registrierungsfunktionen.
ms.assetid: a490b748-42e8-462b-9a7f-a8b21438ea79
title: Registrierungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2cfadd3753b7a269667fee22955f8465495458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216334"
---
# <a name="registry-functions"></a>Registrierungsfunktionen

Im folgenden finden Sie die Registrierungsfunktionen.



| Funktion                                                           | BESCHREIBUNG                                                                                                                                    |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getsystemregistryquota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)           | Ruft die aktuelle Größe der Registrierung und die maximale Größe ab, die die Registrierung auf dem System erreichen darf.                          |
| [**Fehler bei RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey)                                 | Schließt ein Handle für den angegebenen Registrierungsschlüssel.                                                                                                 |
| [**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya)                   | Stellt eine Verbindung mit einem vordefinierten Registrierungs Handle auf einem anderen Computer her.                                                                  |
| [**Regcopytree**](/windows/desktop/api/Winreg/nf-winreg-regcopytreea)                                 | Kopiert den angegebenen Registrierungsschlüssel zusammen mit den zugehörigen Werten und unter Schlüsseln in den angegebenen Ziel Schlüssel.                                        |
| [**Regkreatekeyex**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa)                           | Erstellt den angegebenen Registrierungsschlüssel.                                                                                                            |
| [**Regkreatekeytransagiert**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda)           | Erstellt den angegebenen Registrierungsschlüssel und ordnet ihn einer Transaktion zu.                                                                       |
| [**Regdeletekey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya)                               | Löscht einen Unterschlüssel und seine Werte.                                                                                                               |
| [**Regdeletekeyex**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyexa)                           | Löscht einen Unterschlüssel und seine Werte aus der angegebenen plattformspezifischen Sicht der Registrierung.                                                     |
| [**Regdeletekeytranshandelten**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeytransacteda)           | Löscht einen Unterschlüssel und seine Werte aus der angegebenen plattformspezifischen Sicht der Registrierung als transaktiven Vorgang.                           |
| [**Regdeletekeyvalue**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyvaluea)                     | Entfernt den angegebenen Wert aus dem angegebenen Registrierungsschlüssel und Unterschlüssel.                                                                        |
| [**Regdeletetree**](/windows/desktop/api/Winreg/nf-winreg-regdeletetreea)                             | Löscht die Unterschlüssel und Werte des angegebenen Schlüssels rekursiv.                                                                               |
| [**Fehler bei RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea)                           | Entfernt einen benannten Wert aus dem angegebenen Registrierungsschlüssel.                                                                                         |
| [**Regdisablepredefinedcache**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcache)     | Deaktiviert das Handle Zwischenspeichern für das vordefinierte Registrierungs Handle für den aktuellen **HKEY- \_ \_ Benutzer** für den aktuellen Prozess.                                |
| [**Regdisablepredefinedcacheex**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcacheex) | Deaktiviert das Zwischenspeichern von Handles für alle vordefinierten Registrierungs Handles für den aktuellen Prozess.                                                           |
| [**Regdisablereflectionkey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey)         | Deaktiviert die Registrierungs Reflektion für den angegebenen Schlüssel.                                                                                            |
| [**"Regenablereflectionkey"**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey)           | Aktiviert die Registrierungs Reflektion für den angegebenen deaktivierten Schlüssel.                                                                                    |
| [**Regenum keyex**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)                               | Listet die Unterschlüssel des angegebenen geöffneten Registrierungsschlüssels auf.                                                                                     |
| [**RegenWert**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea)                               | Listet die Werte für den angegebenen geöffneten Registrierungsschlüssel auf.                                                                                     |
| [**Wurde von regflushkey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey)                                 | Schreibt alle Attribute des angegebenen geöffneten Registrierungsschlüssels in die Registrierung.                                                                    |
| [**Reggetkeysecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity)                | Ruft eine Kopie der Sicherheits Beschreibung ab, die den angegebenen geöffneten Registrierungsschlüssel schützt.                                                        |
| [**Reggetvalue**](/windows/desktop/api/Winreg/nf-winreg-reggetvaluea)                                 | Ruft den Typ und die Daten für den angegebenen Registrierungs Wert ab.                                                                                  |
| [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya)                                   | Erstellt einen Unterschlüssel unter **HKEY- \_ Benutzer** oder **HKEY \_ local \_ Machine** und speichert Registrierungsinformationen aus einer angegebenen Datei in diesem Unterschlüssel. |
| [**Regloadmuistring**](/windows/desktop/api/Winreg/nf-winreg-regloadmuistringa)                       | Lädt die angegebene Zeichenfolge aus dem angegebenen Schlüssel und Unterschlüssel.                                                                                  |
| [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue)         | Benachrichtigt den Aufrufer über Änderungen an den Attributen oder Inhalten eines angegebenen Registrierungsschlüssels.                                                   |
| [**Regopencurrentuser**](/windows/desktop/api/Winreg/nf-winreg-regopencurrentuser)                   | Ruft ein Handle für den **aktuellen HKEY \_ - \_ Benutzer** Schlüssel für den Benutzer ab, der vom aktuellen Thread angenommen wird.                                        |
| [**Fehler bei RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa)                               | Öffnet den angegebenen Registrierungsschlüssel.                                                                                                              |
| [**Regopenkeytransagiert**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda)               | Öffnet den angegebenen Registrierungsschlüssel und ordnet ihn einer Transaktion zu.                                                                         |
| [**Regopenuserclassesroot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot)           | Ruft ein Handle für den **HKEY- \_ Klassen \_** Stamm Schlüssel für den angegebenen Benutzer ab.                                                                  |
| [**Regoverridepredefkey**](/windows/desktop/api/Winreg/nf-winreg-regoverridepredefkey)               | Ordnet einem angegebenen Registrierungsschlüssel einen vordefinierten Registrierungsschlüssel zu.                                                                                    |
| [**Regqueryinfokey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya)                         | Ruft Informationen über den angegebenen Registrierungsschlüssel ab.                                                                                        |
| [**Regquerymultiplevalues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa)           | Ruft den Typ und die Daten für eine Liste von Wert Namen ab, die einem geöffneten Registrierungsschlüssel zugeordnet sind.                                                    |
| [**Regqueryreflectionkey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey)             | Bestimmt, ob die Reflektion für den angegebenen Schlüssel deaktiviert oder aktiviert wurde.                                                              |
| [**Fehler bei RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa)                         | Ruft den Typ und die Daten für einen angegebenen Wert Namen ab, der einem geöffneten Registrierungsschlüssel zugeordnet ist.                                                   |
| [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)                             | Ersetzt die Datei, die einen Registrierungsschlüssel und alle seine Unterschlüssel durch eine andere Datei unterstützt.                                                                |
| [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya)                             | Liest die Registrierungsinformationen in einer angegebenen Datei und kopiert Sie über den angegebenen Schlüssel.                                                       |
| [**Regsavekey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya)                                   | Speichert den angegebenen Schlüssel und alle seine Unterschlüssel und Werte in einer neuen Datei.                                                                       |
| [**Regsavekeyex**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa)                               | Speichert den angegebenen Schlüssel und alle seine Unterschlüssel und Werte in einer neuen Datei. Sie können das Format für den gespeicherten Schlüssel oder die Hive-Struktur angeben.                 |
| [**Regsetkeyvalue**](/windows/desktop/api/Winreg/nf-winreg-regsetkeyvaluea)                           | Legt die Daten für den angegebenen Wert im angegebenen Registrierungsschlüssel und Unterschlüssel fest.                                                                |
| [**Regsetkeysecurity**](/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity)                | Legt die Sicherheit eines geöffneten Registrierungsschlüssels fest.                                                                                                     |
| [**Fehler bei RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa)                             | Legt die Daten und den Typ eines angegebenen Werts unter einem Registrierungsschlüssel fest.                                                                              |
| [**Regunloadkey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya)                               | Entlädt den angegebenen Registrierungsschlüssel und dessen Unterschlüssel aus der Registrierung.                                                                          |



 

Die folgenden Shellfunktionen können mit der Registrierung verwendet werden:

-   [**Assoccreate**](/windows/desktop/api/shlwapi/nf-shlwapi-assoccreate)
-   [**Assocquerykey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerykeya)
-   [**Assocquerystring**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringa)
-   [**Assocquerystringbykey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringbykeya)
-   [**Shcopykey**](/windows/desktop/api/shlwapi/nf-shlwapi-shcopykeya)
-   [**Shdeleteemptykey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeleteemptykeya)
-   [**Shdeletekey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletekeya)
-   [**Shdeletevalue**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletevaluea)
-   [**Shenumkeyex**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumkeyexa)
-   [**Shenumvalue**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumvaluea)
-   [**Shgetvalue**](/windows/desktop/api/shlwapi/nf-shlwapi-shgetvaluea)
-   [**Shqueryinfokey**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryinfokeya)
-   [**Shqueryvalueex**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryvalueexa)
-   [**Shregcloseukey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcloseuskey)
-   [**Shregkreateuskey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcreateuskeya)
-   [**Shregdeleteemptyukey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteemptyuskeya)
-   [**Shregdeletestartvalue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteusvaluea)
-   [**Shregduplialisiehkey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregduplicatehkey)
-   [**Shregenumuskey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumuskeya)
-   [**Shregenumusvalue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumusvaluea)
-   [**Shreggetboolsvalue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetboolusvaluea)
-   [**Shreggetintw**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetintw)
-   [**Shreggetpath**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetpatha)
-   [**Shreggetusvalue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetusvaluea)
-   [**Shregopenukey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya)
-   [**Shregqueryinfouskey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryinfouskeya)
-   [**Shregqueryusvalue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryusvaluea)
-   [**Shregsetpath**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetpatha)
-   [**Shregeintewert**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetusvaluea)
-   [**Shregschreitestartwert**](/windows/desktop/api/shlwapi/nf-shlwapi-shregwriteusvaluea)
-   [**Shsetvalue**](/windows/desktop/api/shlwapi/nf-shlwapi-shsetvaluea)

Im folgenden finden Sie die Funktionen für die Initialisierungsdatei. Sie rufen Informationen aus ab und kopieren Informationen in eine System-oder Anwendungs definierte Initialisierungsdatei. Diese Funktionen werden nur aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt. Neue Anwendungen sollten die Registrierung verwenden.



| Funktion                                                               | BESCHREIBUNG                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**Getprivateprofileint**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofileint)                   | Ruft eine Ganzzahl ab, die einem Schlüssel im angegebenen Abschnitt einer Initialisierungsdatei zugeordnet ist.     |
| [**GetPrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesection)           | Ruft alle Schlüssel und Werte für den angegebenen Abschnitt einer Initialisierungsdatei ab.             |
| [**GetPrivateProfileSectionNames**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesectionnames) | Ruft die Namen aller Abschnitte in einer Initialisierungsdatei ab.                                     |
| [**GetPrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestring)             | Ruft eine Zeichenfolge aus dem angegebenen Abschnitt in einer Initialisierungsdatei ab.                           |
| [**Getprivateprofilestruct**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestruct)             | Ruft die einem Schlüssel zugeordneten Daten im angegebenen Abschnitt einer Initialisierungsdatei ab.       |
| [**GetProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprofileinta)                                 | Ruft eine ganze Zahl aus einem Schlüssel im angegebenen Abschnitt der Win.ini Datei ab.                      |
| [**GetProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprofilesectiona)                         | Ruft alle Schlüssel und Werte für den angegebenen Abschnitt der Win.ini Datei ab.                   |
| [**GetProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprofilestringa)                           | Ruft die Zeichenfolge ab, die einem Schlüssel im angegebenen Abschnitt der Win.ini Datei zugeordnet ist.           |
| [**"Beschreib teprivateprofilesection"**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilesectiona)       | Ersetzt die Schlüssel und Werte für den angegebenen Abschnitt in einer Initialisierungsdatei.                  |
| [**"Schreibprivateprofilestring"**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestringa)         | Kopiert eine Zeichenfolge in den angegebenen Abschnitt einer Initialisierungsdatei.                              |
| [**"Schreibprivateprofilestruct"**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestructa)         | Kopiert Daten in einen Schlüssel im angegebenen Abschnitt einer Initialisierungsdatei.                         |
| [**Beschreibprofilesection**](/windows/desktop/api/Winbase/nf-winbase-writeprofilesectiona)                     | Ersetzt den Inhalt des angegebenen Abschnitts in der Win.ini Datei durch angegebene Schlüssel und Werte. |
| [**"Schreibprofilestring"**](/windows/desktop/api/Winbase/nf-winbase-writeprofilestringa)                       | Kopiert eine Zeichenfolge in den angegebenen Abschnitt der Win.ini Datei.                                    |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Diese Funktionen werden nur für die Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt:

-   [**Regkreatekey**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeya)
-   [**Regen Taste**](/windows/desktop/api/Winreg/nf-winreg-regenumkeya)
-   [**RegOpenKey**](/windows/desktop/api/Winreg/nf-winreg-regopenkeya)
-   [**RegQueryValue**](/windows/desktop/api/Winreg/nf-winreg-regqueryvaluea)
-   [**RegSetValue**](/windows/desktop/api/Winreg/nf-winreg-regsetvaluea)

 

 
