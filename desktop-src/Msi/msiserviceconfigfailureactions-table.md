---
description: Die Tabelle MsiServiceConfigFailureActions listet Vorgänge auf, die ausgeführt werden sollen, nachdem ein Dienst ausfällt. Die in dieser Tabelle angegebenen Vorgänge werden beim nächsten Start des Systems ausgeführt.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: MsiServiceConfigFailureActions-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907c0feb2e331c1e19ff4292d11cc58b65340a7543d9af5d0a1ccf23d2e80a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944417"
---
# <a name="msiserviceconfigfailureactions-table"></a>MsiServiceConfigFailureActions-Tabelle

Die Tabelle MsiServiceConfigFailureActions listet Vorgänge auf, die ausgeführt werden sollen, nachdem ein Dienst ausfällt. Die in dieser Tabelle angegebenen Vorgänge werden beim nächsten Start des Systems ausgeführt.

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Wird nicht unterstützt. Diese Tabelle ist ab Windows Installer 5.0 verfügbar.

Die Tabelle MsiServiceConfigFailureActions enthält die folgenden Spalten.



| Spalte                         | Typ                         | Key | Nullwerte zulässig |
|--------------------------------|------------------------------|-----|----------|
| MsiServiceConfigFailureActions | [Identifier](identifier.md) | J   | N        |
| Name                           | [Formatiert](formatted.md)   | N   | N        |
| Ereignis                          | [Integer](integer.md)       | N   | N        |
| ResetPeriod                    | [Integer](integer.md)       | N   | J        |
| RebootMessage                  | [Formatiert](formatted.md)   | N   | J        |
| Get-Help                        | [Formatiert](formatted.md)   | N   | J        |
| Aktionen                        | [Text](text.md)             | N   | J        |
| DelayActions                   | [Text](text.md)             | N   | J        |
| Komponente\_                    | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions
</dt> <dd>

Dies ist der Primärschlüssel dieser Tabelle, der eine Fehleraktion identifiziert.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Diese Spalte enthält den Namen eines Diensts, der Teil dieses Pakets ist oder bereits installiert ist.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ereignis
</dt> <dd>

Diese Spalte gibt an, wann die Konfiguration des Diensts geändert werden soll. Die folgenden Werte sind Bitfelder, die kombiniert werden können, um mehrere Vorgänge darzustellen. Alle anderen Bitfeldwerte werden ignoriert.



| Konstante                                         | BESCHREIBUNG                                     |
|--------------------------------------------------|-------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Änderung während der Installation der Komponente.    |
| **msidbServiceConfigEventUninstall** 2<br/> | Änderung während der Deinstallation der Komponente.  |
| **msidbServiceConfigEventReinstall** 4<br/> | Änderung während der erneuten Installation der Komponente. |



 

</dd> <dt>

<span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod
</dt> <dd>

Der Zurücksetzungszeitraum in Sekunden der Fehleranzahl des Diensts. Der [Dienststeuerungs-Manager (Service Control Manager,](../services/service-control-manager.md) SCM) zählt die Anzahl von Dienstfehlern seit dem letzten Neustart des Systems. Die Anzahl wird auf 0 (null) zurückgesetzt, wenn der Dienst während des Zurücksetzungszeitraums nicht fehlschlägt. Wenn der Dienst zum n. Mal fehlschlägt, führt das System die Aktion aus, die im Element \[ N-1 des Arrays angegeben ist, \] das im Feld Aktionen angegeben ist.

Lassen Sie das Feld ResetPeriod leer, um anzugeben, dass die Fehleranzahl nie zurückgesetzt werden soll.

</dd> <dt>

<span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage
</dt> <dd>

Die Meldung, die an Benutzer gesendet wird, bevor der Computer als Reaktion auf eine **SC \_ ACTION \_ REBOOT-Aktion** neu gestartet wird, die in der Spalte Aktionen angegeben ist. Sie können eine leere Zeichenfolge "" verwenden, um die aktuelle Nachricht unverändert zu senden. Sie können \[ ~ \] die Syntax des Datentyps [Formatted](formatted.md) verwenden, um die aktuelle Nachricht zu löschen und keine Nachricht zu senden.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Befehl
</dt> <dd>

Die Befehlszeile, die von dem Prozess ausgeführt wird, der von der [**CreateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) als Reaktion auf eine **SC ACTION RUN \_ \_ \_ COMMAND-Aktion** erstellt wurde, die in der Spalte Aktionen angegeben ist. Der neue Prozess wird unter demselben Konto wie der Dienst ausgeführt und nur, wenn das Feld Aktion **SC \_ ACTION RUN \_ \_ COMMAND** lautet. Sie können die leere Zeichenfolge "" verwenden, um die aktuelle Befehlszeile unverändert zu verwenden. Sie können \[ ~ \] die Syntax des Datentyps [Formatted](formatted.md) verwenden, um die aktuelle Befehlszeile zu löschen und keinen Vorgang auszuführen, wenn der Dienst ausfällt.

</dd> <dt>

<span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Aktionen
</dt> <dd>

Dieses Feld enthält ein Array ganzzahliger Werte, die die aktionen angeben, die vom SCM ausgeführt werden, wenn der Dienst ausfällt. Trennen Sie die Werte im Array durch \[ ~ \] . Der ganzzahlige Wert im N.-Element des Arrays gibt die Aktion an, die ausgeführt wird, wenn der Dienst zum n. Mal fehlschlägt. Jedes Element des Arrays ist einer der folgenden ganzzahligen Werte.



| Konstante                                 | BESCHREIBUNG           |
|------------------------------------------|-----------------------|
| **SC \_ AKTION \_ NONE** 0<br/>         | Keine Aktion.            |
| **SC \_ \_AKTIONSNEUSTART** 2<br/>       | Starten Sie den Computer neu. |
| **SC \_ \_AKTIONSNEUSTART** 1<br/>      | Starten Sie den Dienst neu.  |
| **SC \_ \_ \_ AKTIONSLAUFBEFEHL** 3<br/> | Führen Sie einen Befehl aus.        |



 

</dd> <dt>

<span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions
</dt> <dd>

Dieses Feld enthält ein Array ganzzahliger Werte, die die Zeit in Millisekunden angeben, die gewartet werden soll, bevor die in der Spalte Aktion angegebene Aktion ausgeführt wird. Trennen Sie die Werte im Array durch \[ ~ \] . Die Anzahl der Elemente im DelayActions-Array muss der Anzahl der Elemente im Actions-Array entsprechen. Das Nth-Element des DelayActions-Arrays gibt die Zeitverzögerung für das nth-Element des Actions-Arrays an.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel zu Spalte 1 der [Komponententabelle.](component-table.md)

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

 

 
