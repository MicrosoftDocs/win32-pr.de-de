---
title: AppID-Schlüssel
description: Gruppiert die Konfigurationsoptionen für ein oder mehrere DCOM-Objekte an einem zentralen Speicherort in der Registrierung. DCOM-Objekte, die von derselben ausführbaren Datei gehostet werden, werden in einer AppID gruppiert, um die Verwaltung allgemeiner Sicherheits-und Konfigurationseinstellungen zu vereinfachen.
ms.assetid: 4e3d8c87-e6d7-4b4d-8f72-7180be1e51cf
keywords:
- AppID-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b283a9cc47907cf418c2d7d6d613d151c7e5c5e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391086"
---
# <a name="appid-key"></a>AppID-Schlüssel

Gruppiert die Konfigurationsoptionen für ein oder mehrere DCOM-Objekte an einem zentralen Speicherort in der Registrierung. DCOM-Objekte, die von derselben ausführbaren Datei gehostet werden, werden in einer AppID gruppiert, um die Verwaltung allgemeiner Sicherheits-und Konfigurationseinstellungen zu vereinfachen.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ \_Software Klassen für lokale Computer \\ \\ \\ AppID** \\ *{* AppID \_ GUID *}*



| Registrierungswert                                           | BESCHREIBUNG                                                                                                                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Access spermission**](accesspermission.md)             | Beschreibt die Access Control Liste (ACL) der Prinzipale, die auf Instanzen dieser Klasse zugreifen können. Diese ACL wird nur von Anwendungen verwendet, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufzurufen. |
| [**Activateatstorage**](activateatstorage.md)           | Konfiguriert den Client für die instanzialisierung von Objekten auf dem gleichen Computer wie der persistente Zustand, den Sie verwenden oder von dem Sie initialisiert werden.                                                                    |
| [**AppID**](appid.md)                                   | Identifiziert die AppID-GUID, die der benannten ausführbaren Datei entspricht.                                                                                                                                             |
| [**Appidflags**](appidflags.md)                         | Konfiguriert, wie ein com-Server, der für die Verwendung als interaktiver Benutzer konfiguriert ist, von einem Client auf einem nicht standardmäßigen Desktop gestartet oder an ihn gebunden wird.                                                              |
| [**AuthenticationLevel**](authenticationlevel.md)       | Legt die Authentifizierungs Ebene für Anwendungen fest, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) nicht aufzurufen, oder für Anwendungen, die **CoInitializeSecurity** anrufen und eine AppID angeben.               |
| [**Dllersatz**](dllsurrogate.md)                     | Ermöglicht das Ausführen von DLL-Servern in einem Ersatz Vorgang. Wenn eine leere Zeichenfolge angegeben wird, wird das vom System bereitgestellte Ersatz Zeichen verwendet. Andernfalls gibt der Wert den Pfad des zu verwendenden Ersatz Zeichens an.                 |
| [**Dllsurrogateausführ Bare Datei**](dllsurrogateexecutable.md) | Ermöglicht das Ausführen von DLL-Servern in einem benutzerdefinierten Ersatzprozess in Verbindung mit dem Registrierungs Wert [**dllersatz**](dllsurrogate.md) .                                                                          |
| [**Endpunkte**](endpoints.md)                           | Konfiguriert eine COM-Anwendung so, dass eine angegebene TCP-Portnummer für die DCOM-Kommunikation verwendet wird.                                                                                                                        |
| [**Launchberechtigung**](launchpermission.md)             | Beschreibt die Access Control Liste (ACL) der Prinzipale, die neue Server für diese Klasse starten können.                                                                                                            |
| [**Loadusersettings**](loadusersettings.md)             | Bestimmt, ob com das Benutzerprofil für com-Server lädt, die als Anwendungs Identität des Anwendungs Starts ausgeführt werden.                                                                                           |
| [**LocalService**](localservice.md)                     | Installiert ein-Objekt als Dienst Anwendung.                                                                                                                                                                    |
| [**Preferredserverbitness**](preferredserverbitness.md) | Legt die bevorzugte Architektur (32-Bit oder 64-Bit) für diesen com-Server fest.                                                                                                                                         |
| [**RemoteServerName**](remoteservername.md)             | Konfiguriert den Client so, dass das Objekt auf einem bestimmten Computer ausgeführt wird, wenn eine Aktivierungsfunktion aufgerufen wird, für die keine [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur angegeben ist.              |
| [**Rotflags**](rotflags.md)                             | Steuert die Registrierung eines COM-Servers in der laufenden Objekttabelle (rot).                                                                                                                                    |
| [**RunAs**](runas.md)                                   | Konfiguriert eine Klasse so, dass Sie unter einem bestimmten Benutzerkonto ausgeführt wird, wenn Sie von einem Remote Client aktiviert wird, ohne als Dienst Anwendung geschrieben zu werden.                                                                       |
| [**Service Parameters**](serviceparameters.md)           | Gibt die Befehlszeilenparameter an, die an ein Objekt zu übertragen sind, das zur Verwendung durch com über den Registrierungs Wert [**LocalService**](localservice.md) installiert wird.                                                       |
| [**SRPTrustLevel**](srptrustlevel.md)                   | Legt die Richtlinie für die Software Einschränkungs Richtlinie (SRP) für Anwendungen fest.                                                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

APPIDs werden ausführbare Dateien und Klassen mit zwei verschiedenen Mechanismen zugeordnet:

-   Verwenden eines 128-Bit-GUID (Global Unique Identifier), der den **AppID** -Schlüssel identifiziert. Eine Klasse gibt die zugehörige AppID unter dem [**CLSID**](clsid-key-hklm.md) -Schlüssel in einem benannten Wert "AppID" an. Diese Zuordnung wird während der Aktivierung verwendet.
-   Verwenden eines benannten Werts, der einen Namen für eine ausführbare Datei (z. b. "MYOLDAPP.EXE") angibt. Dieser benannte Wert ist vom Typ **reg \_ SZ** und enthält die Zeichen folgen Darstellung der der ausführbaren Datei zugeordneten AppID. Diese Zuordnung wird verwendet, um die Standard Zugriffsberechtigungen und die Authentifizierungs Ebene abzurufen.

Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.

Bei com-Servern wird die Zuordnung normalerweise generiert und während des Registrierungsvorgangs in die Registrierung geschrieben, oder wenn dcomcnfg.exe ausgeführt wird. Allerdings müssen com-Clients, die die Sicherheit mithilfe des **AppID** -Schlüssels festlegen möchten, entsprechende Registrierungsschlüssel erstellen und die erforderliche Zuordnung angeben, indem Sie die [Registrierungsfunktionen](/windows/desktop/SysInfo/registry-functions) aufrufen oder Regedit.exe. Anschließend können Werte wie [**AccessPermission**](accesspermission.md) oder [**AuthenticationLevel**](authenticationlevel.md) für den Client festgelegt werden. Angenommen, der Name der ausführbaren Datei für den Client Prozess lautet "YourClient.exe", und Sie möchten die Authentifizierungs Ebene auf "None" festlegen. Verwenden Sie Guidgen.exe oder Uuidgen.exe, um die GUID zu erstellen, bei der es sich um die AppID der ausführbaren Datei handelt. Dann würden Sie Werte in der Registrierung festlegen, wie im folgenden Beispiel gezeigt, wobei 00000001 eine Authentifizierungs Ebene von "None" darstellt:

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {MyGuid}
      AuthenticationLevel = 00000001
   MyClient.exe
      AppID = {MyGUID}
```

 

 