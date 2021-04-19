---
description: Die msiserviceconfig-Tabelle konfiguriert einen Dienst, der vom aktuellen Paket installiert oder installiert wird.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Msiserviceconfig-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360736"
---
# <a name="msiserviceconfig-table"></a>Msiserviceconfig-Tabelle

Die msiserviceconfig-Tabelle konfiguriert einen Dienst, der vom aktuellen Paket installiert oder installiert wird.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Diese Tabelle ist ab Windows Installer 5,0 verfügbar.

Die msiserviceconfig-Tabelle weist die folgenden Spalten auf.



| Spalte           | Typ                         | Schlüssel | Nullwerte zulässig |
|------------------|------------------------------|-----|----------|
| Msiserviceconfig | [Bezeichner](identifier.md) | J   | N        |
| Name             | [Großformatige](formatted.md)   | N   | N        |
| Ereignis            | [Integer](integer.md)       | N   | N        |
| ConfigType       | [Integer](integer.md)       | N   | N        |
| Argument         | [Großformatige](formatted.md)   | N   | J        |
| Komponente\_      | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>Msiserviceconfig
</dt> <dd>

Dies ist der Primärschlüssel dieser Tabelle.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Diese Spalte enthält den Namen eines dienstanteils, der Teil dieses Pakets ist oder bereits installiert ist.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Veranstalter
</dt> <dd>

Diese Spalte gibt an, wann die Dienst Konfiguration geändert werden soll. Die folgenden Werte können kombiniert werden, um mehrere Vorgänge darzustellen. Alle darin enthaltenen Werte werden ignoriert.



| Konstante                                         | BESCHREIBUNG                                              |
|--------------------------------------------------|----------------------------------------------------------|
| **msidbserviceconfgeventinstall** 1<br/>   | Führt die Aktion während der Installation der Komponente aus.   |
| **msidbserviceconfgeventuninstall** 2<br/> | Führt die Aktion während der deinstalstallation der Komponente aus. |
| **msidbserviceconfgeventreinstall** 4<br/> | Führt die Aktion während der erneuten Installation der Komponente aus. |



 

</dd> <dt>

<span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType
</dt> <dd>

Der Wert in diesem Feld, in Kombination mit dem Wert im Feld Argumente, gibt an, welche Änderung an der Dienst Konfiguration vorgenommen werden soll. Die angegebene Änderung wird wirksam, wenn das System das nächste Mal gestartet wird.



| Config                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dienst \_ Konfigurations \_ Verzögertes \_ Automatisches \_ starten** 3<br/>       | Konfigurieren Sie die Zeitverzögerung eines [automatischen Start Dienstanbieter](../services/automatically-starting-services.md). <br/> Geben Sie im Feld Argument den Wert 1 ein, um den Dienst nach anderen automatischen Start Diensten und einer Zeitverzögerung zu starten. <br/> Geben Sie im Feld Argument den Wert 0 ein, um die Verzögerung für den automatischen Start Dienst zu deaktivieren.<br/> Gilt nur für installierte Auto Start Dienste oder Dienste, die von diesem Paket mit **dem \_ automatischen \_ Start des Diensts** im Feld StartType der [Tabelle ServiceInstall](serviceinstall-table.md)installiert wurden.<br/>                                                                         |
| **Dienst \_ Konfigurations \_ erforderliche \_ Berechtigungen \_ Info** 6<br/> | Ändern Sie die Liste der Berechtigungen, die für den Dienst erforderlich sind.<br/> Geben Sie eine Liste der angeforderten Berechtigungen in das Argument Feld ein. Der [formatierte](formatted.md) Zeichen folgen Wert im Feld Argument listet die [**Berechtigungs Konstanten**](../secauthz/privilege-constants.md) für die angeforderten Berechtigungen auf. Sie können die \[ ~ \] Syntax der [formatierten](formatted.md) Zeichenfolge verwenden, um ein NULL-Zeichen einzufügen. Trennen Sie die Berechtigungs Konstanten in der Liste durch \[ ~ \] .<br/>                                                                                                                              |
| **Dienst \_ Konfigurations \_ Dienst- \_ sid \_ Informationen** 5<br/>         | Fügen Sie dem Prozess Token, das diesen Dienst enthält, einen Dienst-SID-Typ hinzu.<br/> Geben Sie im Feld Argument einen gültigen Dienst-SID-Typ für die [**Dienst- \_ sid- \_ Informations**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) Struktur ein: **Dienst-SID- \_ \_ Typ \_ None** (0x00), **Dienst-SID- \_ \_ Typ \_ eingeschränkt** (0x03) oder **Dienst-SID- \_ \_ Typ \_ uneingeschränkt** (0x01). <br/>                                                                                                                                                                                                                                              |
| **Dienst \_ Configuration \_ Preshutdown \_ Info** 7<br/>          | Konfigurieren Sie die Zeitspanne, die der [Dienststeuerungs-Manager](../services/service-control-manager.md) (SCM) wartet, bevor Sie mit anderen Shutdown-Vorgängen fortfahren. Der SCM wartet in diesem Zeitraum nach dem Senden der Dienst Steuerungs Benachrichtigung vor dem **\_ \_ herunter** fahren an den Dienst. <br/> Geben Sie die Zeitverzögerungs Länge (in Millisekunden) in das Argument Feld ein. Belassen Sie das Argument Feld leer, um die Zeitverzögerung auf den Standardwert von 3 Minuten zurückzusetzen. <br/>                                                                                                                               |
| **Dienst \_ Flag für Konfigurations \_ Fehler \_ Aktionen \_** 4<br/>     | Konfigurieren Sie, wann die Fehler Aktionen für diesen Dienst ausgeführt werden sollen. Diese Einstellung wird ignoriert, wenn für den Dienst keine Fehler Aktionen konfiguriert sind.<br/> Geben Sie 0 ein, um die Aktionen nur dann auszuführen, wenn der Dienst beendet wird, ohne den Berichterstattungs **Dienst \_**<br/> Geben Sie 1 ein, um die Aktionen auszuführen, wenn der Dienst beendet wird, dass der Bericht Erstellungs Dienst beendet wird und der **dwWin32ExitCode** -Member der [**Dienst \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) Struktur nicht **Fehler \_** **\_** Konfigurierte Fehler Aktionen werden auch ausgeführt, wenn der Dienst beendet wird, ohne dass der Berichterstattungs **Dienst \_** beendet wird<br/> |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Gestritten
</dt> <dd>

Der Wert in diesem Feld, in Kombination mit dem Wert im Feld ConfigType, gibt an, welche Änderung an der Dienst Konfiguration vorgenommen werden soll. Die angegebene Änderung wird wirksam, wenn das System das nächste Mal gestartet wird.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel zur Komponenten Spalte der [Komponenten Tabelle](component-table.md).

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE102](ice-102.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 
