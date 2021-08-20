---
description: Die MsiServiceConfig-Tabelle konfiguriert einen Dienst, der vom aktuellen Paket installiert oder installiert wird.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: MsiServiceConfig-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b72e21fdfecd59780b862d3bfe7d68ef829b59b847dbceb0e9c13befae9d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828590"
---
# <a name="msiserviceconfig-table"></a>MsiServiceConfig-Tabelle

Die MsiServiceConfig-Tabelle konfiguriert einen Dienst, der vom aktuellen Paket installiert oder installiert wird.

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Wird nicht unterstützt. Diese Tabelle ist ab Windows Installer 5.0 verfügbar.

Die MsiServiceConfig-Tabelle enthält die folgenden Spalten.



| Spalte           | Typ                         | Key | Nullwerte zulässig |
|------------------|------------------------------|-----|----------|
| MsiServiceConfig | [Identifier](identifier.md) | J   | N        |
| Name             | [Formatiert](formatted.md)   | N   | N        |
| Ereignis            | [Integer](integer.md)       | N   | N        |
| ConfigType       | [Integer](integer.md)       | N   | N        |
| Argument         | [Formatiert](formatted.md)   | N   | J        |
| Komponente\_      | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig
</dt> <dd>

Dies ist der Primärschlüssel dieser Tabelle.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Diese Spalte enthält den Namen eines Diensts, der Teil dieses Pakets ist oder bereits installiert ist.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ereignis
</dt> <dd>

Diese Spalte gibt an, wann die Dienstkonfiguration geändert werden soll. Die folgenden Werte können kombiniert werden, um mehrere Vorgänge darzustellen. Alle anderen enthaltenen Werte werden ignoriert.



| Konstante                                         | Beschreibung                                              |
|--------------------------------------------------|----------------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Führt die Aktion während der Installation der Komponente aus.   |
| **msidbServiceConfigEventUninstall** 2<br/> | Führt die Aktion während der Deinstallation der Komponente aus. |
| **msidbServiceConfigEventReinstall** 4<br/> | Führt die Aktion während der Neuinstallation der Komponente aus. |



 

</dd> <dt>

<span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType
</dt> <dd>

Der Wert in diesem Feld in Kombination mit dem Wert im Feld Argumente gibt an, welche Änderung an der Dienstkonfiguration vorzunehmen ist. Die angegebene Änderung wird beim nächsten Start des Systems wirksam.



| Config                                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SERVICE \_ CONFIG \_ DELAYED \_ AUTO \_ START** 3<br/>       | Konfigurieren sie die Zeitverzögerung eines Diensts für [den automatischen Start.](../services/automatically-starting-services.md) <br/> Geben Sie 1 in das Feld Argument ein, um den Dienst nach anderen automatisch gestarteten Diensten zuzüglich einer Zeitverzögerung zu starten. <br/> Geben Sie 0 in das Feld Argument ein, um die Verzögerung beim automatischen Starten des Diensts zu deaktivieren.<br/> Gilt nur für installierte Dienste zum automatischen Starten oder dienste, die von diesem Paket mit **SERVICE \_ AUTO \_ START** im Feld StartType der [ServiceInstall-Tabelle](serviceinstall-table.md)installiert werden.<br/>                                                                         |
| **SERVICE \_ CONFIG \_ REQUIRED \_ PRIVILEGES \_ INFO** 6<br/> | Ändern Sie die Liste der berechtigungen, die vom Dienst benötigt werden.<br/> Geben Sie im Feld Argument eine Liste der angeforderten Berechtigungen ein. Der [Formatierte](formatted.md) Zeichenfolgenwert im Feld Argument listet die [**Berechtigungskonstanten**](../secauthz/privilege-constants.md) für die angeforderten Berechtigungen auf. Sie können die \[ ~ \] Syntax der [formatierten](formatted.md) Zeichenfolge verwenden, um ein NULL-Zeichen einzufügen. Trennen Sie die Berechtigungskonstanten in der Liste durch \[ ~ \] .<br/>                                                                                                                              |
| **SERVICE \_ \_ \_ KONFIGURATIONSDIENST-SID \_ INFO** 5<br/>         | Fügen Sie dem Prozesstoken, das diesen Dienst enthält, einen Dienst-SID-Typ hinzu.<br/> Geben Sie im Feld Argument einen gültigen Dienst-SID-Typ für die [**STRUKTUR SERVICE SID \_ \_ INFO**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) ein: **SERVICE SID TYPE \_ \_ \_ NONE** (0x00), **SERVICE SID TYPE \_ \_ \_ RESTRICTED** (0x03) oder **SERVICE SID TYPE \_ \_ \_ UNRESTRICTED** (0x01). <br/>                                                                                                                                                                                                                                              |
| **SERVICE \_ CONFIG \_ PRESHUTDOWN \_ INFO** 7<br/>          | Konfigurieren Sie die Zeitspanne, die der [Dienststeuerungs-Manager (Service Control Manager,](../services/service-control-manager.md) SCM) wartet, bevor Sie mit anderen Herunterfahren-Vorgängen fortfahren. Der SCM wartet nach dem Senden der **SERVICE \_ CONTROL \_ PRESHUTDOWN-Benachrichtigung** an den Dienst für diesen Zeitraum. <br/> Geben Sie die Länge der Zeitverzögerung in Millisekunden in das Feld Argument ein. Lassen Sie das Feld Argument leer, um die Zeitverzögerung auf den Standardwert von 3 Minuten zurückzusetzen. <br/>                                                                                                                               |
| **SERVICE \_ CONFIG \_ FAILURE \_ ACTIONS \_ FLAG** 4<br/>     | Konfigurieren Sie, wann die Fehleraktionen für diesen Dienst ausgeführt werden sollen. Diese Einstellung wird ignoriert, wenn der Dienst über keine konfigurierten Fehleraktionen verfügt.<br/> Geben Sie 0 ein, um die Aktionen nur auszuführen, wenn der Dienst beendet wird, ohne **SERVICE \_ BEENDET zu** melden.<br/> Geben Sie 1 ein, um die Aktionen auszuführen, wenn der Dienst die Meldung **SERVICE \_ STOPPED** beendet und der **dwWin32ExitCode-Member** der [**SERVICE \_ STATUS-Struktur**](/windows/win32/api/winsvc/ns-winsvc-service_status) nicht **ERROR \_ SUCCESS** ist. Konfigurierte Fehleraktionen werden auch ausgeführt, wenn der Dienst beendet wird, ohne **SERVICE \_ STOPPED zu** melden.<br/> |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument
</dt> <dd>

Der Wert in diesem Feld in Kombination mit dem Wert im Feld ConfigType gibt an, welche Änderung an der Dienstkonfiguration vorzunehmen ist. Die angegebene Änderung wird beim nächsten Start des Systems wirksam.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel für die Spalte Komponente der [Komponententabelle](component-table.md).

</dd> </dl>

## <a name="validation"></a>Überprüfung

<dl>

[ICE102](ice-102.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 
