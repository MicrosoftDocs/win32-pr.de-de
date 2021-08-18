---
description: Im Folgenden finden Sie die Registrierungsfunktionen.
ms.assetid: a490b748-42e8-462b-9a7f-a8b21438ea79
title: Registrierungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81f5aff4dad00691f606911c1cf092933aa121eaf7a2d25aacbcc8a83948b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885213"
---
# <a name="registry-functions"></a>Registrierungsfunktionen

Im Folgenden finden Sie die Registrierungsfunktionen.



| Funktion                                                           | BESCHREIBUNG                                                                                                                                    |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)           | Ruft die aktuelle Größe der Registrierung und die maximale Größe ab, die die Registrierung auf dem System erreichen darf.                          |
| [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey)                                 | Schließt ein Handle für den angegebenen Registrierungsschlüssel.                                                                                                 |
| [**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya)                   | Stellt eine Verbindung mit einem vordefinierten Registrierungshand handle auf einem anderen Computer ein.                                                                  |
| [**RegCopyTree**](/windows/desktop/api/Winreg/nf-winreg-regcopytreea)                                 | Kopiert den angegebenen Registrierungsschlüssel zusammen mit seinen Werten und Unterschlüsseln in den angegebenen Zielschlüssel.                                        |
| [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa)                           | Erstellt den angegebenen Registrierungsschlüssel.                                                                                                            |
| [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda)           | Erstellt den angegebenen Registrierungsschlüssel und ordnet ihn einer Transaktion zu.                                                                       |
| [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya)                               | Löscht einen Unterschlüssel und seine Werte.                                                                                                               |
| [**RegDeleteKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyexa)                           | Löscht einen Unterschlüssel und seine Werte aus der angegebenen plattformspezifischen Ansicht der Registrierung.                                                     |
| [**RegDeleteKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeytransacteda)           | Löscht einen Unterschlüssel und seine Werte aus der angegebenen plattformspezifischen Ansicht der Registrierung als transaktiven Vorgang.                           |
| [**RegDeleteKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyvaluea)                     | Entfernt den angegebenen Wert aus dem angegebenen Registrierungsschlüssel und Unterschlüssel.                                                                        |
| [**RegDeleteTree**](/windows/desktop/api/Winreg/nf-winreg-regdeletetreea)                             | Löscht die Unterschlüssel und Werte des angegebenen Schlüssels rekursiv.                                                                               |
| [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea)                           | Entfernt einen benannten Wert aus dem angegebenen Registrierungsschlüssel.                                                                                         |
| [**RegDisablePredefinedCache**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcache)     | Deaktiviert die Handlezwischenspeicherung für das vordefinierte Registrierungshand handle für **HKEY \_ CURRENT USER \_ für** den aktuellen Prozess.                                |
| [**RegDisablePredefinedCacheEx**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcacheex) | Deaktiviert die Handlezwischenspeicherung für alle vordefinierten Registrierungshandles für den aktuellen Prozess.                                                           |
| [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey)         | Deaktiviert die Registrierungslektion für den angegebenen Schlüssel.                                                                                            |
| [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey)           | Aktiviert die Registrierungslektion für den angegebenen deaktivierten Schlüssel.                                                                                    |
| [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)                               | Enumeriert die Unterschlüssel des angegebenen offenen Registrierungsschlüssels.                                                                                     |
| [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea)                               | Enumeriert die Werte für den angegebenen offenen Registrierungsschlüssel.                                                                                     |
| [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey)                                 | Schreibt alle Attribute des angegebenen offenen Registrierungsschlüssels in die Registrierung.                                                                    |
| [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity)                | Ruft eine Kopie der Sicherheitsbeschreibung ab, die den angegebenen offenen Registrierungsschlüssel schützt.                                                        |
| [**RegGetValue**](/windows/desktop/api/Winreg/nf-winreg-reggetvaluea)                                 | Ruft den Typ und die Daten für den angegebenen Registrierungswert ab.                                                                                  |
| [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya)                                   | Erstellt einen Unterschlüssel unter **HKEY \_ USERS** oder **HKEY \_ LOCAL \_ MACHINE** und speichert Registrierungsinformationen aus einer angegebenen Datei in diesem Unterschlüssel. |
| [**RegLoadMUIString**](/windows/desktop/api/Winreg/nf-winreg-regloadmuistringa)                       | Lädt die angegebene Zeichenfolge aus dem angegebenen Schlüssel und Unterschlüssel.                                                                                  |
| [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue)         | Benachrichtigt den Aufrufer über Änderungen an den Attributen oder Inhalten eines angegebenen Registrierungsschlüssels.                                                   |
| [**RegOpenCurrentUser**](/windows/desktop/api/Winreg/nf-winreg-regopencurrentuser)                   | Ruft ein Handle für den **HKEY \_ CURRENT \_ USER-Schlüssel** für den Benutzer ab, der die Identität des aktuellen Threads anspricht.                                        |
| [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa)                               | Öffnet den angegebenen Registrierungsschlüssel.                                                                                                              |
| [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda)               | Öffnet den angegebenen Registrierungsschlüssel und ordnet ihn einer Transaktion zu.                                                                         |
| [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot)           | Ruft ein Handle für den **HKEY \_ CLASSES \_ ROOT-Schlüssel** für den angegebenen Benutzer ab.                                                                  |
| [**RegOverridePredefKey**](/windows/desktop/api/Winreg/nf-winreg-regoverridepredefkey)               | Karten vordefinierten Registrierungsschlüssel in einen angegebenen Registrierungsschlüssel.                                                                                    |
| [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya)                         | Ruft Informationen zum angegebenen Registrierungsschlüssel ab.                                                                                        |
| [**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa)           | Ruft den Typ und die Daten für eine Liste von Wertnamen ab, die einem geöffneten Registrierungsschlüssel zugeordnet sind.                                                    |
| [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey)             | Bestimmt, ob die Reflektion für den angegebenen Schlüssel deaktiviert oder aktiviert wurde.                                                              |
| [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa)                         | Ruft den Typ und die Daten für einen angegebenen Wertnamen ab, der einem geöffneten Registrierungsschlüssel zugeordnet ist.                                                   |
| [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)                             | Ersetzt die Datei, die einen Registrierungsschlüssel und alle ihre Unterschlüssel durch eine andere Datei ersetzt.                                                                |
| [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya)                             | Liest die Registrierungsinformationen in einer angegebenen Datei und kopiert sie über den angegebenen Schlüssel.                                                       |
| [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya)                                   | Speichert den angegebenen Schlüssel und alle seine Unterschlüssel und Werte in einer neuen Datei.                                                                       |
| [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa)                               | Speichert den angegebenen Schlüssel und alle seine Unterschlüssel und Werte in einer neuen Datei. Sie können das Format für den gespeicherten Schlüssel oder die Struktur angeben.                 |
| [**RegSetKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regsetkeyvaluea)                           | Legt die Daten für den angegebenen Wert im angegebenen Registrierungsschlüssel und Unterschlüssel fest.                                                                |
| [**RegSetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity)                | Legt die Sicherheit eines geöffneten Registrierungsschlüssels fest.                                                                                                     |
| [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa)                             | Legt die Daten und den Typ eines angegebenen Werts unter einem Registrierungsschlüssel fest.                                                                              |
| [**RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya)                               | Entlädt den angegebenen Registrierungsschlüssel und seine Unterschlüssel aus der Registrierung.                                                                          |



 

Die folgenden Shellfunktionen können mit der Registrierung verwendet werden:

-   [**AssocCreate**](/windows/desktop/api/shlwapi/nf-shlwapi-assoccreate)
-   [**AssocQueryKey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerykeya)
-   [**AssocQueryString**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringa)
-   [**AssocQueryStringByKey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringbykeya)
-   [**SHCopyKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shcopykeya)
-   [**SHDeleteEmptyKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeleteemptykeya)
-   [**SHDeleteKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletekeya)
-   [**SHDeleteValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletevaluea)
-   [**SHEnumKeyEx**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumkeyexa)
-   [**SHEnumValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumvaluea)
-   [**SHGetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shgetvaluea)
-   [**SHQueryInfoKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryinfokeya)
-   [**SHQueryValueEx**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryvalueexa)
-   [**SHRegCloseUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcloseuskey)
-   [**SHRegCreateUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcreateuskeya)
-   [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteemptyuskeya)
-   [**SHRegDeleteUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteusvaluea)
-   [**SHRegDuplicateHKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregduplicatehkey)
-   [**SHRegEnumUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumuskeya)
-   [**SHRegEnumUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumusvaluea)
-   [**SHRegGetBoolUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetboolusvaluea)
-   [**SHRegGetIntW**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetintw)
-   [**SHRegGetPath**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetpatha)
-   [**SHRegGetUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetusvaluea)
-   [**SHRegOpenUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya)
-   [**SHRegQueryInfoUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryinfouskeya)
-   [**SHRegQueryUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryusvaluea)
-   [**SHRegSetPath**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetpatha)
-   [**SHRegSetUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetusvaluea)
-   [**SHRegWriteUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregwriteusvaluea)
-   [**SHSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shsetvaluea)

Im Folgenden finden Sie die Initialisierungsdateifunktionen. Sie rufen Informationen aus ab und kopieren Informationen in eine system- oder anwendungsdefinierte Initialisierungsdatei. Diese Funktionen werden nur zur Kompatibilität mit 16-Bit-Versionen von Windows. Neue Anwendungen sollten die Registrierung verwenden.



| Funktion                                                               | BESCHREIBUNG                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**GetPrivateProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofileint)                   | Ruft eine ganze Zahl ab, die einem Schlüssel im angegebenen Abschnitt einer Initialisierungsdatei zugeordnet ist.     |
| [**GetPrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesection)           | Ruft alle Schlüssel und Werte für den angegebenen Abschnitt einer Initialisierungsdatei ab.             |
| [**GetPrivateProfileSectionNames**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesectionnames) | Ruft die Namen aller Abschnitte in einer Initialisierungsdatei ab.                                     |
| [**GetPrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestring)             | Ruft eine Zeichenfolge aus dem angegebenen Abschnitt in einer Initialisierungsdatei ab.                           |
| [**GetPrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestruct)             | Ruft die Daten ab, die einem Schlüssel im angegebenen Abschnitt einer Initialisierungsdatei zugeordnet sind.       |
| [**GetProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprofileinta)                                 | Ruft eine ganze Zahl aus einem Schlüssel im angegebenen Abschnitt der Win.ini ab.                      |
| [**GetProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprofilesectiona)                         | Ruft alle Schlüssel und Werte für den angegebenen Abschnitt der Win.ini ab.                   |
| [**GetProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprofilestringa)                           | Ruft die Zeichenfolge ab, die einem Schlüssel im angegebenen Abschnitt der Win.ini zugeordnet ist.           |
| [**WritePrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilesectiona)       | Ersetzt die Schlüssel und Werte für den angegebenen Abschnitt in einer Initialisierungsdatei.                  |
| [**WritePrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestringa)         | Kopiert eine Zeichenfolge in den angegebenen Abschnitt einer Initialisierungsdatei.                              |
| [**WritePrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestructa)         | Kopiert Daten in einen Schlüssel im angegebenen Abschnitt einer Initialisierungsdatei.                         |
| [**WriteProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprofilesectiona)                     | Ersetzt den Inhalt des angegebenen Abschnitts in der Win.ini durch angegebene Schlüssel und Werte. |
| [**WriteProfileString**](/windows/desktop/api/Winbase/nf-winbase-writeprofilestringa)                       | Kopiert eine Zeichenfolge in den angegebenen Abschnitt der Win.ini Datei.                                    |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Diese Funktionen werden nur zur Kompatibilität mit 16-Bit-Versionen von Windows:

-   [**RegCreateKey**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeya)
-   [**RegEnumKey**](/windows/desktop/api/Winreg/nf-winreg-regenumkeya)
-   [**RegOpenKey**](/windows/desktop/api/Winreg/nf-winreg-regopenkeya)
-   [**RegQueryValue**](/windows/desktop/api/Winreg/nf-winreg-regqueryvaluea)
-   [**RegSetValue**](/windows/desktop/api/Winreg/nf-winreg-regsetvaluea)

 

 
